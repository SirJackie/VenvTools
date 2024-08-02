# VenvTools

An Python Virtual Environment Migration Toolset.

**<u>注意：运行本程序，请务必使用管理员权限！MAKE SURE YOU RUN THIS WITH ADMIN PRIVILEDGE!</u>**

## 解决了什么痛点？

- Python创建的Venv虚拟环境，是不能通过“剪切粘贴”移动到其他位置的，一旦路径改变，就会出错无法使用
- 并且，需要把Venv从一台电脑，迁移到另一台电脑时，缺乏好的方法（一般使用导出 `requirements.txt` 的方法，但这种方法，恢复时需要网络；并且在没有指定版本的情况下，不能保证恢复后版本完全相同）
- 所以，我设计了一套迁移工具，只需要运行程序，就能导出 `wheels + requirements.txt` 的全量安装包，帮助您轻松迁移Venv！

## 功能介绍

工具集一共包含三个程序，是互相独立的，都可以单独运行：

- `VENV_EXTRACT.bat`：提取Venv的全量安装包（路径需要放在Venv里面使用，和 `Scripts` 目录同文件夹）
- `VENV_REBUILD.bat`：使用全量安装包，重建Venv虚拟环境（重建在这个路径：`./Venv/`）
- `VENV_DESTROY.bat`：销毁当前目录下的Venv（在 `./Venv/`，也就是 `VENV_REBUILD.bat` 创建的位置）

