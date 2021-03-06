# Fcitx输入法皮肤;
## !!警告!!
### 皮肤均来自对***搜狗输入法皮肤***的***移植***,  
### 仅供***个人使用***,切勿用于***商业用途***;

# 部分皮肤演示;
![image](https://imedl.sogoucdn.com/cache/skins/uploadImage/2014/07/02/14042792144232_former.png)

![image](https://imedl.sogoucdn.com/cache/skins/uploadImage/2019/10/25/15719976584269_former.png)

![image](https://imedl.sogoucdn.com/cache/skins/uploadImage/2020/04/07/15862697371423_former.png)

![image](https://imedl.sogoucdn.com/cache/skins/uploadImage/2016/06/28/14671001506148_former.gif)

![image](https://imedl.sogoucdn.com/cache/skins/uploadImage/2019/05/27/15589524354055_former.png)

![image](https://imedl.sogoucdn.com/cache/skins/uploadImage/2019/10/23/15718259392751_former.png)

![image](https://imedl.sogoucdn.com/cache/skins/uploadImage/2019/12/11/15759991576262_former.png)

![image](https://imedl.sogoucdn.com/cache/skins/uploadImage/2019/05/27/15589521991642_former.png)

![image](https://imedl.sogoucdn.com/cache/skins/uploadImage/2019/07/29/15643605903600_former.png)

![image](https://imedl.sogoucdn.com/cache/skins/uploadImage/2019/11/11/15734856135635_former.gif)

![image](https://imedl.sogoucdn.com/cache/skins/uploadImage/2019/07/23/15638527973670_former.gif)

## 使用前须知:
1,本人***精力有限***,如果发现***bug***请先自行研究;  
2,你可以***自由传播***,但请注明我的***github地址***;  
3,请勿用于***商业用途***,以及各种***盈利手段***;  
4,研究不易,好些天觉都没有睡,且用且珍惜;

## 安装教程;
必须工具,***脑子***和***心***;  
(***不管你使用任何GNU/Linux发行版,都可以使用此方法,前提你必须安装好下面这些;***)

#### 安装git
```ruby
Arch/manjaro pacman -Syy git
Debian/Ubuntu  apt-get update && apt-get -y install git
Fedora dnf makecache && dnf -y install git
```

#### 安装fcix
```ruby
Arch { 
pacman -Syy fcitx fcitx-configtool fcitx-googlepinyin
cat << EOF > ~/.xprofile
export GTK_IM_MODULE=fcitx
export QT_IM_MODULE=fcitx
export XMODIFIRS=''@im=fcitx''
EOF
修改/etc/gdm/custom.conf
禁用Wayland,以开启Xorg
}

Debian/Ubuntu {  
apt-get update 
apt-get -y install fcitx fcitx-googlepinyin
}

Fedora { 
dnf makecache 
dnf -y install fcitx fcitx-googlepinyin
}
```

## 安装fcitx皮肤
```ruby
你必须知道的一些配置文件;

/usr/share/fcitx/skin/    #fcitx皮肤系统级目录,次目录放置皮肤,所有用户都可使用;
~/.config/fcitx/skin      #用户级fcitx皮肤目录,仅对当前用户生效;
~/.config/fcitx/conf/fcitx-classic-ui.config  #fcitx皮肤配置文件修改此文件可更换当前用户fcitx皮肤;

复制下面命令在Terminator中运行;
if [ -d ~/.config/fcitx/skin/ ]; then  git clone https://github.com/wo2ni/fcitx-skin.git ~/.config/fcitx/skin; else mkdir -p ~/.config/fcitx/skin &&  git clone https://github.com/wo2ni/fcitx-skin.git ~/.config/fcitx/skin; fi
然后用vim,或nano等,修改~/.config/fcitx/conf/fcitx-classic-ui.config 
fcitx -r  #重启fcitx
Enjoy
```

# 💕特别感谢:💕

|💕Google💕|💕Youtube💕 |💕Github💕 |

- [→ 本人永久的Github地址](https://github.com/wo2ni)
