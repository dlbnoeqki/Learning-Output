EventLoop的构造：
1. 单个线程
2. Selector
3. 异步任务队列


EventLoop的运行机制：如何监听并处理Channel上的IO就绪事件

EventLoop主要负责三件事：
1. 轮询注册在Reactor上的所有Channel感兴趣的IO就绪事件
2. 处理Channel上的IO就绪事件
3. 执行Netty中的异步任务

EventLoop=死循环，在死循环中不断的通过Selector去轮询IO就绪事件，如果发生IO就绪事件则从Selector系统调用中返回并处理IO就绪事件，如果没有发生IO就绪事件则一直阻塞在Selector系统调用上，直到满足Selector唤醒条件。

EventLoop被唤醒的时机：
1. 当Selector轮询到有IO活跃事件发生时。
2. 当EventLoop需要执行的定时任务到达任务执行事件deadline时。
3. 当有异步任务提交给EventLoop时，EventLoop需要从Selector上被唤醒，及时的去执行异步任务。
