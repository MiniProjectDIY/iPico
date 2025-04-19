# install sdk
```
git clone -b master https://github.com/raspberrypi/pico-sdk.git
cd pico-sdk
 git submodule update --init  --recursive
```
# install toolchain
`sudo apt install cmake gcc-arm-none-eabi build-essential   `
# install pico-fido source
```
git clone https://github.com/polhenarejos/pico-fido.git -b development
cd pico-fido
git submodule update --init  --recursive
mkdir build
cd build
```
# export PICO_SDK_PATH
`export PICO_SDK_PATH=/home/lifetyper/Code/pico-sdk`
# build using yubikey 5 NFC pid
```
cmake .. -DPICO_BOARD=pico2  -DUSB_VID=0x1050 -DUSB_PID=0x0407 -DENABLE_EDDSA=1
make
``` 
