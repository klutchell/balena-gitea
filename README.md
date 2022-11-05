# balena-gitea

[Gitea](https://gitea.io/) - Git with a cup of tea

A painless self-hosted Git service.

## Getting Started

You can one-click-deploy this project to balena using the button below:

[![deploy with balena](https://balena.io/deploy.svg)](https://dashboard.balena-cloud.com/deploy?repoUrl=https://github.com/klutchell/balena-gitea)

## Manual Deployment

Alternatively, deployment can be carried out by manually creating a [balenaCloud account](https://dashboard.balena-cloud.com) and application,
flashing a device, downloading the project and pushing it via the [balena CLI](https://github.com/balena-io/balena-cli).

## Usage

Once your device joins the fleet you'll need to allow some time for it to download the various services.

When it's done you should be able to access the access the app at <http://gitea.local>.

Documentation for Gitea can be found at <https://docs.gitea.io/>.

### Installation Notes

- On the Initial Configuration page, set `Run As Username` to `gitea`
- On the Initial Configuration page, set `Server Domain` to the IP of your device
- On the Initial Configuration page, set `Gitea Base URL` to the IP of your device with the `http://` prefix

## Customization

### Environment Variables

| Name           | Description                                                                                                       |
| -------------- | ----------------------------------------------------------------------------------------------------------------- |
| `TZ`           | Inform services of the [timezone](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) in your location. |
| `SET_HOSTNAME` | Set a custom hostname on application start. Default is `gitea`.                                                   |

Additional Gitea environment variables can be found in the [documentation](https://docs.gitea.io/en-us/install-with-docker/#managing-deployments-with-environment-variables).

## Extras

### restic

Rest easy knowing that your application data volumes are automatically and securely backed up to local or cloud storage!

<https://github.com/klutchell/balena-restic>

### hostname

An utility block to set the hostname of devices running balenaOS. This service is expected to remain `Exited` during normal operation.

<https://github.com/balenablocks/hostname>

### tailscale

Add your device to your [Tailscale](https://tailscale.com/) network with this block!

<https://github.com/klutchell/balena-tailscale>

## Contributing

Please open an issue or submit a pull request with any features, fixes, or changes.
