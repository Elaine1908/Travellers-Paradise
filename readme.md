PJ 1 说明文档
==========
[TOC]

### 个人信息
*****
姓名：朱亦文<br>
学号：19302010075

[我的GitHub地址](https://github.com/Elaine1908/)
>GitPages地址见仓库描述

### 项目完成情况
****
#### 0.网站设计与整体风格
本网站名称为*Travellers' Paradise*；网站整体色调为紫、灰；整体风格为复古极简风

#### 1.页面制作
**·Home**

1.使用css动画制作实现网站首页高清图片**幻灯片展示**的效果,动画部分代码如下

    @keyframes move {
                        0%, 15% {
                            margin-left: 0;
                        }
                        30%, 45% {
                            margin-left: -580px;
                        }
                        55%, 75% {
                            margin-left: -1060px;
                        }
                        80%, 100% {
                            margin-left:0;
                        }
                    }                               
>将每张图片的宽度设置为580px，五张图片组合成一个横向长图，以百分比来规定改变发生的时间，0% 是动画的开始时间，100% 动画的结束时间, 每隔2秒滚动一次  
                                          
2.在幻灯片轮播图下方是一条表示欢迎的文字，有高亮效果，点击该文字，页面则会跳转至下方的六张缩略图部分(利用锚点实现)    

3.六张缩略图均使用*normal*文件夹中的图片，采用`div`块布局，六张图又全部包含于一个大`div`块中以实现居中布局

4.两个悬浮图标均采用`position: fixed`实现，背景颜色设置为半透明

5.页脚个人彩蛋包括学号与微信头像

**·Browser**

1.使用左右布局 : 左侧边栏漂浮在右侧内容的外边距上
>之后的左右布局均用这种方法实现

2.左侧栏的三个表格设置了固定宽度，右侧Filter一栏没有固定宽度，固在一定程度上可以实现响应式布局

3.所有图片设置阴影，视觉效果更为立体

**·Search**

1.将两个radio的name设置为相同，使得搜索栏变为单选

2.搜索栏的Filter按钮，鼠标移上去会有颜色变化（背景色与字体色颠倒）后面my photo/details/my favorite界面的按钮皆是如此

3.搜索结果中多于文字省去采用了如下实现方法：

    text-overflow: ellipsis;
    overflow: hidden;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp:3;
    height: 120px;
    line-height: 25px;
其中`-webkit-line-clamp:3`为浏览器显示的行数(?)

**·Details**

设置图片的宽高，高清大图显示；图片底部为图片名称与拍摄者名字

**·My photos & My favorites**

1.以`div`为单位布局，每个`div`的模式为左侧图片，右侧标题+描述，下侧分割线

2.图片均为超链接

**·Upload**

上传图片区域设置左外边距略大于右外边距，实现图片上传后的居中效果；上传图片前，按钮右侧提示：未选择图片，上传后该文字则变为图片名称

**·Log in & Sign up**

1.页面图标均选自*font-awesome*矢量图并将其放大

2.表单居中：采用设置左右相同的外边距，设置表单宽度百分比，同时设置min-width的方式

>但是这么做有一个问题：当屏幕缩小到宽度小于两侧外边距之和时，表单实际上就并不能真正地居中。所以这种情况下该怎么做呢...

3.footer：这两个页面内容较少，需要将footer固定在最下方，我使用了`position:absolute`的方法

#### 2.Bonus
**·图片裁剪**

我在网上搜索到资料说对img文件设置` object-fit: cover;`可以实现在固定宽高的情况下任意大小图片自适应的效果（默认选取中间部分）在代码中也有所尝试

**·响应式布局**

网站上大部分的元素宽度都是用百分比设置的，在我的电脑屏幕上可以正常显示

该网站可以在比我的屏幕宽度更小的屏幕上实现响应式布局，在更大的屏幕上我没有尝试过，但，说不定也可以呢

#### 3.建议

期待PJ2的精彩故事~（误


