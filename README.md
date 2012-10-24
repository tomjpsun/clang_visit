**About:**
	This is a simple progra which make use of **Clang** to show indexing.
	Since **Clang** support C,C++,Objective-C. This program does the same.
	
**Pre-requisite:**
	Pre-requisite packages are CMake and Clang.
	In Debian/Ubuntu, it is suffice to type "sudo aptitude install clang cmake".
	To build Clang from source: http://clang.llvm.org/get_started.html

**Build procedures:**

	$ mkdir build
	$ cd build
	$ cmake ..

**Test:**
	Suppose we copy NSArray.m (under GNUstep project) to the build directory,
	i.e. the same dir with the clang_visitor executable.
	
	$ ./clang_visitor  -s initWithCoder: -f NSArray.m 
	query symbol 'initWithCoder:'
	total 1 ast files:
	NSArray.m
	/usr/GNUstep/Local/Library/Headers/Foundation/NSObject.h: (282, 8) ObjCInstanceMethodDecl	: initWithCoder:
	NSArray.m: (706, 8) ObjCInstanceMethodDecl	: initWithCoder:

That't all.


	
