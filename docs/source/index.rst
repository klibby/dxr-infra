Overview
======================================

**dxr-docker** is a set of tools and configurations to manage the infrastructure behind
https://dxr.mozilla.org/; it includes:
* `Ansible` playbooks to manage the build and webapp infrastructure
* `Docker` Dockerfiles for images used to index trees
* `Jenkins Job Builder` YAML configs to manage Jenkins build jobs
* A deploy script built around `mach` to run all of the above

The canonical repository is https://github.com/klibby/dxr-docker/.

.. _Ansible: https://github.com/ansible/ansible/
.. _Docker: https://www.docker.com/
.. _Jenkins Job Builder: http://docs.openstack.org/infra/jenkins-job-builder/
.. _mach: https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/mach

Contents:

.. toctree::
   :maxdepth: 2

   setup
   docker
   jenkins
   usage
   contributing

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

