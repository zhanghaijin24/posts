---
title: "mac"
date: 2021-07-23T16:05:32+08:00
draft: true
---
# 安装mac系统Mojave
通过command-R重装，得到的系统就算重装前的系统

通过option-command-R重装，得到的系统就是最新系统

通过shift-command-R重装，得到的系统就是刚买时的出厂系统

***command-R***
 [![安装](http://101.201.197.193/images/2021/02/03/85A1BF9A-7693-4A4F-A1D4-AAED27EBD017.jpg)](http://101.201.197.193/image/spO)

 [![格式化磁盘](http://101.201.197.193/images/2021/02/03/3C01983E-64E4-434F-AD09-C2AAA610A570.jpg)](http://101.201.197.193/image/gnI)

[![选择磁盘](http://101.201.197.193/images/2021/02/03/AE4C8AF5-59FA-4D30-8336-E0AD9B6F7FC1.jpg)](http://101.201.197.193/image/BMR)

 [![抹掉磁盘选择](http://101.201.197.193/images/2021/02/03/2111DE5A-819F-435D-992E-E98E6C036687.jpg)](http://101.201.197.193/image/77x)

 [![抹掉磁盘配置](http://101.201.197.193/images/2021/02/03/435C59F2-3FFA-4358-AB2D-978B24143F88.jpg)](http://101.201.197.193/image/CIc)
 
 [![抹掉磁盘完成](http://101.201.197.193/images/2021/02/03/724AF29F-0720-4B1C-B7B9-BDD41C4783BA.jpg)](http://101.201.197.193/image/Hii)
 
 [![抹掉磁盘退出](http://101.201.197.193/images/2021/02/03/7EC34458-BE23-47FF-91DB-6FC2A806F05F.jpg)](http://101.201.197.193/image/kdP)

 [![重新安装](http://101.201.197.193/images/2021/02/03/228D04BD-55F3-4C04-80EF-4EA62848E766.jpg)](http://101.201.197.193/image/5u3)


# 安装fzf
---
- git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
- ~/.fzf/install
*安装fd*
- brew install fd
*~/.zshrc 配置fzf*
- 
- 

# 安装ranger
---
- tar -vxf ranger-stable.tar
- cd /usr/local/bin
- ln -s /Users/zhanghaijin/Downloads/ranger/ranger.py ranger


# Mac使用终端格式化U盘
---
- diskutil list
- sudo diskutil eraseDisk FAT32 MYUSB MBRFormat /dev/disk2

# 安装homebrew
---
- /bin/zsh -c "$(curl -fsSL https://gitee.com/jyotish/HomebrewCN/raw/master/Homebrew.sh)"
- git config --global http.postBuffer 924288000
- git -C /usr/local/Homebrew/Library/Taps/homebrew/homebrew-core fetch --unshallow
-  git -C /usr/local/Homebrew/Library/Taps/homebrew/homebrew-cask fetch --unshallow
- export HOMEBREW_CORE_GIT_REMOTE="https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-core.git"

- export HOMEBREW_BOTTLE_DOMAIN="https://mirrors.tuna.tsinghua.edu.cn/homebrew-bottles"

# 安装ohmyzsh
- brew install zsh
- cat /etc/shells
- chsh -s /bin/zsh
- reboot

- git clone https://gitee.com/zhanghaijin24/ohmyzsh.git ~/.oh-my-zsh
- cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc

- git clone https://gitee.com/zhanghaijin24/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting

- git clone https://gitee.com/zhanghaijin24/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions

***修改.git/config***
将gitee修改成github
- cd .git/config

=======
# 安装hexo以及nodejs
---
- brew install node
- sudo npm install -g hexo-cli
- cd cd zhanghaijin24.github.io
- sudo npm install
- sudo npm install hexo-deployer-git

# 安装neovim
---
- brew install neovim

*下载vim-plug*
- cd /Users/zhanghaijin/.config/nvim
- git clone  --depth 1 https://github.com/junegunn/vim-plug.git
- mv vim-plug autoload 

* 安装coc.nvim*
- brew install node 
- sudo npm i -g neovim yarn
-

***mac安装pip***
- sudo easy_install pip

***mac安装pip3***
- curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
- python3 get-pip.py

***GIT创建公匙，并放置远程库***
1，Git配置
- git config --global user.name "zhanghaijin24"
- git config --global user.email "zhanghaijin24@163.com"
2,生成公匙
- ssh-keygen -t rsa -C "zhanghaijin24@163.com"

- cd ~/.ssh
复制id_rsa.pub到gitee设置 SSH keys

***添加SSH可信列表***
- ssh -T git@gitee.com

- ssh-add id_rsa

# Mac OS 更换pip3国内源
---
- cd ~
- mkdir .pip
- nvim pip.conf
```
[global]
index-url = http://mirrors.aliyun.com/pypi/simple/
[install]
trusted-host=mirrors.aliyun.com
```

# nvim导入github
- cd .config/nvim/
- git status
- git add .
- git commit -m "first commit"
- git remote -v
- git push origin

# 在Linux VPS搭建V2Ray
- wget https://git.io/v2ray.sh
- chmod +x v2ray.sh
- ./v2ray.sh
```
1.安装
1.TCP
端口：10086
后面默认回车
```
firewall-cmd --zone=public --add-port=10086/tcp --permanent
firewall-cmd --query-port=10086/tcp
systemctl restart firewalld
```

