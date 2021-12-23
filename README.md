# My Smart Blinds component for Home Assistant

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg)](https://github.com/hacs/integration)

A custom component to support controlling My Smart Blinds in Home Assistant using the My Smart Blinds Smart Bridge.

Adapted and updated from original source: https://gist.github.com/ianlevesque/f97e3a9bfafc72cffcb4cec5059444cc

NOTE: This repository / project is highly unsupported and unlikely to get updates or bug fixes. Use at your own risk.


## Installation

- The easiest way is to install it with [HACS](https://hacs.xyz/). First install
[HACS](https://hacs.xyz/) if you don't have it yet. After installation you can
add this repository as a custom component in the HACS store under integrations.

- Alternatively, you can install it manually. Just copy paste the content of the
`custom_components/mysmartblinds` folder in your `config/custom_components`
directory. As example, you will get the `cover.py` file in the following path:
`/config/custom_components/mysmartblinds/cover.py`.


## Configuration
key | type | description
:--- | :--- | :---
**platform (Required)**                    | string        | `mysmartblinds`
**username (Required)**                    | string        | Username for the MySmartBlinds application.
**password (Required)**                    | string        | Password for the MySmartBlinds application.
**close_position**                         | int           | Tilt position to use when closing blinds. 0 - 100
**invert_open_close**                      | boolean       | Invert the open/close values. Can be used to close the blinds with the slates in the opposite direction.
**include_rooms**                          | boolean       | NOTE: This feature doesn't work correctly. Always set it to `False`.

As mentioned above, the `include_rooms` should be set to False. It was in the original source and I've never seen it work, but haven't removed it either.


## Example

**Default configuration with credentials from a `secret.yaml` file:**

```yaml
cover:
  - platform: mysmartblinds
    username: !secret mysmartblinds_username
    password: !secret mysmartblinds_password
    include_rooms: False
    open_position: 50
```

**Tilt the other way to close:**

```yaml
cover:
  - platform: mysmartblinds
    username: !secret mysmartblinds_username
    password: !secret mysmartblinds_password
    invert_open_close: True
```


## Troubleshooting
To turn on debug logging, modify your `configuration.yaml` and add the following:
```yaml
logger:
  logs:
    custom_components.mysmartblinds: debug
```
