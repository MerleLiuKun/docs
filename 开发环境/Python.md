## 使用 pyenv 配置环境

#### 依赖安装

- Debian/Ubuntu 系列

```
sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev \
libreadline-dev libsqlite3-dev llvm libncurses5-dev libncursesw5-dev \
xz-utils tk-dev libffi-dev liblzma-dev python-openssl
```

- CentOS/Fedora/RHEL 系列

```
sudo yum install @development zlib-devel bzip2 bzip2-devel readline-devel sqlite \
sqlite-devel openssl-devel xz xz-devel libffi-devel findutils
```

#### 安装 pyenv

使用官方提供的安装脚本进行安装

```
curl https://pyenv.run | zsh
# 等同于
curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | zsh
```

命令完成之后，重启 `shell` ：

```
exec $SHELL
```

#### 常见命令

升级 `pyenv` ：

```
pyenv update
```

查看当前可安装的 `Python` 版本：

```
pyenv install --list
```

安装指定版本的 `Python` 环境：

```
pyenv install 3.8.1
```

#### 卸载 pyenv

`pyenv` 安装在 `$PYENV_ROOT` 目录下，默认是 `~/.pyenv`。卸载只需要删除该目录即可：

```
rm -rf ~/.pyenv
```

移除 `.zshrc` 中的配置：

```
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

重启 `shell` ：

```
exec $SHELL
```
