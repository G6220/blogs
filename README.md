# blogs  
个人的学习笔记  

## Java
### JVM、JRE和JDK  
1、JVM : Java虚拟机  
2、JRE : Java运行环境  
3、JDK : Java开发环境(不止一个，但Sun公司的JDK最有名)

### 常用及生僻关键字  
1、byte : 整型，8bit(1字节)，范围为-128 ~ 127  
2、short : 整型，16bit(2字节)，范围为-32768 ~ 32767  
3、int : 整型，32bit(4字节)，范围为 -2^31 ~ 2^31-1(大概20亿)  
4、long : 整型，64bit(8字节)，范围为 -2^63 ~ 2^63-1(正常使用基本不会超)  
5、float : 浮点型，32bit(4字节)，有效数字为7位  
6、double ：浮点型，64bit(8字节)，有些数字为16位  
7、char : 字符型，16bit(2字节)，存储一个Unicode字符(意味着汉字也能正常存储)  
8、String ：字符串  
9、enum : 枚举  
10、continue : 继续，跳过本次循环  
11、break : 打断，跳出当前循环  
12、static : 静态，修饰变量和方法  
13、final : 最终，修饰常量、最终方法（不可被重写，但是可以被重载）、最终类（不可被继承）  
14、instanceof : 是……什么的实例，判断数据类型  
15、assert : 断言，若满足条件则程序执行，否则报错并中止程序  
16、native : 本地，调用其他编程语言的代码  
17、strictfp : 精确浮点，修饰类、方法和接口，使得方法内的浮点数运算满足 IEEE 754   
18、synchronized : 同步，修饰方法和代码块，加锁  
19、transient ：暂时的，修饰变量，避免变量被序列化，提高性能   
20、volatile : 易变的，修饰变量，避免代码重排序，使被线程修改的数据立即刷新，让其他线程可以读取最新值

### Java的三大特性  
1、封装 : 隐藏细节，控制访问，提高代码的安全性和可维护性  
2、继承 : 子类继承父类，复用、修改父类的属性和方法，提高代码复用性  
3、多态 : 通过方法重载与方法重写，提高代码灵活性  

### 方法重载与方法重写  
1、方法重载 : 同一个类定义多个同名不同参的方法(参数个数、参数类型、参数顺序)  
2、方法重写 : 子类重写父类的方法

### 多线程  
1、线程 : 执行流的最小单位，不能独立于进程存在，共享进程的资源  
2、多线程的意义 : 提高并发性和响应性  
3、线程的创建 : 继承Thread类和实现Runnable接口  
4、线程安全 : 程序的行为是正确的，可预测的  
5、死锁 : 多个线程互相等待释放资源，程序无法继续运行  
6、竞态条件 : 多个线程同时访问数据，其中一个线程修改了数据导致其他线程读取了错误数据  
7、同步 : Synchronized、ReentrantLock、ReadWriteLock、Semaphore、CountDownLatch  
8、线程方法 : start、join、sleep、interrupt、getState、setPriority

### 多继承  
1、类 : 不能被多继承  
2、接口 : 可以被多继承  
3、原因 : 接口没有实现方法，不会造成方法调用的冲突

### 常见数据结构  
1、Array : length  
2、List :   
(1) 常用实现类 : ArrayList、LinkedList    
(2) 常用方法 : add、remove、get    
3、Set :   
(1) 常用实现类 : HashSet、TreeSet   
(2) 常用方法 : add、remove、contains     
4、Queue :  
(1) 常用实现类 : LinkedList、PriorityQueue    
(2) 常用方法 : offer、poll、peek   
5、Map :  
(1) 常用实现类 : HashMap、TreeMap    
(2) 常用方法 : put、remove、get   
6、Stack : push、pop、peek

### 垃圾回收  
1、原理 : 周期性扫描对象的内存区，将没有被引用的对象收集起来，定期释放内存空间  
2、显示调用 : System.gc()  
3、撤销 : finalize()  

### 深拷贝与浅拷贝
1、浅拷贝 : 两个引用指向同一片内存空间  
2、深拷贝 : 重新开辟一片内存空间，并将拷贝对象的值赋进来  
3、应用场景 : 浅拷贝性能高，深拷贝安全性高

## 数据结构
### 线性表
1、顺序表  
(1) 构成要素 : 数组、长度  
(2) 方法 : add、get、delete、update  
(3) 特点 : 查找、修改元素方便，增加、删除元素麻烦  

