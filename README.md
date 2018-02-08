## resign
ipa重签名工具 支持签名Watch和Plugins

只需 签名证书+mobileprovsion文件即可完成重签名

## 使用效果

 ![image](https://github.com/kevll/resign/blob/master/screenshots/effect.png)

## 如何使用

命令行输入：
```
resign -i xxx.ipa -c "iPhone Developer: xxx(xxx)" -p ~/Desktop/xxx_dev.mobileprovision
```

可选参数：
-o <output-file-path>           重签名后的文件输出路径
-e <entitlements-file-path>  entitlements.plist文件路径
-b <new-bundle-identifier>  新的bundleId
-h                                          显示帮助信息
-v                                          显示版本号

详细使用说明：
```
Usage: resign -i <input.ipa> -c "<certificate-name>" -p <provision-file-path>

where options are:
-o <output-file-path>       resigned file output path
-e <entitlements-file-path> entitlements.plist path
-b <new-bundle-identifier>  new bundle id match with mobileprovsion
-h                          show help information
-v                          show resign tool version
```

## 如何安装
1. 命令行输入：(推荐)
```
brew tap kevll/resign && brew install resign
```
2. clone仓库或者下载resign.tar.xz，解压缩resign.tar.xz文件，然后在命令行使用解压后的resign

3.clone仓库或者下载resign.py，使用python3运行

## 如何同时注入dylib到ipa
1.先使用[inject_dylib](https://github.com/kevll/inject_dylib)注入dylib到ipa</br>
2.再使用resign进行签名打包

## Hope

如果觉得有用，欢迎star</br>
如果使用发现问题，欢迎issue
