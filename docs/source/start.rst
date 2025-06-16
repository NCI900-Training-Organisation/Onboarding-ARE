.. _getting-started:

Getting Started
-------

This document provides an overview and instructions for using ARE (short for Australian Research Environment) for NCI training events. 

* What is ARE?
 ARE is an online HPC portal that provides web-platform access to NCI's HPCD resources, such a file management, shell access to the backend HPC system, HPC job management, and access to certain web-enabled applications such as Jupyter Notebooks, RStudio.

* How to access ARE?
    To access ARE, you need to have an NCI account. If you do not have one, please refer to the NCI documentation on how to create an account. Once you have an account, you can access ARE by visiting the following URL:
    
    .. admonition:: Note
        :class: note

         https://are.nci.org.au

    

    You will be prompted to log in using your NCI credentials. **Note:** The Username is the NCI account name not your email address; the password is the same as your NCI account password.

* How to use ARE?
    After logging in to ARE, you will see a web platform with various options.

    .. image:: ./figures/ARE_login.png
        :width: 600px
        :align: center

    As the dashboard image above shows, you can access different services through the ARE portal including:

    - **Jupyter Notebooks**: A web-based interactive computing environment where you can access Gadi file systems, and python programming.

    - **RStudio**: A web-based integrated development environment (IDE) for R programming.

    - **Virtual Desktop**: A web-based mate desktop environment that allows you to access a virtual machine with a graphical user interface (GUI). It's useful for graphical applications.

    - **Gadi Terminal**: A web-based terminal that provides shell access to the Gadi HPC system. You can use it to run commands, manage files, and submit jobs.


    .. admonition:: Note
        :class: note

        For NCI training events, we will primarily use the **Jupyter Notebooks** as the main interface for accessing Gadi resources, even for non-python programming materials.

* How to use ARE Jupyter Notebooks?
To use Jupyter Notebooks in ARE is simple. After logging in to ARE, click on the **Jupyter Notebooks** option in the dashboard. This will direct us to the next page where you can specify the resources you want to use for your Jupyter Notebook session.

    .. image:: ./figures/ARE_param.png
        :width: 600px
        :align: center

 The basic parameters needed are shown in the image above, which are:

 - **Walltime**: The maximum time duration for your Jupyter Notebook session. 

 - **Queue**: The queue to which your Jupyter Notebook session will be submitted (For details of different types of queues available on Gadi; See https://opus.nci.org.au/x/ZIQeDg). For training events, we typically use the **normal** queue. **Note:** The field is free-text, so you can type in the queue name.

 - **Compute Size**: Amount of CPU/Memory resources available to your jupyter session

 - **Project**: Project to submit gadi job under; requires an SU allocation. For training events, we typically use  **vp91**. 

 - **Storage**: The storage space accessible to your Jupyter Notebook session. Default if **/scratch/vp91**.

 In some training sessions, we may need to specify additional parameters. 
 They are provided in the **advanced options**. 
 In those events, usually we need to specify **Modules** and **Python or Conda virtual environment base**. 
 
 - **Modules**: The software modules that you need to load such as a particular version of Python.

 - **Python or Conda virtual environment base**:  Some of our trainings materials are delieved using tailored Python 
 virtual environments. In those cases, your instructor will provide you with the path to the virtual environment.


Once you have specified the parameters, click on the **Launch** button to start your Jupyter Notebook session. 
In the backend, this will parse your parameters and convert them into a batch job script to submit to Gadi.
Launching the job will also redirect to the page **My Interactive Sessions** where you can see the status of your Jupyter Notebook session.

    .. image:: ./figures/ARE_launching.png
        :width: 600px
        :align: center

Depending on the size of the job and the status of Gadi. You might need to wait for a few seconds to a few minutes.
Once your Jupyter Notebook session is ready, you will see the status change to **Running**.
You can then click on the **Open** button to access your Jupyter Notebook session.

    .. image:: ./figures/ARE_running.png
        :width: 600px
        :align: center 

Once you click on the **Open** button, it will open a new tab in your web browser with the Jupyter Notebook interface.
    .. image:: ./figures/ARE_web.png
        :width: 600px
        :align: center

Notice that the Gadi file system is mounted and accessible in the left panel.

* Common Issues

    - **Bad request**: This error is often caused by issues with cookies or cache. To resolve it, open another tab and log in again, or try using incognito mode.

    - **Not a Member of vp91**: If you only have been granted access to vp91, you need to wait for 20 minutes or so until your access is updated in the system.
``