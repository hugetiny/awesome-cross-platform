前端跨平台框架的对比思考

试过很多跨平台框架，踩过很多坑后想思考整理一下。
Taro等实际只支持web和小程序的框架不考虑在内（无rn的UI框架）

| 框架   | Flutter  | Quasar | uni-app | react native |
|  ----  | ----  |   ----  | ----  | ----  |
| Windows/macOS/Linux  | 3.0起全支持 | Electron | 无 | 微软windows方案、社区macOS方案 |
| Android/iOS  | 支持 | Capacitor/Cordova | Hybird/webview/weex | 支持 |
| Web | 支持 | Vue | Vue/无宽屏框架或者案例 | react |
| 官方UI框架 | Material/Cupertino 自带全屏幕 | 自带全屏幕 | 自带竖屏 | 社区|
| 小程序（中国特有）| 不支持 | 不支持 | 最全支持 | Taro有方案编译，但是没有UI框架 |
| 后端集成方案 | Firebase深度 | Firebase插件 | 阿里腾讯提供的小程序云 | 无 |



### Flutter
跨平台框架性能最好，社区热度最高。但是桌面平台刚刚支持，功能支持的不多，无法像Electron那样做出成熟的桌面应用（底部托盘，顶部菜单，右键菜单等等功能）。

### 小程序
如果考虑跨平台小程序，只有uni-app可以选择，如果不考虑小程序，推荐Flutter/Quasar。

### Firebase和后端集成
对于小团队来说后端集成对于开发效率太重要了。
Flutter会深度集成Firebase，当然firebase有很多替代supabase等。Flutter应该体验会最好，可惜国内无法访问。
国内serverless没有集成的是分开的云函数/云数据库这一套，uni-app前端有组件直接访问操作数据库，不需要写js的方案。
