# vimix

参考 [k-vim](https://github.com/wklken/k-vim)

### 安装

运行 __./install.sh__ 即可，如需缩短安装插件的时间，可以注释掉vimrc.bundles中相关耗时插件的行，如 _Bundle 'Valloric/YouCompleteMe'_

### 快捷键

	逗号 , 表示 <leader>

关闭方向键移动光标，强制使用hjkl

上排F功能键

	F5  粘贴模式开关

	F6  换行开关

	F7  语法开关

	F8  显示行号开关

	F9  tagbar

分屏窗口移动

	ctrl + h/j/k/l

搜索

 	<space>  空格，进入搜索状态

按键修改

	kj         代替<esc>

 	Y	       复制到行尾

 	H          跳转到行首，等同于^

 	L          跳转到行尾，等同于$

 	U          取消回退编辑操作，等同于ctrl-r

 	;          替换 : ，直接进入命令模式

 	<leader>q  退出vim

 	<leader>w  保存文件

 	<leader>v  选中段落

 	ctrl-n     切换相对/绝对行号

---

### 插件介绍

1. [Vundle](https://github.com/VundleVim/Vundle.vim)
	插件管理，具体添加插件参见vimrc.bundles的实现，命令模式下使用PluginInstall来安装添加的插件

2. [vim-man](https://github.com/vim-utils/vim-man)
	在vim使用查看man手册，命令模式下 Man printf，会分屏显示printf的说明手册

3. [syntastic](https://github.com/scrooloose/syntastic)
	静态语法检查插件，<leader>s 来打开/关闭当前文件的错误列表

4. [YouCompleteMe](https://github.com/Valloric/YouCompleteMe)
	代码自动补全插件(需vim版本高于7.3.5并支持python2)，需要手动安装一下，下载好该插件后，进入vimix/bundle/YouCompleteMe目录，执行 ./install.sh --clang-completer

	函数跳转快捷键：

		<leader>jd  跳转函数定义处
		<leader>gd  跳转函数声明处

5. [ultisnips](https://github.com/SirVer/ultisnips) 和 [vim-snippets](https://github.com/honza/vim-snippets)
	快速定义代码片段，快捷键如下：

		ctrl + j/k  上一个/下一个
		<tab>       使用片段
		<leader>us  编辑对应文件类型的代码片段

6. [delimitMate](https://github.com/Raimondi/delimitMate)
	自动补全单引号、双引号

7. [closetag](https://github.com/docunext/closetag.vim)
	自动补全html、xml的标签

8. [nerdcommenter](https://github.com/scrooloose/nerdcommenter)
	快速添加/取消注释，快捷键设置如下：

		<leader>cc    添加注释
		<leader>cu    取消注释

9. [vim-repeat](https://github.com/tpope/vim-repeat)
	使用 . 重复之前的vim操作

10. [vim-surround](https://github.com/tpope/vim-surround)
	帮助快速添加、去除和修改环绕字符

11. [vim-trailing-whitespace](https://github.com/bronson/vim-trailing-whitespace)
	去除行尾空格，使用 <leader\><space\>

12. [vim-easy-align](https://github.com/junegunn/vim-easy-align)
	赋值语句对齐，常用快捷设置

		<leader>a=		    对齐等号表达式
		<leader>a2<space>  	第二个空格对齐
		<leader>a*<space>  	所有空格依次对齐

13. [vim-easymotion](https://github.com/easymotion/vim-easymotion)
	强大的光标移动插件，使用<leader\><leader\>m(b)来进行基础跳转移动

14. [matchit](https://github.com/vim-scripts/matchit.zip)
	括号匹配跳转， 使用 %

15. [vim-signature](https://github.com/kshenoy/vim-signature)
	标记以及跳转

		m[a-zA-Z]		添加标签
		'[a-zA-Z]       跳转到标签
		'.				最后一次变更的位置
		''				跳回到跳转之前的位置
		m<space>        去除所有标签

16. [ctrlp](https://github.com/kien/ctrlp.vim)
	文件搜索插件，在当前目录进行检索

		<leader>p        打开ctrlp检索
		<leader>f        显示最近打开的文件
		ctrl + j/k       进行上下移动
		ctrl + v/x       分屏打开该文件
		ctrl + t         在新tab中打开该文件

17. [ctrlp-funky](https://github.com/tacahiroy/ctrlp-funky)
	文件内的函数搜索插件

		<leader>fu        在当前文件内进行指定的函数搜索
		<leader>fU        搜索光标对应单词的函数

18. [ctrlsf](https://github.com/dyng/ctrlsf.vim)
	全局搜索字符串

		\			  全局搜索光标所在单词
		<leader>so    打开搜索结果面板，使用<space>进行跳转打开

19. [vim-fugitive](https://github.com/tpope/vim-fugitive) 和 [vim-gitgutter](https://github.com/airblade/vim-gitgutter)
	git相关，使用<leader\>ge进行当前文件的diff比对

20. [vim-airline](https://github.com/bling/vim-airline)
	状态栏增强显示插件

21. [rainbow_parentheses](https://github.com/kien/rainbow_parentheses.vim)
	括号显示增强插件

22. [molokai](https://github.com/tomasr/molokai)
	Sublime的经典主题

23. [nerdtree](https://github.com/scrooloose/nerdtree)
	目录树导航，使用<leader\>n进行打开和关闭

24. [vim-ctrlspace](https://github.com/szw/vim-ctrlspace)
	基于tab的buffer管理插件

		ctrl-<space>		得到当前tab的buffer列表
		j/k                 上下移动
		回车                 选择打开
		v/s                 分屏打开
		<esc>               关闭buffer列表
		d                   删除buffer

25. [tagbar](https://github.com/majutsushi/tagbar)
	文件结构大纲显示，使用F9打开/关闭

26. [vim-tmux-navigator](https://github.com/christoomey/vim-tmux-navigator)
	tmux分屏下的vim之间可以直接使用ctrl + h/j/k/l来进行切换

26. 编程语言相关

	[pyflakes](https://github.com/kevinw/pyflakes-vim)

	[python-syntax](https://github.com/hdima/python-syntax)

	[vim-markdown](https://github.com/tpope/vim-markdown)

	[vim-javascript-syntax](https://github.com/jelera/vim-javascript-syntax)

	[vim-javascript](https://github.com/pangloss/vim-javascript)

	[emmet-vim](https://github.com/mattn/emmet-vim)

	[lua](https://github.com/vim-scripts/lua.vim)

	[vim-misc](https://github.com/xolox/vim-misc)

	[vim-lua-ftplugin](https://github.com/xolox/vim-lua-ftplugin)

---