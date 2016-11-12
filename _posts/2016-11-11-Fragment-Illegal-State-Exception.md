---
published: true
layout: post
---
### 原因
> 原因：在activity调用了onSaveInstanceState()方法之后，尝试提交Fragment Transaction。

那么问题来了，为什么调用了onSaveInstanceState()之后，为嘛就不能再提交Fragment的Transaction了？

先说下onSaveInstanceState()。
onSaveInstanceState()方法主要是用来保存activity的现有状态的，比如EditText输入的文字。Android的activity对自己的生命是没有太多控制的，在系统要对activity进行回收，或者点击home键回到桌面，或者转屏等情形下，为了保持用户体验的完整性，系统会在回收掉activity之前给activity一个机会保存现有的状态。

再说下Fragment Transaction。Fragment事务用来添加、删除、或者替换Activity中的一个fragment。大多数的fragment事务都是在Activity的onCreate函数或者用户交互中完成的。只要FragmentActivity位于后台了（被其他应用挡住了，该应用暂停了）， FragmentManagerImpl’s
mStateSaved 就会标记为true。该标记用来检测是否有状态丢失。当该标记为true的时候去提交一个事务，上面的IllegalStateException 异常就会发生。

### 如何避免
1.避免在onSaveInstanceState()之后提交fragment事务。大部分的fragment事务是在onCreate中完成的，这是OK的。但是如果在Activity的其他状态中，如onResume,onStart(),onActivityResult()等方法中去提交Fragment事务就可能存在问题。因为这时候activity的状态可能还没有恢复。
> onResume():可以考虑增加在onResumeFragments(),或者onPostResume()。
> onActivityResult()：可以参考[SO的方法](http://stackoverflow.com/questions/16265733/failure-delivering-result-onactivityforresult)

2.避免在异步回调方法中提交Fragment事务。
包括AsyncTask的onPostExcute()，LoaderManager的onLoadFinished().因为回调的时候是无法确认Activity的状态的。

3.最后一招commitAllowingStateLoss().
commitAllowingStateLoss()的意思也就是如果出现了stateLoss的状态，那么也不会跑出异常，如果可以通过前面的处理而不用这个方法，就可以尽量不用。

### 参考资料
1.IllagalState Exception的详细解释，推荐阅读[fragment-transaction-commit-state-loss](http://www.androiddesignpatterns.com/2013/08/fragment-transaction-commit-state-loss.html)
2.这里有说明如何实现自动保存Fragment/Activity的的状态[The Real Best Practices to Save/Restore Activity's and Fragment's state](https://inthecheesefactory.com/blog/fragment-state-saving-best-practices/en)
