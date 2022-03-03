# running-jupyter-on-venv
This creates an isolated python virtual environment in witch you can run jupyter notebook and avoid confusion of different version python libs and also with system libs 

Steps on Linux:

###  install ipykernel virtual env

conda create -n myenv python=3.6
conda install ipykernel 
python -m ipykernel install --user --name myenv --display-name "Python (myenv)"
conda install -c conda-forge ipywidgets
pip install -r requirements.txt 
conda install pytorch torchvision torchaudio cpuonly -c pytorch

### Run jupyter notebook and select the created vm

jupyter notebook
myenv

### Delete env
conda remove -n myenv --all

###  Verify that the environment was removed
conda info --envs
