polkadot-library
=========

This role prepares the node for installation of the Polkadot client as a full "library" node.

Role Variables
--------------

### Sync
These variables are used in the Source of Truth sync

- aws_access_key_id: none
- aws_secret_access_key: none
- region: us-east-1
- sync_bucket_name: none
- chain_stub: polkadot

### Polkadot Client
- project: default
- chain: polkadot
- loggingFilter: "sync=trace,afg=trace,babe=debug"
- relay_ip_address: none
- relay_p2p_address: none
- telemetryUrl: none

### Enable flags
use_source_of_truth: true

Dependencies
------------

- w3f_insight.polkadot_base

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: insight_w3f.polkadot_library }

License
-------

Apache 2.0

Author Information
------------------

Maintained by [Richard Mah](https://github.com/shinyfoil) at [Geometry Labs](https://github.com/geometry-labs)
