Builds [OpenFire XMPP server](https://www.igniterealtime.org/projects/openfire/) adapted for Cloudron.
Resulting Docker is available at https://hub.docker.com/r/getzendev/openfire

# Configuring GitHub Actions

1. Ensure that Github Actions is enabled in `Actions/General` setting (`Settings` tab) of forked repository;
2. Set next `Repository secrets` in `Secrets/Actions` setting (`Settings` tab) of forked repository:
  * **IMAGE_NAME** to image name with namespace (for example: my_account/openfire)
  * **REGISTRY** to registry on which the image will be pushed (for example: docker.io)
  * **REGISTRY_USERNAME** - to the username to access to the specified registry
  * **REGISTRY_TOKEN** - to the password to access to the specified registry

# Setting up Cloudron app

```
sudo npm install cloudron
npx cloudron login my.domain.com
wget https://raw.githubusercontent.com/GetZenDev/build-openfire-docker/main/CloudronManifest.json
npx cloudron install --image getzendev/openfire:latest
```

Then setup the app from the web interface.

# References
- [Cloudron CLI](https://docs.cloudron.io/packaging/cli/)
- [OpenFire Docs](https://www.igniterealtime.org/projects/openfire/documentation.jsp)
