# OpenSSH host key signing

This role uses an OpenSSH certification authority -- whose private key resides
locally on the computer running Ansible -- to sign all SSH host keys of the
servers.

The advantage is that, assuming a user trusts the CA for the matching domain,
Trust-On-Fist-Use is avoided without having to manage fetching, authenticating
and merging large `known_hosts` files.

In particular, this should be very useful in large deployments,
or in cloud-based deployments with short-lived hosts.
