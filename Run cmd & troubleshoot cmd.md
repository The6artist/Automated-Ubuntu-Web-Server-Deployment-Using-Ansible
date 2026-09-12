## Run cmd & Troubleshooting 


Use this cmd to run the entire project 

`ansible-playbook -i inventory.ini setup.yml`

Check Inventory loaded correctly 

`ansible all -i inventory.ini --list-hosts` 

Check Ansible can reach the host 

`ansible all -i inventory.ini -m ping` 

Check Playbook syntax is valid 

`ansible-playbook -i inventory.ini setup.yml --syntax-check` 

Check Nginx is running 

`systemctl status nginx --no-pager` 

Check Nginx config is valid 

`nginx -t` 

Check Site is actually serving 

`curl http://localhost` 

Check Website file was deployed 

`ls -l /var/www/html/index.html` 

Check Tarball exists 

`ls -lh roles/app/files/` 

Check Tarball contents are correct 

`tar -tzf roles/app/files/my-website.tar.gz` 

SSH key is present 

`ls -l ~/.ssh/id_ed25519.pub` 
