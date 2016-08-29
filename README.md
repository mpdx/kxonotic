# Spin Xonotic Kappa Server on Digital Ocean using Ansible 

## System requirements 

* Python 2.7+
* pip's dopy package
* Ansible 2.0+

## Installation

The following assumes Debian distro

### Ansible

```
sudo apt-add-repository -y ppa:ansible/ansible
sudo apt-get update
sudo apt-get install -y ansible 
```

### Python

```
sudo apt-get install -y python python-pip
sudo pip install dopy
```

or just run `./requirements`

### Clone repo
Next, clone this repository.

```
git clone https://github.com/mpdx/kappa-xonotic
```

### Digital Ocean Token

You should have one, obviously. Generate it then set environmental variable like:

```
export DO_API_TOKEN=tokenStringHere
```

also, change record for digital ocean dns in all.yml file:

```
sed -i 's/xonotic.example.com/your.custom.domain/' group_vars/all.yml
```

### Other settings  

For email notifications just set:
```
export EMAIL_USERNAME=youremail@gmail.com
export EMAIL_PASSWORD=yourpassword
export EMAIL_FROM="Your Name"
export EMAIL_TO="first.friend@example.org,second.friend@example.net"
```

### Usage

```
./server init
./server destroy
```

## License
Whatever.
