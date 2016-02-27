# s3backup

## Prerequisites

#### Redhat based

```
yum install git  python-setuptools
cd /usr/src;
git clone https://github.com/s3tools/s3cmd.git
cd s3cmd
python setup.py install
s3cmd --configure
```

#### Debian/Ubuntu 

```
sudo apt-get install git python-setuptools
cd /usr/src;
git clone https://github.com/s3tools/s3cmd.git
cd s3cmd
sudo python setup.py install
s3cmd --configure
```

## Installation

```
mkdir /backup
cd /backup
git clone https://github.com/RubenHarms/s3backup.git ./
chmod +x /backup/bin/bk
```

## Add Crontab

```
export EDITOR=nano
crontab -e
```

Add the following code:

```
1 3 * * * /backup/bin/bk
```
