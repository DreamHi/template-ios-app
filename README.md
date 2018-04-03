# template-ios-app
iOS app开发模版


## 用户指南

- [目录结构](#目录结构)
- [工具库](#工具库)


## 目录结构
### 原则
- 主目录结构中，按机能划分（文件太多时），使用group不使用文件夹
- 画面使用.xlb， 不使用Storyboard

### controller中应该放什么代码
Controller
在初始化时，构造相应的 View 和 Model。
监听 Model 层的事件，将 Model 层的数据传递到 View 层。
监听 View 层的事件，并且将 View 层的事件转发到 Model 层。
如果 Controller 只有以上的这些代码，那么它的逻辑将非常简单，而且也会非常短。

### 目录结构

```shell
Classes/
┣ AppDelegate.swift
┣ Protocols/
┣ Enumerations/
┣ Extensions/
┣ Entities/
┣ Models/
┣ ViewControllers/ 
┣ ViewModels/ Services
┣ Views/
┣ Helpers/
┣ Resources/
┣ - Fonts 字体
┣ - Images 图片
┣ - Sounds 声音
┣ - Videos 视频
┗ Vendors/

```

|文件夹	| 说明 |
|---------|------------------------|
|Protocols|协议|
|Enumerations|枚举类型|
|Extensions|扩张既存类。文件名格式<対象+目的>.swift。|
|Entities|本地数据库保存。|
|Models|网络请求数据，restAPI等|
|ViewControllers|初期化view， 监听事件|
|ViewModels|数据验证，从model获取数据|
|Views|	UIView的子类|
|Helpers|常量，宏，工具类，网络，数据库,共通等|
|Resource|图片，视频，声音等|
|Vendors|第三方的类库|

## 工具库
### 选择原则
* 少（尽可能少使用）
* 热（流行，社区强大）
* 稳（版本稳定）

#### lib
- http: Alamofire
- coreData: Realm
- JSON: SwiftyJSON
- QUICK （单体测试）
- UI测试（TODO）
