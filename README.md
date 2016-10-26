# 前端开发人员的开发环境配置
## mac篇
###  homebrew
[homebrew](http://brew.sh)
mac上的软件管理工具，可以安装很多东西。使用需墙外网速。
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
$ echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.bash_profile
$ brew doctor
$ brew update
$ brew upgrade

$ brew search node #搜索
$ brew install node #安装
```
###  alfred
[alfred](https://www.alfredapp.com/)
替换系统的spotlight,取消spotlight的快捷键，设置Alfred的快捷键

###  terminal
[iterm2](https://www.iterm2.com/)
替换系统终端

iterm2->preferences->profiles 

colors
选择配色方案，修改颜色。

text
设置字体，大小

### zsh
mac自带zsh，在terminal中设置 
终端->偏好设置->描述文件->shell 


修改启动命令，选择-zsh

### oh-my-zsh
[oh-my-zsh](http://ohmyz.sh/)
``` 
$ sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)" 
```

pure-theme.zsh 配色方案 [pure](https://github.com/sindresorhus/pure)

- 1 npm install -g pure-prompt
- 2 down sources
```
    ln -s /usr/pure/pure.zsh /usr/local/share/zsh/site-functions/prompt_pure_setup
    ln -s /usr/pure/async.zsh /usr/local/share/zsh/site-functions/async
    ln -s /usr/pure/pure.zsh ~/.oh-my-zsh/custom/themes/pure.zsh-theme
``` 
- 3 vim .zshrc
```
#.zshrc

#change
ZSH_THEME="pure"

#add
autoload -U promptinit; promptinit

# optionally define some options
PURE_CMD_MAX_EXEC_TIME=10

prompt pure

```