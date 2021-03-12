# Basic Markdown Syntax

> Overview over the most common and basic markdown commands and their syntax. Intended as a quick reference and showcase (cheatsheet).

## Table of Contents

<details>
  <summary>Click to show TOC</summary>

  <p>

- [Basic Markdown Syntax](#basic-markdown-syntax)
  - [Table of Contents](#table-of-contents)
  - [Headlines](#headlines)
<!-- [Headline level 1](#headline-level-1)
  - [Sub headline (level 2)](#sub-headline-level-2)
    - [Sub headline (level 3)](#sub-headline-level-3)
      - [Sub headline (level 4)](#sub-headline-level-4)
        - [Sub headline (level 5)](#sub-headline-level-5)
          - [Sub headline (level 6)](#sub-headline-level-6)-->
  - [Paragraphs](#paragraphs)
  - [Emphasizing text](#emphasizing-text)
  - [Horizontal Rules](#horizontal-rules)
  - [Links](#links)
    - [Linking to Heading IDs](#linking-to-heading-ids)
    - [Linking objects (like images)](#linking-objects-like-images)
  - [Images](#images)
    - [Loading images from local file system](#loading-images-from-local-file-system)
    - [Loading images from remote URL](#loading-images-from-remote-url)
    - [Images as Link](#images-as-link)
  - [Table of contents (TOC)](#table-of-contents-toc)
    - [Create TOC manually](#create-toc-manually)
    - [Using VS Code plugin Markdown All in One](#using-vs-code-plugin-markdown-all-in-one)
  - [Markdown plugins for Visual Studio Code](#markdown-plugins-for-visual-studio-code)
  - [Tables](#tables)
  - [Lists](#lists)
    - [Unordered lists<a name="unordered-lists">](#unordered-listsa-nameunordered-lists)
    - [Nested unordered lists](#nested-unordered-lists)
    - [Ordered lists](#ordered-lists)
    - [Checklists](#checklists)
    - [Numbered Lists](#numbered-lists)
      - [Manually counted list items](#manually-counted-list-items)
      - [Auto counted list items](#auto-counted-list-items)
      - [Nested numbered list (auto count)](#nested-numbered-list-auto-count)
    - [Bullet list](#bullet-list)
    - [Resources list](#resources-list)
    - [Definition lists](#definition-lists)
  - [Blockquotes](#blockquotes)
    - [Blockquotes with multiple paragraphs](#blockquotes-with-multiple-paragraphs)
    - [Nested blockquotes](#nested-blockquotes)
  - [Backslash escapes for special characters](#backslash-escapes-for-special-characters)
  - [CODE](#code)
    - [Single lines of code](#single-lines-of-code)
    - [Code blocks](#code-blocks)
      - [Line indention](#line-indention)
      - [Backticks or tildes](#backticks-or-tildes)
        - [Enclosing with backticks](#enclosing-with-backticks)
        - [Enclosing with tilde characters](#enclosing-with-tilde-characters)
    - [Code highlighting](#code-highlighting)
  - [CREDITS](#credits)
  - [License](#license)

</p>
</details>

## Headlines

***markdown***

```markdown
# Headline            (level 1)
## Sub headline       (level 2)
### Sub headline      (level 3)
...                      ...
###### Sub headline   (level 6)
```

***result***

# Headline level 1
## Sub headline (level 2)
### Sub headline (level 3)
#### Sub headline (level 4)
##### Sub headline (level 5)
###### Sub headline (level 6)

## Paragraphs

> To create paragraphs, use a blank line to separate one or more lines of text. Unless the paragraph is in a [list](#lists), don’t indent paragraphs with spaces or tabs.

***markdown***

```markdown
I really like using Markdown.

I think I'll use it to format all of my documents from now on.
```

***result***

I really like using Markdown.

I think I'll use it to format all of my documents from now on.

## Emphasizing text

To emphasize text use:

+ *italic*: use `*italic*` OR `_italic_`
+ **bold**: use `**bold**` OR `__bold__`
+ ***bold and italic***: use `***bold and italic***` OR `___bold and italic___`
+ to *nest one **inside** the other*: use `*nest one **inside** the other*` OR `_nest one __inside__ the other_`
+ ~~strikethrough~~: use `~~strikethrough~~`

Because different markdown interpreters handle underscores different it's best practice to **avoid using underscores** ( \_ ). Use asterisks ( \* ) instead when writing markdown!

## Escaping special characters

> In markdown any special characters are escaped by a leading backslash ( e.g. \\special-char ).

|  character  |                                                       escaped                                                        | description         |
| :---------: | :------------------------------------------------------------------------------------------------------------------: | :------------------ |
|     \\      |                                                         `\\`                                                         | backslash           |
| \`     | \` | backtick (escaping [backticks in code](#escape-backtick-code "Link: how to escape backtick in markdown code block")) |
|     \>      |                                                         `\>`                                                         | greater than        |
|     \*      |                                                         `\*`                                                         | asterisk            |
|     \_      |                                                         `\_`                                                         | underscore          |
|    \{ \}    |                                                        `\{\}`                                                        | curly braces        |
|    \[ \]    |                                                        `\[\]`                                                        | square brackets     |
|    \( \)    |                                                        `\(\)`                                                        | parentheses         |
|     \#      |                                                         `\#`                                                         | hash mark           |
|     \+      |                                                         `\+`                                                         | plus sign           |
|     \-      |                                                         `\-`                                                         | minus sign (hyphen) |
|     \.      |                                                         `\.`                                                         | dot                 |
|     \!      |                                                         `\!`                                                         | exclamation mark    |

## Horizontal Rules

> To create a horizontal rule, use three or more asterisks ( \*\*\* ), dashes ( \-\-\- ), or underscores ( \_\_\_ ) on a line by themselves. The rendered output of all three looks identical.

***markdown***

```markdown
***

---

_________________
```

***result***

***

## Links

```markdown
[Link text](http://some.url.com "Link title")

[Link text](#link-id "Link title")

[Link text<a name="#link-id">](#link-id "Link title")
```

+ [Some test link](http://some.url.com "Link title")
+ [Inner text link](#MAIO-plugin "Inner text link to MAIO plugin")

### Linking to heading IDs

> You can link to headings with custom IDs in the file by creating a standard link with a number sign (#) followed by the custom heading ID.

```markdown
[Heading IDs](#heading-ids)
```

Other websites can link to the heading by adding the custom heading ID to the full URL of the webpage (e.g, [Heading IDs](https://www.markdownguide.org/extended-syntax#heading-ids)).

### Linking objects (like images)

Just enclose the "link part" of an [image link](#images) with another pair of square brackets

```markdown
[![image-alt-text](./images/code-tag.png "Link to CODE section")](#code)
```

[![image-alt-text](./images/code-tag.png "Link to CODE section")](#code)

## Images

### Loading images from local file system

To include an image from the local file system just put a "!" (exclamation mark) in front of a decent markdown [text link](#links). 

```markdown
![alternate image text](./relative/path/to/file.type "Image title")
```

**Output**

![Markdown icon image](./images/markdown.png "Image title")

Alternatively just use "old school" HTML syntax, where you can also set any required image dimensions:

```html
<img src="./images/markdown.png" width="75">
```

**Output**

<img src="./images/markdown.png" width="75">

### Loading images from remote URL

```markdown
![image-alt-text](http://url.to.image "Image title")
```

![image alt-text](http://url.to.image "Image title")

### Images as Link

```markdown
[![image-alt-text](http://url.to.image "Image title")](#link-URL)
```

[![image-alt-text](http://url.to.image "Image title")](#link-URL)

## Table of contents (TOC)

### Create TOC manually 

+ ...

### Using VS Code plugin [Markdown All in One](MAIO-plugin)

+ navigate to the place in your markdown file where you want to have your TOC created and set your cursor there
+ press **Shift + Command + P** to open the VSCode command prompt
+ type >**Create Table of Contents** => DONE
+ TOC is automatically updated on file save by default

## Markdown plugins for Visual Studio Code

+ <img src="https://yzhang.gallerycdn.vsassets.io/extensions/yzhang/markdown-all-in-one/3.4.0/1605323530575/Microsoft.VisualStudio.Services.Icons.Default" width="24px" height="24px" /> [Markdown All in One<a name="MAIO-plugin" />](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one "Get Markdown All in One plugin on Visual Studio Marketplace") (Visual Studio Marketplace)

+ <img src="https://raw.githubusercontent.com/goessner/mdmath/master/img/icon.png" width="24px" height="24px" /> [Markdown + Math<a name="MM-plugin">](https://marketplace.visualstudio.com/items?itemName=goessner.mdmath "Get Markdown + Math plugin on Visual Studio Marketplace") (Visual Studio Marketplace)

+ <img src="https://davidanson.gallerycdn.vsassets.io/extensions/davidanson/vscode-markdownlint/0.39.0/1613431006608/Microsoft.VisualStudio.Services.Icons.Default" width="24px" height="24px" /> [markdownlint<a name="ML-plugin">](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint "Get markdownlint plugin on Visual Studio Marketplace") (Visual Studio Marketplace)

## Tables

**markdown**

```markdown
| left | center | right |
| :--- | :----: | ----: |
| 1    |   2    |     3 |
| 4    |   5    |     6 |
| 7    |   8    |     9 |
```

* If you have the [Markdown All in One](#MAIO-plugin) plugin installed you can format a table like so:
  * First mark the table, then press 'Shift + Command + F' to format the table

**result**

| left | center | right |
| :--- | :----: | ----: |
| 1    |   2    |     3 |
| 4    |   5    |     6 |
| 7    |   8    |     9 |

## Lists

> Lists are a way to structure data. They allow us to group sets of related items. Lists can be "nested" (you can have lists inside lists).

### Unordered lists<a name="unordered-lists">

> Unordered lists are lists whose elements are not related to each other (nor numerically neither alphanumerically). List items of unordered lists are marked as bullets (small black circles) by default.
> 
> To start an **unordered list** simply start a new line using one of the following three indicating characters: asterisk ( \* ), minus ( \- ) or plus ( \+ ) character. Those indicators can be mixed.

**markdown**

```markdown
* an asterisk ( \* ) starts an unordered list
+ alternatively use the ( \+ ) character for an unordered list
- the minus character ( \- ) can also be used for an unordered list
```

**result**

* an asterisk ( \* ) starts an unordered list

+ alternatively use the ( \+ ) character for an unordered list

- the minus character ( \- ) can also be used for an unordered list

### Nested unordered lists

> Unordered lists can be nested. The indicating characters can also be mixed when nested.

**markdown**

```markdown
* Level 1, Item 1 using an asterisk ( \* )
  * Level 2, Item 1 using an asterisk ( \* )
    * Level 3, Item 1 using an asterisk ( \* )
    + Level 3, Item 2 using the ( \+ ) character
    - Level 3, Item 3 using the ( \- ) character
  + Level 2, Item 2 using the ( \+ ) character
  - Level 2, Item 3 using the ( \- ) character
+ Level 1, Item 2 using the ( \+ ) character
- Level 1, Item 3 using the ( \- ) character
```

**result**

* Level 1, Item 1 using an asterisk ( \* )

  * Level 2, Item 1 using an asterisk ( \* )

    * Level 3, Item 1 using an asterisk ( \* )

    + Level 3, Item 2 using the ( \+ ) character

    - Level 3, Item 3 using the ( \- ) character

  + Level 2, Item 2 using the ( \+ ) character

  - Level 2, Item 3 using the ( \- ) character

+ Level 1, Item 2 using the ( \+ ) character

- Level 1, Item 3 using the ( \- ) character

### Ordered lists

> To start an ordered list, write this:

**markdown**

```markdown
1. this starts a list *with* numbers
+  this will show as number "2"
*  this will show as number "3."
9. any number, +, -, or * will keep the list going.
    * just indent by 4 spaces (or tab) to make a sub-list
        1. keep indenting for more sub lists
    * here i'm back to the second level
```

**result**

1. this starts a list *with* numbers
+  this will show as number "2"
*  this will show as number "3."
9. any number, +, -, or * will keep the list going.
    * just indent by 4 spaces (or tab) to make a sub-list
        1. just keep indenting for more sub lists
    * here i'm back to the second level

### Checklists

> To start a check list, write this:

**markdown**

```markdown
- [ ] this is not checked
- [ ] this is not checked too
- [x] but THIS is checked
```

**result**

- [ ] this is not checked
- [ ] this is not checked too
- [x] but ***THIS*** is checked

### Numbered Lists

#### Manually counted list items

**markdown**

```markdown
1. Level 1, Item 1
2. Level 1, Item 2
3. Level 1, Item 3
```

**result**

1. Level 1, Item 1
2. Level 1, Item 2
3. Level 1, Item 3

#### Auto counted list items

> Start every new list item on a new line with indicator symbol "1." to auto increment the numbering.

**markdown**

```markdown
1. Level 1, Item 1
1. Level 1, Item 2
1. Level 1, Item 3
```

**result**

1. Level 1, Item 1
1. Level 1, Item 2
1. Level 1, Item 3

#### Nested numbered list (auto count)

> Nested list with auto counted list items.

**markdown**

```markdown
1.  Level 1, Item 1

    1.  Level 2, Item 1

            func emptyFunc() { }

        ***

    1.  Level 2, Item 2

    1.  Level 2, Item 3

1.  Level 1, Item 2

    1.  Level 2, Item 1

        1.  Level 3, Item 1
        1.  Level 3, Item 2
        1.  Level 3, Item 3

    1.  Level 2, Item 2

    1.  Level 2, Item 3

1.  Level 1, Item 3
```

**result**

1.  Level 1, Item 1

    1.  Level 2, Item 1

            func emptyFunc() { }

        ***

    1.  Level 2, Item 2

    1.  Level 2, Item 3

1.  Level 1, Item 2

    1.  Level 2, Item 1

        1.  Level 3, Item 1
        1.  Level 3, Item 2
        1.  Level 3, Item 3

    1.  Level 2, Item 2

    1.  Level 2, Item 3

1.  Level 1, Item 3

### Bullet list

**markdown**

```markdown
- paragraph:

  - with:

    linebreak (1 line space between)

  - and here:
    without linebreak
```

**result**

- paragraph:

  - with:

    linebreak (1 line space between)

  - and here:
    without linebreak

### Resources list

...

### Definition lists

**markdown**

```markdown
First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.
```

**result**

First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.

## Blockquotes

To create a blockquote, add a ">" (greater than character) in front of a paragraph.

**markdown**

```markdown
> Dorothy followed her through many of the beautiful rooms in her castle.
```

**result**

> Dorothy followed her through many of the beautiful rooms in her castle.

### Blockquotes with multiple paragraphs

**markdown**

```markdown
> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```

**result**

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

### Nested blockquotes

Blockquotes can be nested. Add a >> in front of the paragraph you want to nest.

```markdown
> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```

> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

## CODE

### Single lines of code

```markdown
`a single line of code`
```

`single line code block`

### Code blocks

To create code blocks, there are several ways.

#### Line indention

Indent every line of the block by at least four spaces or one tab.

**Markup**

~~~markdown
....{
......"firstName": "John",
......"lastName": "Smith",
......"age": 25
....}
~~~

**Output**

    {
      "firstName": "John",
      "lastName": "Smith",
      "age": 25
    }

#### Backticks or tildes

To form code blocks in Markdown, the code can be enclosed between certain special characters. This is why these code blocks are called "fenced code blocks".

##### Enclosing with backticks

To enclose the code you want to display use ***three backticks*** (```) followed by a ***linebreak*** at the beginning *and* the end of your code.

**Markdown**

~~~markdown
```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
~~~

**Output**

```markdown
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

##### Enclosing with tilde characters

To enclose the code you want to display use ***three tilde characters*** (~~~) followed by a ***linebreak*** at the beginning *and* the end of your code.

**Markdown**

```markdown
~~~
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
~~~
```

**Output**

~~~markdown
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
~~~

### Code highlighting

Many markdown processors support syntax highlighting for fenced code blocks. This feature allows you to add color highlighting for whatever language your code was written in. To add syntax highlighting, specify a language next to the backticks or tildes before the fenced code block.

+ [Samples](https://sourceforge.net/p/tabulator/wiki/markdown_syntax/#md_ex_code "External link")
+ [Link](https://www.markdownguide.org/extended-syntax/#syntax-highlighting)

JSON code

~~~markdown
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
~~~

**Output**

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

HTML code

~~~markdown
```html
<ul>
  <li>
    <a href="#">My code</a>
  </li>
</ul>
```
~~~

**Output**

```html
<ul>
  <li>
    <a href="#">My code</a>
  </li>
</ul>
```

JavaScript code

~~~markdown
```js
const Complex = require('Complex');
console.log(new Complex(3, 4).abs()); // 5
```
~~~

**Output**

```js
const Complex = require('Complex');
console.log(new Complex(3, 4).abs()); // 5
```

Python code

~~~markdown
```py
#!/usr/bin/python
import abc
```
~~~

**Output**

```py
#!/usr/bin/bash
import abc
```

Script code with leading shebang (here: bash script)

~~~markdown
```bash
#!/usr/bin/bash

# maintain bash profiles that work on BOTH, Linux and MacOS
[[ -f ~/.bashrc ]] && . ~/.bashrc
```
~~~

**Output**

```bash
#!/usr/bin/bash

# maintain bash profiles that work on BOTH, Linux and MacOS
[[ -f ~/.bashrc ]] && . ~/.bashrc
```

## CREDITS

> For more complete info, please see:

- [Markdown Guide](https://www.markdownguide.org/)
- [John Gruber's original markdown spec](https://daringfireball.net/projects/markdown/)
- [GitHub Flavoured Markdown Spec](https://github.github.com/gfm/)
- [Basic writing and formatting syntax in GitHub](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax)
- [Online Markdown editor "Dillinger"](https://dillinger.io/)

## License

Published under the [MIT Licence](LICENSE.md)
