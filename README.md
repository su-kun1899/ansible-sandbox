# ansible-sandbox

Ansibleの実験場

## Requirements

- Python 3.6.6
- ansible 2.6.3
- Vagrant 2.1.2

## Setup

1. clone したら `vagrant up` してリモートホストを起動
1. `vagrant ssh-config` で確認した情報を元にリモートホストにsshできるようにする

## Run

```console
$ ansible-playbook -i hosts.ini --ask-vault-pass web.yml
```

#### Note

トークンなどの秘匿情報はansible-vaultで暗号化している。  
復号化や実行にはパスワードが必要。

```console
$ ansible-vault edit confidential-vars.yml
```
