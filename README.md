# Artifactory Send Script

This bash script, named `artifactory_send`, uploads a file to an Artifactory instance using the Artifactory URL, username, and password. The script accepts one argument: the target file to send. The remote file name will be the same as the target file name.

## Usage

1. Save the script as `artifactory_send` and give it execute permission using:

```shell
chmod +x artifactory_send
```

2. Run the script by providing the target file as an argument:

```shell
./artifactory_send <TARGET_FILE>
```

The script will check for the required environment variables: `USERNAME`, `PASSWORD`, and `ARTIFACTORY_URL`. If any of these variables are missing, the script will prompt the user for input.

After collecting the necessary credentials and Artifactory URL, the script will update the user's .profile or .bashrc file with the environment variables.

**Note**: This script stores the password in plain text in the .profile or .bashrc file, which could be a security risk. Consider alternative methods for securely storing sensitive information, such as using a secrets management tool.
