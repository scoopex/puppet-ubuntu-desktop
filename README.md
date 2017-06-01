# Overview

I use this repo/code to setup my personal system.

This project is GNU GPLv3 (see LICENCE file). Contributions or forks are welcome.

# Setup my workstation

 * Clone repo
   ```
   sudo apt install git
   mkdir -p ~/src/
   cd ~/src/
   git clone https://github.com/scoopex/puppet-ubuntudesktop.git
   git clone git@github.com:scoopex/puppet-ubuntudesktop.git # alternative way
   cd ~/src/puppet-ubuntudesktop
   ```

 * Install Puppet infrastructure
   ```
   ./setup.sh
   ```

 * Execute setup
   ```
   puppet apply --modulepath /etc/puppetlabs/puppet/modules/ /etc/puppetlabs/puppet/modules/ubuntudesktop/manifests/localrun.pp  --test
   ```

# Develop

```
bundle install
rake
```

# Open TODOs

 * Enable all neccessary package sources
 * Add a custom/local configuration
 * Rollout ms-env 
 * Add the correct Virtualbox apt keys
 * Use gconftool to provision specific settings
   ```
   gconftool-2  --recursive-list /
   ```
 * Autostart & Configure: clipit
 * Autostart & Configure: pidgin
 * Set Terminal Settings
   * Scrolling
   * Hotkeys
 * Configure Nextcloud
 * Configure Backup
 * Setup ms-env
 * Testing
   * Puppet-Lint
   * RSPec Tests
   * Serverspec Tests
