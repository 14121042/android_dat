**Dat轉Img(Ext4)**


sudo sdat2img system.transfer.list system.new.dat system.img


**掛載System**


sudo mount -t ext4 -o loop system.img system


**將掛載的System寫成Img(普通)**


sudo make_ext4fs -l 1306001408B -s -a system system_new.img system

(1306001408B爲system.img大小)


**將Img(普通)轉成Img(Ext4)**


sudo simg2img system_new.img system_ext4.img


**將Img(Ext4)轉成Dat**


sudo rimg2sdat system_ext4.img


##需要使用的程式##

**sdat2img**

**make_ext4fs**

**simg2img**

**rimg2sdat**
