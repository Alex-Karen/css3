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

    border-radius 定义元素的圆角

        border-top-left-radius border-top-right-radius
        border-bottom-left-radius border-bottom-right-radius

    box-shadow 定义元素的阴影

        none：无阴影
        <length>第 1 个长度值定义元素的阴影水平偏移值。正值，阴影出现在元素右侧；负值，则阴影出现在元素左侧
        <length>第 2 个长度值定义元素的阴影垂直偏移值。正值，阴影出现在元素底部；负值，则阴影出现在元素顶部
        <length>第 3 个长度值定义元素的阴影模糊值半径（如果提供了）。
                该值越大阴影边缘越模糊，若该值为0，阴影边缘不出现模糊。不允许负值
        <length>第 4 个长度值定义元素的阴影外延值（如果提供了）。正值，阴影将向四面扩展；负值，则阴影向里收缩
        <color>定义元素阴影的颜色。如果该值未定义，阴影颜色将默认取当前最近的文本颜色
        inset：定义元素的阴影类型为内阴影。该值为空时，则元素的阴影类型为外阴影

    border-image 定义将图像应用到元素的边框上

        border-image-source：定义元素边框背景图像，可以是图片路径或使用渐变创建的“背景图像”。
        border-image-slice：定义元素边框背景图像从什么位置开始分割。
        border-image-width：定义元素边框背景图像厚度。
        border-image-outset：定义元素边框背景图像的外延尺寸。
        border-image-repeat：定义元素边框背景图像的平铺方式。

    background-image:url(), url()

    background-size

        <length>：用长度值指定背景图像大小。不允许负值。
        <percentage>：用百分比指定背景图像大小。不允许负值。
        auto：背景图像的真实大小。
        cover：将背景图像等比缩放到完全覆盖容器，背景图像有可能超出容器。
        contain：将背景图像等比缩放到宽度或高度与容器的宽度或高度相等，背景图像始终被包含在容器内。

    background-repeat

        repeat-x：背景图像在横向上平铺
        repeat-y：背景图像在纵向上平铺
        repeat：背景图像在横向和纵向平铺
        no-repeat：背景图像不平铺
        round：当背景图像不能以整数次平铺时，会根据情况缩放图像。（CSS3）
        space：当背景图像不能以整数次平铺时，会用空白间隙填充在图像周围。（CSS3）

    background-position 指定背景图像在元素中出现的位置

    background-origin   指定的背景图像计算background-position时的参考原点(位置)

        border-box：从border区域（含border）开始显示背景图像。
        padding-box：从padding区域（含padding）开始显示背景图像。默认值
        content-box：从content区域开始显示背景图像。

    background-clip 指定对象的背景图像向外裁剪的区域

        border-box：从border区域（含border）开始向外裁剪背景。
        padding-box：从padding区域（含padding）开始向外裁剪背景。
        content-box：从content区域开始向外裁剪背景。
        text：从前景内容的形状（比如文字）作为裁剪区域向外裁剪，如此即可实现使用背景作为填充色之类的遮罩效果

    background-attachment   定义滚动时背景图像相对于谁固定

        fixed：背景图像相对于视口（viewport）固定。
        scroll：背景图像相对于元素固定，也就是说当元素内容滚动时背景图像不会跟着滚动，因为背景图像总是要跟着元素本身。
                但会随元素的祖先元素或窗体一起滚动。
        local：背景图像相对于元素内容固定，也就是说当元素随元素滚动时背景图像也会跟着滚动，
                因为背景图像总是要跟着内容。（CSS3）

    linear-gradient 用线性渐变创建图像

        <angle>：用角度值指定渐变的方向（或角度）。
        to left：设置渐变为从右到左。相当于: 270deg
        to right：设置渐变从左到右。相当于: 90deg
        to top：设置渐变从下到上。相当于: 0deg
        to bottom：设置渐变从上到下。相当于: 180deg。这是默认值，等同于留空不写。
        <color-stop> 用于指定渐变的起止颜色：
        <color>：指定颜色。
        <length>：用长度值指定起止色位置。不允许负值
        <percentage>：用百分比指定起止色位置。

    radial-gradient 用径向渐变创建图像

        radial-gradient(circle, #f00, #ff0, #080);
        radial-gradient(circle at center, #f00, #ff0, #080);
        radial-gradient(circle at 50%, #f00, #ff0, #080);
        radial-gradient(circle farthest-corner, #f00, #ff0, #080);

## text

    text-shadow 定义文字是否有阴影及模糊效果

        none： 无阴影
        <length>：第1个长度值用来设置对象的阴影水平偏移值。可以为负值
        <length>：第2个长度值用来设置对象的阴影垂直偏移值。可以为负值
        <length>：如果提供了第3个长度值则用来设置对象的阴影模糊值。不允许负值
        <color>：设置对象的阴影的颜色。

    work-break  定义元素内容文本的字间与字符间的换行行为

## 多列

    columns 设置或检索对象的列数和每列的宽度

## box  盒模型

    box-sizing: content-box  border-box;

    overflow hidden scroll auto //overflow-x or -y

    resize 设置或检索对象的区域是否允许用户缩放，调节元素尺寸大小 必须设置overflow

    flex

## transition

## animation
