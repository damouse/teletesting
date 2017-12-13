# Testing

This is a testing directory for teletraan deployments.

## Setup Instructions

Clone teletraan to your local machine: 

```
git clone git@github.com:pinterest/teletraan.git
```

`deploy-agent` is written against python2.7, so you'll need to be careful with python versions when you set it up. The following install commands are all for python 2.

Install virtualenv:

```
pip install virtualenv
```

Create a new virtualenv and activate it: 

```
virtualenv venv
source venv/bin/activate
```

Install the deploy-agent:

```
pip install -e teletraan/deploy-agent
```

## Prompting for Builds

Run the deploy-agent: 
```
deploy-agent -f teletraan-agent.conf
```

Watch the logs: 

```
tail -f /tmp/deployd/logs/deploy-agent.log
```

### Other Info

To see all possible config options for the config file, check out `teletraan/deploy-agent/deployd/common/config.py`