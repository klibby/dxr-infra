Setting up Docker
=================

DXR only runs on Linux at the moment,so  the indexing images and 
infrastructure are all Ubuntu or RHEL based, respectively.

If you're not running Linux on your host machine, you'll need a
virtualization provider. If you're on Windows or OSX, we recommend
using `Docker Toolbox` to install both VirtualBox and all of the
docker tools. If you're on Linux or a cloud-based system, follow
the `Docker Engine` installation instructions.

If the install did not create and start a Linux VM to host your containers
(run *docker-machine ls* to check!), then you'll need to do so manually:

    docker-machine create --driver virtualbox --virtualbox-disk-size 50000 --virtualbox-cpu-count 2 --virtualbox-memory 1024 default
    eval "$(docker-machine env default)"

Feel free to adjust the resource allocation numbers above as you see fit.

.. note:
    Next time you reboot (or run ``make docker_stop``), you'll need to restart
    the VM::

        docker-machine start default

    And each time you use a new shell, you'll need to set the environment
    variables that tell Docker how to find the VM::

        eval "$(docker-machine env default)"

    When you're done with DXR and want to reclaim the RAM taken by the VM,
    run... ::

        make docker_stop 


.. _Docker Toolbox: https://www.docker.com/docker-toolbox
.. _Docker Engine: https://docs.docker.com/engine/installation/
