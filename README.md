# vagrantfiles

# SoftWare Version
## Host OS
Windows10 Home

## Vagrant-Version
```[command pronpt]
[command pronpt]
vagrant -v
Vagrant 2.2.6
```

## VirtualBox-Version  (if error resume next... this is Path error.)
```[command pronpt]
[command pronpt]
VBoxManage -v
6.0.14r133895
```

# How to use vagrant
### Open command prompt
{Win} + R
```
cmd
```
```[command pronpt]
[command pronpt]
powershell start cmd -verb runas & exit
```
Yes

### On command prompt (path setting :p)
If use VBoxManage
```[command pronpt]
[command pronpt]
set PATH=%PATH%;C:\Program Files\Oracle\VirtualBox\;
```

vagrant get status command
```[command pronpt]
[command pronpt]
vagrant global-status
vagrant global-status --prune
```

VirtualBox get virtual-machine-list command
```[command pronpt]
[command pronpt]
VBoxManage list vms
```

vagrant init,start,restart,shutdown virtual-machine command
```[command pronpt]
[command pronpt]
vagrant init
vagrant up
vagrant reload
vagrant halt
```

vagrant ssh connection command
```[command pronpt]
[command pronpt]
vagrant ssh
```

vagrant plugin command
```[command pronpt]
[command pronpt]
vagrant plugin list
vagrant plugin install {plugin-name1} {plugin-name2}
vagrant plugin uninstall {plugin-name1} {plugin-name2}
```

vagrant plugin @vbguest unmatch version fix command
```[command pronpt]
[command pronpt]
vagrant vbguest --status
vagrant vbguest --do install

#OR

vagrant plugin uninstall vagrant-vbguest
vagrant plugin install vagrant-vbguest
vagrant reload
```

ubuntu 18.04 LTS settings ( CUI(bash) on GUI(Gnome) )
```[bash]
[bash]
#Lock Screen Disable.
gsettings set org.gnome.desktop.lockdown disable-lock-screen true
```

if ubuntu 18.04 LTS use [su -]
```[bash]
[bash]
sudo -i
```

## !WARNING
vagrant deleate virtual-machine command
```
vagrant destory -f {virtual-machine-name}
```

VirtualBox deleate virtual-machine command
```
VBoxManage unregistervm {virtual-machine-name} --delete
```

# Trouble Shooting
## 0001
エラーが出た場合(Windows10 creaters updateのバグ)
'HostInterfaceNetworking-VirtualBox Host-Only Ethernet Adapter' (VERR_INTNET_FLT_IF_NOT_FOUND).
"ネットワークと共有センター" を開く"アダプターの設定の変更" を開く
コマンドプロンプトで↓
```
ncpa.cpl
```
"VirtualBox Host-Only Network #N" のプロパティを開く
"VirtualBox NDIS6 Bridged Networking Driver" にチェックを入れる
"インターネットプロトコル バージョン6(TCP/IPv6)" のチェックを外す
[OK] を押し、プロパティウィンドウを閉じる
"VirtualBox Host-Only Network #N" の右クリックメニューで「無効」にする
再度、「有効」にし直す


