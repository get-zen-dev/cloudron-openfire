Builds XMPP server - OpenFire (https://www.igniterealtime.org/projects/openfire/) and pushes resulting Docker at https://hub.docker.com/r/getzendev/openfire.

**Setup**

1. Ensure that Github Actions is enabled in `Actions/General` setting (`Settings` tab) of forked repository;
2. Set next `Repository secrets` in `Secrets/Actions` setting (`Settings` tab) of forked repository:
  * **IMAGE_NAME** to image name with namespace (for example: my_account/openfire)
  * **REGISTRY** to registry on which the image will be pushed (for example: docker.io)
  * **REGISTRY_USERNAME** - to the username to access to the specified registry
  * **REGISTRY_TOKEN** - to the password to access to the specified registry
