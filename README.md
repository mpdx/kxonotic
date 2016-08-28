# Spin Xonotic on Digital Ocean by Ansible 

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
export DO_API_TOKEN=YourIMPRESSIVEtokenHere
```

### Usage

```
./server init
./server destroy
```

## License
Whatever.
