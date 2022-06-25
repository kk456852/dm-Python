# dm-Python

usage:

前提依赖以centos7原生python3为例,存在自身python(例如使用cdc的python解释器)解释器的则忽略
yum install -y python3 gcc python3-devel

1.解压安装包
tar -zxf python-dm.tar.gz

2.添加lib库索引
echo `pwd`/python >> /etc/ld.so.conf
# 刷新并查看lib库索引是否添加
ldconfig -v |grep libdmdpi.so

3. 安装三方库
cd python/dmPython_C/dmPython/ && xxx/python3.x setup.py install

4.验证
xxx/python3.x
import dmPython
无错误则安装成功 