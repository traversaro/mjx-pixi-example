# mujoco-mjx-pixi-example

Example of running the official Mujoco MJX Jupyter Notebook example without Colab with pixi.

## Requirements

Linux system with Nvidia GPU with CUDA support, with at least 4 GB of VRAM (tested on GeForce RTX 3050 Ti).

## Run

If you do not have it, install [pixi](https://github.com/prefix-dev/pixi#macos-and-linux) (in a nutshell: `curl -fsSL https://pixi.sh/install.sh | bash`), then:

~~~
git clone https://github.com/traversaro/mujoco-mjx-pixi-example
cd mujoco-mjx-pixi-example
pixi run notebook_tutorial
~~~

and then follow the notebook.

If you are running the notebook on a remote machine to which you are connecting via ssh, make sure to [setup an SSH tunnel for the port of the notebook](https://docs.anaconda.com/free/anaconda/jupyter-notebooks/remote-jupyter-notebook/), i.e. : 
~~~
ssh -L 8888:localhost:8888 <REMOTE_USER>@<REMOTE_HOST>
cd mujoco-mjx-pixi-example
pixi run notebook_tutorial --no-browser --port=8888
~~~

## Details

The notebook is based on https://github.com/google-deepmind/mujoco/blob/3.1.3/mjx/tutorial.ipynb, with some modifications to permit to run the notebook outside Google Colab.
