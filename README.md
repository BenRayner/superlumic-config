# nBOS Environment Configuration using Superlumic and Ansible

Superlumic is a utility wrapper around Ansible that simplifies the process of bootstrapping a new MacOS developer environment with the necessary tools and utilities used at Versent for the nBOS project.

## What will be installed?
The Superlumic utility will install the following utilities and Ansible roles prior to installing a user specific playbook
1. Homebrew Package Manager
2. Ansible
3. Sensible OSX Environment Defaults (Computer Name, Dock Size, Dock Position)
4. CLI Environment (Bash 4, Git, Git username and email configuration, CLI theme and bash completion)
5. Configurable role dependent package installation using Ansible

## Versent Confluence Guide

https://versent.atlassian.net/wiki/spaces/BR/pages/114556998/Development+Environment+Setup+with+Superlumic+and+Ansible

## Quick Start
1. Clone the repo and modify the "username.yml", replacing username with the intended username for the target MacOS machine.
2. Merge the modified "username.yml"
3. On the target developer machine, retrieve the superlumic bash script with curl.
```
$ curl -O https://raw.githubusercontent.com/Versent/superlumic-config/master/superlumic
```
4. Execute the superlumic-config bash script on the target machine, referencing the cloned repository with the user playbook
```
$ bash superlumic https://github.com/<forked_repository_url>/superlumic-config.git
```
