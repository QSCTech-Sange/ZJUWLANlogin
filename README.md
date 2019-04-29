# ZJUWLAN 自动登录 （Engilsh Version in the following）

>  由于最（一）近（直）校园网有线网网络频繁波动，我开始转向无线网日常使用和开发，所以想要一个自动登陆的脚本，看了很多github上已有的仓库，都比较复杂（当然也是更全面更周到啦），想要一个简单的zjuwlan登录脚本，遂建了这个仓库，希望能够帮到大家:)

这个 repo 的目的很简单——让我们向

![1556537115516](C:\Users\jimmy\AppData\Roaming\Typora\typora-user-images\1556537115516.png)

说再见吧！

## 使用帮助

### 我不是小白

1. 在终端中获取仓库

```shell
$ git clone https://github.com/QSCTech-Sange/ZJUWLANlogin.git
$ cd ZJUWLANlogin
```

2. 修改 `.ps1` （针对 Windows 用户）或 `.sh` （针对 Mac OS/Linux）的文件，相应位置填入你的用户名和密码。

3. 对 Windows 用户而言(使用PowerShell)

```powershell
$ .\ZJUWLANlogin.ps1
```

> 第一次使用可能需要开启能够执行 .ps1 文件的权限

对 Mac OS/Linux 用户而言，

```shell
$ sh ZJUWLANlogin.sh
```

即可。



### 我是小白

那就不要用 git 了——

#### Windows 用户

1. 使用记事本新建一个文件，里面输入（可复制）

```powershell
Invoke-WebRequest -Uri "https://net.zju.edu.cn/include/auth_action.php" -Method "POST" -Body "action=login&username=YOURID&password=YOURPASSWORD&ac_id=3&user_ip=&nas_ip=&user_mac=&save_me=0&ajax=1"
```

请注意上面的 YOURID 和 YOURPASSWORD 这两处请替换为你的学号和zjuwlan的连接密码。

2. 然后用一个你喜欢的名字保存它，注意扩展名要设置为 `.ps1` ——这是PowerShell 能够运行的脚本的文件拓展名。

> 以上两步也可以简化为
>
> 1. 在这个仓库中下载 ZJUWLANlogin.ps1
> 2. 使用记事本编辑它，修改 YOURID 和 YOURPASSWORD 这两处请替换为你的学号和zjuwlan的连接密码。

2. 每次双击它即可直接登录。我建议建立一个Windows 任务计划，使得每次连接 ZJUWLAN 都能自动登录。



#### Mac OS / Linux 用户

1. 使用记事本新建一个文件，里面输入（可复制）

```shell
curl  -d  "action=login&username=YOURID&password=YOURPASSWORD&ac_id=3&user_ip=&nas_ip=&user_mac=&save_me=0&ajax=1"  https://net.zju.edu.cn/include/auth_action.php
```

请注意上面的 YOURID 和 YOURPASSWORD 这两处请替换为你的学号和zjuwlan的连接密码。

2.  然后用一个你喜欢的名字保存它，注意扩展名要设置为 `.sh` ——这是 Shell 能够运行的脚本的文件拓展名。

> 以上两步也可以简化为
>
> 1. 在这个仓库中下载 ZJUWLANlogin.sh
> 2. 使用记事本编辑它，修改 YOURID 和 YOURPASSWORD 这两处请替换为你的学号和zjuwlan的连接密码。

2.  每次双击它即可直接登录。我建议建立一个Mac OS / Linux 任务计划，使得每次连接 ZJUWLAN 都能自动登录。



# 五一快乐！ 玩得开心！

# ZJUWLAN auto-login

> Due to the frequent crash of  ZJU’s wired network recently(always),  I started to turn to the wireless network for daily use and development. So I am in need of an auto login script. I have seen many existing repos on GitHub, many of which are too complicated (and of course more comprehensive and thoughtful). So here is a super simple zjuwlan login script, hoping to help you:)

The purpose of this repo is simple - let’s 