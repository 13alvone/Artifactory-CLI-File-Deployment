# Artifactory Send Script

This bash script, named `artifactory_send`, uploads a file to an Artifactory instance using the Artifactory URL, username, and password. The script accepts one argument: the target file to send. The remote file name will be the same as the target file name.

## Usage

1. Save the script as `artifactory_send` and give it execute permission using:

```shell
chmod +x artifactory_send
```

2. Run the script by providing the target file as an argument:

```shell
./artifactory_send <TARGET_FILE> <TARGET_REPO>

Available REPO's:
----------------------
'vm' --> VM ISO, OVF, etc
'vb' --> VM Backup
'b' --> Binary
'd' --> Docker
'db' --> Docker Backup
'a' --> Audio
'pdf' --> PDF
'f' --> Funny
'g' --> Games
'o' --> Other
```

The script will check for the required environment variables: `USERNAME`, `PASSWORD`, and `ARTIFACTORY_URL`. If any of these variables are missing, the script will prompt the user for input.

**Note** This script requires seperate Artifactory-OSS installation with an addressable LAN IP with proper permissions, as well as the properly created repositories as precisely named below:

> 'vm'             --> http://$ARTIFACTORY_IP:8082/artifactory/vm/
> 'vb'             --> http://$ARTIFACTORY_IP:8082/artifactory/vm_backup/
> 'binary'         --> http://$ARTIFACTORY_IP:8082/artifactory/binary/
> 'docker'         --> http://$ARTIFACTORY_IP:8082/artifactory/docker/
> 'docker_backup'  --> http://$ARTIFACTORY_IP:8082/artifactory/docker_backup/
> 'audio'          --> http://$ARTIFACTORY_IP:8082/artifactory/audio/
> 'pdf'            --> http://$ARTIFACTORY_IP:8082/artifactory/pdf/
> 'funny'          --> http://$ARTIFACTORY_IP:8082/artifactory/funny/
> 'games'          --> http://$ARTIFACTORY_IP:8082/artifactory/games/
> 'other'          --> http://$ARTIFACTORY_IP:8082/artifactory/other/
