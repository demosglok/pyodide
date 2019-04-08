# Pyodide


The Python nucypher stack, compiled to WebAssembly.

This is the attempt to run nucypher code in browser. For now only pyUmbral stuff and dependencies was added as modules

It provides transparent conversion of objects between Javascript and Python.
When inside a browser, this means Python has full access to the Web APIs.

**See the original project [pyodide project](https://github.com/iodide-project/pyodide)

# Building

Building was checked only on Linux Ubuntu. 

## Using Docker

We provide a Debian-based Docker image on Docker Hub with the dependencies
already installed to make it easier to build Pyodide.

1. Install Docker

2. From a git checkout of Pyodide, run `./run_docker`

3. cd `/src`

4. Run `make` to build.

5. Run `setup_libs` to setup libs necessary for cffi and other umbral stuff

6. Run `make`  again to build modules

You can edit the files in your source checkout on your host machine, and then
repeatedly run `make` inside the Docker environment to test your changes.


# Manual Testing

Exit docker container or just use another console
Copy all contents of ./build folder into public folder of your frontend app
I used public/pyodide and public/pyodide2 for experiments with http://github.com/demosglok/nucypher_webassembly
