# autoComplie
自动打包

 http://blog.csdn.net/xjh093/article/details/78688112 
 
 xcode9打包报错：xcrun: error: unable to find utility "PackageApplication", not a developer tool or in PAT
 
 
 Xcode升级到8.3后 用命令进行打包 提示下面这个错误
 xcrun: error: unable to find utility "PackageApplication", not a developer tool or in PATH
 
 后面根据对比发现新版的Xcode少了这个PackageApplication
 先去找个旧版的Xcode里面copy一份过来
 放到下面这个目录：
 
 /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/usr/bin/
 
 
 然后执行命令
 
 sudo xcode-select -switch /Applications/Xcode.app/Contents/Developer/
 
 chmod +x /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/usr/bin/PackageApplication
 
