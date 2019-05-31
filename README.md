# ansible-tower-samples
Ansible Tower Playbook Samples

## hello_world.yml
### tasks
- Hello Message
- Show IP Address
- Ansible Jinja2 for range
- Ansible Jinja2 filters
- Exploring register
- Show register
- Use of tags: press return to separate a tag; use prompt 

## include_import_playbook.yml
### tasks
- Use of include_tasks
- Use of import_tasks
- Use of import_playbook

## Get into a container 
`$ docker exec -it <container_name> sh`
## Find current Docker network
`$ docker network ls`
## Connect a running container to a network
Don’t put --network here; the container must be a running one.
`$ docker network connect <network_name> <container_name>`

## Connect a container to a network when it starts
Put --network; to start a new container of an image
`$ docker run -itd --network=<network_name> <image_name>`

## Add hosts to AWX controller 
* Add `ssh-keygen` for the controller and hosts
* Add controller’s `.ssh/id_rsa` on AWX credentials field
* Add controller’s `.ssh/id_rsa.pub` on all hosts’ `.ssh/authorized_keys`
* `chmod 700 .ssh`
* `chmod 600 .ssh/authorized_keys `
* Add hosts that have been authorized in inventories on AWX 
