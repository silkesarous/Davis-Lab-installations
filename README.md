# Davis-Lab-installations
## Run

### napari

- Launch 'Miniforge Prompt' Windows application
- Activate the napari virtual environment: `conda activate napari-env`
- Launch: `napari`

### cellpose

- Launch 'Miniforge Prompt' Windows application
- Activate the cellpose virtual environment: `conda activate cellpose-env`
- Launch: `python -m cellpose`

## Install

### miniforge

Reference: `https://github.com/conda-forge/miniforge`

- Need an Anaconda distribution so we can setup a virtual environment with the 'conda' commands, there are several options like miniforge, miniconda, or the full Anaconda Distribution. Chosen miniforge.
- Follow the miniforge GitHub installation instructions for your OS, for example, for Windows download the `Miniforge3-Windows-x86_64.exe` mentioned here: `https://github.com/conda-forge/miniforge?tab=readme-ov-file#windows`
    - Windows:
        - Run the installer
            - Install for 'Just me'
            - Choose install location
            - Tick 'Create shortcuts' but untick other advanced options
            - Can now launch 'Miniforge Prompt' to run conda commands
    - MacOS: 
        - Open terminal: Click the Launchpad icon in the Dock, type Terminal in the search field, then click Terminal
        - Run the miniforge downloader: `curl -L -O "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"`
        - Run the miniforge installer: `bash Miniforge3-$(uname)-$(uname -m).sh`
        - Can now use terminal to run conda by typing `conda`
        


### napari

Reference: `https://napari.org/stable/tutorials/fundamentals/installation`

- Launch 'Miniforge Prompt' Windows application
- Create a virtual environment for napari: `conda create -y -n napari-env -c conda-forge python=3.10`
    - Tip: virtual environment will end up somewhere like this: `C:\Users\au704457\AppData\Local\miniforge3\envs\napari-env`
- Activate the virtual environment: `conda activate napari-env`
- Install napari: `conda install -c conda-forge napari pyqt`
- Update napari: `conda update napari`

### cellpose

Reference: `https://github.com/MouseLand/cellpose#local-installation--2-minutes`

- Launch 'Miniforge Prompt' Windows application
- Create a virtual environment for cellpose: `conda create --name cellpose-env python=3.10`
    - Tip: virtual environment will end up somewhere like this: `C:\Users\au704457\AppData\Local\miniforge3\envs\cellpose-env`
- Activate the virtual environment: `conda activate cellpose-env`
- Install cellpose3.0 (recommended for personal computers):
    - With GUI (recommended): `python -m pip install cellpose[gui]==v3.1.1.2`
    - Without GUI: `python -m pip install cellpose`
- Install cellposeSAM (newest version, recommended for workhorse computers):
    - With GUI (recommended): `python -m pip install cellpose[gui]`
    - Without GUI: `python -m pip install cellpose`
- Update cellpose: `python -m pip install cellpose[gui] --upgrade`

### (OPTIONAL) Jupyter notebooks

- If you want to use Jupyter notebooks in a virtual env, need to install them in that env, for example, launch 'Miniforge Prompt' Windows application, then:

```
conda activate cellpose-env
python -m pip install notebook
python -m pip install matplotlib
```
