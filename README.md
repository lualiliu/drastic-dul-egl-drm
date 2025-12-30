# drastic-dul-egl-drm-rgds
A dual-screen drastic (a demo on RGDS)

I. Directory Structure

drastic -- emulator folder

SDL2.3 -- source code of the SDL2 library called by drastic

Please place both folders in the /root folder

II. Key Files:

SDL2.3/Makefile.bak -- backup of the makefile needed for SDL2.3 compilation

drastic/libs/libSDL2-2.0.so.0 -- the .so library compiled by SDL2.3 is placed in this path

III. Run the emulator

drastic/launch.sh gamerom.nds -- run the emulator

IV. Compile

cd SDL2.3

make clean

make

V. Run
Copy the libSDL2-2.0.so related files from the build directory to drastic/libs/

drastic/launch.sh gamerom.nds to run the game

VI. Display Path

crtcs is specified as id 1 by default

crtc_id = res->crtcs[1];
conn_id = res->connectors[1];

The crtcs of the other screen is specified as id 0 by default.

crtc_id_dul = res->crtcs[0];
conn_id_dul = res->connectors[0];

If it is not displayed, modify it according to the actual situation.


一、目录结构
drastic	--模拟器文件夹
SDL2.3	--drastic调用的SDL2库的源码

请将两个文件夹放在/root文件夹

二、关键文件：
SDL2.3/Makefile.bak		--SDL2.3编译需要用到的makefile备份
drastic/libs/libSDL2-2.0.so.0	--SDL2.3编译出来的.so库放在这个路径

三、运行模拟器
drastic/launch.sh 游戏rom.nds	--运行模拟器

四、编译
cd SDL2.3
make clean
make

五、运行
将build目录的libSDL2-2.0.so相关文件拷贝到drastic/libs/
drastic/launch.sh 游戏rom.nds运行游戏

六、显示通路
crtcs默认指定为id 1
crtc_id = res->crtcs[1];
conn_id = res->connectors[1];
另一个屏幕的crtcs默认指定为id 0
crtc_id_dul = res->crtcs[0];
conn_id_dul = res->connectors[0];
假如没有显示，按实际情况修改
