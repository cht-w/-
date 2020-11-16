# -
这是一个使用column-count和column-gap实现的瀑布流效果

##column 实现瀑布流效果思路分析

1. column-count属性：将文档分为多少列。
2. column-gap 属性： 列与列之间的间距。

如果只是单纯的做一个瀑布流效果，使用 flex 或者 column属性可以完成。但是如果需要迎合复杂的业务场景（动态渲染，滚动加载等），无疑 使用js来实现瀑布流是最好不过了。

##js结合绝对定位实现瀑布流效果

1. 基本布局结构相似
```
    /**样式**/
    * {
        margin: 0;
        padding: 0;
    }
    #box {
        position: relative;
        width: 1200px;
        margin: 0 auto;
    }
    .item {
        position: absolute;
        box-shadow: 3px 2px 2px #ccc;
    }
    img {
        width: 200px;
        display: block;
    }
```

```
<!--html 结构-->
 <div id="box">
        <div class="item">
            <img src="./img/01.jpg" alt="">
        </div>
        ...
 </div>
```
利用绝对定位，让每一个item都重叠在左上角，然后通过js计算出每一个item的top 和left 值。

步骤： 

   1. 首先获取页面的宽度 和每一张图片的宽度， 计算出当前窗口 可以摆放多少列     columns = 页面宽度 / 每一张图片的宽度   （如果想要美观一点，可以设置间距 gap 那么列数 columns = 页面宽度 /（ 每一张图片的宽度 + gap））









