# reproducability-tutorial    1  ls

## Install Conda
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
ln -s /opt/conda/pkgs/*/bin/* /bin
ln -s /opt/conda/pkgs/*/lib/* /usr/lib
/opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
/opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
/opt/conda/bin/pip install bash_kernel
/opt/conda/bin/pip install ipykernel

## Start Jupyter Notebook
/opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
/opt/conda/bin/python3 -m bash_kernel.install
