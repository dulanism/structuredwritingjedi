### Linux Tutorial to Getting Started with DITA Open Toolkit

#### Open a console, paste the set of commands

```
cd && wget http://downloads.sourceforge.net/project/dita-ot/DITA-OT%20Stable%20Release/DITA%20Open%20Toolkit%201.5.4/DITA-OT1.5.4_full_easy_install_bin.tar.gz && tar xzvf DITA-OT1.5.4_full_easy_install_bin.tar.gz && wget http://www.redaction-technique.org/media/dita-env.txt && workingdirectory=`pwd | sed "s/\//slash/g;"` && perl -pi -e "s/personal-dita-home/$workingdirectory/g;" dita-env.txt && perl -pi -e "s/slash/\//g;" dita-env.txt && cp .bashrc .bashrc.bak && cat .bashrc | sed '$a\' > .bashrc.tmp && mv .bashrc.tmp .bashrc && cat dita-env.txt >> .bashrc && exit
```

Description of above commands:

* Changes the current working directory to your user account root directory
* Downloads the DITA Open Toolkit archive
* Uncompresses the Dita Open Toolkit archive
* Downloads the Dita Open Toolkit environment variables file
* Writes your user account root directory in the Dita Open Toolkit environment variables file
* Makes a backup copy of the .bashrc file (.bashrc.bak)
* Appends the Dita Open Toolkit environment variables at the end of the .bashrc file
* Closes the current console


#### Open a new console to take into account the new .bash_profile (or .bashrc) version

#### Install [Openjdk 6](http://openjdk.java.net/projects/jdk6/) and [Apache Ant](http://ant.apache.org/)

```sudo apt-get install openjdk-6-jre ant```

* Enter the administrator password. Press Enter at the Do you want to continue? [Y/n/?] prompt.
* Note: On a Debian system, if you are not sudoer, type su -.

#### Paste the following command:

```cd DITA-OT1.5.4```

* This command changes the current working directory to the DITA-OT1.5.4 directory

#### Paste the following command:

```java -jar lib/dost.jar /i:samples/taskbook.ditamap /outdir:. /transtype:pdf2```

* This command creates a PDF file from a DITA XML sample project. 

**Congratulations, you’ve just compiled your first DITA XML project! The taskbook.pdf target file is located in the DITA-OT1.5.4 directory. Skip steps 1 and 2 to compile new projects.**

====

#### Troubleshooting

If several Java versions are installed and an error occurs, open an administrator console and select the Open JDK 6 version:

```
# update-alternatives --config java
Selection Path Priority Status
------------------------------------------------------------
* 0 /usr/lib/jvm/java-6-openjdk-i386/jre/bin/java 1061 automatic mode
```

You can specify one of the following values for the *transtype* option:

| Value         | Target Format         |         
| ------------- |:---------------------:|
| xhtml         | xhtml                 |
| col 2 is      | centered              |  
| eclipsehelp   | Eclipse help          |
| javahelp      | Javahelp help         |
| htmlhelp      | Windows compiled help |
| pdf2          | PDF                   |
| troff         | troff                 |
| docbook       | DocBook               |
| wordrtf       | Microsoft RTF         |