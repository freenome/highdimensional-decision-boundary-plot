## Install steps
python 3.5 was installed prior, also I installed `gcc-5` through `homebrew`. `clang` did not work.

```
virtualenv venv --python=python3.5
pip install -r update_requirements.txt
wget http://ab-initio.mit.edu/nlopt/nlopt-2.4.2.tar.gz
cd nlopt-2.4.2
./configure --with-python --enable-shared --prefix=$HOME/src/highdimensional-decision-boundary-plot/venv/ CC=gcc-5 CXX=g++-5 --without-guile
make -j 10
make -j 5 install
cd ..
python demo.py
```

