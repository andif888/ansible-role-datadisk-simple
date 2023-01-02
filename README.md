# ansible-role-datadisk-simple

Partition, format and mount simple datadisk

## Table of content

- [Default Variables](#default-variables)
  - [datadisks_simple](#datadisks_simple)
  - [datadisks_simple_mount_by_uuid](#datadisks_simple_mount_by_uuid)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Default Variables

### datadisks_simple

Define your datadisks.

Example:

```yaml

datadisks_simple:

- device: /dev/sdb
  by_uuid: "/dev/disk/by-uuid/db068db6-7d70-4195-b75d-c435855a4b6f"
  label: "gpt"
  align: "optimal"
  number: 1
  part_end: "100%"
  part_start: "0%"
  part_type: "primary"
  resize: false
  fstype: ext4
  resizefs: false
  path: /mnt/filer/speed
  opts: discard,noatime
- device: /dev/sdc
  path: /mnt/filer/data
  opts: discard,noatime
- device: /dev/sdd
  path: /mnt/filer/backup
  opts: discard,noatime
- device: /dev/sde
  path: /mnt/filer/cams
  opts: discard,noatime
```

#### Default value

```YAML
datadisks_simple: []
```

### datadisks_simple_mount_by_uuid

mount by uuid instead of /dev/sdX

#### Default value

```YAML
datadisks_simple_mount_by_uuid: false
```



## Dependencies

None.

## License

license (GPL-2.0-or-later, MIT, etc)

## Author

andif888
