## 项目说明

这是一个使用 python 语言编写的项目，用于将 kindle 笔记导出为网页文件。kindle Clippings 终极管理大法，替代 clipplings.io! 😘
此项目 fork 自[https://github.com/cyang812/kindleNote](https://github.com/cyang812/kindleNote)。

## 使用说明
> 首先要保证你的机器安装了 `python3` 环境，macos 系统自带了 python 2.7.16 版本（不适合开发），安装 python3 用 homebrew 只需要 ** brew install python ** 即可，homebrew 会自动选择合适的 pip

```bash
# 1. 进入此项目根目录
cd kindleNotes

# 2. 从 kindle 中拷贝出标注文件，重命名为 source.txt，并替换成此项目根目录下的 source.txt 文件

# 3、在 Python3 环境下执行 `python demo.py` 指令，等待生成网页文件。
#（如果报错`TypeError: 'encoding' is an invalid keyword argument for this function`,需要执行 `python3 demo.py` 指令）
```


## 碎碎念

我通常会把一本书的标注整理在一个txt文件，一方面是因为通常一次性只读一本书，标注比较整齐不乱，还有一个原因是kindle的 DRM 限制，每本书的标注不能超过一个百分比，需要删掉以前的标注。

但是生成网页的时候，会希望所有书的标注一次性生成，所以我会把很多书的txt文件手动合并成一个 source_all.txt 文件，然后再运行命令去生成静态网页 - 要注意手动合并的时候不要加入多余的空行，否则会出现下面的报错 👇：

如果报错 `IndexError: list index out of range`：  
![](https://raw.githubusercontent.com/easterfan/picgo/master/blingbling/2020/20200403101719.png)

要检查 txt 文件 是不是有多余的空行（直接导入 My Clipplings 不会出现这个问题，如果手动编辑过 My Clipplings 需要注意一下）:  

![](https://raw.githubusercontent.com/easterfan/picgo/master/blingbling/2020/20200403100317.png)
