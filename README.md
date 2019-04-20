本仓库的文件由以下步骤得到(https://sourceforge.net/u/uecasm/etherlab-patches/ci/default/tree/#readme):<br>

1,Install Mercurial, if you don't already have it, eg:<br>
sudo apt install mercurial<br>
2,Create or edit your ~/.hgrc file and ensure it has at least the following contents:<br>
[ui]<br>
username = yourname<br>
[extensions]<br>
mq =<br>
3,Clone the main upstream repository:<br>
hg clone -u 33b922ec1871 http://hg.code.sf.net/p/etherlabmaster/code etherlab<br>
4,Clone the patch repository:<br>
hg clone http://hg.code.sf.net/u/uecasm/etherlab-patches etherlab/.hg/patches<br>
5,Apply the patches:<br>
cd etherlab<br>
hg qpush -a<br>
6,You're now ready to build, as usual:<br>
./bootstrap<br>
./configure --help<br>
And then choose the options you wish, and follow the rest of the instructions in the INSTALL file.<br>
