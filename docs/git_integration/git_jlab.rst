Starting with git on the jupyterhub
===========================


Adding your git username and email
----------------------------------

First thing that you would want to do is to add your github username and email to the ``git config``.
To do that, open a terminal (f.e. through launcher) and do:

.. code-block:: bash


   git config --global user.name "<your_username>"
   git config --global user.email "<your_email>"

You can check if the config is added by doing ``git config --get user.name``.

Using git GUI extension:
------------------------

.. |gitico| image:: img/git_ico.png

We have added a GUI extension ti jupyterlab for easier work with git.
You can see a git icon |gitico| on the left panel. To clone a repository, click on the icon and then on **Clone Reopsitory**. 
You should see the following promt:

.. image:: img/clone-repo.png
   :width: 800
   :alt: Cloning repo GUI

Chek both boxes and press **Clone**. You will get the following promt:

.. image:: img/gui-credentials.png
   :width: 300
   :alt: Credentials promt GUI

If you do not know what a personal access token is follow `official github instructions <https://docs.github.com/en/enterprise-server@3.9/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens>`_ to create one. Usually, the tokens start with ``ghp_***``. Treat this token as a password. 
Once you've logged in you will see in the file browser that a folder was created with the same name as the repo you have cloned.
Go into that folder in the file browser and then click on the git tab |gitico| in the left panel. You will see the following:

.. image:: img/repo-tab.png
   :width: 200
   :alt: Repo tab GUI

You can hover over different tabs and buttons too see what they do. If you click on **History** tab, you will see the beautiful graph of the commit-history of the branch you are currently on.
You can clone multiple repositories and if you are in some repo folder within your file browser you can always click on the git icon to use version control for that specific repository.

Using git CLI
-------------
