# **How to dockerize jupyter**

If you don't want to install jupyter on your PC, you can dockerize it, that is
set up a virtual machine with all the needed software. Refer to the [official
website](https://www.docker.com) for a general introduction to Docker and for
installation instructions. Once you have a Docker engine running in your PC,
you can run jupyter by entering the following command in a terminal:

`docker run -it --rm -p 8888:8888 -v /local/folder:/notebooks nazgul/simulation`

this command will print a URL to point your browser to in order to get to
the jupyter installation in the virtual machine, that is a HTTP server
listening on the port 8888. Note that the value for the `-v` flag should be
set to the local pathname of the directory where the lectures' repository has
been cloned. In this way the default working directory is mounted on the host,
to preserve work even when the container is destroyed and recreated.
