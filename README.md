```bash
# install anaconda
pyenv install anaconda3-4.2.0
pyenv rehash
pyenv activate anaconda3-4.2.0
conda create -n jupyter-notebook-pandas python=3.5
pyenv activate anaconda3-4.2.0/envs/jupyter-notebook-pandas
pyenv rehash

# install tools
conda install pandas matplotlib nb_conda
conda install -y -c conda-forge jupyter_contrib_nbextensions
conda install -c anaconda pillow=4.0.0

pyenv rehash
conda list -n jupyter-notebook-pandas
conda list -n jupyter-notebook-pandas --export > env.txt

# reinstall
# pyenv install anaconda3-4.2.0
# pyenv rehash
# pyenv activate anaconda3-4.2.0
# conda create -n jupyter-notebook-pandas python=3.5 --file env.txt
# pyenv activate anaconda3-4.2.0/envs/jupyter-notebook-pandas
# pyenv rehash

# add vim binding
# Create required directory in case (optional)
mkdir -p $(jupyter --data-dir)/nbextensions
# Clone the repository
cd $(jupyter --data-dir)/nbextensions
git clone https://github.com/lambdalisue/jupyter-vim-binding vim_binding
# Activate the extension
jupyter nbextension enable vim_binding/vim_binding
```


