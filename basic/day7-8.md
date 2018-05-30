# basic style

  ``` css
    html {
      font-family: sans-serif;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
    }
  ```
# 盒子模型

    元素 内容 + 内边距 + border + 外边距

# 正常的文档流

    将元素放置在浏览器视口内的系统

    默认情况下，
    块状元素在视口中垂直布局
      每个都将显示在上一个元素的新行上，并且它们的外边距将分隔它们
      如果相邻两个元素都有外边距，且接触到，则保留大的外边距，而不是两个外边距相加（外边距折叠）

    内联元素则按顺序排列下去，如果没有空间了，才会换到新行上，继续按顺序排列

# 定位

 position 

    - 允许元素脱离普通的文档流，并使有不同的行为
    
  ``` 

  position: static(default) relative absolute;

  static : 将元素放到普通文档流的正常位置

  relative : 将元素放到普通文档流的正常位置
             除占据正常的位置外，可以修改值，使其偏离正常位置，还占据了原来的位置
             偏离的原点是原来位置的左上角

  absolute : 元素将脱离普通文档流
             默认位置为原来普通文档流的位置，但独立层，不会影响其他元素的位置
             可以修改值，设置其位置，设置的原点是根据元素的定位上下文决定
    ###定位上下文 ？？


  fixed : 元素将脱离普通文档流
          默认位置为原来普通文档流的位置，但独立层，不会影响其他元素的位置???
          可以修改值，设置其位置，设置的原点是根据浏览器视口左上角
  
  实验属性: position sticky
    相对位置和固定位置之间的混合，其允许定位的元件像它被相对定位一样动作
    直到其滚动到某一阈值点（例如，从视口顶部10像素），之后它变得固定

  top/right/bottom/left : 指定非static元素移动到的位置 单位可以设置（px / mm / rems / %）任何单位
  1. 不设置 width/height   left & right 、 top & bottom  均生效
  2. 设置 width/height   left & right （根据方向生效）、 top生效 & bottom


  z-index ： 决定absolute的独立层的堆叠顺序，默认为 0，直接搜无单位索引值

  ```
# 布局
  flexbox
    display: flex;
    flex-firection: column;
    flex: flex-grow flex-shrink flex-basis;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    order: 1;


# 浮动
  float 被设置了float的元素会脱离文档流。
    破坏性/包裹性/去空格
  clear

# 方法
双inline-block
双float
float+margin-left
absolute+margin-left
float+BFC
flex
grid

