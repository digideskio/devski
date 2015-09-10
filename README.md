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
commands
disable
enable
enabled
help
link
open
reload
remove
templates
test
❯
```

### Install

Follow the instructions here if you do not have dnsmasq and .dev domain already
setup http://passingcuriosity.com/2013/dnsmasq-dev-osx/

Then clone the devski repo to your home directory:

```shell
git clone git@github.com:mynameisrufus/devski.git ~/.devski
```

Add ~/.devski/bin to your $PATH for access to the devski command-line utility.

```shell
echo 'export PATH="$HOME/.devski/bin:$PATH"' >> ~/.bash_profile
```

Zsh note: Modify your `~/.zshenv` file instead of `~/.bash_profile`

Symlink your sites dir to your devski enabled dir with `devski link` this is
equivalent to:

```shell
rm -rf /opt/boxen/config/nginx/sites
ln -s ~/.devski/nginx/sites-enabled /opt/boxen/config/nginx/sites
```

Each time you run boxen your symlink will go missing so currently you will have
to re-run this command.

### Debugging Nginx

``` 
tail -f /opt/boxen/log/nginx/*.log
```
