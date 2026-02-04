# 小米小白条沉浸模块/Hide-xiaomi-home-indicator-background
## 我很懒，如果你刷入模块后无效，请参考以下自行修改

> 讲真，进我 Group 的有一半人进来就问为什么小白条沉浸模块失效了......
> 
> 这倒是提醒我了，一开始我我在澎湃 2.0.2.0 下测试，我的那个模块还是能用的，但是昨天我更新到了澎湃 2.0.202.0，发现确实不能用了
> 
> 这我能忍？简单查了查发现酷安内好像也没有相关教程，于是乎花了十多分钟研究了一下，是因为在澎湃新系统中小米实际上更换了新的主题目录，导致了旧模块的失效（金凡！！！）。
> 
> 好了前言结束，开始教程

1.首先先在应用好你要用的主题，主题壁纸里的模块混搭也可以，实际上小白条是归模块混搭中的通知栏管的，所以你只要应用好这个就行。👌

![20260204-165840-958c79](https://github.com/user-attachments/assets/561373cb-e70d-4194-9eef-f7af7b59ed27)

2.在 MT 管理器中打开/data/system/theme/目录，长按其中的 framework-res（ps.有些主题没有这个？不要哭，往后看），选择✅打开方式···，点击其中的浏览压缩包。

![20260204-165841-777798](https://github.com/user-attachments/assets/a7ba3713-eac2-4f19-b3ae-75bd4d76b8d5)

3.点击其中的 theme_values.xml，在最底下</MIUI_Theme_Values>之上添加如下代码，右上角保存。
```
<dimen name="navigation_bar_height">0.1dp</dimen>导航栏高度
<dimen name="navigation_bar_height_landscape">0.1dp</dimen>横屏高度
<dimen name="navigation_bar_frame_height">16dp</dimen>范围
<dimen name="navigation_bar_frame_height_landscape">16dp</dimen>横屏范围
```

![20260204-165957-d0a8bb](https://github.com/user-attachments/assets/569ff183-d30e-4ab3-b4c9-019fd9e6c7fe)

4.Stop！你以为现在你就要重启了？（好吧如果你不用深色模式的情况下确实可以保存重启了），继续跟着做，在 framework-res 里创建一个名为 nightmode 的文件夹，把上一步你改好的*.xml 文件复制丢进去，再打开编辑，把第二句的 LightTemplate 改为 NightTemplate，就像这样：

![20260204-165904-ef745c](https://github.com/user-attachments/assets/76ccfaf4-f936-4416-b38c-f33c5750c941)

5.大功告成！保存重启即可～❤️

---

Q&A：
Q:我没有 framework-res 怎么办˃̣̣̥᷄⌓˂̣̣̥᷅？
A：傻啊，你找一个有这个主题，复制一下，再换到你想用的主题，粘贴进去改不就完了

Q:我换了个主题就失效了怎么办˃̣̣̥᷄⌓˂̣̣̥᷅？
A:？？？你猜这是怎么实现的（）

