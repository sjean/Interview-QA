**1. 构造函数可以是虚函数吗**

	virtual call is a mechanism to get work done given partial
	information. In particular, "virtual" allows us to call a
	function knowing only an interfaces and not the exact type of the
	object. To create an object you need complete information. In
	particular, you need to know the exact type of what you want to
	create. Consequently, a "call to a constructor" cannot be
	virtual.


**2. 成员函数可以调用delete this吗？为什么？**
		 析构函数里面不可以
     
**3. 四种类型转换？static_cast向上向下转换时的会出现什么问题。dynamic_cast失败的话会怎样。**

**4. 成员函数里memset(this,0,sizeof(*this))会发生什么**

	一个C++类中除了需要空间来存放数据成员之外，还可能保存着虚函数表指针S，偏移量等信息，一但你memset之后全都没有了。所以这是错误的行为。
		
5. 菱形的多继承下虚函数的内存结构

6. 方法调用的原理（栈，汇编）

7. TCP/IP卷1看过没？有什么协议是你觉得最吸引你的？滑动窗口是什么？如何用UDP来模拟TCP

8. 图片拓扑流听过吗？像百度图片那样的。你会如何设计客户端？

9. string a；字符串a这是存在哪里的。为什么在a在栈上，但是在动态增长的时候，栈不会溢出？

10. 为什么delete []就可以删除整个数组。char *p = new char[32]; 如果用delete p，会发生什么

11. 大数乘法，手写代码

12. **select/poll/epoll的区别**

select，poll，epoll都是IO多路复用的机制。I/O多路复用就通过一种机制，可以监视多个描述符，一旦某个描述符就绪（一般是读就绪或者写就绪），能够通知程序进行相应的读写操作。但select，poll，epoll本质上都是同步I/O，因为他们都需要在读写事件就绪后自己负责进行读写，也就是说这个读写过程是阻塞的，而异步I/O则无需自己负责进行读写，异步I/O的实现会负责把数据从内核拷贝到用户空间。

13. 基类的析构函数必须为虚函数吗？ 为什么?

14. 虚函数，虚函数表里面内存如何分配？

