REST API
-------------

### `/api/v1/interfaces`

#### GET

Take a list of WLAN interfaces 

##### response

```json
{
    "interfaces": [
        "wlan0",
        "wlan1"
    ]
}
```

### `/api/v1/interfaces/<id>`

#### GET

Take WLAN interface information

##### Response

```json
{
    "interfaces": {
        "wlan0": [
            {
                "addr": "192.168.5.1",
                "broadcast": "192.168.5.255",
                "netmask": "255.255.255.0"
            }
        ]
    }
}
```

#### POST

Connect WLAN interface to access point

##### Request

* `ssid` - access point SSID
* `password` - access point WPA/WPA2 password

##### Response

```json
{
    "interfaces": {
        "wlan1": {
            "connected": true,
            "password": "1234567890",
            "ssid": "myssid"
        }
    }
}
```