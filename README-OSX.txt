
************************
 Port x11docker for OSX
************************

https://github.com/mviereck/x11docker/issues/15
https://github.com/mviereck/x11docker/issues/242
https://github.com/mviereck/x11docker/issues/269

*******
 Fixed
*******

# switch to a modern bash, as Apple does not include GPLv3 code in their deliveries
brew install bash 
export PATH=/opt/homebrew/bin:$PATH

# coreutils provides 'realpath'
brew install coreutils




*******************
 Work In Progress
*******************

karawitan$ ./x11docker
./x11docker: line 6676: ip: command not found

There is no docker0 bridge on macOS
Because of the way networking is implemented in Docker Desktop for Mac, 
you cannot see a docker0 interface on the host. 
This interface is actually within the virtual machine.


stat: illegal option -- c
usage: stat [-FlLnqrsx] [-f format] [-t timefmt] [file ...]
./x11docker: line 1290: getfacl: command not found

x11docker ERROR: User karawitan does not have write access to cache folder
  /Users/karawitan/.cache/x11docker
