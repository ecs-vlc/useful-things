% JUPYTER-REMOTE(1)
% Jonathon Hare
% July 2018

# NAME

jupyter-remote – run jupyter notebook on a remote machine

# SYNOPSIS

**jupyter-remote** [OPTION]... [user@]hostname

# DESCRIPTION

**jupyter-remote** is a simple tool to launch a jupyter notebook server on a remote machine, set up ssh tunnels and optionally share the local working directory to the remote machine to use as 
the root directory for the notebook server. This is particularly useful if you want to run a locally stored notebook on a machine with a different hardware configuration (e.g. GPUs, more memory, faster processors, etc).

# GENERAL OPTIONS

**-f**, **--no-fs**
:   Do not mount the local working directory on the remote server and use it as the remote working directory. If this option is not selected the remote working directory will by default be the remote home directory unless **--remote-base** is set.

**-r**, **--remote-port**
:   Override the port to use on the remote side for the jupyter server. By default we try to choose an open port automatically.

**-l**, **--local-port**
:   Override the port to use on the local side to tunnel the jupyter server to. By default we try to choose an open port automatically.

**-rf**, **--remote-fs-port**
:   Override the port to use on the remote side for serving the local filesystem. By default we try to choose an open port automatically.

