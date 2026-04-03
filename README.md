# Flutter 表单（TextField + InputDecoration）

## 简介

单列 **`TextField`**，使用 `InputDecoration` 设置 `labelText` 与 `OutlineInputBorder`，外包 `Padding`。演示「最小输入框样式」而非整套 `Form` + `GlobalKey` 校验（可在此基础上扩展）。

## 快速开始

### 环境要求

Flutter SDK。

### 运行

```bash
flutter pub get
flutter run
```

## 概念讲解

### 第一部分：`TextField` 与 `TextFormField`

`TextField` 适合自控 `TextEditingController`；若要和 `Form` 校验集成，多用 `TextFormField`。

### 第二部分：`InputDecoration`

`labelText` 为浮动标签，`border` 控制描边形态。可继续加 `hintText`、`errorText`、`prefixIcon` 等。

## 完整示例

见 `lib/main.dart`：`Padding` + `TextField`。

## 注意事项

- 键盘遮挡可考虑 `Scaffold.resizeToAvoidBottomInset`、滚动视图。
- 校验与提交请接 `validator`、`onFieldSubmitted` 或状态管理。

## 完整讲解（中文）

表单往往被想得太重：**先有一个好看的输入框**，再谈校验、焦点链、提交按钮。这个 Demo 只停在第一步，避免一上来就 `FormField` 全家桶劝退。等你需要「点提交才标红」这类行为，再把 `TextFormField` 和外层 `Form` 接上即可。
