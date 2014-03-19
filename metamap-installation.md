### 100 [Prerequisites](http://metamap.nlm.nih.gov/MetaMap.shtml)

* MetaMap requires a minimum of 7GB of disk space when it has been uncompressed.
* MetaMap requires a minimum of 1GB of memory to run. At least 2GB is recommended.
* You will need a working version of [bunzip2](http://www.bzip.org/) to uncompress the MetaMap download file.
* Java Runtime Environment (JRE) 1.7 or greater is required.
* You must activate a [UMLS Terminology Services (UTS)](https://uts.nlm.nih.gov/home.html) account if you don't have one. This might take a couple of days.
* To download MetaMap, you must have accepted the terms of the [UMLS Metathesaurus License Agreement](https://uts.nlm.nih.gov/license.html).

### 101 Download Full MetaMap and MetaMap Java API

* Download [Full MetaMap](http://metamap.nlm.nih.gov/MainDownload.shtml) Release 2013v2 according to the OS platform.

* Download the [MetaMap Java API](http://metamap.nlm.nih.gov/JavaApi.shtml) Release (2013v2) according to the OS platform.

### 102 [Install MetaMap](http://metamap.nlm.nih.gov/Installation.shtml)

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

### 103 [Install MetaMap Java API](http://metamap.nlm.nih.gov/Docs/README_javaapi.html)

Move the downloaded file `public_mm_<platform>_javaapi_<year>.tar.bz2` to `<parent_directory>`.

```
cd <parent_directory>
bzip2 -dc public_mm_<platform>_javaapi_<year>.tar.bz2` | tar xvf -
```

Re-run ./bin/install.sh from the `public_mm` directory to setup the files for javaapi.

```
cd <parent_directory>/public_mm
./bin/install.sh
```

### 104 Using the MetaMap server

The MetaMap server `mmserver` must first be running to use the Java API. Before start `mmserver`, two supporting servers need to be started:

Start the SKR/Medpost Tagger:

```
./bin/skrmedpostctl start
```

Start the Word Sense Disambiguation (WSD) Server:

```
./bin/wsdserverctl start
```

Start the MetaMap server:

```
./bin/mmserver
```

### 105 Using ConceptAnnotator.jar to annotate data dictionary variables

```
java -jar ConceptAnnotator.jar <InputPath> <OutputPath>
```

### 106 Possible Trouble Shooting

If you see errors that MMServer denying client connection similar as:

```
! [PBEANS] - denied connection from 192.168.1.123
```

Edit the file `<parent_directory>/public_mm/bin/SKRrun.13` and change the environment variable ACCEPTED_HOSTS:

```
# for mmserver
export ACCEPTED_HOSTS="['127.0.0.1']"
```

Add the IP address of the client machine (not the host running mmserver) to the client list assigned to ACCEPTED_HOSTS. For example, to allow mmserver to accept clients on host `192.168.1.123`, add it to the list:

```
export ACCEPTED_HOSTS="['127.0.0.1','192.168.1.123']"
```

After this, mmserver will accept clients at host 192.168.1.123 (all of the entries must be ip-addresses, hostnames will not work)
