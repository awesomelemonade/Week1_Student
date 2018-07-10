## Installation Requirements
Anaconda with Python 3.{5, 6}, ffmpeg, portaudio (Mac & Ubuntu only), pyaudio, and librosa. See following sections for installation instructions.

### Installing Required Packages (verified for Windows)
```shell
conda install -c conda-forge ffmpeg

pip install pyaudio

conda install -c conda-forge librosa
```


### Installing Required Packages (Mac OSX)
There are a few things to consider when installing this project for OS X. 

First, the `portaudio` library must be installed before running `pip install pyaudio`. 

This can be done with [Homebrew](https://brew.sh/) using 
  - `brew install portaudio` 

or MacPorts using 
  - `sudo port install portaudio` 
  
it may also be available through conda, although this is not verified (there seems to be issues with this method..)
  - `conda install -c anaconda portaudio=19`
  
Having installed `portaudio`, proceed as follows:
```shell
conda install -c conda-forge ffmpeg

pip install pyaudio

conda install -c conda-forge librosa
```

### Installing Required Packages (Ubuntu)

Install ffmpeg
  - `conda install -c conda-forge ffmpeg`

Install pyaudio
  - `pip install pyaudio`

Pyaudio requires you to install a C library called `portaudio`
  - [Download Stable](http://www.portaudio.com/download.html)
  - Follow [instructions](http://portaudio.com/docs/v19-doxydocs/compile_linux.html) to build and install
  - In short: `./configure && make` and `sudo make install`

Portaudio requires you to install [msgpack](https://msgpack.org/index.html)
  - `pip install msgpack`

Install librosa - librosa may ask you to DOWNGRADE ffmpeg, which is fine
  - `conda install -c conda-forge librosa`
