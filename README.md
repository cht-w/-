# -
这是一个使用column-count和column-gap实现的瀑布流效果

##column 实现瀑布流效果思路分析

1. column-count属性：将文档分为多少列。
2. column-gap 属性： 列与列之间的间距。

如果只是单纯的做一个瀑布流效果，使用 flex 或者 column属性可以完成。但是如果需要迎合复杂的业务场景（动态渲染，滚动加载等），无疑 使用js来实现瀑布流是最好不过了。
