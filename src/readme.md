# Layers source code

## Compile and install

> 
> you need to have **g++** and **make** installed. For the parser you need Flex library to link (-lfl)
>

* Enter in the netparser directory
* Compile the parser


~~~shell
cd netparser
make clean
make
~~~


* Copy the parser to some PAHT directory (e.g. ~/bin)

~~~shell
mkdir ~/bin
export PATH="~/bin:$PATH" >> ~/.bashrc
cp cmc ~/bin
source ~/.bashrc
~~~

* back to layers src and compile layers

~~~shell
cd ..
make clean
make
cp layers ~/bin
~~~

DONE!

### Compiling on MAC:

* You need some alternative to:
 
 clock_gettime and CLOCK_MONOTONIC
 
* See this stackoverflow [post](http://stackoverflow.com/questions/5167269/clock-gettime-alternative-in-mac-os-x) or just comment the following line in the net.cpp:

~~~c
#define USETIME 
~~~

* To compile the netparser, use the MAC CC_LIB flag:

  C_LIB = -ll

* Also in the Makefile use the MAC CXXFLAGS:
 
  CXXFLAGS = -I . -O3 

### Compiling on Windows:

* Try and push it! ...  ¯\\\_(ツ)_/¯ 



## Changelog

### V0.3 - June 2016

* New functions for data:
	* center
	* div
* New parameters for data:
	* balance
* Added a types.h to change from float to double precision
* Other improvements

* Note: **Parser must be compiled**

### V0.2 - June 2016

* New functions available:
	* Network save and load are now available. 
	* Write the output of test data is also available
	* Write out the weights of a particular layer

* Check the new functions in [Scripts-functions](https://github.com/RParedesPalacios/Layers/tree/master/Tutorial#scripts-functions) in the tutorial

* Note: **Parser must be compiled**


### V0.1.1 - June 2016

* Important memory problem solved.


### V0.1 - May 2016
 * Initial commit of source code
 
 * Things to do:
 	* Full integration of the parser
 	* Robust implementation 
 	* Clean code
 	* Improve reusability of some parts
 	* ...

 * Major things to do (we are in the way!):
 	* Recurrent Neural networks
 	* GPU support





