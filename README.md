# xxe docbook fauthoring project

## Table of contents
<!-- TOC started -->

 * [About](#about)
 * [Limitations](#limitations)
 * [Installation](#installation)
 * [Usage](#usage)
 * [FAQ](#faq)
 * [Status](#status)
 * [Roadmap](#roadmap)
 * [Contributing](#contributing)
 * [Authors](#authors)
 * [License](#license)

<!-- TOC ended -->

## About

xxe-docbook-fauthoring is a simple configuration file for using in conjunction with [XMLMind XML Editor](https://www.xmlmind.com/xmleditor/), XXE for short.

BTW, if you don't aware about what XMLMind XML Editor is suitable for, check out its [FAQ](https://www.xmlmind.com/xmleditor/).

Project's aim is to speed-up an authoring and editing of any DocBook-based documents within XXE.

**NOTE**: BTW, XMLMind XML Editor (XXE, for short) is free for use for any non-commercial and open source projects - see its [license](https://www.xmlmind.com/xmleditor/license_xxe_perso.html) for a details. You can [download](https://www.xmlmind.com/xmleditor/download.shtml) and use it for such projects for free.

## Limitations

Due to author's limited resources this addon works only with a DocBook 5.1 version of a source files (NS-based files). Support of documents v. 5.0 requires some additional alternations (hope to be done later, although not guaranteed). It doesn't support Docbook 4.5 (non NS-awared) documents. In case of high volume feedback from a 4.x users of an addon, author will try to add a v. 4.5 support later. 

## Installation

### Prerequisites

- XXE version 7.3.0 or higher installed and working. For XXE system requirements look at [this page](https://www.xmlmind.com/xmleditor/_distrib/doc/help/installing_xxe.html) 

### Installation ways

xxe docbook fauthoring addon can be installed in three different ways:

1. Built-in direct installation method, using XXE itself (RECOMMENDED!).

2. Manual installation (using prepared `.zip` file - either from XXE's [contribution page](http://www.xmlmind.com/xmleditor/_usercontrib/index.shtml), or from the author's [addon page](http://www.singlesourcing.ru/pub/xxe-addons/xxe-docbook-fauthoring/), or from the [release page](https://github.com/eduardtibet/xxe-docbook-fauthoring/releases) (TBD!)

3. Installation using projects's Github page.

### Built-in direct installation

To install an addon using XXE itself:

1. Open XXE.

2. Choose menuitem **Options|Install Add-ons**. XXE will scan a locations for addons and gives you a list of available addons for the current version of XXE.

3. Search for and click on a checkbox with a **DocBook fast authoring addon** addon name.

4. Press **OK** button.

5. Restart XXE to apply changes.

**NOTE:** For detailed explanation, how to work with an **Install Add-ons** dialog box look at [this page](https://www.xmlmind.com/xmleditor/_distrib/doc/help/wh/com.xmlmind.xmleditapp.app.part.InstallAddonsDialog.html)

### Manual installation

XXE itself has a [perfect help page, describing how to do this](https://www.xmlmind.com/xmleditor/addons.shtml#manual_install).

### Installation using projects's Github page

To install using project's Github page:

1. Close XXE, in case it is running.

2. Locate a user preference directory - [how to locate?](https://www.xmlmind.com/xmleditor/addons.shtml#manual_install)

3. Change a directory to an `addon` folder.

4. Get a project files by directly cloning it to an `addon` folder:

```
$ git clone https://github.com/eduardtibet/xxe-docbook-fauthoring.git
```
5. Start XXE.

## Usage

Addon assumes intense using of your keyboard. Addon applies to two kind of elements: block and inline.

### Working with a block elements

If you need to insert a block element (`para`, `section`, `orderedlist/listitems`, `procedure`, ):

1. Select a block element using **Ctrl + UP** or **Ctrl + DOWN** as usual in XXE.

2. Press an appropriate keyboard shortcut.

Here are a short list of keyboard shortcuts of block elements:

- `section` - insert after: **Alt + S**, insert before: **Shift + Alt + S**
- `para` - insert after: **Alt + P**, insert before: **Shift + Alt + P**
- `orderedlist` - insert after: **Alt + O**, insert before: **Shift + Alt + O**
- `itemizedlist` - insert after: **Alt + I**, insert before: **Shift + Alt + I**
- `procedure` - insert after: **Alt + U**, insert before: **Shift + Alt + U**
- `screen` - insert after: **Alt + C**
- `programlisting` - insert after: **Alt + G**

**NOTE**: as you have already noted, add a **Shift** key to your shortcut to insert a block element before the existing one.

If you need to lift a current block element within the list of the same ones:

1. Select a block element using **Ctrl + UP** or **Ctrl + DOWN** as usual in XXE.

2. Press a **Shift + Alt + DOWN** to move it down or **Shift + Alt + UP** to move it up.

**Example**: inserting a section after some other one.

1. Select a section element with **Ctrl + UP**. Selected element will be bordered by a red line.

![Existing section, selected in XXE](/doc/img/xxe_selecting_section.png)

2. Press a **Alt + S** shortcut to insert a section after the selected one.

![New section, inserted in XXE](/doc/img/xxe_inserted_section.png)

**NOTE**: to insert section before selected use **Shift + Alt + S**.

### Working with an inline elements

If you want to insert an inline element:

1. Select a text you want to convert to inline element.

2. Press an appropriate keyboard shortcut.

Here are a short list of keyboard shortcuts for inline elements:

- `filename` - convert to: **Alt + F**
- `parameter` - convert to: **Alt + E**
- `remark` - convert to: **Alt + R**
- `emphasis` - convert to: **Alt + E**
- `guibutton` - convert to: **Alt + B**
- `guimenu` - convert to: **Alt + M**
- `guilabel` - convert to: **Alt + L**

## FAQ

See [FAQ](FAQ.md).

## Status

This project is in a very alpha status. More work and documentation are in progress...

## Roadmap

See [TODO](TODO.md).

## Contributing

It fully depends on a type of your contribution:

1. If you found a bug or have any amazing RFE - just create an [issue](https://github.com/eduardtibet/xxe-docbook-fauthoring/issues). 
2. If you want to add new features to a project - just fork it, make any alternation you want and create a pull request.


## Authors

* Eduard Tibet [eduardtibet](https://github.com/eduardtibet) - initial work based on the stock XXE configuration files and author's own insights.

## License

This project is licensed under the BSD 3-Clause License - see the [LICENSE](LICENSE) for more details.