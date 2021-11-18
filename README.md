# Duniter package for YunoHost
- [Duniter project](https://duniter.org)
- [YunoHost project](https://yunohost.org)

## Requirements
- Debian Buster
- YunoHost ≥ v4.1
- `x64` or `armlv7` architecture
- 200Mo free RAM
- A dedicated domain name to install the app on root path. For instance, `duniter.domain.tld`.
- A YunoHost user which will have access the web admin.

## Install and upgrade
You shall add the application community list into your instance in order to install it and benefit from upgrades:
```bash
sudo yunohost app fetchlist -n community -u https://app.yunohost.org/community.json
sudo yunohost app install duniter
sudo yunohost app upgrade duniter
```
Be carefull when installing applications from the community list.

## Configurations
- In order to compute blocks you will have to set your member credentials with `duniter wizard key` or from the webadmin.
- The BMA API is accessible from `https://duniter.domain.tld/` if enabled.
- Warning: in the case the Duniter webui tells you your network configuration is wrong and proposes to correct it, you shouldn't apply, otherwise it might break the configuration made for yunohost. If you applied this by mistake, you can manually reconfigure it with ``duniter config --bma --ipv4 127.0.0.1 --port CHOSEN_PORT --remoteh YOUR_DOMAIN --remotep 443 --noupnp``, or install again this yunohost package on itself.
- Please note, BMA is used for communication between a node and clients such as Cesium. WS2P is used for inter-node connections.

## Cesium
Cesium is a wallet webapp. You can install it with:
- [With the YunoHost app](https://github.com/YunoHost-Apps/cesium_ynh)
<!--- With a Duniter plugin: `duniter plug git+https://github.com/duniter/duniter-ui-cesium.git`-->

## License
This package and the Duniter software are under GNU AGPL v.3.
