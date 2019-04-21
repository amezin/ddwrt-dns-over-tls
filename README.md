DNS over tls on DD-WRT using Unbound
------------------------------------

Requirements:
- Setup->Basic Setup->Recursive DNS Resolving (Unbound) checked
- Administration->Management->JFFS2 Support->Internal Flash Storage->Enable selected
- Services->Services->Secure Shell->SSHd->Enable selected (needed only during installation)

`jffs/ca-certificates.crt` is copied from Arch Linux (which, in turn, is based on Fedora package)

`install.sh` assumes router's IP to be `192.168.1.1` (edit if necessary). Files are installed to JFFS partition. `jffs/etc/unbound.conf` redirects all requests to CloudFlare's 1.1.1.1
