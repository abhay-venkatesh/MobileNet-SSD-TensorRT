# MobileNet-SSD-TensorRT

TensorRT-Mobilenet-SSD can run 50fps on the Nvidia TX2.

## Pre-requisites

1. TensorRT4

2. cuDNN7

3. OpenCV

4. Install Optimized BLAS
```bash
sudo apt install libopenblas-dev
```

## Execution

```shell
cmake .
make
./build/bin/mobileNet
```

## TODO

- [x] To save serialized model 
- [x] To solve the bug of getting different result with same input
- [ ] The bottleneck of time cost lies in the decoding of pictures. "imread" cost too much ,to resolve it.
- [x] To modify the architecture, decrease the time cost



## Notes

*If want to decrease the time cost of "imread",you could rebuild OpenCV[https://github.com/jetsonhacks/buildOpenCVTX2]*

*Added producer-consumer*

*The bug has been fixed*

![image](testPic/test1.png)
