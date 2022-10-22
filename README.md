## Ansible media stack

#### Configurables
- `group_vars/all.yaml`

| Value | Description | Default |
| :---        |    :----   |          ---: |
| docker.user | User to run containers under | ubuntu |
| optional_tasks.setup_compose | Create media stack directory structure and containers | enabled |
| optional_tasks.compose_basedir | Base directory to create the media_stack sub directories under | docker |
| optional_tasks.restartPolicy | Configure how Docker starts containers on boot | unless-stopped |
| optional_tasks.setup_docker_zfs | Create a ZFS dataset for Docker directories | disabled |
| optional_tasks.zpool_name | ZFS pool name where the Docker dataset will be created | storage |
| optional_tasks.compose_file.containers.radarr | Enable Radarr container in compose file | enabled |
| optional_tasks.compose_file.containers.sonarr | Enable Sonarr container in compose file | enabled |
| optional_tasks.compose_file.containers.jackett | Enable Jackett container in compose file | enabled |
| optional_tasks.compose_file.containers.transmission | Enable Transmission container in compose file | enabled |
| optional_tasks.compose_file.containers.transmission.flood | Enable the Flood web UI for Transmission | enabled |
| optional_tasks.compose_file.containers.plex | Enable Plex container in compose file | enabled |
| optional_tasks.compose_file.containers.plex.tautulli | Enable Tautulli for Plex monitoring in compose file | enabled |
| optional_tasks.compose_file.containers.ombi | Enable Ombi container in compose file | enabled |
| optional_tasks.compose_file.environment | Configure container environment variables | N/A |

_Tested on amd64 Ubuntu 22.04 LTS_