# Hoominer
Hoominer is [Hoosat Networks](https://network.hoosat.fi) closed source miner for CPU/GPU mining. Currently supports only Hoohash algorithm which is open source algorithm based on kHeavyHash. 


## Settings
Welcome to Hoominer v0.4.1
Usage: ./build/hoominer [--stratum <stratum+tcp://domain:port>] [--user <user>] [--pass <pass>]

General parameters: 
- `--algorithm <algorthm>`                          The algorithm to mine, by default 'hoohash'.
- `--stratum <stratum+tcp://domain:port>`           The stratum protocol://address:port to specify connection point (stratum+ssl:// or stratum+tls:// to enable SSL/TLS).
- `--user <user>`                                   Stratum username (Usually mining wallet address).
- `--password <password>`                           Stratum password (Usually not required or used as additional stratum parameters).
- `--disable-cpu`                                   Disable CPU mining completely.
- `--disable-gpu`                                   Disable GPU mining completely.
- `--disable-opencl`                                Disable OpenCL mining.
- `--disable-cuda`                                  Disable CUDA mining.
- `--debug`                                         More information displayed.
- `--algorithm`                                     Which algorithm to use for mining.

Supported algorithms:
|Coin|CUDA|OpenCL|CPU | --algorithm    |
|---------|----|------|---|------------|
|Hoosat   |YES |YES   |YES| hoohash    |
|PepePow  |NO  |YES   |YES| pepepow    |



CPU parameters: 
- `--cpu-threads <thread-count>`                    Select how many CPU threads to create.

GPU parameters: 
- `--list-gpus`                                     List gpu bus id's.
- `--gpu-ids <bus-id list>`                         Select which GPU's to use, seperate bus id's with comma (if not specified all devices will be used).
- `--opencl-o <level>`                              Select OpenCL compile time optimization level (0 no optimizations, 1 basic optimizations, 2 default otimizations, 3 best optimization which might fail).
- `--gpu-work-multiplier <level>`                   Select multiplier for OpenCL global work size or Nvidia blocks size (0 multiplier is default). 

API parameters:
- `--disable-api`                                   Disables API
- `--api-port`                                      API Port


