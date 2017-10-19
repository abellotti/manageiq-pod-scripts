# abellotti/manageiq-pod-scripts

Scripts for setting up and managing ManageIQ application pods.

## To setup

```
$ mkdir ~/pods
$ cd ~/pods
$ git clone https://github.com/abellotti/manageiq-pod-scripts.git
$ ln -s manageiq-pod-scripts/bin .
$ ln -s manageiq-pod-scripts/templates_deploy .
```

## To use

```
$ cd ~/pods
$ cat - > env <<END
. manageiq-pod-scripts/env
# update any environment variables of manageiq-pod-scripts/env here.
END
```

## To deploy ManageIQ

```
$ cd ~/pods
$ git clone https://github.com/ManageIQ/manageiq-pods.git
$ ln -s manageiq-pods/templates .
```

Update the templates/miq-template.yaml to updated memory/cpu requirements as needed.

Configure the minishift as needed. see the bin/manageiq-start for some configuration which can be initially set with minishift config set.

Deploy ManageIQ

```
$ cd ~/pods
$ . ./env
$ deploy-manageiq -f
```


