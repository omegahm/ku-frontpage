# ku-frontpage

A LaTeX package for use at University of Copenhagen.

Using the `titlepage` option will resemble as close as possible the official design for Master projects and PhD theses.
The Microsoft Word templates can be found at http://designguide.ku.dk/.

## Installation

Just copy the `ku-frontpage.sty` and the `logos` folder into your current working directory.
You can then include the package with for example:

```latex
\usepackage[english, science, titlepage]{ku-frontpage}
```

## Options

##### Options when including the package

Name       | Available options             | Default     | Notes
---        | ---                           | ---         | ---
Layout     | `titlepage`, `large`, `small` | `titlepage` |
Language   | `english`, `danish`           | `english`   | Will also include the `babel` package with the same option.
Faculty    | `science`, `sund`, `ku`       | `science`   | Will change the logo and text at the top of the page accordingly.
Hyperref?  | `hyperref`                    |             | Enables the hyperref package and sets default.
Drop caps? | `dropcaps`                    |             | Will allow you to include drop caps with `\lettrine{D}{rop caps}`.

##### Commands for changing the text

Name                         | Function                                                                    | Example
---                          | ---                                                                         | ---
`\assignment{...}`           | Sets the assignment type.                                                   | `\assignment{PhD thesis}`
`\author{...}`               | Sets the author.                                                            | `\author{Mads Ohm Larsen}`
`\title{...}`                | Sets the title of the document.                                             | `\title{Quasicrystal Simulation}`
`\subtitle{...}`             | Sets the subtitle of the document.                                          | `\subtitle{An investigation}`
`\date{...}`                 | Sets the date of the document.                                              | `\date{Handed in: \today}`
`\advisor{...}`              | Sets the advisor.                                                           | `\advisor{Advisor: Anders Andersen}`
`\frontpageimage{...}`       | Sets the image for the titlepage                                            | `\frontpageimage{example.png}`
`\kupdfsetup{...}{...}{...}` | Sets various information in the result PDF. Requires the `hyperref` option. | `\kupdfsetup{My title}{My subject}{My name}`

You can disable a command, by setting it to nothing, for example if you do not want a subtitle, you can use `\subtitle{}`.

Three colors are also defined as well as a setting for current color.
These are `KU`, `KUsund`, and `KUscience`.
Using `\KUCOLOR` will give you the current color, as specified by the selected faculty.

## Examples

### Titlepage
The file `example.tex` contains an example of a titlepage LaTeX file, which when compiled should look like this:

![Titlepage](http://i.imgur.com/bWIDLbN.png)

##### Large and small
---
The large and small design can be used for everyday assignments handed in to your TA.

*Large*

![Large design](http://i.imgur.com/EgEkCy2.png)

*Small*

![Small design](http://i.imgur.com/oZ0ZQa6.png)

## Legal

The UCPH logo is protected by a European patent.
For more information go to the official design guide: http://designguide.ku.dk/ku/om_design/varemaerkebeskyttelse/
