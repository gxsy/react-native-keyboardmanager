# react-native-keyboardmanager

keyboardmanager
Usage

Step 1 - install
```
npm install react-native-keyboardmanager --save  || yarn add react-native-keyboardmanager
```

Step 2 - link
```
react-native link
```

Step 3 - import and use in project

AppDelegate 导入
```
#import <IQKeyboardManager.h>
```

在didFinishLaunchingWithOptions导入下面三句代码:
```
[[IQKeyboardManager sharedManager] setEnable:YES];
[IQKeyboardManager sharedManager].shouldResignOnTouchOutside = YES;
[[IQKeyboardManager sharedManager] setKeyboardDistanceFromTextField:10.f];
```

```
首先，我们在前面创建的ReactNative工程下的node_modules创建一个文件夹react-native-BGNativeModuleExample，然后我们在新创建的文件夹下再创建一个ios文件夹。

$ cd TestProject/node_modules
$ mkdir react-native-BGNativeModuleExample
$ cd react-native-BGNativeModuleExample
$ mkdir ios
然后，由于ReactNative的组件都是一个个静态库，我们发布到npm给别人使用的话，也需要建立静态库。我们使用xcode建立静态库，取名为BGNativeModuleExample。建立之后，我们将创建的静态库中的文件全部copy到node_modules/react-native-BGNativeModuleExample/ios目录下。
ios文件目录如下：

|____BGNativeModuleExample
| |____BGNativeModuleExample.h
| |____BGNativeModuleExample.m
|____BGNativeModuleExample.xcodeproj
最后，我们需要手动将这个静态库链接到工程中
```
1、使用xcode打开创建的静态库，添加一行Header Search Paths，值为$(SRCROOT)/../../react-native/React，并设置为recursive。
```
