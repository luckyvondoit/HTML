## 盒子

- HTML中的每一个元素都可以看成一个盒子

### 盒子模型（Box Model）

![image-20211112161948120](images/image-20211112161948120.png)

- 默认的盒子模型如下所示

<img src="images/image-20211112162027159.png" alt="image-20211112162027159" style="zoom:50%;float:left" />

### 浏览器开发者工具中看到的盒子模型

<img src="images/image-20211112162352122.png" alt="image-20211112162352122" style="zoom:50%;float:left" />

## padding

padding-left：左内边距
padding-right : 右内边距
padding-top：上内边距
padding-bottom ：下内边距
padding : padding-top、padding-right、padding-bottom、padding-left的缩写

![image-20211112162853707](images/image-20211112162853707.png)

### padding取值规律

- 按照顺时针方向设值: top、right、 bottom、 left
- 如果缺少left, 那么left就使用right的值
- 如果缺少bottom, 那么bottom就使用top的

## margin

- margin-left ：左外边距
- margin-right ：右外边距
- margin-top ：上外边距
- margin-bottom ：下外边距
- margin : margin-top、margin-right、margin-bottom、margin-left缩写属性

![image-20211112163303779](images/image-20211112163303779.png)

### 上下margin传递

![image-20211112164646969](images/image-20211112164646969.png)

### 上下margin折叠

![image-20211112164331640](images/image-20211112164331640.png)

- 两个兄弟块级元素之间上下margin的折叠

![image-20211112164758246](images/image-20211112164758246.png)

- 父子块级元素之间margin的折叠

![image-20211112164928368](images/image-20211112164928368.png)

- 无内容块级元素内部margin折叠

![image-20211112165220324](images/image-20211112165220324.png)

- 无内容块级元素之间margin的折叠（折叠是可以连续的）

![image-20211112165408574](images/image-20211112165408574.png)

- 块级元素折叠问题看似有点莫名其妙,实际上还是有实用之处的
  - 比如连续段落之间的margin ,恰好需要这种折叠效果

<img src="images/image-20211112165745421.png" alt="image-20211112165745421" style="zoom:50%;float:left" />

## border

- 边框宽度
  - border-top-width、border-right-width、border-bottom-width、border-left width
  - border-width是上面4个属性的简写属性
- 边框颜色
  - border-top -color、border-right-color、border-bottom-color、border-left-color
  - border- color是上面4个属性的简写属性
- 边框样式
  - border-top-style、border right-style、border-bottom-style、border-left-style
  - border- style是上面4个属性的简写属性

### 边框样式的取值

![image-20211112170336627](images/image-20211112170336627.png)

<img src="images/image-20211112170522110.png" alt="image-20211112170522110" style="zoom:50%;float:left" />

### 边框的形状

![image-20211112171139393](images/image-20211112171139393.png)

### 边框的妙用-实现三角形

![image-20211112171225643](images/image-20211112171225643.png)

### 边框妙用-实现双色平分

<img src="images/image-20211112171443996.png" alt="image-20211112171443996" style="zoom:50%;float:left" />

## 行内级元素注意点

- 以下属性对行内级非替换元素不起作用
  - width、 height、 margin-top、 margin-bottom
- 以下属性对行内级非替换元素的效果比较特殊
  - padding-top、padding-bottom、border-top、border-bottom

## border-radius

### border-\*-\*-radius

<img src="images/image-20211112172602611.png" alt="image-20211112172602611" style="zoom:50%;float:left" />

### border-top-left-radius: 55pt 25pt

<img src="images/image-20211112172731811.png" alt="image-20211112172731811" style="zoom:50%;float:left" />

<img src="images/image-20211112172851265.png" alt="image-20211112172851265" style="zoom:50%;float:left" />

<img src="images/image-20211112173227467.png" alt="image-20211112173227467" style="zoom:50%;float:left" />

## outline

- outline表示元素的外轮廓
  - 不占用空间
  - 默认显示在border的外面
  - 每个部位都是完整连接的，不会像border那样有可能会断开(比如行内级非替换元素的换行)
- outline相关属性有
  - outline-width
  - outline-style :取值跟border的样式一 样，比如solid. dotted等
  - outline-color
  - outline : outline-width、outline-style、 outline -color的简写属性，跟border用法类似
  - outline-offset :设置outline和border之间的间距
- 应用实例
  - 去除a元素、input元素的focus轮廓效果

## box-shadow

- box-shadow属性可以设置一 个或者多个阴影
  - 每个阴影用\<shadow\>表示
  - 多个阴影之间用逗号隔开,从前到后叠加
  - \<shadow\> 的常见格式如下

### \<shadow\>

<img src="images/image-20211112174249796.png" alt="image-20211112174249796" style="zoom:50%;float:left" />

### 实例

![image-20211112174731310](images/image-20211112174731310.png)

![image-20211112174802833](images/image-20211112174802833.png)

## text-shadow

- text-shadow用法类似于box-shadow，用以给文字添加阴影效果。
- text-shadow同样适用于::first-line、::first-letter

## box-sizing

<img src="images/image-20211112175533993.png" alt="image-20211112175533993" style="zoom:50%;float:left" />

### box-sizing: content-box;

![image-20211112175808810](images/image-20211112175808810.png)

### box-sizing: border-box;

![image-20211112180016035](images/image-20211112180016035.png)

### 盒子模式

![image-20211112180155275](images/image-20211112180155275.png)

## 水平居中

- 在一些需求中，需要元素在父元素中水平居中显示(元素一般都是块级元素、 inline-block )
- 行内级元素、 inline-block元素
  - 水平居中：在父元素中设置text-align: center
- 块级元素
  - 水平居中: 给自己设置margin-left:  auto；margin-right: auto;
  - 水平居中（合并一起）:给自己设置 margin: 0 auto;

