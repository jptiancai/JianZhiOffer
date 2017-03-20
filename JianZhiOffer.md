[TOC]



# 准备阶段

## 简历

- 简短的项目背景
- 完成的任务
- 为完成任务做了哪些工作，怎么做的
- 自己的贡献

## 为什么跳槽

## 技术需求

### 扎实的基础知识 

> 基础知识扎实全面，包括编程语言、数据结构、算法等

### 高质量代码

> 能写出正确的、完整的、鲁棒的高质量代码

### 清晰的思路

> 能思路清晰地分析、解决复杂问题

### 优化效率的能力

> 能从时间、空间复杂度两方面优化算法效率

### 优秀的综合能力

> 具备优秀的沟通能力、学习能力、发散思维能力等

## 应聘者提问环节



# 第一章 面试的流程



## 新浪大牛看待面试

![](xinlang.png)



> 以上来自[独酌逸醉-新浪技术部笔试题](http://www.perfect-is-shit.com/sina-written-exam.html)



## 把一个字符串转换成整数



# 第二章 面试需要的基础知识

编程语言 + 数据结构 + 算法和数据操作



## 在线挑战[剑指offer](https://www.nowcoder.com/ta/coding-interviews?query=&asc=true&order=&page=1)

## [大志非才不就，大才非学不成—我的博文资源汇总](http://www.cnblogs.com/edisonchou/p/3843287.html)

## 设计模式

- 实现singleton模式

1. 参考

> 在这里可以详细做一些练习：
> [Java：单例模式的七种写法](http://www.blogjava.net/kenzhh/archive/2011/09/02/357824.html):一般单例都是五种写法。懒汉，恶汉，双重校验锁，枚举和静态内部类。
> [面试题：线程安全的单例模式](http://www.iteye.com/topic/537563):文章最后的一些参考资料也很不错！



2. 项目中的实际应用




- jdk

Calendar.getInstance()

SecretKeyFactory.getInstance("PBEWithMD5AndDES").generateSecret(keySpec);

Cipher.getInstance(key.getAlgorithm())

MessageDigest.getInstance("MD5");

NumberFormat.getInstance().parse(params.get(key).toString().trim());





- 项目中，搜索instance得到

JVMMonitor ： public static final JVMMonitor instance = new JVMMonitor();

UdpLoggerClient ： log服务器客户端

ServerStatusLog ：服务器状态日志

ArenaMemberDbManager ： private static ArenaMemberDbManager arenaMemberDbManager = new ArenaMemberDbManager();

CurrencyProcessor ： 金钱处理器,单实例

TimeDifferenceStr：时间区分字符串

UseItemOperPool ： 道具使用支持类，单实例，用于为UseItemAction提供合适的UseItemOperation

MoveItemServicePool ： MoveItemService的对象池，用于根据源、目的包的id查询取得相应的MoveItemService，这些service对象都是公用的对象，单实例

DBConnection : 定义DBConnection

ShowOffPageNums：显示页码

PageNumForEach：每页显示数目

RobotManager : 机器人管理





3. 实战


枚举单例模式
- [如何正确地写出单例模式](http://wuchong.me/blog/2014/08/28/how-to-correctly-write-singleton-pattern/)
- [为什么java中用枚举实现单例模式会更好](https://my.oschina.net/zhoujy/blog/134958)
- [JAVA 枚举单例模式](https://segmentfault.com/q/1010000000646806)





## 数组

- 二维数组中的查找




当我们需要解决一个复杂的问题时，一个很有效的满发就是从一个具体的问题入手，通过分析简单的例子，试图寻找普遍的规律。比如该题目中给出的数组中查找数字7位例来一步步分析查找的过程。


```java
public class FindIt {
    public static void main(String[] args) {
        int [][] arrays={{1,2,8,9},{2,4,9,12},{4,7,10,13},{6,8,11,15}};
        for (int[] i : arrays) {
            System.out.print(i[0]);
            System.out.print(" ");
            System.out.print(i[1]);
            System.out.print(" ");
            System.out.print(i[2]);
            System.out.print(" ");
            System.out.print(i[3]);
            System.out.println();
        }
        FindIt findIt=new FindIt();
        System.out.println(findIt.find(arrays, 4, 4, 4));
    }
    boolean find(int [][] matrix,int rows,int columns,int number){
        boolean found=false;
        if (matrix!=null&&rows>0&&columns>0) {
            int row=0;
            int column=columns-1;
            while(row<rows&&column>=0){
                if (matrix[row][column]==number) {
                    found=true;
                    break;
                }
                else if(matrix[row][column]>number)
                    --column;
                else
                    ++row;
            }
        }
        return found;
    }
```
```
输出为

1 2 8 9
2 4 9 12
4 7 10 13
6 8 11 15
true
```







# 图

## 无向图



SLG游戏中解决最短路径的问题

- [数据结构基础温故-5.图（下）：最短路径](http://www.cnblogs.com/edisonchou/p/4691020.html)
- [无向图的处理算法（三）](https://segmentfault.com/a/1190000002680208)
- [无向图的最短路径求解算法之——Dijkstra算法(二)](http://sbp810050504.blog.51cto.com/2799422/1163565)
- [国立台湾师范大学-演算法笔记](http://www.csie.ntnu.edu.tw/~u91029/Circuit.html)








