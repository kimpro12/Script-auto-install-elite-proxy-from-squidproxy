# Script-auto-install-elite-proxy-from-squidproxy

- This script is for centos 7
- You must run the script on root (sudo -i) then run the script

- Port of the ip is 8888 ip is your public ip address

- If you want your ip have username,pass follow this command:
- yum -y install httpd-tools
- touch /etc/squid/passwd && chown squid /etc/squid/passwd
- htpasswd /etc/squid/passwd youruser
- After that the system will prompt you to enter and confirm a password for ‘youruser.’
- Edit the /etc/squid/squid.conf file, and add the following command lines:
* auth_param basic program /usr/lib64/squid/basic_ncsa_auth /etc/squid/passwd
* auth_param basic children 5
* auth_param basic realm Squid Basic Authentication
* auth_param basic credentialsttl 2 hours
* acl auth_users proxy_auth REQUIRED
* http_access allow auth_users
- systemctl restart squid
- FInish
