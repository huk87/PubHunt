# PubHunt
- Это измененная программа [PubHunt](https://github.com/kanhavishva/PubHunt) для любителей головоломки pazzles"
## PubHunt рандомно ищет сжатые открытые ключи для заданного хэша160.
- Эта программа подходит только для [транзакций биткойн - головоломки](https://www.blockchain.com/btc/tx/08389f34c98c606322740c0be6a7125d9860bb8d5cb182c02f98461e5fa6cd15).
- Для головоломки ```64```, ```66```, ```67```, ```68```, ```69```, ```71``` или ```72``` 
## Параметры:
-  Работает только на GPU.
-  Меняйте GRIDSIZE для поиска на оптимальной скорости. Пример 8192,1024 
```
PubHunt.exe -h
PubHunt [-check] [-h] [-v]
        [-gi GPU ids: 0,1...] [-gx gridsize: g0x,g0y,g1x,g1y, ...]
        [-o outputfile] [inputFile]

 -v                       : Print version
 -gi gpuId1,gpuId2,...    : List of GPU(s) to use, default is 0
 -gx g1x,g1y,g2x,g2y, ... : Specify GPU(s) kernel gridsize, default is 8*(MP number),128
 -o outputfile            : Output results to the specified file
 -l                       : List cuda enabled devices
 -check                   : Check CPU and GPU kernel vs CPU
 inputFile                : List of the hash160, one per line in hex format (text mode)
```

## Пример работы:
```
C:\Users\user>PubHunt.exe -gi 0 -gx 16384,1024 hashP64.txt

PubHunt v1.00

DEVICE       : GPU
GPU IDS      : 0
GPU GRIDSIZE : 16384x1024
NUM HASH160  : 1
OUTPUT FILE  : Found.txt
PubHunt SITE : https://github.com/phrutis/PubHunt
GPU          : GPU #0 NVIDIA GeForce RTX 2070 (36x64 cores) Grid(16384x1024)

[00:01:19] [GPU: 1068.75 MH/s] [T: 84,590,723,072 (37 bit)] [F: 0]
```
## Donation
- BTC: bc1qh2mvnf5fujg93mwl8pe688yucaw9sflmwsukz9
