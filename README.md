# ThreadPool-
~高并发网络服务器
~master-slave(主从)线程模型
~耗时任务处理

##项目名称: 基于可变参数模板实现的线程池
github地址: https://github.com/xtu2020/
##平台及工具 gdb(调试分析死锁问题) 
            cmake(编译器)    
            clang(编译器) 
            vccode(编辑器)
##项目描述:
        1.基于可变参模板实现的线程池,实现线程池 submitTask()接口,支持任意任务和任意参数的传递
        2.使用 future 类型定制 submitTask提交任务的返回值
        3.使用 map 管理线程对象,使用 queue 管理任务
        4.基于条件变量 condition_variable和互斥 mutex 实现线程池的同步机制
        5.支持 fixed 和 cached 模式的线程池的定制

##项目难点:
        用户任务外界的传递和绑定
        线程池的同步机制
##项目问题
        1.ThreadPool回收资源时,等待线程池所有线程退出,死锁问题
        2.linux下 thread库是默认析构,而 windows库是

    
##项目解决方案:
        1.使用的调试相关命令如下:
            gdb:gdb attach pid(进程号)
                info threads(查看线程信息)
                thread tid 
                bt(查看调用栈)
            cmake:
                cmake .. && make
