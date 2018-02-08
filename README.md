# ECR Credential Helper

This is a container image that when run will build [amazon-ecr-credential-helper](https://github.com/awslabs/amazon-ecr-credential-helper)
binary.

## Usage example

Running the following command will compile the amazon-ecr-credential-helper binary into `/opt/bin` and will place the
docker configuration file into `/root/.docker/config.json`.

```sh
docker run --rm -v /root:/data -v /opt/bin:/go/src/github.com/awslabs/amazon-ecr-credential-helper/bin/local kasko/ecr-credential-helper
```

## Build

Automated build of this repository are handled by [Docker Hub](https://hub.docker.com/r/kasko/ecr-credential-helper).

To build this image locally clone this repository and run the following command from CLI:

```sh
docker build -t kasko/ecr-credential-helper .
```

## License

For license please check the [LICENSE](LICENSE) file.

## Links

- https://github.com/awslabs/amazon-ecr-credential-helper
- https://github.com/erinmcgill/docker-ecr-helper
