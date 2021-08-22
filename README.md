# Sean Repo
## Supported Distro
* Debian Bullseye (11)

## Import GPG public key for repo
* Import apt key
```bash
curl -fsSL https://www.clam.ml/gpg-pubkey/sean.gpg | sudo gpg --dearmor -o  /usr/share/keyrings/sean-test-keyring.gpg
```

* Add custom repo info in `/etc/apt/sources.list.d/seanrepo.list`:
```
deb [signed-by=/usr/share/keyrings/sean-test-keyring.gpg] https://gh.pkg.clam.ml/bullseye ./
```

* Check if repo works:
```
sudo apt update
```
