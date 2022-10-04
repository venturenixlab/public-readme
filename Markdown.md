## Markdown Language
##### GitLab Markdown - [Offical GitLab Markdown](https://docs.gitlab.com/ee/user/markdown.html)

##### GitHub Markdown - [Offical GitHub Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

****
## 目录
* [横线](#横线)
* [标题](#标题)
* [文本](#文本)
    * 普通文本
    * 单行文本
    * 多行文本
    * 文字高亮
    * 换行
    * 斜体
    * 粗体
    * 删除线
* [图片](#图片)
    * 来源于网络的图片
    * GitHub仓库中的图片
* [链接](#链接) 
    * 文字超链接
        *  链接外部URL
        *  链接本仓库里的URL
    *  锚点
    * [图片链接](#图片链接)
* [列表](#列表)
    * 无序列表
    * 有序列表
    * 复选框列表
* [引用](#引用)
* [代码高亮](#代码高亮)
* [表格](#表格) 
* [表情](#表情)
* [diff语法](#diff语法)
* [HTML](#HTML语法)
* [Variable](#Variable语法)

横线
------
***、---、___可以显示横线效果

***
---
___



标题
------

# 一级标题  
## 二级标题  
### 三级标题  
#### 四级标题  
##### 五级标题  
###### 六级标题  


文本
------
### 普通文本
这是一段普通的文本

### 单行文本
    Hello,大家好
在一行开头加入1个Tab或者4个空格。

### 文本块
#### 语法1
在连续几行的文本开头加入1个Tab或者4个空格。

    欢迎到访
    很高兴见到您
    祝您，早上好，中午好，下午好，晚安

#### 语法2
使用一对各三个的反引号：
```
欢迎到访
你可以在知乎、CSDN、简书搜索
```
该语法也可以实现代码高亮，见[代码高亮](#代码高亮)

### 文字高亮
文字高亮功能能使行内部分文字高亮，使用一对反引号。
语法：
```
`linux` `网络编程` `socket` `epoll` 
```
效果：`linux` `网络编程` `socket` `epoll`

也适合做一篇文章的tag

#### 换行
直接Enter不能换行，  
可以在**上一行文本后面补两个空格**，  
这样下一行的文本就换行了。

或者就是在两行文本**直接加一个空行**。
也能实现换行效果，不过这个行间距有点大。

#### 斜体、粗体、删除线

|语法|效果|
|----|-----|
|`*斜体1*`|*斜体1*|
|`_斜体2_`| _斜体2_|
|`**粗体1**`|**粗体1**|
|`__粗体2__`|__粗体2__|
|`这是一个 ~~删除线~~`|这是一个 ~~删除线~~|
|`***斜粗体1***`|***斜粗体1***|
|`___斜粗体2___`|___斜粗体2___|
|`***~~斜粗体删除线1~~***`|***~~斜粗体删除线1~~***|
|`~~***斜粗体删除线2***~~`|~~***斜粗体删除线2***~~|

    斜体、粗体、删除线可混合使用

图片
------
基本格式：
```
![alt](URL "title")
```
alt和title即对应HTML中的alt和title属性（都可省略）：
- alt表示图片显示失败时的替换文本
- title表示鼠标悬停在图片时的显示文本（注意这里要加引号）

URL即图片的url地址，如果引用本仓库中的图片，直接使用**相对路径**就可了，如果引用其他github仓库中的图片要注意格式，即：`仓库地址/raw/分支名/图片路径`，如：
```
https://github.com/guodongxiaren/ImageCache/raw/master/Logo/foryou.gif
```

|#|语法|效果|
|---|---|----
|1|`![baidu](http://www.baidu.com/img/bdlogo.gif "百度logo")`|![baidu](http://www.baidu.com/img/bdlogo.gif "百度logo")
|2|`![][csdn-logo]`|![][csdn-logo]


链接
------
### 链接外部URL

```
[Google](https://www.google.com/)
[Youtube](https://www.youtube.com/)
```
[Google](https://www.google.com/)

[Youtube](https://www.youtube.com/)

语法2由两部分组成：
- 第一部分使用两个中括号，[ ]里的标识符, 可以是数字，字母等的组合
- 第二部分标记实际URL ()。

### 链接本仓库里的URL


|语法|效果|
|----|-----|
|`[EMOJI](/emoji/EMOJI.md)`|[EMOJI](/emoji/EMOJI.md)|

### 图片链接
给图片加链接的本质是混合图片显示语法和普通的链接语法。普通的链接中[ ]内部是链接要显示的文本，而图片链接[ ]里面则是要显示的图片。  
直接混合两种语法当然可以，但是十分啰嗦，为此我们可以使用URL标识符的形式。

|#|语法|效果|
|---|----|:---:|
|1|`By URL: [![weibo-logo]](http://weibo.com)`|[![weibo-logo]](http://weibo.com)|
|2|`By project path: [![](/img/zhihu.png "知乎，欢迎关注")][zhihu]`|[![](/img/zhihu.png "知乎，欢迎关注")][zhihu]|
|3|`By markdown varaible: [![csdn-logo]][csdn]`|[![csdn-logo]][csdn]|

### 锚点
和HTML的锚点（`#`）类似

|语法|效果|
|---|---|
|`[回到顶部](#readme)`|[回到顶部](#目录)|

不过要注意，标题中的英文字母都被转化为**小写字母**了。
> 以前GitHub对中文支持的不好，所以中文标题不能正确识别为锚点，但是现在已经没问题啦

列表
---------
### 无序列表
#### 语法
```
* 昵称
- 别名：隔壁老王
* 英文名：James
```
#### 效果
* 昵称：
- 别名：隔壁老王
* 英文名：James

### 多级无序列表
#### 语法
```
* 编程语言
    * 脚本语言
        * Python
```
#### 效果
* 编程语言
    * 脚本语言
        * Python

### 一级有序列表
#### 语法
就是在数字后面加一个点，再加一个空格。不过看起来起来可能不够明显。 
```
面向对象的三个基本特征：

1. 封装
2. 继承
3. 多态
```

#### 效果
面向对象的三个基本特征：

1. 封装
2. 继承
3. 多态


### 多级有序列表
和无序列表一样，有序列表也有多级结构。
#### 语法
```
1. 这是一级的有序列表，数字1还是1
   1. 这是二级的有序列表，阿拉伯数字在显示的时候变成了罗马数字
      1. 这是三级的有序列表，数字在显示的时候变成了英文字母
```

#### 效果

1. 这是一级的有序列表，数字1还是1
   1. 这是二级的有序列表，阿拉伯数字在显示的时候变成了罗马数字
      1. 这是三级的有序列表，数字在显示的时候变成了英文字母
	 

### 复选框列表
#### 语法
```
- [x] 需求分析
- [x] 系统设计
- [x] 详细设计
- [ ] 编码
- [ ] 测试
- [ ] 交付
```
#### 效果

- [x] 需求分析
- [x] 系统设计
- [x] 详细设计
- [ ] 编码
- [ ] 测试
- [ ] 交付

您可以使用这个功能来标注某个项目各项任务的完成情况。
> Tip:
>> 在GitHub的**issue**中使用该语法是可以实时点击复选框来勾选或解除勾选的，而无需修改issue原文。

引用
---------

### 常用于引用文本
#### 文本摘自《深入理解计算机系统》P27
> **“端”（endian）的起源**  
以下是Jonathan Swift在1726年关于大小端之争历史的描述：  
“……下面我要告诉你的是，Lilliput和Blefuscu这两大强国在过去36个月里一直在苦战。战争开始是由于以下的原因：我们大家都认为，吃鸡蛋前，原始的方法是打破鸡蛋较大的一端，可是当今的皇帝的祖父小时候吃鸡蛋，一次按古法打鸡蛋时碰巧将一个手指弄破了，因此他的父亲，当时的皇帝，就下了一道敕令，命令全体臣民吃鸡蛋时打破较小的一端，违令者重罚。”

### 块引用有多级结构
#### 语法
```
> 数据结构
>> 树
>>> 二叉树
>>>> 平衡二叉树
>>>>> 满二叉树
```
#### 效果
> 数据结构
>> 树
>>> 二叉树
>>>> 平衡二叉树
>>>>> 满二叉树

代码高亮
----------
### 语法
在三个反引号后面加上编程语言的名字，另起一行开始写代码，最后一行再加上三个反引号。

![][md-code-highlight]
### 效果
```Java
public static void main(String[]args){} //Java
```
```C
int main(int argc, char *argv[]) //C
```
```Bash
echo "hello GitHub" #Bash
```
```Javascript
document.getElementById("myH1").innerHTML="Welcome to my Homepage"; //javascipt
```
```Cpp
string &operator+(const string& A,const string& B) //cpp
```
表格
--------
```
表头1  | 表头2|
--------- | --------|
表格单元  | 表格单元 |
表格单元  | 表格单元 |
```

表头1  | 表头2|
--------- | --------|
表格单元  | 表格单元 |
表格单元  | 表格单元 |

### 对齐
表格可以指定对齐方式
```
| 左对齐 | 居中  | 右对齐 |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |
```

| 左对齐 | 居中  | 右对齐 |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |

### 混合其他语法
表格单元中的内容可以和其他大多数GFM语法配合使用，如：  
#### 使用普通文本的删除线，斜体等效果
```
| 名字 | 描述 |
| ------------- | ----------- |
| Help      | ~~Display the~~ help window.|
| Close     | _Closes_ a window     |
```

| 名字 | 描述 |
| ------------- | ----------- |
| Help      | ~~Display the~~ help window.|
| Close     | _Closes_ a window     |

#### 表格中嵌入图片（链接）
其实前面介绍图片显示、图片链接的时候为了清晰就是放在在表格中显示的。
```
| 图片 | 描述 |
| ---- | ---- |
|![baidu][baidu-logo] | 百度|
```

| 图片 | 描述 |
| ---- | ---- |
|![baidu][baidu-logo] | 百度|

表情
----------
Markdown语法支持添加emoji表情，输入不同的符号码（两个冒号包围的字符）可以显示出不同的表情。

比如`:blush:`，可以显示:blush:

Refer to [EMOJI.md](/emoji/EMOJI.md)

diff语法
---------
版本控制的系统中都少不了diff的功能，即展示一个文件内容的增加与删除。
GFM中可以显示的展示diff效果。使用绿色表示新增，红色表示删除。
#### 语法
其语法与代码高亮类似，只是在三个反引号后面写diff，
并且其内容中，可以用 `+ `开头表示新增，`- `开头表示删除。
另外还有有 `!`和`#`的语法。
```
```diff
```
#### 效果

```diff
normal text
+ add text
- remove text
! alert text
# comment.
```

HTML语法
---------
#### Not support span style/ font color
```html
<span style="color:green">Suppose it is text in green</span>
<font color=#0000FF>Title with blue color</font>
```

<span style="color:green">Suppose it is text in green</span>

<font color=#0000FF>Title with blue color</font>

--------------

Variable语法
---------
```
[csdn]:http://blog.csdn.net "CSDN 博客"
[zhihu]:https://www.zhihu.com "知乎"
[weibo]:http://weibo.com "微博"
[baidu-logo]:http://www.baidu.com/img/bdlogo.gif "百度logo"
[weibo-logo]:/img/weibo.png "点击图片进入微博"
[csdn-logo]:/img/csdn.png "我的CSDN博客"
```
[csdn]:http://blog.csdn.net "CSDN 博客"
[zhihu]:https://www.zhihu.com "知乎"
[weibo]:http://weibo.com "微博"
[baidu-logo]:http://www.baidu.com/img/bdlogo.gif "百度logo"
[weibo-logo]:/img/weibo.png "点击图片进入微博"
[csdn-logo]:/img/csdn.png "我的CSDN博客"
[md-code-highlight]:/img/md-code-highlight.png "code-highlight"