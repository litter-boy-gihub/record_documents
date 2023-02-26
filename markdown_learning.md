# Markdown 语法

[Markdown 基本语法 | Markdown 官方教程](https://markdown.com.cn/basic-syntax/)

---

## 基本语法

1. **标题**

   #和标题之间加空格,######六级标题最小。
2. **段落**

   使用空白行将一行或多行文本进行分隔。
3. **换行**

   直接用回车键，或者使用html语法 `<br>。`
4. **强调**

   *两边一个斜体 两个粗体 三个斜体加粗体。
5. **引用**

   引用块，在段落前加 > 符号，多个段落所有开头都加 >符号，可以嵌套。
6. **列表**

   有序列表，请在每个列表项前添加数字并紧跟一个英文句点。数字不必按数学顺序排列，但是列表应当以数字 1 起始 `<br>。`

   无序列表，请在每个列表项前面添加破折号 (-)、星号 (*) 或加号 (+) 。缩进一个或多个列表项可创建嵌套列表 `<br>。`

   要在保留列表连续性的同时在列表中添加另一种元素，请将该元素缩进四个空格或一个制表符(段落、引用块、代码块、图片、列表 参考 [Markdown 列表语法 | Markdown 官方教程](https://markdown.com.cn/basic-syntax/lists.html) )
7. **代码**

   `cmd /k` 单词或短语表示为代码，请将其包裹在反引号 ` 中。

   代码块，请将代码块的每一行缩进至少四个空格或一个制表符。

   以上不方便，常用围栏代码块，使用三个反引号\``` 或三个~~~来开始和结束。

   ```cpp
   #include<stdio>
   #include<stdlib>
   using namespace std;

   int main(void) {
     return 0;
   }
   ```
8. **分割线**

   创建分隔线，请在单独一行上使用三个或多个星号 (`***`)、破折号 (`---`) 或下划线 (`___`) ，并且不能包含其他内容，为了兼容性，请在分隔线的前后均添加空白行。
9. **链接**

   + 超链接Markdown语法代码：`[超链接显示名](超链接地址 "超链接title")。`

     ```text
     这是一个链接 [Markdown语法](https://markdown.com.cn "最好的markdown教程")。
     ```

     显示效果：这是一个链接 [Markdown语法](https://markdown.com.cn "最好的markdown教程")。
   + 网址和Email

     使用尖括号可以很方便地把URL或者email地址变成可点击的链接。

     ```text
     <https://markdown.com.cn>
     <fake@example.com>
     ```

     [https://markdown.com.cn](https://markdown.com.cn)
   + 引用链接

     引用链接分为两部分：与文本保持内联的部分 及 文件中其他位置的部分

     + 引用第一部分

       使用两组括号 格式： [链接文本][label 可以包含字母、字母、空格、标点]

       两个括号之间可以包含一个空格。
     + 引用第二部分

       第二部分使用以下属性设置格式：

       1. 放在括号中的标签，其后紧跟一个冒号和至少一个空格（例如 `[label]:`）。
       2. 链接URL, 可选放在尖括号<>中。
       3. 链接提示文本， 可选放在双引号/单引号/括号中。

          ```text
          [1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"
          [1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> (Hobbit lifestyles)
          ```
   + URL中的空格用%20代替([https://www.example.com/my%20great%20page](https://www.example.com/my%20great%20page))
10. **图片**

    + 插入图片Markdown语法：`![图片alt](图片链接 "图片title")`。

    ```text
    ![这是图片](https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE53r3m?ver=5d0a "Magic Gardens")
    ```

    ![这是图片](https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE53r3m?ver=5d0a "Magic Gardens")

    + 链接图片语法：

      给图片增加链接，请将图像的Markdown 括在方括号中，然后将链接添加在圆括号中。

      ```text
      [![图片链接](https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE53r3m?ver=5d0a "Shiprock")](https://markdown.com.cn)
      ```

      [![图片链接](https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE53r3m?ver=5d0a "Shiprock")](https://markdown.com.cn)
11. **转义字符**

    显示原本用于格式化 Markdown 文档的字符，在字符前面添加反斜杠 \ 。可以转义的字符：

| Character |                                                              Name                                                              |
| :-------: | :----------------------------------------------------------------------------------------------------------------------------: |
|     \     |                                                           backslash                                                           |
|     `     | backtick (see also[escaping backticks in code](https://markdown.com.cn/basic-syntax/escaping-characters.html#escaping-backticks)) |
|     *     |                                                            asterisk                                                            |
|     _     |                                                           underscore                                                           |
|    { }    |                                                          curly braces                                                          |
|    [ ]    |                                                            brackets                                                            |
|    ( )    |                                                          parentheses                                                          |
|     #     |                                                           pound sign                                                           |
|     +     |                                                           plus sign                                                           |
|     -     |                                                      minus sign (hyphen)                                                      |
|     .     |                                                              dot                                                              |
|     !     |                                                        exclamation mark                                                        |
|          |                                                       pipe管道符无法显示                                                       |

   特殊字符自动转义：

   HTML中有两个字符特殊：`<` 和 `&` 。需要手动转化为实体 `&lt;` 和 `&amp;` 实体。

   如果你使用 `&` 符号的作为 HTML 实体的一部分，那么它不会被转换，而在其它情况下，它则会被转换成 `&amp;`。< 同理。
12. **Markdown内嵌HTML标签**

   如需使用 HTML，不需要额外标注这是 HTML 或是 Markdown，只需 HTML 标签添加到 Markdown 文本中即可。某些应用程序只支持 HTML 标签的子集。

## 拓展标题

1. **表格**

   使用三个或多个连字符（`---`）创建每列的标题，并使用管道（`|`）分隔每列。

   通过在标题行中的连字符的左侧，右侧或两侧添加冒号（`:`），将列中的文本对齐到左侧，右侧或中心。

   表格文本格式化：链接、代码（反引号 ` ）和强调，其他不支持。

   使用表格的HTML字符代码（`&#124;`）在表中显示竖线（`|`）字符。

   ```text
      | Syntax      | Description | Test Text     |
      | :---        |    :----:   |          ---: |
      | Header      | Title       | Here's this   |
      | Paragraph   | Text        | And more      |
   ```
2. **脚注**

   创建脚注参考，请在方括号（`[^1]`）内添加插入符号和标识符。标识符可以是数字或单词，但不能包含空格或制表符。标识符仅将脚注参考与脚注本身相关联-在输出中，脚注按顺序编号。[^1]

   在括号内使用另一个插入符号和数字添加脚注，并用冒号和文本（`[^1]: My footnote.`）
3. **标题编号**

   + 标题ID:    在与标题相同的行上用大括号括起该自定义ID。

     ```text
     ### My Great Heading {#custom-id}
     ```
   + 链接到标题ID(#headid)：

     通过创建带有数字符号（`#`）和自定义标题ID的[标准链接]((/basic-syntax/links.html)，可以链接到文件中具有自定义ID的标题。

     其他网站可以通过将自定义标题ID添加到网页的完整URL（例如 `[Heading IDs](https://markdown.com.cn/extended-syntax/heading-ids.html#headid)`）来链接到标题。
     [拓展](#拓展标题 "拓展标题") 这里在vs code里面没有成功，可能不支持这个拓展。
4. **定义列表**

   创建定义列表，请在第一行上键入术语。在下一行，键入一个冒号，后跟一个空格和定义。

   ```text
   First Term
   : This is the definition of the first term.
   ```
   First Term
   : This is the definition of the first term.

   在VS code里同样没有成功，可能不支持此拓展。
5. **删除线**

   若要删除单词，请在单词前后使用两个波浪号 `~~`。

   ~~世界是平坦的。~~ 世界是圆的。
6. **任务列表语法**

   任务列表使您可以创建带有复选框的项目列表。

   创建任务列表，请在任务列表项之前添加破折号 `-`和方括号 `[ ]`，并在 `[ ]`前面加上空格。要选择一个复选框，请在方括号 `[x]`之间添加 x 。

   ```plaintext
   - [x] Write the press release
   - [ ] Update the website
   - [ ] Contact the media
   ```
   - [X] Write the press release
   - [ ] Update the website
   - [ ] Contact the media
7. **Emoji表情**

   有两种方法可以将表情符号添加到Markdown文件中：将表情符号复制并粘贴到Markdown格式的文本中，或者键入 *emoji shortcodes* 。
8. **自动网址链接

   许多Markdown处理器会自动将URL转换为链接。**

   如果您不希望自动链接URL，则可以通过将URL表示为带反引号的代码来删除该链接。

   `http://example.com`
