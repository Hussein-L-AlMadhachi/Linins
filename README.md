# Linins source code installer
##### Linins 2021 version 0.1.0 (in progress)

![The Linins Project](https://raw.githubusercontent.com/Hussein-L-AlMadhachi/Linins/main/Linins_logo.png)

Linins is souce code installer for compiling and installing source code with the ability to write scripts that runs when a specified operating systems or distribution exist, or when a particular hardware device or software exist on the users computers. this project aim to make an automated installation possible primarly for Linux and also other open source operating systems
---


## Introduction

if you wanted to make an open source project one of the biggest challenges that you have to face, is that your users uses a wide range of hardware devices , operating systems and software. and if your users do not have the needed technical knowladge, they cannot compile the source code and install all the required dependencies to use the program. so the author of the project has to compile the source code for each operating system and in some cases for some certain hardware devices or some certain software. that is why this program aims to solve this problem by providing you with the followings options to add to your shell scripts:


* You can specify a line of shell script to run only when the user is using a certain Linux distribution or a certain operating system
* You can specify a line of shell script to run when a certain hardware device exist (e.g GPU , network adaptors)
* You can specify a line of shell script to run when a certain software path exist (e.g GCC , Python , Nim , R)
* You can clone any other additionl repositories
* You can clone repositories that support Linins Installation file's format "InstallFile" and install additional software that is specified in those repositories installtion files without worrying about how to install them when you writing your installtion files

## how a user should install and use this program

___
### Disclaimer:
You should **NEVER EVER** use this software to install anything **OTHER THAN** source codes from a **TRUSTED** sources  
**DO NOT** use this program to INSTALL **BINARIES** that does **NOT** provide the **SOURCE CODES** even if it was from **TRUSTED SOURCES**.  
if the source code is not provided, For YOUR OWN **SAFETY** **DO NOT** install such programs using **Linins** because there must be an unintentional bug somewhere (e.g root privileges escalation , remote code execution) because these software do not provide any way to detect such severe bugs by any experts  
So we highly discourage the installation of software that does not provide source code **or** the installation of untrusted source codes.
___

### The installation

1. save this [script](https://github.com/Hussein-L-AlMadhachi/Linins/raw/main/install.sh) and run it
``` bash
user@machine:~$ sh install.sh
```

2. Write the following in your shell then select your operating system:

``` bash
user@machine:~$ linins setup
```
### How to use

Now Linins is ready. if you have the repository URL that supports Linins, to install it automatically write:

``` bash
user@machine:~$ linins clone [URL]
```

or if you have a source code for a project and the project has Linins installtion files `InstallFile` write:

``` bash
user@machine:~$ cd (path to the folder that contains 'InstallFile')

```

``` bash
user@machine:~$ linins install
```
