# VS Code Editor Technique

Visual Studio Code 使用技巧(Windows)

## 1. 常用快捷键(keyboard shortcuts)

http://www.52cik.com/vscode-keyboard-shortcuts/

| 快捷键            | 命令              |
| ----------------- | ----------------- |
| Ctrl+Shift+P,F1   | 显示命令面板      |
| Ctrl+P            | 快速打开          |
| Ctrl+Shift+N      | 新建窗口/实例     |
| Ctrl+Shift+W      | 关闭窗口/实例     |
| Ctrl+X            | 剪切行 (空选定)   |
| Ctrl+C            | 复制行 (空选定)   |
| Alt+ ↑ / ↓        | 向上/向下移动行   |
| Shift+Alt + ↓ / ↑ | 向上/向下复制行   |
| Ctrl+Shift+K      | 删除行            |
| Ctrl+Enter        | 在下面插入行      |
| Ctrl+Shift+Enter  | 在上面插入行      |
| Ctrl+Shift+\      | 跳到匹配的括号    |
| Ctrl+K Ctrl+C     | 添加行注释        |
| Ctrl+K Ctrl+U     | 删除行注释        |
| Ctrl+/            | 切换行注释        |
| Shift+Alt+A       | 切换块注释        |
| Ctrl+F            | 查找              |
| Ctrl+H            | 替换              |
| F3 / Shift+F3     | 查找下一个/上一个 |
| Shift+Alt+F       | 格式化文件        |
| Ctrl+K Ctrl+F     | 格式化选定代码    |
| F12               | 转到定义          |
| Alt+F12           | Peek 定义         |
| Ctrl+K F12        | 打开定义到侧边    |
| Ctrl+`            | 显示集成终端      |
| Ctrl+Shift+`      | 新建集成终端      |
| Ctrl+N            | 新建文件          |

## 2. 界面概览(Interface overview)

![vs code 界面概览](http://otnjt3h06.bkt.clouddn.com/image/vscode-interface-overiew.png)

速记：

界面概览上所有快捷键以 `Ctrl` + `Shift` 开头，后面跟对应部件名称。

- 文件资源管理器(Explorer)  `E`
- 跨文件搜索(Search) `F` (Find)
- 源代码管理(Source Control) `G` (Git) 。这里需要注意，按完 `Ctrl` + `Shift` + `G` 组合键后，还需要单独在按一次 `G` 键。
- 启动和调试(Debug) `D`
- 管理扩展(Extensions) `X` 。发音像 Ex
- 查看作物和警告(View erros and warning) `M` (Manage)。调出命令终端也能查看。

## 3. 使用命令行(User Command Line)

1. 查看命令行支持的所有参数

```bash
code --help
```

2. 使用已经打开的窗口来打开文件

```bash
code -r filename
```

3. 打开文件并滚动到特定的行和列

```bash
code -r -g <filename:line[:character]>
```

4. 比较两个文件内容

```bash
code -r -d foo.txt bar.txt
```

5. 使用管道，将当前目录所有文件名展示在编辑器里

```bash
ls | code -f -
```



## 4. 双手不离键盘(Use Keyboard)

核心键盘操作：光标移动、文本选择、文本删除、为编辑器命令绑定快捷键

### 1. 光标移动

- 把光标移动到单词的开头或末尾：`Ctrl` + `←` 或 `→` 。
- 把光标移动到行首或行尾：`Home` 或 `End`
- 光标在括号间切换：`Ctrl` + `Shift` + `\`  或 `Ctrl` + `B`。前提是光标在括号的位置
- 移动到文档第一行或最后一行：`Ctrl` + `Home` 或 `End`

### 2. 文本选择

给以上命令多加一个 `Shift` 就可以达到选中光标跳转区间的所有文本。

### 3. 删除操作

- 删除光标后的所有字符：`Shift` + `Windows` + `Delete`
- 删除光标前的所有字符：`Ctrl` + `Shift` + `Backspace`
- 删除单词内的字符：`Ctrl` + `Delete` 删除光标后的字符，`Ctrl` + `Backspace` 删除光标前的字符。
- 删除整行：`Ctrl` + `L`

### 4. 自定义快捷键

打开快捷键面板，搜索所要设置快捷键的命令名，也可以搜索快捷键，然后双击对应条目，在弹出界面上按下快捷键完成设置。

### 5. 一些有用的快捷键

- 整行代码上移或下移：`Ctrl` + `Shift` + `↑` 或 `↓`
- 在上下行添加光标：`Ctrl` + `Alt` + `↑` 或 `↓`
- 选中括号内的内容：需要自定义设置，名称为 Select to Bracket