clFFT bindings for Go
======================

Requires OpenCL 1.2 libraries to be available.

Default clFFT library needs to be hacked for importing to Go.

The clFFT.h header contains the definition of clfftInitSetupData, which

causes errors with cgo.

The work around is achieved by moving the definition of clfftInitSetupData

into library/lifetime.cpp

Repository containing the hack can be checkouted out using

git clone https://github.com/xfong/clFFT -b repackage
