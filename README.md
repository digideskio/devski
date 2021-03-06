# Devski

### В советской России мы используем Nginx в развитии

Devski manages nginx vhosts on your development machine so you can develop in 
the closest possible environment to production.

Devski enables you to do the following on your local:

* .dev domain
* https
* create a vhost with a single command

Current commands:

```shell
❯ devski commands
--version
add
available
cat
commands
disable
enable
enabled
help
install
link
open
reload
remove
restart
start
stop
templates
test
❯
```

### Install

Then clone the devski repo to your home directory:

```shell
git clone git@github.com:mynameisrufus/devski.git ~/.devski
```

Add ~/.devski/bin to your $PATH for access to the devski command-line utility.

```shell
echo 'export PATH="$HOME/.devski/bin:$PATH"' >> ~/.bash_profile
```

Zsh note: Modify your `~/.zshenv` file instead of `~/.bash_profile`

To configure:
```shell
devski install
```

### Debugging Nginx

``` 
tail -f /usr/local/var/log/nginx/*.log
```

### Debugging launchctl

```
tail -f /var/log/nginx.log
```

### Resources

* http://passingcuriosity.com/2013/dnsmasq-dev-osx/
