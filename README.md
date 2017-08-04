# react-native-keyboardmanager
keyboardmanager
Usage

Step 1 - install

npm install react-native-keyboardmanager --save  || yarn add react-native-keyboardmanager
Step 2 - link

react-native link
Step 3 - import and use in project

AppDelegate 导入 #import <IQKeyboardManager.h>

在didFinishLaunchingWithOptions导入下面三句代码:
[[IQKeyboardManager sharedManager] setEnable:YES];
[IQKeyboardManager sharedManager].shouldResignOnTouchOutside = YES;
[[IQKeyboardManager sharedManager] setKeyboardDistanceFromTextField:10.f];
