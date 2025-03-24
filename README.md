# DSMS Docs

This repository hosts the Sphinx user documentation for the DSMS.

The full documentation is available at [https://dsms.readthedocs.io/](https://dsms.readthedocs.io/).

## Local Rendering

### HTML

A server will start, generate the docs and listen for changes in the source files.
This can be done by using docker or installing the development environment directly on the you machine. Next are installation guides for Docker and Linux OS.

First, build the Docker image by running the following command:

```shell
docker build -f local_build.Dockerfile -t dsms-docs .
```

Then, start the program by running:

```shell
docker run --rm -v $PWD:/app -p 8000:8000 dsms-docs
```

### PDF (LaTeX)

To generate a PDF of the documentation, simply run from the root project folder the following code.
We recommend using virtual environments.

```shell
pip install -r requirements.txt
make -C docs latexpdf
```

The generated PDF can be found under docs/\_build/latex/DSMS_user_docs.pdf
