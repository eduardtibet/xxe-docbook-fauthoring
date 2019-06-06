# xxe docbook fauthoring project

## Table of contents
<!-- TOC started -->

 * [About](#about)
 * [Limitations](#limitation)
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

Due to author's limited resources this addon works only with a DocBook 5.x version of a source files (NS-based files). It doesn't support Docbook 4.5 (non NS-awared) documents. In case of high volume feedback from a users of an addon, author will try to add a v. 4.5 support later. 

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

## Usage

TBD

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