Access and Credentials
======================

Ansible deploys and Jenkins changes both require an active MoCo LDAP 
account and SSH access to the infrastructute. Building docker images
for testing requires no special access.

Visit https://login.mozilla.com/ to set up multi-factor authentication,
upload your SSH key(s), and generate an OpenVPN client certificate.

If you're a DXR developer you'll want to request to be added to the
DXR VPN group, otherwise you'll need to be in the Developer Services
VPN group. After that, infra puppet will do the rest.

