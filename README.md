# ipython-in-docker
Setting up an iPython kernel inside a Docker container for Jupyter notebook.

## Prerequisite
- Have Docker installed. See [Get Docker](https://docs.docker.com/get-docker/)

## Usage
1. Build a docker image.
```
$ docker build -t ipython-in-docker .
```

2. Create a new `ipython-in-docker` directory to set up a new Jupyter kernel.
```
$ mkdir -p ~/.local/share/jupyter/kernels/ipython-in-docker
```

3. Copy the `kernel.json` file to Jupyter. **Note**: Change mount directory `/home/jupyter` to your appropriate workspace directory.
```
$ cp kernel.json ~/.local/share/jupyter/kernels/ipython-in-docker/
```

4. In your Notebook, select `ipython-in-docker` as kernel.
