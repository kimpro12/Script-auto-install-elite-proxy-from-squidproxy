# Script-auto-install-elite-proxy-from-squidproxy

- Port of the ip is 8888 ip is your public ip address

- If you want your ip have username,pass follow this command:
- yum -y install httpd-tools
- touch /etc/squid/passwd && chown squid /etc/squid/passwd
- htpasswd /etc/squid/passwd youruser
- After that the system will prompt you to enter and confirm a password for ‘youruser.’
- systemctl restart squid
- FInish
