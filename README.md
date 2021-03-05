# Basic Markdown Syntax

alksd flkasdjhf lkasdjhf 

# Table of Contents
- [Basic Markdown Syntax](#basic-markdown-syntax)
- [Table of Contents](#table-of-contents)
- [Headlines](#headlines)
- [Emphasizing text](#emphasizing-text)
- [Horizontal Rules](#horizontal-rules)
- [Text links](#text-links)
- [Images](#images)
  - [Loading images from local file system](#loading-images-from-local-file-system)
  - [Loading images from remote URL](#loading-images-from-remote-url)
  - [Images as Link](#images-as-link)
- [Table of contents (TOC)](#table-of-contents-toc)
  - [VS Code Plugins for editing markdown files](#vs-code-plugins-for-editing-markdown-files)
  - [Tables](#tables)
    - [markdown](#markdown)
    - [result](#result)
- [Lists](#lists)
  - [Unordered lists](#unordered-lists)
  - [Ordered lists](#ordered-lists)
  - [Checklists](#checklists)
  - [Numbered List (auto count)](#numbered-list-auto-count)
    - [markdown](#markdown-1)
    - [result](#result-1)
  - [Example: Terminating a Callout Using Two Empty Lines (auto count)](#example-terminating-a-callout-using-two-empty-lines-auto-count)
  - [List termination](#list-termination)
    - [List A](#list-a)
    - [List B](#list-b)
  - [Nested list](#nested-list)
  - [Bullet list](#bullet-list)
  - [Backslash escapes for special characters](#backslash-escapes-for-special-characters)
  - [CODE](#code)
    - [Code blocks](#code-blocks)
    - [Code highlighting](#code-highlighting)
  - [CREDITS](#credits)
  - [License](#license)

# Headlines
```
# Headline
## Sub headline
### Sub sub headline
```

# Emphasizing text

To emphasize text use:
* *italic*: use `*italic*` or `_italic_`
* **bold**: use `**bold**` or `__bold__`
* ***bold and italic***: use `***bold and italic***` or `___bold and italic___`
* to *nest one **inside** the other*: use `*nest one **inside** the other*` or `_nest one __inside__ the other_`

Attention: it's **best practice** for markdown to **avoid using unserscores** (_) instead of asterisks (*) because different interpreters handle them diofferent, especially when used inside words like 

# Horizontal Rules
To create a horizontal rule, use three or more asterisks (***), dashes (---), or underscores (___) on a line by themselves.
```
***

---

_________________
```

The rendered output of all three looks identical:

# Text links
```
[Link text](http://some.url.com "Link title")

[Link text](#inner-text-link "Link title")

[Link text<a name="#inner-text-anchor">](#inner-text-link "Link title")
```
+ [Some test link](http://some.url.com "Link title")
  
+ [Inner text link](#MAIO-plugin "Inner text link to MAIO plugin")

# Images

To include an image, just put a "!" in front of a text link:

## Loading images from local file system
```
![image-alt-text](... "Image title")
```
![image-alt-text]( "Image title")

## Loading images from remote URL
```
![image-alt-text](http://url.to.image "Image title")
```
![image-alt-text](http://url.to.image "Image title")

## Images as Link
```
[![image-alt-text](http://url.to.image "Image title")](#link-to-URL)
```
[![image-alt-text](http://url.to.image "Image title")](#link-to-URL)


# Table of contents (TOC)
* using "Markdown All in One" plugin for VSCode:
  + navigate to the place in your markdown file where you want to have your TOC created and set your cursor there
  + press **Shift + Command + P** to open the VSCode command prompt
  + type >**Create Table of Contents** => DONE
  + TOC is automatically updated on file save by default


## VS Code Plugins for editing markdown files
<!-- ![](https://yzhang.gallerycdn.vsassets.io/extensions/yzhang/markdown-all-in-one/3.4.0/1605323530575/Microsoft.VisualStudio.Services.Icons.Default) -->
+ [Markdown All in One<a name="MAIO-plugin">](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one "Get Markdown All in One plugin on Visual Studio Marketplace")

<!-- ![](https://raw.githubusercontent.com/goessner/mdmath/master/img/icon.png) -->
+ [Markdown + Math<a name="MM-plugin">](https://marketplace.visualstudio.com/items?itemName=goessner.mdmath "Get Markdown + Math plugin on Visual Studio Marketplace")


## Tables
### markdown
```
| left | center | right |
| :--- | :----: | ----: |
| 1    |   2    |     3 |
| 4    |   5    |     6 |
| 7    |   8    |     9 |
```
* press 'Shift + Command + F' to format the table

### result
| left | center | right |
| :--- | :----: | ----: |
| 1    |   2    |     3 |
| 4    |   5    |     6 |
| 7    |   8    |     9 |

# Lists

## Unordered lists

To start an unordered list simple use one of the following characters:
+ \* an asterisk starts an unordered list
+ \* and this is another item in the list
+ \+ alternatively use the \+ character to start an unordered list
+ \- the \- character can also be used to start an unordered list

## Ordered lists
To start an ordered list, write this:
```
1. this starts a list *with* numbers
+  this will show as number "2"
*  this will show as number "3."
9. any number, +, -, or * will keep the list going.
    * just indent by 4 spaces (or tab) to make a sub-list
        1. keep indenting for more sub lists
    * here i'm back to the second level
```

## Checklists
To start a check list, write this:
```
- [ ] this is not checked
- [ ] this is not checked too
- [x] but THIS is checked
```

- [ ] this is not checked
- [ ] this is not checked too
- [x] but THIS is checked

## Numbered List (auto count)
### markdown
```
1. one
1. two
1. three
```

### result
1. one
1. two
1. three

## Example: Terminating a Callout Using Two Empty Lines (auto count)

1.  First list, item 1
1.  First list, item 2


1.  Second list, item 1

## List termination

### List A

1.  Item 1, List A
1.  Item 2, List A

### List B

1.  Item 1, List B

## Nested list

1.  Level 1, Item 1

    1.  Level 2, Item 1

            func emptyFunc() { }

        ***

    1.  Level 2, Item 2

1.  Level 1, Item 2

## Bullet list

- paragraph:

  - with:

    linebreak (1 line space between)

  - and here:
    without linebreak

- ## Ressources list:
  - one
  - two

## Backslash escapes for special characters
\\   backslash
\`   backtick (escape backtick character in [code](#escape-backtick-code "Link: how to escape backtick in markdown code block"))
\*   asterisk
\_   underscore
\{\}  curly braces
\[\]  square brackets
\(\)  parentheses
\#   hash mark
\+   plus sign
\-   minus sign (hyphen)
\.   dot
\!   exclamation mark

## CODE

``
`single code line`
`` (with single backticks)

`single line code block`

### Code blocks

To create code blocks, indent every line of the block by at least four spaces or one tab.

` ```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}

``` `
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
### Code highlighting

[Samples](https://sourceforge.net/p/tabulator/wiki/markdown_syntax/#md_ex_code "External Link:")

For example: JSON code

` ```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
``` `

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

## CREDITS

1. one
2. two (`$ git checkout -b my-new-feature`)
3. three

## License

[CC0 1.0 (Public Domain)](LICENSE.md)
