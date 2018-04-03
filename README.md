# template-ios-app
iOS app开发模版


## 用户指南

- [目录结构]（#目录结构）


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

|グループ	| 説明 |
|---------|------------------------|
|Protocols|プロトコルを配置する。プロトコル拡張の活用は推奨。|
|Enumerations|列挙型を配置する。その型に属する一般的な分岐処理にはEnumに処理させる（SwiftのEnumを活用する）。|
|Extensions|既存クラスの拡張を記述する。ファイル名は<対象+目的>.swift。|
|Entities|本地数据库保存。|
|Models|网络请求数据，restAPI等|
|ViewControllers|初期化view， 监听事件|
|ViewModels|数据验证，从model获取数据|
|Views|	UIView派生クラスを配置する。|
|Helpers|常量，宏，工具类，网络，数据库,共通等|
|Resource|图片，视频，声音等|
|Vendors|第三方的类库|

