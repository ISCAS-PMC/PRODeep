# PRODeep
PRODeep: A Platform for Robustness Verification of Deep Neural Networks
## PRODeep dependency
### dependency for ubuntu
	1) sudo apt-get install g++ qt5-default make
	2）sudo apt-get install libboost-all-dev
	3）sudo apt-get install -yqq libgmp-dev libmpfr-dev
	4）git clone https://github.com/antoinemine/apron 
	   	cd apron
	   	./configure -no-ppl -no-java
       	sudo make 
       	sudo make install
	sudo ldconfig

## Install DeepG and ERAN (Optional)
If you want to add support for DeepG and ERAN, please visit [DeepG](https://github.com/ISCAS-PMC/deepg) to install modified verision of DeepG and ERAN.

If DeepG is installed for example at **/home/USERNAME/Library/deepg** and the python environment for DeepG is **/home/USERNAME/miniconda3/bin/python** , please modify the following lines in _mainui.h_

```
#define PYTHON_EXECUTABLE "/home/USERNAME/miniconda3/bin/python"
#define DEEPG_ROOT "/home/USERNAME/Library/deepg"
```

## Install PLANET (Optional)
If you want to add support for PLANET verifier, please visit [PLANET](https://github.com/progirep/planet) to install it.

If the MNIST casestudy of PLANET is located in **/home/USERNAME/Library/planet/casestudies/MNIST**, please modify the following line in _mainui.h_

```
#define PLANET_DIR "/home/USERNAME/Library/planet/casestudies/MNIST"
```


## Install Reluplex (Optional)
If you want to add support for Reluplex, please visit [Reluplex](https://github.com/ISCAS-PMC/ReluplexCav2017) to install modified verision of Reluplex.

If the Reluplex is located in **/home/USERNAME/Library/reluplex/ReluplexCav2017-master**, please modify the follow line in _mainui.h_.

```
#define Reluplex_ROOT "/home/USERNAME/Library/reluplex/ReluplexCav2017-master"
```

## Compile PRODeep
	1) cd \path\to\PRODeep
	2) qmake
	3) make
