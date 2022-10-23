# deb-rdepend-downloader
This bash script is for downloading Debian rdepended packages of given package.
The script will create folder of package name and subfolder (named "dependencies" - feel free to change it in script) for depended packages.
 
## Prepare:
Sources are normally not installed. Hence, you can only install them if you know the package name and when you enable them. Therefore, edit the /etc/apt/sources.list file, run:
```
$ sudo vi /etc/apt/sources.list
```
Make sure the deb-src type references an Ubuntu distribution’s source code as follows:
```
# Sources specification for the Ubuntu 20.04 LTS distro #
deb-src http://archive.ubuntu.com/ubuntu focal main restricted universe multiverse
deb-src http://archive.ubuntu.com/ubuntu focal-updates main restricted universe multiverse
deb-src http://security.ubuntu.com/ubuntu focal-security main restricted universe multiverse
```
Update index:
```
$ sudo apt update
```
## Usage:
```bash
$ get-rdepend-pkgs.sh [package name]
```
Example:
```bash
$ get-rdepend-pkgs.sh curl
```
