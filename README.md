```shell
sudo perf record
sudo chown user:user perf.data
perf script --insn-trace --xed
```

link https://stuff.mit.edu/afs/sipb/contrib/linux/tools/perf/Documentation/build-xed.txt

For --xed the xed tool is needed. Here is how to install it:  

  $ git clone https://github.com/intelxed/mbuild.git mbuild  
  $ git clone https://github.com/intelxed/xed  
  $ cd xed  
  $ ./mfile.py --share  
  $ ./mfile.py examples  
  $ sudo ./mfile.py --prefix=/usr/local install  
  $ sudo ldconfig  
  $ sudo cp obj/examples/xed /usr/local/bin  
  
but XED version: [12.0.1-72-gd57a3bd]  
  you can find it here [xed directory]/../build/obj/wkit/examples/obj/xed  
  after this: https://intelxed.github.io/build-manual/  
```shell
mkdir build
cd build
../xed/mfile.py
../xed/mfile.py examples       (optional)
../xed/mfile.py doc            (optional, requires doxygen)
../xed/mfile.py doc-build      (optional, requires doxygen)
../xed/mfile.py install        (optional)
../xed/mfile.py install zip    (optional, makes a zip file)
../xed/mfile.py examples install zip    (optional, makes a zip file that includes the examples)
```
