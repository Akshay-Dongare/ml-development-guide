# ML Development Guide
This is a general guide about package installation and system setup

# Windows System Setup
## Windows Terminal
* Download Windows Terminal App from Microsoft Store
* https://www.microsoft.com/store/productId/9N0DX20HK701?ocid=pdpshare
## Windows Powershell
* Download latest Powershell App from Microsoft Store
* https://www.microsoft.com/store/productId/9MZ1SNWT0N5D?ocid=pdpshare
* Open Windows Terminal Settings and select this as the Default Shell
## Miniconda
* Use miniconda to manage virtual environments for projects
* Check your system's configuration (ie, x86, 64 bit or ARM)
* Download the appropriate installer from https://docs.anaconda.com/free/miniconda/
* Run the installer and install miniconda at your preffered path
* Create new environment with latest python: `conda create -n llm python`
* Activate the new environment: `conda activate llm`

## Microsoft Build Tools
* You can potentially need this in the future while developing ML applications and installing packages
* To prevent future errors like this one: https://github.com/Akshay-Dongare/Error-Cpp-Build-Tools
* Install Build Tools using these steps:
1. Download the Visual Studio Build Tools installer at https://visualstudio.microsoft.com/visual-cpp-build-tools/ 
2. Install the 'Desktop Development with C++' components using Visual Studio Build tool. (approx 6.84GB total)
3. Locate the directory where MSBuild is installed (typically "C:\Program Files (x86)\Microsoft Visual Studio\20xx\BuildTools\MSBuild\Current\Bin" where the xx in 20xx signifies the version of Microsoft Build Tools you have downloaded) and add it to the PATH variable (This is an extremely important step as it ensures that Build Tools can be found by other programs like pip). Add it to the System Environment PATH variable rather than User Environment PATH variable.
4. Install cmake (pip install cmake) if not already installed.
5. RESTART your computer.
* Source: https://learn.microsoft.com/en-us/answers/questions/136595/error-microsoft-visual-c-14-0-or-greater-is-requir

# NVIDIA GPU Setup
## Drivers
## CUDA Toolkit
## CUDNN
## Paths
* C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.5\extras\CUPTI\lib64
* C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.5\include
* C:\tools\cudnn-windows-x86_64-8.3.1.22_cuda11.5-archive\bin
* C:\tools\cudnn-windows-x86_64-8.3.1.22_cuda11.5-archive\include
* C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.5\bin

# Docker Setup 
* Use Docker Volumes (docker run -v) to map current working dir to container dir to get real time updates in the container
* Install VS code extensions: Dev Containers (by Microsoft), Docker
* Then from vs code, connect remote to running docker container
* In the new window in Remote VS code, install python extension to get all the vs code features like autocomplete, refactor and peek defination
* `docker-compose.yml` file allows to specify services and to run our container using a single simple command
* Source: https://www.youtube.com/watch?v=6OxqiEeCvMI&t=108s&ab_channel=Docker

# TensorFlow Setup
# PyTorch Setup

# Jupyter Setup
## Jupyter Notebook
### Installation
* `pip install notebook`
### Usage
* In terminal, `jupyter-notebook`
## Jupyter Lab
### Installation
* `pip install jupyterlab`
### Usage
* In terminal, `jupyter lab`

## Setting Conda Environment as Jupyter Kernal

