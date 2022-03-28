# Welcome to HAPE University!

## Introduction
In this lesson of HAPE University, I'll be showing you how to train your computer to recognize hand-written digits with >95% accuracy using the MNIST digit dataset! 

This lesson is intended for individuals with intermediate python programming skills. In the interest of time, you must have your environment properly set up for this lecture beforehand. Please follow the guide below to get set up.

If you have any questions, feel free to ping me on Discord: **Aydin#8215**
## Setup
I'll be running this on Ubuntu 20.04, and  will perform the calculations on my RTX 3070. If you have a weaker GPU or none at all, the script will take longer to train, but should produce the same results. 

### 1. Clone this repository
This repository contains the data and boilerplate code to build our model. You should clone it to access the data and code template by running the command 

    git clone https://github.com/AydinGokce/HAPE-AI.git

After this, unzip the `dev-data.zip` file to the SAME DIRECTORY, with the name as `dev-data/`

### 2. Set Up Anaconda Environment
If you do not have Anaconda installed, you must install it following the installation guide: https://docs.anaconda.com/anaconda/install/index.html

After installation, you must create a virtual environment in python 3.9

    conda create -n hape_ai python==3.9


### 3. (Optional) Install CUDA for GPU Usage
In order to use GPU acceleration to train the model, you must have the right CUDA drivers and [toolkit](https://developer.nvidia.com/cuda-toolkit) installed for your PC. If you are on linux, make sure you're not using the open source nouveau drivers.

Search online and on NVIDIA's website to download the drivers and CUDA toolkit, and follow NVIDIA's installation guide to make sure your environment is properly set up.  

### 4. Install Packages

To install the required python packages for this class, you first need to activate the virtual environment you'll be using.

    conda activate hape_api

***
**Installing PyTorch**

In this class, we will use PyTorch to build our model, so you have to go to their website: https://pytorch.org/get-started/locally/ and follow the instructions there to install the correct version. 

**If you have an NVIDIA GPU**, you can usually install it with the command:

    conda install pytorch torchvision torchaudio cudatoolkit=<YOUR_CUDA_VERSION> -c pytorch

where `<YOUR_CUDA_VERSION>` is the version of CUDA toolkit which you are using. In my case, this is `11.3`.

**If you don't have an NVIDIA GPU**, or have one but don't want to use it, you can install the CPU version with:

    conda install pytorch torchvision torchaudio cpuonly -c pytorch

***
**Installing Packages**

After installing pytorch, there are a handful of other packages you need to install for it to work. To install each of them, make sure you are in the repo's **root directory**, and run:

    pip install -r requirements.txt
***
**Installing Jupyter Kernel**
Lastly, you need to add your virtual environment to jupyter notebook so we can use it to run the code. To do this, run the command:

    python -m ipykernel install --user --name=hape_ai

### 5. Validate Setup
Enter the `src/` directory and load up the file `CNN_Boilerplate.ipynb` in a jupter notebook. You can do this by running the command `jupyter-notebook CNN_Boilerplate.ipynb`, or just by opening the jupyter desktop app and navigating to  `CNN_Boilerplate.ipynb`.

Select `hape_ai` as the project kernel (your screen may look a little different from mine, and that's OK), 
![](https://lh3.googleusercontent.com/Hr3jflkz00AoUX1Li8OXkNxtZpLnvtgzFvJlo9rm9ifupAyNQJwkiORPunXjNWOldplb0T99_Wu7dvuSTRwxKq7hWu7iahdgHGloTKQUOoPl_RgoW4JCRuFFSrREnOEoB08656Lu5euyV6_NjvlsYxvmGe-iB1fH-uk-L0J95nf7wRspGJ2IGm8VNdztR_jXsYwyROmW3Li8gVYY8DQck-S12tJCN4I6n-CrWqlqeC7nG4At4dVO13DBVo4DU_KMQXFmnhkkQJEqHUrHgMemQ6J8ayyeW2KUcwNiD-SywMtcpC5wZ9B1-NDZyDpGASMyrFhP81edxLJwpnZhY91XgWYfyET-CCHVLxo_iD9ZOCtxFcCTJcNN66Y4A_tcsPIdRIuyW5j42nPWbgjBDdwDsz1s7fbFanWFruXuwMavkz4tU5osnS-LjFsHTLqaG5-Q-GrSP3M5SpX4t9M-qQzHtlx9heB2_bJu-Fi9jweWkw_7YE0HEUEsKvw4fFHUEx3gxnYoON4Bs7XVGV2-MB5w-0EQOtKY87KuDK1iJNn99LoqWx-CHNjI2fnHlk6_Y4chxHOwQBzf09SCoMhr2dwDDYAVnevmNWQPnlO00WEu5m9W7AvRMHcjlJkZa95Yc3jS0fBMbS_CvCzqe6BD97YLjzIOIyiHXo3Rh8w3mDo5XPR0_t8b4-DMcg9LyfGOjnBTV52acWaTw7O2gYNU6VURVrwcAtZGrAisDqHOlV9jPpqdoyJ_kbxWRGXBLdAq8fperx_YPIZGLAj7D-O1TbD5gnyU1Ki1NRHIAh26hTz4neDqRIcT313KtDuB1L6KrFE0L4zUGo_waENME-IhDqR-ZK6bFWlt9mxSY8PdReknpA=w1148-h399-no?authuser=1)

And run the first cell. 

If anything goes wrong, make sure you

 1. Have the packages installed correctly (you can check this using the command `pip list`)
 2. Selected the right environment within Jupyter Notebook 

If you can't figure it out, search the web to find a solution, or you can ping me (**Aydin#8215**) in the Discord coding-cave channel and I'd be happy to help out. 

Good luck! I hope to see you soon.
