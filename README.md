# weibo_v6 微博美化样式

## 说明

我非常喜欢的 weibo 美化样式 [weibo_v6](https://userstyles.org/styles/106272/weibo-v6) 因不明原因被其作者删除，本着互联网分享精神，我把备份文件分享出来，因为我觉得有非常多的朋友喜欢并需要。

不用它之前，微博的界面是这样的：

![](https://i.loli.net/2019/01/17/5c40474a4d4ee.png)

用了之后，界面就变成这样了：

![](https://i.loli.net/2019/01/17/5c4047a0904e6.png)

当然如果需要的话，你可以配合 [Yet Another Weibo Filter](https://tiansh.github.io/yawf/zh-cn.html) 之类的脚本做一些自定义设置。使功能/界面更符合自己的偏好：

![](https://i.loli.net/2019/01/17/5c4048a069b09.png)

## 准备

1. 安装 Chrome 或者 FireFox 等现代浏览器：

2. 在浏览器上安装 [Stylish](https://github.com/stylish-userstyles/stylish) 或者 [Stylus](https://github.com/openstyles/stylus) 插件，我推荐安装后者。

## 应用样式（以 Stylus 为例）

1. 在浏览器中打开 Stylus 插件，点击“编写新样式”：

   ![](https://i.loli.net/2019/01/19/5c42f1d30d8b1.png)

2. 将 [Stylish.Stylus.css](https://github.com/XIJINIAN/weibo_v6/blob/master/Stylish.Stylus.css) 中的内容粘贴到输入框，点击“覆盖样式”：

   ![](https://i.loli.net/2019/01/19/5c42f2ba2594f.png)

3. 输入名称“weibo_v6”后，点击“保存”（你可以输入你喜欢的任何名称）：

   ![](https://i.loli.net/2019/01/19/5c42f38e982ef.png)

## 其他说明

使用最新版 [Yet Another Weibo Filter(Version 4.0.46)](https://tiansh.github.io/yawf/zh-cn.html) 的时候发现，它和本样式有冲突，导致微博 feeds 流右侧多出了一块空白，解决办法是注释掉 Yet Another Weibo Filter 中的一句代码：

```css
html .B_index .WB_frame #plc_main,
html .B_message .WB_frame #plc_main,
html .B_discover .WB_frame #plc_main,
html .B_page .WB_frame #plc_main {
  /* 这里注释掉 */
  /* width: calc(var(--yawf-feed-width) + var(--yawf-right-width)) !important; */
}
```
