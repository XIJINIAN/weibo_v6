# weibo_v6 微博美化样式

## update 20190921

修复导航栏下移问题。

## update 20190912

感谢 [MoonFlame](https://github.com/MoonFlame) 同学修复了导航栏下移和微博 logo 缩放的问题。

## 说明

我非常喜欢的 weibo 美化样式 [weibo_v6](https://userstyles.org/styles/106272/weibo-v6) 因不明原因被其作者删除，本着互联网分享精神，我把备份文件分享出来，因为我觉得有非常多的朋友喜欢并需要。如果原作者不想公开分享，请随时联系我删除。

应用这个样式有两种方式，一种是使用 [java.user.js](https://github.com/XIJINIAN/weibo_v6/blob/master/java.user.js)，另一种是使用 [Stylish.Stylus.css](https://github.com/XIJINIAN/weibo_v6/blob/master/Stylish.Stylus.css)。区别不大，**任选其一即可**。

对于文件中的 [java.user.js](https://github.com/XIJINIAN/weibo_v6/blob/master/java.user.js) ，我做了如下修改：① 为防止其在不需要的时候启动，增加了 `@match` 标签；② 为防止被覆盖更新，改了 `@version` 为 `0.20201015123135`。

对于文件中的 [Stylish.Stylus.css](https://github.com/XIJINIAN/weibo_v6/blob/master/Stylish.Stylus.css)，感谢 [thekingofcity](https://github.com/thekingofcity) 同学的 commit。

另：说说我为什么喜欢这个样式吧，不用它之前，微博的界面是这样的：

![](https://i.loli.net/2019/01/17/5c40474a4d4ee.png)

用了之后，界面就变成这样了 orz，好看到炸裂哇：

![](https://i.loli.net/2019/01/17/5c4047a0904e6.png)

当然如果需要的话，你可以配合 [Yet Another Weibo Filter](https://tiansh.github.io/yawf/zh-cn.html) 之类的脚本做一些自定义设置，可以屏蔽更多不想要的东西（如顶栏的用户名），使界面更符合自己的偏好：

![](https://i.loli.net/2019/01/17/5c4048a069b09.png)

## 准备

在应用本样式之前，你需要安装 Chrome 或者 FireFox 等现代浏览器，然后在下面两种应用方式**二选一**：

- 在浏览器上安装自己喜欢的**用户脚本管理器**，如 [Violentmonkey](https://violentmonkey.github.io/)。
- 在浏览器上安装 [Stylish](https://github.com/stylish-userstyles/stylish) 或者 [Stylus](https://github.com/openstyles/stylus) 插件，我推荐安装后者。

## 应用样式

### 使用用户脚本管理器方式（如  [Violentmonkey](https://violentmonkey.github.io/)）

点击  [java.user.js](https://github.com/XIJINIAN/weibo_v6/blob/master/java.user.js) 右上角的 [Raw](https://github.com/XIJINIAN/weibo_v6/raw/master/java.user.js)，再点击“确认安装”即可（感谢 [GregAMO](https://github.com/GregAMO) 同学的补充）：

![](https://i.loli.net/2019/01/19/5c42f00a7aa98.png)

### 使用 [Stylish](https://github.com/stylish-userstyles/stylish) 或者 [Stylus](https://github.com/openstyles/stylus) 方式

本步骤以 Stylus 为例：

1. 在浏览器中打开 Stylus 插件，点击“编写新样式”：

   ![](https://i.loli.net/2019/01/19/5c42f1d30d8b1.png)

2. 将 [Stylish.Stylus.css](https://github.com/XIJINIAN/weibo_v6/blob/master/Stylish.Stylus.css) 中的内容粘贴到输入框，点击“覆盖样式”：

   ![](https://i.loli.net/2019/01/19/5c42f2ba2594f.png)

3. 输入名称“weibo_v6”后，点击“保存”（你可以输入你喜欢的任何名称）：

   ![](https://i.loli.net/2019/01/19/5c42f38e982ef.png)

## 其他说明
使用最新版 [Yet Another Weibo Filter](https://tiansh.github.io/yawf/zh-cn.html) 的时候发现，它 weibo_v6 样式有冲突，导致微博 feeds 流右侧多出了一块空白，解决办法是注释掉 Yet Another Weibo Filter 中的一句代码：

```css
html .B_index .WB_frame #plc_main,
html .B_message .WB_frame #plc_main,
html .B_discover .WB_frame #plc_main,
html .B_page .WB_frame #plc_main {
  // 这里注释掉
  // width: calc(var(--yawf-feed-width) + var(--yawf-right-width)) !important;
}
```
