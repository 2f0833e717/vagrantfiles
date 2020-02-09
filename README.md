# vagrantfiles

# SoftWare Version
## Host OS
Windows10 Home

## Vagrant-Version
```
vagrant -v
Vagrant 2.2.6
```

## VirtualBox-Version
```
VBoxManage -v
6.0.14r133895
```

# How to use vagrant
### Open command prompt
{Win} + R
```
cmd
```
```
powershell start cmd -verb runas & exit
```
Yes

### On command prompt
If use VBoxManage
```
$set PATH=%PATH%;C:\Program Files\Oracle\VirtualBox\;
```

vagrant get status command
```
vagrant global-status
vagrant global-status --prune
```

VirtualBox get virtual-machine-list command
```
VBoxManage list vms
```

vagrant init,start,restart virtual-machine command
```
vagrant init
vagrant up
vagrant reload
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


