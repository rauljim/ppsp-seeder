Seed content (videos) using PPSP.

========================

Installing libevent
-------------------

wget https://github.com/downloads/libevent/libevent/libevent-2.0.18-stable.tar.gz
tar -xaf libevent-2.0.18-stable.tar.gz 
cd libevent-2*
./configure
make
sudo make install


Install submodules
------------------

You need to get the pymdht and libswift submodules. It's simple.

git submodule init
git submodule update 


Compile libswift
----------------

cd libswift
make

Get videos
----------

The video hashes and locations are hardcoded (we should change this) in
ppsp_seeder.py.
The data files should be placed in PATH = "~/swiftcontent-march2012/"


SEED!
-----
Just run:
./ppsp_seeder.py

Better yet, use supervisord with this configuration:
[program:ppsp-seeder]
command=/home/zzzzz/ppsp-seeder/ppsp_seeder.py
directory=/home/zzzzz/ppsp-seeder


