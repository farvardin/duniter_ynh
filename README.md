<!--
N.B.: This README was automatically generated by https://github.com/YunoHost/apps/tree/master/tools/README-generator
It shall NOT be edited by hand.
-->

# Duniter for YunoHost

[![Integration level](https://dash.yunohost.org/integration/duniter.svg)](https://dash.yunohost.org/appci/app/duniter) ![](https://ci-apps.yunohost.org/ci/badges/duniter.status.svg) ![](https://ci-apps.yunohost.org/ci/badges/duniter.maintain.svg)  
[![Install Duniter with YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=duniter)

*[Lire ce readme en français.](./README_fr.md)*

> *This package allows you to install Duniter quickly and simply on a YunoHost server.
If you don't have YunoHost, please consult [the guide](https://yunohost.org/#/install) to learn how to install it.*

## Overview

Crypto-currency software to operate Ğ1 libre currency

**Shipped version:** 1.8.2~ynh0



## Screenshots

![](./doc/screenshots/duniter_admin_g1.png)

## Disclaimers / important information

## Configurations
- In order to compute blocks you will have to set your member credentials with `duniter wizard key` or from the webadmin.
- The BMA API is accessible from `https://duniter.domain.tld/` if enabled.
- **Warning**: In case the Webui tells you your network configuration is wrong and proposes to correct it, do not apply it, otherwise it breaks the specific configuration made for this package.
You can manually reset the configuration with following command:
`duniter config --bma --ipv4 127.0.0.1 --port CHOSEN_PORT --remoteh YOUR_DOMAIN --remotep 443 --noupnp`

## Cesium
Cesium is a wallet webapp. You can install it with:
- [With the YunoHost app](https://github.com/YunoHost-Apps/cesium_ynh)
<!--- With a Duniter plugin: `duniter plug git+https://github.com/duniter/duniter-ui-cesium.git`-->
## Documentation and resources

* Official app website: https://duniter.org
* Upstream app code repository: https://git.duniter.org/nodes/typescript/duniter
* YunoHost documentation for this app: https://yunohost.org/app_duniter
* Report a bug: https://github.com/YunoHost-Apps/duniter_ynh/issues

## Developer info

Please send your pull request to the [testing branch](https://github.com/YunoHost-Apps/duniter_ynh/tree/testing).

To try the testing branch, please proceed like that.
```
sudo yunohost app install https://github.com/YunoHost-Apps/duniter_ynh/tree/testing --debug
or
sudo yunohost app upgrade duniter -u https://github.com/YunoHost-Apps/duniter_ynh/tree/testing --debug
```

**More info regarding app packaging:** https://yunohost.org/packaging_apps
