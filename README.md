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
pyenv rehash
conda list -n jupyter-notebook-pandas
conda list -n jupyter-notebook-pandas --export > env.txt

# reinstall
# pyenv install anaconda3-4.2.0
# pyenv rehash
# pyenv activate anaconda3-4.2.0
# conda create -n jupyter-notebook-pandas python=3.5 --file env.txt
```


