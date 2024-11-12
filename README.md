# Node.js

* [官网](https://nodejs.org/zh-cn)
* [下载](https://nodejs.org/zh-cn/download/package-manager)
* [文档](https://nodejs.org/docs/latest/api/)

## 安装

### Windows

powershell

设置脚本执行策略

* Restricted: 默认设置
* AllSigned: 已签名
* RemoteSigned: 未签名

```shell
#
Get-ExecutionPolicy
#
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
#
Get-ExecutionPolicy -List
#
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

安装fnm&node

```shell
winget install Schniz.fnm
#  %USERPROFILE%\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1
mkdir %USERPROFILE%\Documents\WindowsPowerShell
echo fnm env --use-on-cd ^| Out-String ^| Invoke-Expression > %USERPROFILE%\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1
fnm use --install-if-missing 22
node -v
npm -v
```

### Linux/Mac

```shell
curl -fsSL https://fnm.vercel.app/install | bash
source ~/.bashrc
fnm use --install-if-missing 22
node -v
npm -v
```
