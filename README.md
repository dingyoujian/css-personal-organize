##前端菜鸡的自我修养

```js

css一些知识点总结笔记

```

### Flex布局

弹性布局,子元素的float、clear和vertical-align属性无效

####容器属性

-flex-direction 主轴排列方向
-flex-wrap 如何换行
-flex-flow 主轴换行简写
-justify-content 主轴对其方式
-align-items 交叉轴对其方式
-align-content 多根轴线对其方式 如果项目只有一根轴线，该属性不起作用

>flex-direction: row | row-reverse | column | column-reverse

依次从左到右，从右到左，从上到下，从下到上

>flex-wrap: nowrap | wrap | wrap-reverse

依次不换行，向下换行，向上换行

>flex-flow: <flex-direction> || <flex-wrap>

主轴换行的简写默认 row nowrap

>justify-content: flex-start | flex-end | center | space-between | space-around

依次主轴起点对齐，主轴终点对齐，主轴中点对其，两端对其，每个项目两侧的间隔相等

>align-items: flex-start | flex-end | center | baseline | stretch

依次交叉轴的起点对齐，交叉轴的终点对齐，交叉轴的中点对齐，项目的第一行文字的基线对齐，填满整个主轴

>align-content: flex-start | flex-end | center | space-between | space-around | stretch;

依次交叉轴的起点对齐，交叉轴的终点对齐，交叉轴的中点对齐,交叉轴两端对其，交叉轴每个项目两侧的间隔相等，填满整个交叉轴

####项目属性

-order 定义项目的排列顺序。数值越小，排列越靠前，默认为0。
-flex-grow 定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大。所有都为1则等分
-flex-shrink 定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。为0时不缩小
-flex-basis 定义了在分配多余空间之前，项目占据的主轴空间。默认auto,如果设置具体px数值，则占据固定空间
-flex flex-grow，flex-shrink，flex-basis简写
-align-self 允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch,属性与items一致

#### FFC
1.设置了 display: flex; 或 display: inline-flex的元素 不会被浮动的元素遮盖，不会垂直外边距坍塌

#### Flex item
white-space: pre 空白会被保留，装进flex item