2、链表  
(1) 构成要素 : 数据(其他类)、当前类的指针/引用  
(2) 方法 : getNext、setNext、add、delete、update  
(3) 特点 : 增加、删除元素方便，查找、修改元素麻烦  

3、循环链表  
(1) 构成要素与方法 : 与链表一样，但是把最后一个结点的指针/类指向了第一个结点  
(2) 使用场景 : 约瑟夫问题、缓冲区更新、轮询  
(3) 如何判断 : 快慢指针是否相遇  

4、双向链表  
(1) 构成要素 : 数据(其他类)、两个当前类的指针/引用  
(2) 方法 : getPrior、getNext、setPrior、setNext、add、delete  
(3) 特点 : 容易逆序遍历、插入和删除更高效  
(4) 使用场景 : LRU缓存淘汰、页面置换  

### 栈
1、顺序栈  
(1) 构成要素 : 数组、栈的大小、当前栈元素的数量  
(2)  方法 : getSize、isEmpty、expandSpace、push、pop、peek  
(3) 特点 : 大小固定，容量不够时需要扩容  
(4) 使用场景 : 大小确定，空间紧张

2、链栈  
(1) 构成要素 : 数据(其他类)、当前类的指针/引用、栈的大小  
(2) 方法 : getSize、isEmpty、push、pop、peek  
(3) 特点 : 大小不确定，无需扩容  
(4) 使用场景 : 大小不确定，需要频繁插入和删除元素  

### 队列
1、顺序队列  
(1) 构成要素 : 数组、队列大小、头/尾元素的的下标  
(2) 方法 : getSize、isEmpty、expandSpace、enqueue、dequeue、peek  
(3) 特点 : 大小固定，容量不够时需要扩容  
(4) 使用场景 : 大小确定，空间紧张  

2、循环队列  
(1) 构成要素与方法 : 与顺序队列一样，但是对头/尾元素的下标进行了取余  
(2) 特点 : 充分利用了队列空间，不需要移动元素，效率高  
(3) 使用场景 : 大小确定，空间利用率高  

3、链式队列  
(1) 构成要素 : 数组、队列大小、头/尾元素的的下标   
(2) 方法 : getSize、isEmpty、enqueue、dequeue、peek  
(3) 特点 : 大小不确定，无需扩容  
(4) 使用场景 : 大小不确定，需要频繁插入和删除元素  

### 串
1、静态串  
(1) 构成要素 : char数组、串的长度  
(2) 方法 : length、charAt、indexOf、replace、substring  
(3) 特点 : 线程安全、性能高、不可变  
(4) 紧缩格式 : 每个字节存储一个字符，空间利用率高，但是操作运算要分离字符，比较麻烦  
(5) 非紧缩格式 : 每个存储单元存储一个字符，一个存储单元有多个字节，空间利用率低，但是不需要分离字符，处理字符的速度更快  

## 算法
### 排序算法
1、冒泡排序  
(1) 时间复杂度 : O(n²)  
(2) 空间复杂度 : O(1)  
(3) 稳定性 : 稳定  
(4) 代码实现 :  
```
for (int i = 0; i < array.length - 1; i++)
 {
	for (int j = 0; j < array.length - i - 1; j++)
        {
		if (array[j] > array[j + 1])
               {
			int temp = array[j];
			array[j] = array[j + 1];
			array[j + 1] = temp;
		}
	}
}
```
2、选择排序  
(1) 时间复杂度 : O(n²)  
(2) 空间复杂度 : O(1)  
(3) 稳定性 : 不稳定，a b 1，假设a = b > 1，从小到大排序，则排序后为 1 b a  
(4) 代码实现 :  
```
for (int i = 0; i < array.length - 1; i++)
 {
	int index = i;
	for (int j = i + 1; j < array.length; j++) 
       {
		if (array[j] < array[index]) 
               {
			index = j;
		}
	}
	int temp = array[i];
	array[i] = array[index];
	array[index] = temp;
}
```
3、插入排序  
(1) 时间复杂度 : 最好为O(n)，最坏为O(n²)  
(2) 空间复杂度 : O(1)  
(3) 稳定性 : 稳定  
(4) 代码实现 :  
```
for (int i = 1; i < array.length; i++)
 {
	int temp = array[i];
	int j = i - 1;
	if (j >= 0 && array[j] > temp) 
       {
		array[j] = array[j + 1];
		j--;
	}
	array[j + 1] = temp;
}
```
