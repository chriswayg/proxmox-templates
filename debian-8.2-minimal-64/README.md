## Debian Jessie minimal Template

- based on Debootstrap minimal install
- add python for use with Ansible for example
- remove Postfix to make room for alternate mail server
- permit root login with password temporarily for easy initialisation
  - intended to receive proper SSHD settings and keys via Ansible
- small 117 MB compressed template
- about 250 MB on disk for a running container
