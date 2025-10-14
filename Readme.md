# Urbalytix Deployment

This repo contains Helmfile configuration and Docker compose scripts, to run Urbalytix application. See [Urbalytix repository](https://github.com/starwit/Urbalytix) for more information about the application.

## Helmfile

Helmfile is a powerful tool, to deploy multiple Helm charts. See folder [helmfile](helmfile/) for details how to install Urbalytix using Helmfile.

Installation:

1. Copy env.sh-template to env.sh
2. Set variables to strong passwords
3. Run Helmfile deployment
    ```bash
    # compute changes to cluster
    helmfile -e environment diff -f urbalytix.yaml 
    # run actual deployment
    helmfile -e default apply -f urbalytix.yaml 
    ```

## Docker Compose
TODO

# License

Project is licensed under AGPL 3 and the license can be found [here](LICENSE). This component is part of a publicly funded project by the city of Wolfsburg and thus usage in your community is very much encouraged. It is part of a group of software modules that shall help communities to analyze urban space and to gain statistical insights. 

More details on political and organizational background can be found here: https://www.wolfsburg.de/en-us/leben/smart-city