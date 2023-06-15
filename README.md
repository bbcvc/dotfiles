## windows平台

### 快捷访问文件夹 
> 在Windows操作系统中，使用两个百分号（%%）括起来的语法是环境变量的表示方式。

- %USERPROFILE%：用户文件夹路径（例如C:\Users\username）。
- %TEMP%或%TMP%：临时文件夹路径。
- %SystemRoot%：Windows系统文件夹路径（通常为C:\Windows）。
- %ProgramFiles%：默认程序文件夹路径（例如C:\Program Files）。
- %ProgramFiles(x86)%：64位Windows上32位应用程序的默认文件夹路径（例如C:\Program Files (x86)）。
- %PUBLIC%：公共文件夹路径（例如C:\Users\Public）。
- %APPDATA%：用户的应用程序数据文件夹路径 。

这些环境变量可以方便地访问各种系统和用户相关的文件夹路径，同时也可以在脚本或批处理文件中使用。

### 装机软件
1. scoop安装软件的软件，带有桶(Bucket)功能方便管理其他软件
```bash
# PowerShell terminal
> Set-ExecutionPolicy RemoteSigned -Scope CurrentUser # Optional: Needed to run a remote script the first time
> irm get.scoop.sh | iex
```

2. chocolatey也是安装软件的软件，有些scoop下不到的软件可以用choco安装
```bash
Set-ExecutionPolicy Bypass -Scope Process -Force;
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072;
iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

3. 命令行配置
- 快速
  安装cmder-full
  ```bash
  scoop install sudo
  sudo scoop install cmder-full
  ```

- 一步一步配置

- cmd or powshell
1. 字体
```bash
# 搜索 nerd fonts，这里选择是的FantasqueSansMono这个字体
scoop search FantasqueSansMono-NF
# 添加 nerd fonts 源
scoop bucket add 'nerd-fonts'
# 安装 nerd fonts
scoop install FantasqueSansMono-NF
```
2. starship(https://starship.rs/)
```bash
winget install starship #or scoop install starship
```
3. clink(仅cmd使用)
```bash
scoop install clink
```



### ssh设置
> 支持git多用户访问的设置

文件夹：%USERPROFILE%/.ssh

```bash
# Private 用户1
Host github.com
HostName github.com
User bbcvc 
IdentityFile C:\\Users\\username\\.ssh\\id_rsa_github

# Private 用户2
Host gitlab.xxx.com
HostName gitlab.mycyclone.com
User chenglong.xing
IdentityFile C:\\Users\\username\\.ssh\\id_rsa
```

### cmd
其实可以安装cmder, 只是最快捷提升cmd体验的方法
参考文章：https://zhuanlan.zhihu.com/p/71706782
```bash
scoop install sudo # 提升权限
sudo scoop install cmder-full -g
```

cmder集成了git clink(命令行提示 补全 历史记录工具)


### 其他的
1. nushell(https://www.nushell.sh/zh-CN/)