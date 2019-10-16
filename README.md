# Ansible Swarm Playbook
#You should do this with Kubernetes!

Playbook for creating/managing a Docker Swarm cluster (requires Docker >= 1.12).
Companion files to the following post: https://thisendout.com/2016/09/13/deploying-docker-swarm-with-ansible/
## Assumptions
This playbook assumes a running Docker daemon on the hosts and that the following Ansible inventory groups have been populated: `manager` and `worker`.
## Variables
You can override the `swarm_iface` variable in Ansible to determine the listening interface for your swarm hosts.
## `swarm.yml` vs. `swarm-facts.yml`
The `swarm.yml` playbook uses a shell statement for determining cluster membership where the `swarm-facts.yml` playbook uses the `docker_info_facts` module for injecting Docker info as facts then checking cluster membership against that.

#Traefik
https://medium.com/@joshuaavalon/setup-traefik-step-by-step-406792afe9b2
LetsEncrypt requires a real public domain name (this may of been why it failed with rlab.local, need to test)


# Removed from command: > inside compose-traefik-step-by-step-406792afe9b2
      #--acme
      #--acme.email=${EMAIL}
      #--acme.storage="traefik/acme/account"
      #--acme.entryPoint=https
      #--acme.httpChallenge.entryPoint=http
      #--acme.onhostrule=true
      #--acme.acmelogging=true


