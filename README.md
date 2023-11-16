//*******************************************************
//**************Litex 生成 SoC

PATH=~/gowin/IDE/bin:$PATH
./make.py --board sipeed_tang_primer_20k --with-rvc --uart-baudrate 115200 --build

//*******************************************************
//**************下载SoC到高云FPGA


//*******************************************************
//**************导入Linux镜像

ls /dev/ttyUSB*
sudo chmod 777 /dev/ttyUSB1
litex_term --images=boot.json /dev/ttyUSB1

//*******************************************************
//**************RISCV处理器操作

buildroot login: root
pwd
uname -a
