There are definitions of jobs for Jenkins in Jenkins Job Builder syntax in this directory.
There are 2 job type:
 1. ```1-{clustername}-cluster-create``` - gets machines from CentOS CI machine pool and prepare them for installing Gluster.
 2. ```X-{clustername}-cluster-teardown``` - returns machines back to pool

How to upload jobs to CentOS CI Jenkins:
 1. ```cd ~/usmqe-centos-ci```
 1. ```git pull```
 2. ```jenkins-jobs --conf ~/jenkins-config.ini test tendrl-jobs-create.yml```
 3. if everything is OK do ```jenkins-jobs --conf ~/jenkins-config.ini update tendrl-jobs-create.yml```

*DO NOT* upload jobs whic are not in Git.
