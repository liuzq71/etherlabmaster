本仓库的文件由以下步骤得到(https://sourceforge.net/u/uecasm/etherlab-patches/ci/default/tree/#readme):

1,Install Mercurial, if you don't already have it, eg:

sudo apt install mercurial

2,Create or edit your ~/.hgrc file and ensure it has at least the following contents:
[ui]
username = yourname
[extensions]
mq =

3,Clone the main upstream repository:

hg clone -u 33b922ec1871 http://hg.code.sf.net/p/etherlabmaster/code etherlab

4,Clone the patch repository:

hg clone http://hg.code.sf.net/u/uecasm/etherlab-patches etherlab/.hg/patches

5,Apply the patches:

cd etherlab
hg qpush -a



6,You're now ready to build, as usual:

./bootstrap
./configure --help

And then choose the options you wish, and follow the rest of the instructions in the INSTALL file.
