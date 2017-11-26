<!-- README.md is generated from README.Rmd. Please edit that file -->
remedy
======

`{remedy}` provides addins to facilitate writing in markdown with RStudio.

![](remedy_example.gif)

All the functions are meant to be mapped to keyboard shortcuts. A list of suggested shortcuts is provided towards the end of this README.

> Note that most of the addins/shortcuts below will also work without selecting any text.

Install
-------

``` r
devtools::install_github("ThinkR-open/remedy")
```

Once you've installed the package, you don't need to load it with `library()`, the addins are installed on your machine as part of the package install process.

Using `{remedy}`
----------------

Write quicker in markdown with `{remedy}`!

Here's a list of all available helpers:

![](readme_gif/remedy_example.gif)

### Backtick

Enclose the selected word(s) in backticks.

![](readme_gif/backtick.gif)

### Chunk

Turn the selected text into a chunk.

![](readme_gif/chunck.gif)

### Emphasise

Embolden, italicize or strikethrough the selected text.

![](readme_gif/emphasise.gif)

### Headers

Turn the selected text into a header.

![](readme_gif/header.gif)

### Image

Turn the selected path into an image.

This element is context aware: if you select a text and a link, it turns the text into title between `![]`, and puts the link between `()`.

If the last element of the selection is not a link, you get an error message straight into you markdown document.

![](readme_gif/image.gif)

### LaTeX

LaTeX syntax :

![](readme_gif/latex.gif)

### List

Turn the selected text into an unordered list.

![](readme_gif/list.gif)

### Moving

#### On the right

Copy the selected text or the current line to the right.

![](readme_gif/right.gif)

### Table

Insert a table inside your doc.

There are basically two way to do that with remedy :

#### Empty table

![](readme_gif/table.gif)

#### Parse your data

Turn your dataframe into a markdown table :

![](readme_gif/table_remedy.gif)

### URL

Turn the selected text into an url.

This element is context aware: if you select a text and a link, it turns the text into title between `[]`, and puts the link between `()`.

If the last element of the selection is not a link, you get an error message straight into you markdown document.

![](readme_gif/url.gif)

### xaringan

Insert a xaringan pull-left and pull-right template.

![](readme_gif/xaringan.gif)

Recommended shortcuts
---------------------

Here's a list of recommended shortcuts:

### On mac

You can run `remedy::set_hotkeys` to have the package update for you the hotkey settings for your RStudio IDE. If you want to edit the default settings you can view the defaults `remedy_opts$get('hotkeys')` and change them through `remedy_opts$set(hotkeys=<NEW_SETTINGS>)`.

``` r
remedy::remedy_opts$get('hotkeys')
#>           backtick               bold              chunk 
#>       "Ctrl+Cmd+`"       "Ctrl+Cmd+B"   "Ctrl+Alt+Cmd+C" 
#>         chunksplit                 h1                 h2 
#> "Ctrl+Shift+Alt+C"       "Ctrl+Cmd+1"       "Ctrl+Cmd+2" 
#>                 h3                 h4                 h5 
#>       "Ctrl+Cmd+3"       "Ctrl+Cmd+4"       "Ctrl+Cmd+5" 
#>                 h6              image            italics 
#>       "Ctrl+Cmd+6"       "Ctrl+Cmd+P"       "Ctrl+Cmd+I" 
#>              latex               list              right 
#>       "Ctrl+Cmd+L" "Ctrl+Shift+Cmd+="    "Alt+Cmd+Right" 
#>             strike              table                url 
#>       "Ctrl+Cmd+S"       "Ctrl+Cmd+T"       "Ctrl+Cmd+U" 
#>           xaringan 
#>       "Ctrl+Cmd+X"
```

<!-- 
Due to a [limitation](https://community.rstudio.com/t/keyboard-shortcut-for-addin-in-dcf-file/2753) currently of the IDE you will need to restart the IDE once for the hotkeys to be initialized. 
-->
Feedbacks and enhancement
-------------------------

You've found a bug, or have an enhancment idea? Feel free to open an issue : <https://github.com/ThinkR-open/remedy/issues>.
