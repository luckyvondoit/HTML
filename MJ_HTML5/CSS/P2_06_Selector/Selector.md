## css选择器（selector）

![](images/image-20211109203709303.png)

### 元素选择器（type selectors）

![image-20211109203940850](images/image-20211109203940850.png)

### 通用选择器（universal selectors）

![image-20211109185436692](images/image-20211109185436692.png)

### id选择器（id selectors）

![image-20211109185618485](images/image-20211109185618485.png)

#### id注意点

- 一个HTML文档里面的id值是唯一的，不能重复
- id值如果由多个单词组成，单词之间可以用中划线（-）、下划线（_）连接,也可以使用驼峰标识，（建议用中划线）
- 最好不要用标签名作为id值
- 不能有空格

<img src="images/image-20211109185936406.png" alt="image-20211109185936406" style="zoom:50%;float:left" />

- 中划线又叫连字符（hyphen）

### 类选择器（class selectors）

![image-20211109190322661](images/image-20211109190322661.png)

#### class注意点

![image-20211109190617324](images/image-20211109190617324.png)

- 多余的空格（开头，类名之间，结尾都有多个空格）不影响功能，但还是要按照规范，类名之间加一个空格，首尾不加空格。

### 练习

![image-20211109201450450](images/image-20211109201450450.png)

<img src="images/image-20211109201522246.png" alt="image-20211109201522246" style="zoom:50%;float:left" />

- 多个类显示效果和类的顺序无关，一般把最主要的放在前面，如果类中有重复的属性，顺序会影响显示效果

<img src="images/image-20211109201616687.png" alt="image-20211109201616687" style="zoom:50%;float:left" />

<img src="images/image-20211109201831109.png" alt="image-20211109201831109" style="zoom:50%;float:left" />

### 属性选择器（atdtribute selectors）

####  [attr]

![image-20211109202149201](images/image-20211109202149201.png)

#### [attr=val]

![image-20211109202510981](images/image-20211109202510981.png)

- 建议用双引号

#### [attr~=val]

![image-20211109203017915](images/image-20211109203017915.png)

#### [attr|=val]

![image-20211109203208629](images/image-20211109203208629.png)

#### [attr^=val]

![image-20211109204127727](images/image-20211109204127727.png)

#### [attr$=val]

![image-20211109204353507](images/image-20211109204353507.png)

#### [attr*=val]

![image-20211109204605621](images/image-20211109204605621.png)

## 组合

### 后代组合选择器( descendant combinator )

![image-20211109205254656](images/image-20211109205254656.png)

### 子组合选择器( child combinators )

![image-20211109205601867](images/image-20211109205601867.png)

![image-20211109205817318](images/image-20211109205817318.png)

- 组合中可以放任意选择器
- 后代组合和子组合可以混用

<img src="images/image-20211109210313853.png" alt="image-20211109210313853" style="zoom:50%;float:left" />

- 包括间接元素

<img src="images/image-20211109210136694.png" alt="image-20211109210136694" style="zoom:50%;float:left" />

- 不包括间接元素

### 相邻兄弟组合选择器( adjacent sibling combinator )

![image-20211109210532305](images/image-20211109210532305.png)

### 全体兄弟组合选择器( general sibling combinator )

![image-20211109210728332](images/image-20211109210728332.png)

## 选择器组

 ### 交集选择器

![image-20211110102626760](images/image-20211110102626760.png)

- 注：div元素和类.one直接挨在一起

### 并集选择器

![image-20211110102730992](images/image-20211110102730992.png)

### 交集和并集对比

![image-20211110102810134](images/image-20211110102810134.png)

### 练习

<img src="images/image-20211110102832278.png" alt="image-20211110102832278" style="zoom:50%;float:left" />

<img src="images/image-20211110104646591.png" alt="image-20211110104646591" style="zoom:50%;float:left" />

<img src="images/image-20211110105054147.png" alt="image-20211110105054147" style="zoom:50%;float:left" />

## 伪类（pseudo-classes）

![image-20211110110908191](images/image-20211110110908191.png)

### 动态伪类（dynamic pseudo-classes）

<img src="images/image-20211110111426130.png" alt="image-20211110111426130" style="zoom:50%;float:left" />

<img src="images/image-20211110111543920.png" alt="image-20211110111543920" style="zoom:50%;float:left" />

#### :fouce

![image-20211110112449324](images/image-20211110112449324.png)

#### 去除a元素默认的:focus效果

<img src="images/image-20211110112805158.png" alt="image-20211110112805158" style="zoom:50%;float:left" />

#### tabindex属性

- 使用tabindex可以控制tab键选中元素的顺序，从1开始
- tabindex设置为-1 ，代表禁止使用tab键选中

#### 细节

![image-20211110113442473](images/image-20211110113442473.png)

### 目标伪类 ( target pseudo-classes )

### ![image-20211113153558339](images/image-20211113153558339.png)

### 元素状态伪类( UI element states pseudo-classes )

![image-20211113153722843](images/image-20211113153722843.png)

### 语言伪类( language pseudo-classes )

![image-20211113153444994](images/image-20211113153444994.png)

### 结构伪类（structural pseudo-classes ）

#### :nth-child( )

![image-20211110114003963](images/image-20211110114003963.png)

- :nth-child(n)，n是具体数组则选择第n个元素，直接填n选择所有

![image-20211110134803269](images/image-20211110134803269.png)

![image-20211110134836465](images/image-20211110134836465.png)

![image-20211110140606535](images/image-20211110140606535.png)

- 4个一组

<img src="images/image-20211110140637118.png" alt="image-20211110140637118" style="zoom:50%;float:left" />

#### :nth-last-child()

![image-20211110141104765](images/image-20211110141104765.png)

#### 思考

![image-20211110141335895](images/image-20211110141335895.png)

#### :nth-of-type( )， :nth-last-of-type( )

![image-20211110141636381](images/image-20211110141636381.png)

![image-20211110141933467](images/image-20211110141933467.png)

#### empty

![image-20211110142050091](images/image-20211110142050091.png)

### 否定伪类

![image-20211110142650227](images/image-20211110142650227.png)

- 否定伪类建议和元素标签一起使用。避免把html、body等修改了

![image-20211110142224000](images/image-20211110142224000.png)

## 伪元素（pseudo-elements）

![image-20211110142936277](images/image-20211110142936277.png)

### ::first-line

![image-20211110143246494](images/image-20211110143246494.png)

### ::first-letter

![image-20211110143333857](images/image-20211110143333857.png)

### ::before和::after

![image-20211110143419302](images/image-20211110143419302.png)

### attr()

![image-20211110143831647](images/image-20211110143831647.png)

