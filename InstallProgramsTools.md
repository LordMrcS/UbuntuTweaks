# Install Programs/Tools

   * [Install Programs/Tools](#install-programstools)
      * [Open Source](#open-source)
         * [Basic Utilities](#basic-utilities)
         * [PDF Arranger](#pdf-arranger)
         * [Peek](#peek)
         * [Typora](#typora)
         * [Balena Etcher](#balena-etcher)
         * [VirtualBox](#virtualbox)
         * [TOC](#toc)
         * [Visual Studio Code](#visual-studio-code)
         * [OBS Studio](#obs-studio)
         * [Fritzing](#fritzing)
         * [Youtube-dl](#youtube-dl)
         * [ShrinkPDF](#shrinkpdf)
      * [Closed Source](#closed-source)
         * [GitKraken](#gitkraken)
         * [Skype](#skype)
         * [Foxit Reader](#foxit-reader)
         * [SpaceSniffer (with Wine)](#spacesniffer-with-wine)
         * [Anti-Twin (with Wine)](#anti-twin-with-wine)

Created by [gh-md-toc](https://github.com/ekalinin/github-markdown-toc)

Installation commands may be changed in the future, so it is recommended to check the source.

## Open Source

 ### Basic Utilities

```bash
$ sudo apt update
$ sudo apt install \
	apt-transport-https software-properties-common aptitude ubuntu-restricted-extras \
	wget git rar unzip \
	screen net-tools network-manager-openvpn-gnome \
	gparted htop iotop bmon \
	thunderbird xul-ext-lightning \
	gnome-sound-recorder vlc \
	octave \
	pinta gnome-paint gimp
```

### PDF Arranger

https://github.com/pdfarranger/pdfarranger

Better than `PDF Shuffler`

```bash
$ sudo apt remove pdfarranger # edit: apt package has some problems
$ python3 -m pip install --upgrade pip
$ pip3 install --user pikepdf
$ pip3 install --user --upgrade https://github.com/pdfarranger/pdfarranger/zipball/master
```

### Peek

```bash
$ sudo add-apt-repository ppa:peek-developers/stable
$ sudo apt update
$ sudo apt install peek
```

### Typora

https://typora.io/

Best for markdown files.

```bash
$ wget -qO - https://typora.io/linux/public-key.asc | sudo apt-key add -
$ sudo add-apt-repository 'deb https://typora.io/linux ./'
$ sudo apt update
$ sudo apt install typora
```

### Balena Etcher

https://www.balena.io/etcher/

```bash
$ echo "deb https://deb.etcher.io stable etcher" | sudo tee /etc/apt/sources.list.d/balena-etcher.list
$ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 379CE192D401AB61
$ sudo apt update
$ sudo apt install balena-etcher-electron
```

### VirtualBox

https://www.virtualbox.org/

After installating VirtualBox, install extension pack: https://download.virtualbox.org/virtualbox/

```bash
$ wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add -
$ wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
$ sudo add-apt-repository "deb http://download.virtualbox.org/virtualbox/debian xenial contrib"
$ sudo apt update
$ sudo apt install virtualbox
```

### TOC

https://github.com/ekalinin/github-markdown-toc

Usage: `$ toc README.md`

```bash
$ wget https://raw.githubusercontent.com/ekalinin/github-markdown-toc/master/gh-md-toc
$ sudo mv gh-md-toc /usr/bin/toc
$ sudo chmod 555 /usr/bin/toc
```

### Visual Studio Code

https://code.visualstudio.com/

```bash
$ wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
4 sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
4 sudo rm -f /etc/apt/sources.list.d/vscode.list # somehow adds itself into two different locations. So removing one of them
$ sudo apt update
$ sudo apt install code
```

### OBS Studio

https://obsproject.com/

Very good recording and streaming app.

```bash
$ sudo apt install ffmpeg
$ sudo add-apt-repository ppa:obsproject/obs-studio
$ sudo apt update
$ sudo apt install obs-studio
```

### Fritzing

https://fritzing.org

CAD software for designing electronics hardware. For more: https://en.wikipedia.org/wiki/Fritzing

```bash
$ sudo apt install libqt5printsupport5 libqt5xml5 libqt5sql5 libqt5serialport5 libqt5sql5-sqlite
$ sudo apt install fritzing fritzing-data fritzing-parts
```

### Youtube-dl

https://github.com/ytdl-org/youtube-dl

Youtube video, subtitle, thumbnail, etc. downloader which supports batch downloadings (downloading a list).

```bash
$ sudo wget https://yt-dl.org/downloads/latest/youtube-dl -O /usr/local/bin/youtube-dl
$ sudo chmod a+rx /usr/local/bin/youtube-dl
```

### ShrinkPDF

http://www.alfredklomp.com/programming/shrinkpdf/

Reduces PDF filesize by lossy recompressing (reducing DPI). The script and its usage can be found in the link.



## Closed Source

### GitKraken

https://www.gitkraken.com/

Visualized git operations.

```bash
$ wget https://release.axocdn.com/linux/gitkraken-amd64.deb
$ sudo dpkg -i gitkraken-amd64.deb
$ sudo apt install -f
$ rm gitkraken-amd64.deb
```

### Skype

https://www.skype.com/en/

```bash
$ wget -4 https://go.skype.com/skypeforlinux-64.deb
$ sudo dpkg -i skypeforlinux-64.deb
$ sudo apt install -f
$ rm skypeforlinux-64.deb
```

### Foxit Reader

https://www.foxitsoftware.com/downloads/

It is possible to highlight some texts and save them.



### SpaceSniffer (with Wine)

http://www.uderzo.it/main_products/space_sniffer/index.html

Beautiful alternative to native Disk Usage Analyzer (baobab).



### Anti-Twin (with Wine)

http://www.joerg-rosenthal.com/en/antitwin/

Duplicate file finder with byte and image comparison features.