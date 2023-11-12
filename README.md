# ffmpeg (w/avcpp) bindings for Node.js

Access to video encoding and decoding APIs from Node.js

# Projects goals

* Explore the limits of `nobind`'s design limitations for implementing medium-sized C++ libraries
* Fully debug `nobind` before its first release
* Provide a currently missing feature in server-side JavaScript - video processing - that would never be possible without C++

This project is on the very high end of the `nobind` spectrum - normally SWIG Node-API would have been better suited for it

# Current status

`transcode.js` is working in some cases.

If experimenting, be aware that ffmpeg is a very complex library that is not foolproof at all - it will happily signal invalid arguments with a segfault in some cases. This is true even when using it through avcpp and it is unlikely that the Node.js bindings will ever be completely safe.
