# Mongo DB Cookbook

This cookbook installs mongodb from source.
It creates its own apt package and then installs it.
The recipe also creates the config and the service file with dynamic input of variables.

## Pre-requisites

- Chef
- Git
- Mongodb
- AWS CLI v2
- Virtual Box

## Chef

Chef is a configuration management tool. Using Chef, you can provision cookbooks by giving recipes packages you will need to use in your environment, while being to safely test that everything is installed. This will allow you to easily create an AMI which has a standardised and provisioned environment.

## Options and setting variables

Changes are made in the attribute file.
Changing the port:
```
# attributes/default.rb

$ default['mongo']['port'] = <new_value_here>
```

## Commands

Follow the commands below to run the cookbook.

### Cloning the repo

To clone this repo:
```
$ git clone git@github.com:hovell722/MongoCookbookStarterCode.git
```

### Test locally

Running my unit test:
```
$ chef exec rspec
```

Running integration tests and closing machine:
```
$ kitchen test
```

### Test in AWS

Running integration tests in AWS
```
$ KITCHEN_YAML=kitchen_cloud.yml kitchen test
```
