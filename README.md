# Supply chain attack prevention system

## ABSTRACT

Modern software development becomes faster and faster. That is why we can not inspect every part of development closely. Source code, build system and codesign certificate is under serious threat.

## IDEA & CORE PRINCIPAL

The key part of this idea is integrity. We must secure integrity on source code and build system. Also We must keep our codesign certificate from being taken.

* source code & build system must control with VCS to monitor changes(Git, Docker).
* build system must be disposable(once build is done, build system must destoryed).
* codesign certificate must be stored in usb security token(never be stored on computer storage).

## Release Build Process 

1. Virtual image runs and clones source code from VCS.
2. After fetching source code, network disabled.
3. Usb security token insert and only virtual image can access it.
4. When build is done, the output is saved on storage, virtual build system is destoryed and usb security token is removed from computer.