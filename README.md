# ActiveCampaign Integration pack
[![Build Status](https://circleci.com/gh/StackStorm-Exchange/stackstorm-activecampaign/tree/master.svg?style=shield)](https://circleci.com/gh/StackStorm-Exchange/stackstorm-activecampaign)

API: http://www.activecampaign.com/api/overview.php

To mass-produce actions, see `etc/ac_api_gen.py`

## Configuration

Copy the example configuration in [activecampaign.yaml.example](./activecampaign.yaml.example)
to `/opt/stackstorm/configs/activecampaign.yaml` and edit as required.

* ``url`` - ActiveCampaign account URL
* ``api_key`` - API Key

**Note** : When modifying the configuration in `/opt/stackstorm/configs/` please
           remember to tell StackStorm to load these new values by running
           `st2ctl reload --register-configs`

### Webhook Sensor Configuration

Webhook structure is http://host:port/path/action

* ``host`` - Defaults to "0.0.0.0"
* ``port`` - Defaults to 9991
* ``path`` - Defaults to "webhook"
