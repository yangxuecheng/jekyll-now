---
published: true
layout: post
---
## Android 知识树

这里主要是想将Android开发中需要用到各个知识点以树的形式组织起来，各个知识点下面是我读过的（或者待读的）博客的列表，希望能将最优质最干货的资源索引进来。查漏补缺，与大家共勉。

### Java知识
- 接口&抽象类
- 类加载原理
- 注解，泛型，反射
- 线程
  - [ ] [Thread 和Service总结@CodePath ](https://github.com/codepath/android_guides/wiki/Managing-Threads-and-Custom-Services)
- GC
- NIO
  - [ ][NIO系列教程 @ifeve](http://ifeve.com/overview/)
- 强/弱/软引用
- 单例模式
- 内部类
- synchronized关键字
- JVM
  - [ ][JVM系列@Gityuan](http://gityuan.com/2015/10/17/jvm-class-instruction/)

### Android 基础知识
- Handler/Message/Looper
  - [x][Handler系列分析@Gityuan](http://gityuan.com/2015/12/26/handler-message-framework/)
- [x][Android系统的启动流程@woaitqs](http://www.woaitqs.cc/android/2016/06/15/how-android-launch-itself.html)
- [x][Android应用安装过程](http://www.woaitqs.cc/android/2016/07/28/android-plugin-get-apk-info.html)

### Android 高级知识
- Dalvik ART
- 混淆
- AMS
- PMS
- AIDL
- Binder
  - [ ][Binder源码解读@gityuan ](http://gityuan.com/2015/11/01/binder-driver/)
  - [ ][Android Binder 全解析@woaitqs](http://www.woaitqs.cc/android/2016/05/23/android-binder.html)
- JNI

### UI
- Widget
- Webview
- layout
- view
  - [x][ View详解系列@woaitqs](http://www.woaitqs.cc/android/2016/10/10/android-view-theory-1)
- viewGroup
- Container
- Listview
- Recycleview
- Gridview
- PullrefreshView
- ViewPager

### Activity
- 生命周期
- [x][应用的启动流程@woaitqs](http://www.woaitqs.cc/android/2016/06/21/activity-service.html)

### Fragment
- 生命周期
- Fragment间的交互

### Service

### BroardcastReceiver

### ContentProvider

### Gradle
- gradle语法
  - [ ] [Gradle for Android @neu](https://segmentfault.com/a/1190000004229002)
- gradle插件
  - [x] [如何从零开始写一个Gradle插件](https://afterecho.uk/blog/create-a-standalone-gradle-plugin-for-android-a-step-by-step-guide.html)

### 架构
- mvp
    - 开源项目
      - [ ] [谷歌MVP架构项目](https://github.com/googlesamples/android-architecture/tree/todo-mvp-loaders/)
      - [ ] [Material Mobies](https://github.com/saulmm/Material-Movies)
      - [ ] [EffectiveUI](https://github.com/pedrovgs/EffectiveAndroidUI/)
      - [ ] [AndroidMVP](https://github.com/antoniolg/androidmvp)
      - [ ] [The Clean Way](https://github.com/android10/Android-CleanArchitecture)
      - [ ] [clean Contacts](https://github.com/PaNaVTEC/Clean-Contacts)
    - 文章
      - [ ] [Archritature Android the clean way](http://fernandocejas.com/2014/09/03/architecting-android-the-clean-way/)
- mvvm
- 数据持久化
- SharedPerference
- File
- SQLite

### 第三方库
- 网络
	- Volley
	- Retrofit
    - [x] [Retrofit系列教程@future studio](https://futurestud.io/tutorials/retrofit-getting-started-and-android-client)
    - [x] [Retrofit2.0简介@cheesefactory](http://inthecheesefactory.com/blog/retrofit-2.0/en)

- 图片
	- UIL
	- Picasso
    - [ ] [Picasso系列@future studio](https://futurestud.io/tutorials/picasso-getting-started-simple-loading)
	- Fresco
    - [ ] [Fresco官宣 @Facebook](https://guides.codepath.com/android/Displaying-Images-with-the-Fresco-Library)
	- Glide
    - [ ] [Glide系列教@futurestudio](https://futurestud.io/tutorials/glide-getting-started)

- 消息框架
	- Otto
	- EventBus

### 依赖注入
- dagger2
  - [x][使用Dagger2进行依赖注入系列@frogermcs](http://frogermcs.github.io/dependency-injection-with-dagger-2-the-api/)
  - [ ] [依赖注入@codepath](https://guides.codepath.com/android/Dependency-Injection-with-Dagger-2)
  - [ ] [Test Dagger@fernandocejas](http://fernandocejas.com/2015/04/11/tasting-dagger-2-on-android/)
  - [ ] [dagger介绍@antonioleiva](http://antonioleiva.com/dependency-injection-android-dagger-part-1/)  
  - [ ] [依赖注入@future@future](https://www.future-processing.pl/blog/dependency-injection-with-dagger-2/)

### 调试优化
- 常用工具
  - logcat
  - DDMS
  - HierarchyView
  - Lint
  - debug
- 内存分析
  - 内存泄露
    - [ ] [Android可能的八种内存泄漏 @nimbledroid](http://blog.nimbledroid.com/2016/05/23/memory-leaks.html)
    - [ ] [Android防止内存泄漏的八个方法 @nimbledroid](http://blog.nimbledroid.com/2016/09/06/stop-memory-leaks.html)

### 效率工具
- Android Studio
  - 插件
    - [ ][好插件集合](https://github.com/dreamlivemeng/androidstudio-plugins)
  - 使用技巧
    - [ ][Android Studio奇技@zlv](http://zlv.me/posts/2015/07/13/14_android-studio-tips/)
- 快速编译工具
	- [快速编译利器 Freeline @蚂蚁聚宝](https://yq.aliyun.com/articles/59122?spm=5176.8091938.0.0.1Bw3mU)

### RxJava
  - 干货博文
    - [ ][RxJava的详解@扔物线](https://github.com/rengwuxian/RxJavaSamples)
    - [ ][Grokking With RxJava @DanLew](http://blog.danlew.net/2014/09/15/grokking-rxjava-part-1/)
  - 开源项目
    - [ ][RxJava好资源集合 Awesome-RxJava @lzyzsd](https://github.com/lzyzsd/Awesome-RxJava)

### 热修复
  - 微信Tinker
    - [ ][微信热补丁 Tinker 的实践演进之路](https://segmentfault.com/a/1190000006657614)
    - [ ][微信Tinker的一切都在这里，包括源码(一)](https://segmentfault.com/a/1190000007092400)
  - 基于ClassLoader热修复方案
    - [ ] [安卓App热补丁动态修复技术介绍@QZone技术团队](https://mp.weixin.qq.com/s?__biz=MzI1MTA1MzM2Nw==&mid=400118620&idx=1&sn=b4fdd5055731290eef12ad0d17f39d4a)
  - Dexposed

### 插件化
  - [ ] [插件化系列博客@Weisu](http://weishu.me/2016/01/28/understand-plugin-framework-overview/)

### 单元测试


### 资料
- 周/日报
  - [AndroidWeekly](http://androidweekly.net/)
  - [Android开发技术周报](http://www.androidweekly.cn/)
  - [干货集中营](http://gank.io/)
