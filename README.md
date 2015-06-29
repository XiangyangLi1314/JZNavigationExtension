# JZNavigationExtension
The "UINavigationController+JZExtension" category integrates some convenient features and open some hide functions for UINavigationController.
___
"UINavigationController+JZExtension"分类为UINavigationController集成了许多方便的功能点，同时为它打开了一些隐藏功能。
# Features【功能】
* [To gives you a fullscreen interactivePopGestureRecognizer](#FPG)
* [To hides navigation bar when the view controller is pushed on to a navigation controller](#HNBP)
* [To Push/PopViewController With Blocks](#PWB)
* [To change navigation/tool bar background alpha](#NBTA)
* [To change navigation/tool bar size](#NBTS)

# Overview

![overview](https://raw.githubusercontent.com/JazysYu/JZNavigationExtension/master/Snapshots/JZNavigationExtensionDemo.gif)

#	Why JZNavigationExtension?
* Pop Gesture Works Perfect With UITableView【全屏Pop手势完美匹配UITableView无冲突】
* Enable or disable property for each view controller conveniently.【简单地针对每一个Controller开关属性】
* Pushes/Pops a view controller when hides/shows navigation bar display soomthly【当控制器做Push/Pop时无缝、平滑地显隐导航栏】
* Release some restrictions make your navigation controller stronger【解除一些限制，使你的导航控制器更加强大】
* Follow Apple's API design principles,uses as natural
 as system api【遵循Apple Inc的API设计原则，使用就像系统API一样自然】

# Usage

[To gives you a fullscreen interactivePopGestureRecognizer](id:FPG)【打开全屏Pop手势】:

``` objc
navigationController.fullScreenInteractivePopGestureRecognizer = YES;
```
___

[To hides navigation bar when the view controller is pushed on to a navigation controller](id:HNBP)【支持转场隐藏、显示导航栏】:
``` objc
UIViewController *viewController = [UIViewController new];
viewController.hidesNavigationBarWhenPushed = YES;
[self.navigationController pushToViewController:viewController animated:YES];
```
___

[To Push/Pop view controller With blocks](id:PWB)【导航控制器转场回调】:
``` objc
[self.navigationController pushViewController:viewController animated:YES completion:^(BOOL finished) {
		///Do any thing
}];
```
___

[To adjust navigation/tool bar background alpha](id:NBTA)【调节导航控制器的导航栏、工具条透明度】:

``` objc
navigationController.navigationBarBackgroundAlpha = yourAlpha;
```
___

[To change navigation/tool bar size](id:NBTS)【改变导航控制器的导航栏、工具条大小】:

``` objc
[navigationController setNavigationBarSize:size];
```

or you can also change their frame.size manually 【你也可以手动改变它们的frame】

``` objc
CGRect rect = self.navigationBar.frame;
rect.size = navigationBarSize;
self.navigationBar.frame = rect;
```
___

# Installation
#### Use cocoapods

``` ruby
pod 'JZNavigationExtension'
```

#### Manually
Drag all source files under floder JZNavigationExtension to your project.

``` objc
JZNavigationExtension.h			JZNavigationExtension.m
```