# Box-Model
对盒子模型的理解

css3中定义了 

            box-sizing: content-box    | border-box | inherit
                             w3c标准盒模型    IE传统盒子模型
来改变盒子模型

<p>w3c标准盒模型中盒子大小会被内容包括 content padding border撑大</p>


<p>IE传统盒子模型大小不会被上述内容撑大</p>

<h3>栗子</h3>
<p>1. CSS2中，元素(例如div)的内边距(padding)和边框(border)会把元素自身撑大。
想要个100*100px的div，都要事先计算，例如，内容80px + 内边距15px + 边框5px = 100px</p>

<p>2. CSS3中，新增 box-sizing 属性，如果设置元素为 box-sizing: border-box，
那么元素的内边距(padding)和边框(border)不会再把元素自身撑大。
例如，设置div为100*100px，那么无论div里内容、内边距、边框的宽高怎么变化，div的大小永远都是100*100px</p>
<p>
至于为什么，W3C的标准盒模型中，内容、内边距和边框变化会把元素撑大，而传统IE盒模型中则没有这个问题：<br>

box-sizing:content-box，按W3C的盒子模型计算，内容+内边距+边框=元素大小<br>

这是搭积木，三块积木搭出一个房子，任何一块积木大小变化了，房子结构就不稳定了，表现为把元素撑大<br>

box-sizing:border-box，按传统IE盒子模型计算，元素大小=内容+内边距+边框<br>

这是盖房子，事先定好尺寸，盖好一个房子，里边放三块积木，随便你们三个怎么变化，只要不超过房子的大小，随你们折腾<br>

原先W3C认为IE的 border-box 模型是逗比，事实证明W3C才是逗比
</p>
