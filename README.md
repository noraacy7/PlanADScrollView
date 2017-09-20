


这里主要介绍了iOS多线程NSThread，GCD，NSOperation的使用
-----------------------------------------------------

#点击右上角的 star、watch 按钮，可以收藏本仓库，看到本仓库的更新！




* 什么是进程？什么是线程？
    
    进程是指在操作系统中正在运行的一个应用程序，每个进程之间是相互独立的；线程是指进程内独立执行某个任务的一个单元线程,开启一个线程比开启一个进程更加节省资源。

* 什么是多线程？

    一个进程中可以开启多条线程，每条线程可以同时执行不同的任务。
    
* 多线程的优缺点？

    多线程的优点：能适当的提高程序的执行效率，提高资源利用率（CPU、内存利用率）
    
    多线程的缺点：开启线程需要占用一定的内存空间（默认情况下，主线程占用1M，子线程占用512kb），如果开启大量的线程，会占用大量的内存空间，降低程序的性能。线程越多，CPU的调度线程上的开销就越大。
    
* iOS多线程的种类
   
  * 1.NSThread 是轻量级的多线程开发，使用起来也并不复杂，但是使用NSThread需要自己管理线程生命周期。   

  * 2.GCD 是iOS4推出的，C语言框架，能够自动利用更多cpu的核数，自动管理线程的生命周期。
    队列分为四种:
    串行（Serial）:让任务一个完毕之后接着另一个执行
    并发（Concurrent）:可以让多个任务并发（同时）执行（自动开启多个线程同时执行任务）并发功能只有在异步（dispatch_async）函数下才有效。
    同步（Synchronous）:在当前线程中执行任务，不具备开启新线程的能力
    异步（Asynchronous）:在新的线程中执行任务，具备开启新线程的能力

  * 3.NSOperation是基于GCD的一个封装. 但是比GCD多了一些简单实用的功能, 这就使NSOperation变的更加的面向对象.
    NSOperation是一个抽象基类，我们使用最多的是它的子类NSInvocationOperation和NSBlockOperation。

  在iOS开发的过程中如有遇到问题，欢迎联系我进行探讨交流.

  邮箱：peiliancoding@gmail.com 

  QQ ：2877025939.
