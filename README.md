# SunloginClient
ubuntu24.04/mint 提示libgconf-2-4依赖问题, 替换为libwebkit2gtk-4.1-0重新打包


# 下载：https://github.com/SindreYang/SunloginClient/releases/download/0.1/SunloginClient_15.2.0.63064_amd64.deb

# 替换方式：

1.解开deb文件

dpkg-deb -X SunloginClient-10.1.1.38139_amd64.deb sun

2.解开依赖文件

dpkg-deb -e SunloginClient-10.1.1.38139_amd64.deb sun/DEBIAN


3.修改control文件

vim sun/DEBIAN/control


4.修改文件内容
将libwebkitgtk 3.0-0修改为libwebkit2gtk-4.0-37

5.重新进行打包
dpkg-deb -b sun

