Vim/Gvim
===

 I found this vim package in[ Here](http://www.oschina.net/code/snippet_574132_13357 "OSChina") and I modify some of the configurations and Add two registry file to add two entry (`open in gvim tab` and `Open with gvim`) in Windows right click context menu.

----------

# For Windows: #
1. After clone the this repo, move this repo directory to where you want to place. 
2. Add the path to system environment variable[path], if you want to using the ctags and cscope.
3. Modify the path string where store the gvim.exe in registry file `EditWithVim-tab.reg`  and  `EditWithVim.reg`. The default is `D:\\software\\gVimPortable\\vim73\\gvim.exe\`
4. Double click the registry files to merge them to system. As the registry file name imply, each of them will add a enty in right click context menu.

# For Linux #

1. Clone this repo. eg: `mkdir ~/github` `cd ~/github` `git clone https://github.com/tonyho/VIM.git`
2. Install the vim(or gvim) using the proper commands, for example in Ubuntu: `sudo apt-get install vim`
3. Install the cscope, ctags and taglist plugin. eg: `sudo apt-get install ctags cscope`
4. Move the _vimrc file to you home directory, and rename it to .vimrc. Or make ln to it `cd ~ && ln -s  ~/github/VIM/_vimrc  .vimrc`
5. Move the vimfiles directory to you home directory, and rename it to .vim,or ln it `ln -s  ~/github/VIM/vimfiles/ .vim` ;then clone the vundle:

 `git clone http://github.com/gmarik/vundle.git ~/.vim/bundle/vundle`
# For Cygwin #
These is no much different between cygwin and linux to use vim.  

# Post clone, we should install the plugins #
Since we use the vundle to manage the plugins, we should install the plugins. Open a terminal, then open the vim:
    `vim`
In Vim, we just call the PluginInstall to let the vundle install all the needed plugins:
    `:PluginInstall`
After do this, the vundle will auto install the plugins. 

If error occurs, use the `l` to see the logs, or save it the a file. Usually, there're 2 kinds of error:
1. Git repo not existed anymore:
    We should search in github to a new repo, see the _vimrc content for reference.
2. Plugin directory already existed in vimfiles/vundle, so just delete it.

About the vundle, you can refer this artcle: [How To Use Vundle to Manage Vim Plugins on a Linux VPS](https://www.digitalocean.com/community/tutorials/how-to-use-vundle-to-manage-vim-plugins-on-a-linux-vps)
    

----------

----------
