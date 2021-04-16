#  Ubtuntu 18.04 & Ubuntu 16.04

## 1 Install mosquitto and json-c

sudo add-apt-repository ppa:mosquitto-dev/mosquitto-ppa 
sudo apt-get update

sudo apt-get install mosquitto-clients libmosquitto-dev

sudo apt install libjson-c-dev

## 2 Fetch code and compile on two different machine
git clone https://github.com/xuyaozhong/stunp2pexample.git
cd stunp2pexample
cmake .
make -j 4

## 3 Run test code

on Machine A via 1st 4G (e.g. CMCC)
./udpstunclient

on Machine B via 2nd 4G (e.g. CTCC)
./udpstunclient
