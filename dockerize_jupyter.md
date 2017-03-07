# **How to dockerize jupyter**
If you don't want to install jupyter on your PC, you can dockerize it.  
If you don't know docker, you can look at [docker's website](https://www.docker.com). Here you can also find how to install Docker on your computer.  
When you have docker engine running on your PC, you can run jupyter with:  

`docker run -it --rm -p 8888:8888 -v /local/folder/for/work:/notebooks nazgul/simulation`

Then you have to open in your browser the link that you see in the terminal. At this link you will find your Notebook server listening for HTTP connections on port 8888.  
Near the -v flag you have to put your local path to the directory where you have your jupyter files. With -v flags, host mounts the default working directory on the host to preserve work even when the container is destroyed and recreated.
