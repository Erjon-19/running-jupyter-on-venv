# running-jupyter-on-venv
This creates an isolated python virtual environment in witch you can run jupyter notebook and avoid confusion of different version python libs and also with system libs 

Steps on Linux (assume that we have jupyter and miniconda installed on our system):

###  install ipykernel virtual env

```sh
conda create -n myenv python=3.6
conda install ipykernel 
python -m ipykernel install --user --name myenv --display-name "Python (myenv)"
conda install -c conda-forge ipywidgets
pip install -r requirements.txt 
conda install pytorch torchvision torchaudio cpuonly -c pytorch
```

### Run jupyter notebook and select the created venv
```sh
jupyter notebook
```
myenv

### Delete env
```sh
conda remove -n myenv --all
```

###  Verify that the environment was removed
```sh
conda info --envs
```
