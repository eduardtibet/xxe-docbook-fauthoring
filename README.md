# xxe docbook fauthoring project

## Table of contents
<!-- TOC started -->

 * [About](#about)
 * [Installation](#installation)
   * [Prerequisites](#prerequisites)
   * [Installation modes and steps](#installation-modes-and-steps)
   	 * [About an installation modes](#about-an-installation-modes)
     * [Installation in AOP mode](#installation-in-aop-mode)
     * [Installation in FOD mode](#installation-in-fod-mode)
 * [Usage](#usage)
 * [FAQ](#faq)
 * [Roadmap](#roadmap)
 * [Contributing](#contributing)
 * [Authors](#authors)
 * [License](#license)

<!-- TOC ended -->

## About

xxe-docbook-fauthoring is a simple configuration file for using in conjunction with [XMLMind XMl Editor](https://xmlgraphics.apache.org/fop). Its aim is to produce pretty looking `.pdf` files using only free OFL-licensed fonts to avoid any patent- or/and license-related issues.

BTW, if you don't aware about what Apache FOP is suitable for, check out its [FAQ](https://xmlgraphics.apache.org/fop/faq.html).

foponts is for anyone who creates `.pdf` files with Apache FOP. It's specially designed and highly recommended for everyone working with DocBook/XML files and who wants to get a predictable result without any headache.

foponts is strongly recommended when:
- you are not sure about fonts you are using and/or have and feel uncomfortable with any patent-related issues with fonts within your documents;
- you want to be sure that you use fonts that are free to use anywhere, where [OFL license](https://scripts.sil.org/cms/scripts/render_download.php?format=file&media_id=OFL_plaintext&filename=OFL.txt) allows you (in fact, you can use these fonts near everywhere);
- you are using Cyrillic characters in your documents or deal with a Cyrillic documents only (work with a documents in Russian) and want to get a `.pdf` without any hassle - you are boring to get a document full of **####** signs instead of Cyrillic characters.


## Installation

### Prerequisites

1. Any machine (PC, Mac, headless server, ...) with OS, that supports Java.
2. XXE installed and working Java (JRE) 1.6 or newer installed and working. Check if Java is installed correctly:

```
$ java -version
```

3. Apache FOP 2.1 or newer. You can get the latest FOP [from official download page](https://xmlgraphics.apache.org/fop/download.html). Check if APache FOP is installed correctly:

```
$ fop -version
```

4. Git - to clone the repo (in case)
5. Any utility (or web browser) - to download a files (`wget` is recommended).
6. Any utility that can extract a bzipped tar (`.tar.bz2`) archives.
7. Any `.fo` file (document) you need to get a `.pdf` file from. You have to have a `serif`, `sans-serif` and `monospace` font families within your `.fo` file.

**NOTE 1**: To check how foponts works, a sample `.fo` file is provided within a `docbook-samples` directory (direct link to a sample [file](https://github.com/eduardtibet/docbook-samples/blob/67a87ce684ac4a6baacdb12a26528aeb585b5eeb/stdf/stdf_manual.fo)

**NOTE 2**: Due to samples, used in this project, are the core of another [project](https://github.com/eduardtibet/docbook-samples/), `docbook-samples` directory is provided as a git submodule within a current project.

### Installation modes and steps

#### About an installation modes

There are 2 installation modes of the addon:

 - (**RECOMMENDED**) Direct download and installation of complete addon directly from XMLmind XML Editor, using menu item **Options**|**Install Add-ons**.

 - Manual installation including cloning this project, packing it using any utility that produces a `.zip` file and configuring XXE to feed a packed file.
 
#### Installation in AOP mode

1. Create a directory, where you want to store a foponts:

```
$ mkdir foponts-pdf-generation
```

2. Change a directory to the created one:

```
$ cd foponts-pdf-generation
```

3. Get the archive from the author's website with all fonts included:

```
$ wget http://www.singlesourcing.ru/pub/foponts/dist/foponts-fonts.tar.bz2
```

4. Extract archive content to the created folder:

```
$ tar -xjf foponts-fonts.tar.bz2
```

5. Get the foponts project:

```
$ git clone --recursive https://github.com/eduardtibet/foponts.git
```

**NOTE:** You have to use `--recursive` option, because the directory with a samples is a separate author's [project](https://github.com/eduardtibet/docbook-samples) and is included as a git submodule here!

6. Change a directory to the foponts project:

```
$ cd foponts
```

7. foponts is initially configured to run in a FOD mode, so use your favorite text editor to change the default value of a `<font-base>` element in `foponts.xml` file to the actual local path to a directory with a downloaded fonts:

Default:

```xml
<font-base>http://www.singlesourcing.ru/pub/foponts/foponts-fonts/</font-base>
```

Changed sample:

```xml
<font-base>/home/[your_user_directory]/foponts-pdf-generation/foponts-fonts/</font-base>
```

**NOTE:** Trailing slash is a must thing here!

#### Installation in FOD mode

1. Create a directory, where you want to store a foponts:

```
$ mkdir foponts-pdf-generation
```

2. Change directory to the created one:

```
$ cd foponts-pdf-generation
```

3. Get the foponts project:

```
$ git clone --recursive https://github.com/eduardtibet/foponts.git
```

**NOTE:** You have to use `--recursive` option, because the directory with a samples is a separate author's [project](https://github.com/eduardtibet/docbook-samples) and is included as a git submodule here!

4. Change a directory to the foponts project:

```
$ cd foponts
```

6. Check that you have a stable internet connection, due to all required fonts will be downloaded on demand.


## Usage

To your reference, this readme and all procedures within it assumes the following directory structure:
```
foponts-pdf-generation
  |
  /foponts
  |  |
  |  /docbook-samples
  |     |
  |     /stdf
  /foponts-fonts *(in case you use AOP mode)*
```

To use foponts project to generate a `.pdf` file from your `.fo` file: 

1. Run FOP with the following command line (an example below shown how to generate a `.pdf` from a project's sample `.fo` file):

```
$ fop -c foponts.xml -fo docbook-samples/stdf/stdf_manual.fo -pdf docbook-samples/stdf/stdf_manual.pdf
```

2. Look at the result by just opening the generated file `stdf_manual.pdf` (or any other generated file of your own) in your favorite PDF viewer:

```
$ xpdf docbook-samples/stdf/stdf_manual.pdf
```

You can compare the result with the reference file, generated by the author of foponts. It can be downloaded from:

```
$ wget http://www.singlesourcing.ru/pub/docbook-samples/stdf/stdf_manual.pdf
```


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