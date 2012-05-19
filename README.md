# Awestruct for OpenShift

Template for running awestruct on OpenShift.

## Status

Work in progress, please report issues.

## Installation

Create OpenShift application

    rhc app create -a $name -t php-5.3

and enter the directory

    cd $name

Add this repository as new remote

    git remote add template -m master git://github.com/marekjelen/openshift-awestruct.git

and pull locally

    git pull -s recursive -X theirs template master

now build your application using Awestruct.

To deploy to OpenShift just push

    git push origin master

Now, your application is available at

    http://$name-$namespace.rhcloud.com

## What it does?

* Install awestruct if not available
* Update awestruct when already available
* Generate the site to static files

## Tools

* Awestruct