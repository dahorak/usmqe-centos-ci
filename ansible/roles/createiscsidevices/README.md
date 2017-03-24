Create iSCSI Devices
====================

This role creates iSCSI devices on machine so they can be used for creating Ceph OSDs.

Parameters:
  - `devices_count`: number of created devices (default: `5`)
  - `device_size`: device size (default: `5GB`)
