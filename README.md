## Intro

This is an experiemental terraform provider for managing your Mikrotik's router's DNS. It allows you to create records via the routeos API.

## Examples

Creating a new DNS record

```terraform
provider "mikrotik" {
  host = "http://router:8728" # Or set MIKROTIK_HOST
  username = "username of api user" # Or set MIKROTIK_USER
  password = "xxxxxx" #  # Or set MIKROTIK_PASSWORD
}

resource "mikrotik_dns_record" "www" {
    name = "router"
    address = "192.168.88.1"
    ttl = 300
}
```
