### 100 Prerequisites

[Prerequisites](http://metamap.nlm.nih.gov/MetaMap.shtml)

* MetaMap requires a minimum of 7GB of disk space when it has been uncompressed.
* MetaMap requires a minimum of 1GB of memory to run. At least 2GB is recommended.
* You will need a working version of [bunzip2](http://www.bzip.org/) to uncompress the MetaMap download file.
* Java Runtime Environment (JRE) 1.7 or greater is required.
* You must activate a [UMLS Terminology Services (UTS)](https://uts.nlm.nih.gov/home.html) account if you don't have one. 
* To download MetaMap, you must have accepted the terms of the [UMLS Metathesaurus License Agreement](https://uts.nlm.nih.gov/license.html)

### 101 Download MetaMap and MetaMap Java API

Download [MetaMap](http://metamap.nlm.nih.gov/MainDownload.shtml) Release 2013v2 according to the OS.

Download the [MetaMap Java API](http://metamap.nlm.nih.gov/JavaApi.shtml) Release (2013v2) according to the OS.

### 102 Install MetaMap

[MetaMap Installation](http://metamap.nlm.nih.gov/Installation.shtml)

Move the downloaded file `public_mm_<platform>_<year>.tar.bz2` into a directory where you want to install MetaMap. This directory will then be referred to as `<parent_directory>` throughout the rest of the installation instructions. 

```
cd <parent_directory>
bunzip2 -c public_mm_<platform>_<year>.tar.bz2 | tar xvf - 
cd public_mm
```

Set the environment variable JAVA_HOME.

Add the `<parent_directory>/public_mm/bin` directory to your program path:

```
export PATH=<parent_directory>/public_mm/bin:$PATH
```

Run the installation script:

```
cd <parent_directory>/public_mm
./bin/install.sh
```

### 103 Install MetaMap Java API

Move the downloaded file `public_mm_<platform>_javaapi_<year>.tar.bz2` to `<parent_directory>`.

```
cd <parent_directory>
bzip2 -dc public_mm_<platform>_javaapi_<year>.tar.bz2` | tar xvf -
```

Re-run ./bin/install.sh from the `public_mm` directory to setup the files for javaapi.

```
cd <parent_directory>/public_mm
bzip2 -dc public_mm_<platform>_javaapi_<year>.tar.bz2` | tar xvf -
```

### Using the MetaMap server

The MetaMap server `mmserver` must first be running to use the Java API. Before start `mmserver`, two supporting servers need to be started:

Start the SKR/Medpost Tagger:

```
./bin/skrmedpostctl start
```

Start the Word Sense Disambiguation (WSD) Server.

```
./bin/wsdserverctl start
```

Start the MetaMap server:

```
./bin/mmserver
```


