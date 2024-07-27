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
* Check your system's configuration (ie, x86 aka 32 bit, 64 bit or ARM)
* Download the appropriate installer from https://docs.anaconda.com/free/miniconda/
* Run the installer and install miniconda at your preffered path. If username has spaces in between, install it in a new folder in another new folder in C drive (example: C:\AkshayTools\Miniconda3) or else some third party packages might cause issue later.
* Create new environment with latest python: `conda create -n llm python`
* Activate the new environment: `conda activate llm`
## Git
* Download latest from https://git-scm.com/download/win
* Install in new folder in C drive (C:\AkshayTools)
* Choose whichever options you feel right during install 
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

* Install the Latest Microsoft Visual C++ Redistributable Version (2022) from https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170

# NVIDIA GPU Setup
## Drivers
1. Download GeForce Experience App from https://www.nvidia.com/en-in/geforce/geforce-experience/
2. Open it and Choose Studio Driver as it will be more stable than Game Ready Driver which is for latest releases
3. Check for updates and download latest Studio Driver 
## CUDA Toolkit
1. Check this site for compatibility table of Cuda Toolkit version and NVIDIA Driver Version : https://docs.nvidia.com/deploy/cuda-compatibility/index.html#binary-compatibility__table-toolkit-driver
## CUDNN
## Paths
* C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.5\extras\CUPTI\lib64
* C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.5\include
* C:\tools\cudnn-windows-x86_64-8.3.1.22_cuda11.5-archive\bin
* C:\tools\cudnn-windows-x86_64-8.3.1.22_cuda11.5-archive\include
* C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.5\bin

# Docker For Isolated Local Python Development Environment  Setup 
* Use Docker Volumes (docker run -v) to map current working dir to container dir to get real time updates in the container
* Install VS code extensions: Dev Containers (by Microsoft), Docker, Remote Development (an extension pack by Microsoft)
* Then from vs code, connect remote to running docker container
* In the new window in Remote VS code, install python extension to get all the vs code features like autocomplete, refactor and peek defination
* `docker-compose.yml` file allows to specify services and to run our container using a single simple command: `docker-compose up`
* If you change something in `requirements.txt`, for example you added a python module dependancy for the new service you added in `docker-compose.yml` so that you can use that service in your python code; you must build the docker image again like so: `docker-compose up --build -d` (d is for detached mode)
* To setup debugging, add debugpy module to python dependancies `requirements.txt`, then in `docker-compose.yml` file, under `ports:` map the 5678 port to 5678 (on local machine). Now in the Remote Docker container attached VS Code window, go to debugger and select `attach to remote debug server`, now enter `localhot` and port `5678`  
* Source: https://www.youtube.com/watch?v=6OxqiEeCvMI&t=108s&ab_channel=Docker

# TensorFlow Setup
# PyTorch Setup
1. Go to this site and copy paste the download command according to your configuration into your desired Conda env : https://pytorch.org/get-started/locally/
2. You can use Pip or Conda to install Pytorch. Both binaries ship with their CUDA dependencies and allow you to execute PyTorch code directly without installing a full CUDA toolkit locally. You would only need to install the NVIDIA drivers.
3. Check the Cuda Compatibility Table mentioned above in `Cuda Toolkit` to match the Cuda Toolkit binary you install from Pytorch to your installed NVIDIA Driver version
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

## Github CLI
1. https://cli.github.com/
### Github CoPilot in Github CLI
1. Source: https://docs.github.com/en/copilot/github-copilot-in-the-cli/using-github-copilot-in-the-cli
2. https://www.youtube.com/watch?v=P8MfgV9us4o&ab_channel=BeyondFireship
## Bitwarden Password Manager
1. Download from Microsoft Play Store
2. Published by 8Bit Solutions
