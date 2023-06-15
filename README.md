## windows平台
###快捷访问文件夹 

在Windows操作系统中，使用两个百分号（%%）括起来的语法是环境变量的表示方式。除了%appdata%，还有很多其他的环境变量可以使用，以下是其中一些常见的环境变量及其含义：

- %USERPROFILE%：用户文件夹路径（例如C:\Users\username）。
- %TEMP%或%TMP%：临时文件夹路径。
- %SystemRoot%：Windows系统文件夹路径（通常为C:\Windows）。
- %ProgramFiles%：默认程序文件夹路径（例如C:\Program Files）。
- %ProgramFiles(x86)%：64位Windows上32位应用程序的默认文件夹路径（例如C:\Program Files (x86)）。
- %PUBLIC%：公共文件夹路径（例如C:\Users\Public）。
- %APPDATA%：用户的应用程序数据文件夹路径 。

这些环境变量可以方便地访问各种系统和用户相关的文件夹路径，同时也可以在脚本或批处理文件中使用。

### ssh

支持git多用户访问的设置

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

