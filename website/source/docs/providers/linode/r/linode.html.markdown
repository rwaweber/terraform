---
layout: "linode"
page_title: "Linode: linode_linode"
sidebar_current: "docs-linode-resource-linode"
description: |-
  Provides a Linode linode resource. This can be used to create, modify, and delete droplets. Linodes also support provisioning.
---

# linode\_linode

Provides a Linode linode resource. This can be used to create,
modify, and delete linodes. Linodes also support
[provisioning](/docs/provisioners/index.html).

## Example Usage

```
# Create a new Web linode in the nyc2 datacenter
resource "linode_linode" "web" {
    image = "Debian 8.1"
    name = "web-1"
    datacenter = frankfurt"
    plan = "1024"
}
```

## Argument Reference

The following arguments are supported:

* `image` - (Required) The linode image ID or slug.
* `name` - (Required) The linode name
* `datacenter` - (Required) The datacenter to start in
* `plan` - (Required) The instance plan to start
* `backups` - (Optional) Boolean controlling if backups are made.
* `ipv6` - (Optional) Boolean controlling if IPv6 is enabled.
* `private_networking` - (Optional) Boolean controlling if private networks are enabled.
* `ssh_keys` - (Optional) A list of SSH fingerprints to enable in.

## Attributes Reference

The following attributes are exported:

* `id` - The ID of the linode
* `name`- The name of the linode
* `datacenter` - The datacenter of the linode
* `image` - The image of the linode
* `ipv6` - Is IPv6 enabled
* `ipv6_address` - The IPv6 address
* `ipv6_address_private` - The private networking IPv6 address
* `ipv4_address` - The IPv4 address
* `ipv4_address_private` - The private networking IPv4 address
* `locked` - Is the Linode locked
* `private_networking` - Is private networking enabled
* `plan` - The instance plan
* `status` - The status of the linode

