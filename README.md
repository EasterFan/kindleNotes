## 项目说明

这是一个使用 python 语言编写的项目，用于将 kindle 笔记导出为网页文件。kindle Clippings 终极管理大法，替代 clipplings.io! 😘
本项目模仿自[https://github.com/cyang812/kindleNote](https://github.com/cyang812/kindleNote)。

## 使用说明
> 首先要保证你的机器安装了 `python3` 环境，macos 系统自带了 python 2.7.16 版本（不适合开发），安装 python3 用 homebrew 只需要 ** brew install python ** 即可，homebrew 会自动选择合适的 pip

```bash
# 1. 进入此项目根目录
cd kindleNotes

# 2. 从 kindle 中拷贝出标注文件，重命名为 source.txt，并替换成此项目根目录下的 source.txt 文件

# 3、在 Python3 环境下执行 `python demo.py` 指令，等待生成网页文件。
#（如果报错`TypeError: 'encoding' is an invalid keyword argument for this function`,需要执行 `python3 demo.py` 指令）
```

## TODO

- [ ]  笔记和标注作样式上的区分
- [ ]  新建一个 source_backup 文件夹， 导出 My Clippings.txt 文件时，每一个 txt 文件只保存一本书的标注，
生成 html 文件时，先将 source_backup 文件夹中所有的 txt 文件合并成一个 source 文件，然后到处成 html  
（这主要是因为 kindle 的 DRM 保护， 限制了标注数量，只能删掉先前的标注，所以需要将每本书存放在单独的 txt 文件中，方便做 txt 文件的版本管理）
bre



## 注意！
如果报错：  

要检查 txt 文件 是不是有多余的空行（直接导入 My Clipplings 不会出现这个问题，如果手动编辑过 My Clipplings 需要注意一下）:  

![](https://raw.githubusercontent.com/easterfan/picgo/master/blingbling/2020/20200403100317.png)
