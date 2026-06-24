Install CHALK on Your Desktop
=============================

Follow these steps to install CHALK on your desktop:

1\. Create and Activate Anaconda Environment
--------------------------------------------

Create an Anaconda virtual environment with Python 3.9 or higher, and activate it:

```
conda create -n CHALK python=3.9 -y
```
```
conda activate CHALK
```

2\. Clone the CHALK Repository
------------------------------

Navigate to the directory where you want to install CHALK, clone the repository, and move into the folder:

```
cd {path-to-chalk-folder}
```
```
git clone https://github.com/kongeun3/CHALK.git
```
```
cd CHALK
```

3\. Install Required Packages
-----------------------------

Install the necessary packages by running the following command in your terminal or command prompt:

```
pip install -r requirements.txt
```

4\. Install PyTorch Compatible with Your Desktop Environment
------------------------------------------------------------

Install PyTorch 2.1 compatible with CUDA 12.1 (updated at: 2026-06-25):

```
conda install pytorch==2.1.0 torchvision==0.16.0 torchaudio==2.1.0 pytorch-cuda=12.1 -c pytorch -c nvidia
```

5\. Install MMSegmentation and MMDetection Using OpenMIM
--------------------------------------------------------

To install MMSegmentation, MMDetection, and their required dependencies, run the following commands:

```
pip install -U openmim
```
```
mim install "mmcv<2.2.0"
```
```
mim install "mmsegmentation>=1.0.0"
```
```
mim install mmdet
```

6\. Install the Segment Anything Model (SAM1)
---------------------------------------------

Install the Segment Anything Model by running this command:

```
pip install git+https://github.com/facebookresearch/segment-anything.git
```

7\. Install PyDenseCRF from Lucas Beyer's GitHub Repository
-----------------------------------------------------------

Install PyDenseCRF by running this command:

```
pip install git+https://github.com/lucasb-eyer/pydensecrf.git
```

8\. Setup CHALK 
---------------

To setup CHALK, run the following command:

```
python setup.py develop
```

9\. Download checkpoint files for Autolabeling Function 
-------------------------------------------------------

Checkpoints for the autolabeling function are available at the following links and should be placed in the `dnn/checkpoints` directory:

[CGNet trained for Crack Detection](https://www.dropbox.com/s/okikp25lw58jg8y/cgnet.pth?dl=0)\
[Segment Anything Model (vit_h)](https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth)

Once you've completed these steps, CHALK should be installed and ready to use on your desktop.