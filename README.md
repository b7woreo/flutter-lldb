# flutter-lldb

使用 VsCode 调试运行在 Android 平台上的 Flutter Engine.

## 安装指南

1. 下载源码:
    ```bash
    git clone https://github.com/b7woreo/flutter-lldb.git
    ```

2. 将 `flutter-lldb` 添加到 `PATH` 环境变量中:
    ```bash
    export PATH="path/to/flutter-lldb:$PATH"
    ```

## 使用指南

1. 启动待调试的应用程序.

2. 运行 `flutter-lldb`:
    ```bash
    flutter-lldb \
    --local-engine-src <local-engine-src> \
    --local-engine <local-engine> \
    <package-id>
    ```
    __参数说明__:
    - `local-engine-src`: Flutter Engine 的源码目录, 同`flutter run` 命令使用的值.
    - `local-engine`: 产物目录, 同`flutter run` 命令使用的值.
    - `package-id`: 待调试的应用包名.

3. 将 `flutter-lldb` 输出的 JSON 对象拷贝到在 VsCode 的 `launch.json` 配置中, 选择 `flutter-lldb` 配置并运行.
