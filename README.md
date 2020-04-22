# Mongo DB Cookbook

This cookbook installs mongodb from source.
It creates its own apt package and then installs it.
The recipe also creates the config and the service file with dynamic input of variables.

## List of what installs
- Mongodb

## Options and setting variables

Changes are made in the attribute file.
Changing the port:
```
# attributes/default.rb

default['mongo']['port'] = <new_value_here>
```

## Commands

### Test locally

Running my unit test:
```
chef exec rspec
```

Running integration tests and closing machine:
```
kitchen test
```

### Test in AWS

Running integration tests in AWS
```
KITCHEN_YAML=kitchen_cloud.yml kitchen test
```
