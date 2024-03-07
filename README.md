# blogs  
个人的学习笔记  

##Java
1、JVM、JRE和JDK  
(1) JVM : Java虚拟机  
(2) JRE : Java运行环境  
(3) JDK : Java开发环境(不止一个，但Sun公司的JDK最有名)

2、常用及生僻关键字  
(1) byte : 整型，8bit(1字节)，范围为-128 ~ 127  
(2) short : 整型，16bit(2字节)，范围为-32768 ~ 32767  
(3) int : 整型，32bit(4字节)，范围为 -2^31 ~ 2^31-1(大概20亿)  
(4) long : 整型，64bit(8字节)，范围为 -2^63 ~ 2^63-1(正常使用基本不会超)  
(5) float : 浮点型，32bit(4字节)，有效数字为7位  
(6) double ：浮点型，64bit(8字节)，有些数字为16位  
(7) char : 字符型，16bit(2字节)，存储一个Unicode字符(意味着汉字也能正常存储)  
(8) String ：字符串  
(9) enum : 枚举  
(10) continue : 继续，跳过本次循环  
(11) break : 打断，跳出当前循环  
(12) static : 静态，修饰变量和方法  
(13) final : 最终，修饰常量、最终方法（不可被重写，但是可以被重载）、最终类（不可被继承）  
(14) instanceof : 是……什么的实例，判断数据类型  
(15) assert : 断言，若满足条件则程序执行，否则报错并中止程序  
(16) native : 本地，调用其他编程语言的代码  
(17) strictfp : 精确浮点，修饰类、方法和接口，使得方法内的浮点数运算满足 IEEE 754   
(18) synchronized : 同步，修饰方法和代码块，加锁  
(19) transient ：暂时的，修饰变量，避免变量被序列化，提高性能   
(20) volatile : 易变的，修饰变量，避免代码重排序，使被线程修改的数据立即刷新，让其他线程可以读取最新值

3、Java的三大特性  
(1) 封装 : 隐藏细节，控制访问，提高代码的安全性和可维护性  
(2) 继承 : 子类继承父类，复用、修改父类的属性和方法，提高代码复用性  
(3) 多态 : 通过方法重载与方法重写，提高代码灵活性  

4、方法重载与方法重写  
(1) 方法重载 : 同一个类定义多个同名不同参的方法(参数个数、参数类型、参数顺序)  
(2) 方法重写 : 子类重写父类的方法

5、多线程  
(1) 线程 : 执行流的最小单位，不能独立于进程存在，共享进程的资源  
(2) 多线程的意义 : 提高并发性和响应性  
(3) 线程的创建 : 继承Thread类和实现Runnable接口  
(4) 线程安全 : 程序的行为是正确的，可预测的  
(5) 死锁 : 多个线程互相等待释放资源，程序无法继续运行  
(6) 竞态条件 : 多个线程同时访问数据，其中一个线程修改了数据导致其他线程读取了错误数据  
(7) 同步 : Synchronized、ReentrantLock、ReadWriteLock、Semaphore、CountDownLatch  
(8) 线程方法 : start、join、sleep、interrupt、getState、setPriority

6、多继承  
(1) 类 : 不能被多继承  
(2) 接口 : 可以被多继承  
(3) 原因 : 接口没有实现方法，不会造成方法调用的冲突

7、常见数据结构  
(1) Array : length  
(2) List : ArrayList、LinkedList | add、remove、get  
(3) Set : HashSet、TreeSet | add、remove、contains  
(4) Queue : LinkedList、PriorityQueue | offer、poll、peek  
(5) Map : HashMap、TreeMap | put、remove、get  
(6) Stack : push、pop、peek

8、垃圾回收  
(1)原理:周期性扫描对象的内存区，将没有被引用的对象收集起来，定期释放内存空间  
(2)显示调用:System.gc()  
(3)撤销:finalize()  
