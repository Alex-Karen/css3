# css3

## 介绍 Introduction

upgrade version css2 升级版本

预处理器 pre-processor

    less/sass cssNext

后处理器 post-processor

    autoprefixer(插件)

    postCss 用js实现的css的抽象的语法树

## 选择器

关系选择符 Relationship Selectors

    E + F   选择紧贴在E元素之后F元素，元素E与F必须同属一个父级

    E ~ F   选择E元素后面的所有兄弟元素F，元素E与F必须同属一个父级

属性选择符 Attribute Selectors

    E[att~="val"]   E[att^="val"]   E[att$="val"]   E[att*="val"]   E[att|="val"]

伪元素选择符 Pseudo-Element Selectors

    E::placeholder      伪元素用于控制表单输入框占位符的外观 改变默认字体颜色

    E::selection        设置对象被选择时的颜色 只能定义被选择时的background-color，color及text-shadow

伪类选择符 Pseudo-Classes Selectors 被选中元素状态

    E:not(s) 匹配不含有s选择符的元素E

    E:root 匹配E元素在文档的根元素。在HTML中，根元素永远是HTML

    E:target 匹配相关URL指向的E元素

        URL后面跟锚点#，指向文档内某个具体的元素。这个被链接的元素就是目标元素(target element)，:target选择器用于选取当前活动的目标元素。

    E:first-child 匹配父元素的第一个子元素E

    E:last-child 匹配父元素的最后一个子元素E

    E:only-child 匹配父元素仅有的一个子元素E

    E:nth-child(n) 匹配父元素的第n个子元素E，假设该子元素不是E，则选择符无效

    E:nth-last-child(n) 匹配父元素的倒数第n个子元素E，假设该子元素不是E，则选择符无效

    E:first-of-type 匹配父元素下第一个类型为E的子元素

    E:last-of-type 匹配父元素下的所有E子元素中的倒数第一个

    E:only-of-type 匹配父元素的所有子元素中唯一的那个子元素E

    E:nth-of-type(n) 匹配父元素的第n个子元素E

    E:nth-last-of-type(n) 匹配父元素的倒数第n个子元素E

    E:empty 匹配没有任何子元素（包括text节点）的元素E

    E:checked 匹配用户界面上处于选中状态的元素。(用于input type为radio与checkbox时)

    E:enabled 匹配用户界面上处于可用状态的元素E

    E:disabled 匹配用户界面上处于禁用状态的元素E

    E:read-only     E:read-write

## border background