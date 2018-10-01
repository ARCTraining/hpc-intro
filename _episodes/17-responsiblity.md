---
title: "Using resources effectively"
teaching: 10
exercises: 5
questions:
- "How can I be a responsible cluster user?"
objectives:
- "Be a good person and be nice to the other researchers."
keypoints:
- "Don't run stuff on the login nodes."
- "Again, don't run stuff on the login nodes."
- "Don't be a bad person and run stuff on the login nodes."
---

You now have everything you need to run jobs, transfer files, use/install software, and monitor how
many resources your jobs are using.

So here are a couple final words to live by:

## Be kind to the login nodes!

* The login nodes are very busy managing lots and lots of jobs! It doesn’t have any extra space to run
  computational work. **Please** don’t run jobs on the login node, though quick tests are generally fine. A
  “quick test” is generally anything that uses less than 10GB of memory, 4 CPU cores, and 15 minutes of
  time. Remember, the login nodes are to be shared with other users.

> ## Login Node Etiquette
> 
> Which of these commands would probably be okay to run on the login node?
> 1. python physics_sim.py
> 2. make
> 3. create_directories.sh
> 4. molecular_dynamics_2
> 5. tar -xzf R-3.3.0.tar.gz
{: .challenge}

* If someone is being inappropriate and using the login node to run all of their stuff, please let us know.
  We'll contact the user and ask them to change their behaviour.

## Test before scaling

* Before submitting a large run of jobs, submit one as a test first to make sure everything works. Find out 
  how long the job takes to run, how much memory it uses and an optimal number of CPU cores.  Fine tune your
  later job submissions to be close to this (we normally suggest add 20% to these figures as an overhead) and you'll
  get much better throughput on the systems.

## Have a backup plan

* Use a Version Control system like `git` to keep track of your code and think carefully where and how you store your
  input and output data. Only your home directories are backed up and although we trust these backups, you shouldn't rely on it for something as key as your research code. The best backup system is one you manage yourself.

* The `nobackup` file systems (sometimes called *scratch* or temporary storage) are called **nobackup** for a reason. They 
  are intended for short term storage of input and output data and should not be the only copy you keep of essential data.

* Eventually, your data will need to leave the cluster. You should have a plan of where you’ll store
  all your results *before* you run jobs.  This should be part of your **data management plan** and **software manahement plan**.  

## Save time

* Compress files before transferring to save file transfer times with large datasets.

* The less resources you ask for, the faster your jobs will find a slot in which to run. Lots of
  small jobs generally beat a couple of big jobs.

## Software tips

* You can generally install software yourself (and we run a workshop that shows you a few ways of doing this), but if you     want a shared installation as a software module, let us know and we'll discuss the best way of accomplishing this.

* Always use the default compilers if possible. Newer compilers are great, but older stuff generally
  has fewer compatibility issues.

{% include links.md %}
