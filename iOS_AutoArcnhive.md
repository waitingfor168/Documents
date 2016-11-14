iOS自动打包
===========

* **整理：** [吴海金](mailto:632234936@qq.com)
* **日期：** 2016年05月31日
* **更新日期：** 2016年05月31日

目录
---

- 简介；
- 命令;
- 脚本;

内容
---
1. 首先，`cd ~/...`到你的项目的根目录。使用`xcodebuild -h`，或是到[官网](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/xcodebuild.1.html)，查看所有命令。
和使用`xcodebuild -list`，查看项目`Targets`,`Build Configurations`,`Schemes`。

2. 其次，生成xxx.xcarchive文件:

```
xcodebuild -workspace Dream.xcworkspace -scheme Dream -configuration Release -archivePath ~/Desktop/Ipa/Dream.xcarchive archive
```

3. 然后，生成说需要的xxx.ipa 

```
xcodebuild  -exportArchive -archivePath ~/Desktop/Ipa/Dream.xcarchive -exportPath ~/Desktop/Ipa/PuJiangCruise -exportOptionsPlist ~/Desktop/Ipa/exportOptions.plist
```
这里需要的plist文件,内容使用`xcodebuild -h`查看：

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>method</key>
    <string>enterprise</string>
    <key>uploadBitcode</key>
    <false/>
    <key>uploadSymbols</key>
    <true/>
</dict>
</plist>
```

备注
---