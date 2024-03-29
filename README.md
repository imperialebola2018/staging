## Staging

### Getting going

On the _host_ machine (ebola2018.dide.ic.ac.uk), run the following commands.

```
git clone https://github.com/imperialebola2018/staging staging
cd staging
```

### Requirements

Install [Vagrant](https://www.vagrantup.com/downloads.html) and [VirtualBox](https://www.virtualbox.org/wiki/Downloads) in the host machine, along with [Vault](https://www.vaultproject.io)

```
sudo ./provision/setup-vagrant
sudo ./provision/setup-vault
```

### Build the VM


First, login to the vault and arrage credentials

```
./scripts/vault-login
```

then

```
vagrant up
cp scripts/ssh-testing ~server
```

After a while you should be able to log into https://ebola2018.dide.ic.ac.uk:1443

## Rebuild the VM

```
vagrant destroy
./scripts/remove-disk
vagrant up
```
