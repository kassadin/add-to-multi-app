https://github.com/flutter/flutter/wiki/Add-Flutter-to-existing-apps

1. 创建 android 项目
2. 创建 flutter module
3. 更新 flutter module, 生成 .android 项目及 gradle 部分
4. 配置 android app
    setting.gradle
    ```gradle
    setBinding(new Binding([gradle: this]))
    evaluate(new File(
            settingsDir,
            'flutter_module/.android/include_flutter.groovy'
    ))
    ```
    
    app/build.gradle 
    ```gradle
          implementation project(':flutter')
    ```
    
5. 复制 .android MainActivity 到 android，替换为 app 首页


```
Found extracted resources res_timestamp-1-1569346267916
Resource version mismatch res_timestamp-1-1569346310986
Extracted baseline resource assets/flutter_assets/kernel_blob.bin
Extracted baseline resource assets/flutter_assets/vm_snapshot_data
Extracted baseline resource assets/flutter_assets/isolate_snapshot_data
```