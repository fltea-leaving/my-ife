# 盒模型
  - 每个元素 ===> 矩形方框
  - 内容、内边距、边界和外边距
    - (max/min) width & height （content box）
    - padding (-[left | right | top | bottom])
    - border (-[left | right | top | bottom]) (- [width | style | color] ) *框的高度（宽度）不遵守百分比的长度
    - margin (-[left | right | top | bottom])
  - box-sizing 诡异模式 和 正常模式
## 其他属性
  overflow ： auto | hidden | visible(default);
  background-clip : border-box | padding-box | content-box;
  outline：看起来像是边界但又不属于框模型的东西，不改变框的尺寸，被勾画于在框边界之外，外边距区域之内

## 框 类型
  - block
  - inline
  - inline-block

# 盒子
 ![Alt text](../img/box-model-standard-small.png)
*： 
1. 盒子高度设置百分比时，不会遵循（除非父级盒子设置了具体高度，盒子设置的高度可以计算出具体值）
2. border 忽略百分比宽度
3. margin 外边距塌陷(两个盒子挨在一起，二者之间挨着的外边距取最大的值，而不是和)

# 浮动
  清除浮动 & 闭合浮动
  
