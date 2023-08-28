## sensitive_file
This file is encripted by [Transcrypt](https://github.com/elasticdog/transcrypt) - A script to configure transparent encryption of sensitive files stored in a Git repository.

1. In order to read `sensitive_file`, configure your repo with `Transcrypt`.
    Start by cloning `Transcrypt` repo next to `drummachina/treasury` repo. 
```
$ git clone https://github.com/elasticdog/transcrypt.git
$ cd transcrypt/
$ sudo ln -s ${PWD}/transcrypt /usr/local/bin/transcrypt
```
2. Now, in `treasury` check if `transcrypt` is working and detecting `sensitive_file`:
```
$ cd treasury
$ transcrypt --list
sensitive_file
```
3. Initialize a clone of a configured repository
```
transcrypt -c aes-256-cbc -p '<secret_password>'
```
4. Now, your `sensitive_file` should be decrypted.
