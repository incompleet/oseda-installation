# oseda-installation

**This repo holds installation instructions for Docker, Magic, Netgen, ngspice, xschem, openlane, pdk**

**(Tested on 17th Nov 2021 - platform ubuntu 20.04.3 version)**

## Dependencies

`sudo apt install python3-tk tcl-dev tk-dev m4 libx11-dev gcc mesa-common-dev libglu1-mesa-dev`

---

## Docker

`sudo apt install apt-transport-https ca-certificates curl software-properties-common`

`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`

`sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"`

`apt-cache policy docker-ce`

`sudo systemctl status docker`

`sudo apt install docker-ce`

`sudo systemctl status docker`

`which docker`

---

## Ngspice

[Ngspice Manual](https://sourceforge.net/projects/ngspice/files/ng-spice-rework/35/ngspice-35-manual.pdf/download )

Look into chapter 32 for details of NgSpice installation

First download the tarball from http://sourceforge.net/projects/ngspice/files/ng-spice-rework/35/ngspice-35.tar.gz, then untar it.

`tar -zxvf <tarball name>`

`cd <tarball name>`

`sudo apt install bison flex libx11-dev libxaw7-dev libgtk2.0-dev libreadline-dev`

`mkdir release`

`cd release/`

`../configure --with-x --enable-xspice --disable-debug --enable-cider --with-readline=yes`

`make 2>&1 | tee make.log`

`sudo make install`

`which ngspice `

---

## Xschem

`git clone https://github.com/StefanSchippers/xschem.git`

`./configure && make`

`cd xschem/`

`./configure && make`

`sudo make install`

---

## Magic

http://opencircuitdesign.com/magic/index.html

`git clone git://opencircuitdesign.com/magic`

`sudo apt-get install m4 tcsh csh libx11-dev libcairo2-dev libglu1-mesa-dev libncurses-dev`

`cd magic/`

`./configure`

`make`

`sudo make install`

`which magic`

---

## Netgen

http://opencircuitdesign.com/netgen/index.html

`git clone git://opencircuitdesign.com/netgen`

`cd netgen/`
 
`./configure`

`sudo make`

`sudo make install`

`which netgen`

---

## Openlane

Repo - https://github.com/The-OpenROAD-Project/OpenLane

`python3 -m pip install pyyaml click`

`git clone https://github.com/The-OpenROAD-Project/OpenLane.git`

`cd OpenLane/`

`sudo make pull-openlane`

`sudo make pdk`

`sudo make test`

---
