<div align="center">
<h1 align="center">Yacy Nebula</h1>

A custom version of [Yacy](https://github.com/yacy/yacy_search_server) created by webman168.
</div>


## What is Yacy Nebula?
Yacy Nebula is a distributed web search engine based on the original YaCy. The original was developed by Michael Peter Christen.

## Installation
Yacy Nebula is written in Java and can be compiled using a Java 11 or 17 JDK and apache ant.

Pre-compiled YaCy packages may be available at a later date.

You need Java 11 or later to run Yacy Nebula.

### Compile and run YaCy from git sources
This would install the requirements on debian:

```
sudo apt-get install openjdk-11-jdk-headless ant
```

Then clone the repository and build the application:

```
git clone --depth 1 https://github.com/yacy/yacy_search_server.git
cd yacy_search_server
ant clean all
```

To start YaCy, run

```
./startYACY.sh
```

The administration interface is then available in your web browser at `http://localhost:8090`.
Some of the web pages are protected and need an administration account; these pages are usually
also available without a password from the localhost, but remote access needs a log-in.
The default admin account name is `admin` and the default password is `yacy`.
Please change it after installation using the ``http://<server-address>:8090/ConfigAccounts_p.html`` service.

Stop YaCy on the console with
```
./stopYACY.sh
```

## Help develop YaCy

- clone https://github.com/yacy/yacy_search_server.git using build-in Eclipse features (File -> Import -> Git) 
- or download source from this site (download button "Code" -> download as Zip -> and unpack)
- Open Help -> Install New Software -> add.. -> add archived IvyDE Updatesite "https://archive.apache.org/dist/ant/ivyde/updatesite/" -> Install "Apache IvyDE"
- right-click on the YaCy project in the package explorer -> Ivy -> resolve

This will build YaCy in Eclipse. To run YaCy:
- Package Explorer -> YaCy: navigate to source -> net.yacy
- right-click on yacy.java -> Run as -> Java Application

Join our development community, got to https://community.searchlab.eu

Send pull requests to https://github.com/yacy/yacy_search_server

## APIs and attaching software

YaCy has many built-in interfaces, and they are all based on HTTP/XML and
HTTP/JSON. You can discover these interfaces if you notice the orange "API" icon in
the upper right corner of some web pages in the YaCy web interface. Click it, and
you will see the XML/JSON version of the respective webpage.
You can also use the shell script provided in the /bin subdirectory.
The shell scripts also call the YaCy web interface. By cloning some of those
scripts you can easily create more shell API access methods.

## License

This project is available as open source under the terms of the GPL 2.0 or later. However, some elements are being licensed under GNU Lesser General Public License. For accurate information, please check individual files. As well as for accurate information regarding copyrights.
The (GPLv2+) source code used to build YaCy is distributed with the package (in /source and /htroot).


