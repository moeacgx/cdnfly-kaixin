# cdnfly-kaixin
仅支持CENTOS7
web目录为云端验证文件，请自行搭建

wget https://raw.githubusercontent.com/Steady-WJ/cdnfly-kaixin/main/web/web.tar.gz

tar -zxvf web.tar.gz

0.0.0.0改成(自己搭建的验证服务器IP)
nano /etc/hosts

0.0.0.0  auth.cdnfly.cn

主控登录地址为: http://主控IP/
管理员账号和密码： wenjian/wenjian
普通用户账号和密码： ceshi/ceshi


v5.1.13主控

curl -fsSL https://github.com/Steady-WJ/cdnfly-kaixin/raw/main/master.sh -o master.sh && chmod +x master.sh && ./master.sh --es-dir /home/es

安装好主控需要替换下面板文件，dnfly开心版主控财务系统被删除，可以把这个文件夹替换，还好以前搭建了，刚刚提取出来的，安装好了路径在
/opt/cdnfly/master
下载链接：https://t.me/vpsbbq/17323

v5.1.16被控

curl -fsSL https://github.com/Steady-WJ/cdnfly-kaixin/raw/main/agent.sh -o agent.sh  && chmod +x agent.sh && ./agent.sh --master-ver v5.1.13 --master-ip  --es-ip  --es-pwd 



