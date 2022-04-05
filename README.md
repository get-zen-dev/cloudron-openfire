# Github Actions pipeline for building Openfire docker-image and push to registry

## Requirements

* Github account
* Registry account (for example on hub.docker.com)

## Installation

1. Fork this repository to your Github's account;
2. Ensure that Github Actions is enabled in `Actions/General` setting (`Settings` tab) of forked repository;
3. Set next `Repository secrets` in `Secrets/Actions` setting (`Settings` tab) of forked repository:
  * **IMAGE_NAME** to image name with namespace (for example: my_account/openfire)
  * **REGISTRY** to registry on which the image will be pushed (for example: docker.io)
  * **REGISTRY_USERNAME** - to the username to access to the specified registry
  * **REGISTRY_TOKEN** - to the password to access to the specified registry
4. Re-run the build pipeline in `Actions` tab if it was already launched earlier,
   wait for the build to finish and verify that the required image appears in the registry
