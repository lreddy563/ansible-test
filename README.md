### Ansbile Installation
Commands:
    1  sudo apt-get update
    2  sudo apt-get upgrade -y
    3  sudo apt-add-repository ppa:ansible/ansible
    4  sudo apt-get update
    5  sudo apt-get install ansible -y
    6  sudo apt-get install python -y
    7  ansible --version

Done!

### Test:

ansible --version
ansible 2.9.6
  config file = /etc/ansible/ansible.cfg
  configured module search path = ['/home/ubuntu/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/lib/python3/dist-packages/ansible
  executable location = /usr/bin/ansible
  python version = 3.8.5 (default, Jan 27 2021, 15:41:15) [GCC 9.3.0]

### Ping:

ansible -m ping localhost

localhost | SUCCESS => {
    "changed": false,
    "ping": "pong"
}


### Run the Playbook:

ansible-playbook -i localhost nginx.yaml


### Checking the Web:

root@ip-10-20-1-74:/etc/ansible/nginx# curl http://54.205.68.251/
<h1>Hello! World</h1>



## Jenkins Setup:

sudo apt install openjdk-8-jdk
sudo ufw allow 8080
sudo ufw status
sudo ufw enable
wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt install jenkins
sudo apt update
sudo apt install jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins
sudo cat /var/lib/jenkins/secrets/initialAdminPassword


## Jenkins Server is Up and Running!

http://54.205.68.251:8080/

User Name: admin
Password: admin

