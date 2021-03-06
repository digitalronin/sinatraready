#Sinatra Ready
## Adapted from Rails Ready by Josh Frye <joshfng@gmail.com>
###Ruby and Sinatra setup script for Linux systems
###Distros supported:
 * Ubuntu 10.04 LTS and 10.10

# 
###Run this on a fresh install. It WILL update your system!

###To run:
  * `wget --no-check-certificate https://github.com/digitalronin/sinatraready/raw/master/sinatraready.sh && bash sinatraready.sh`
  * The script will ask if you want to build Ruby from source or install RVM

###What this gives you:
  * An updated system
  * Ruby 1.9.2 latest patch level (installed to /usr/local/bin/ruby) or RVM running 1.9.2 latest patch level
  * Bundler, Passenger, and Sinatra gems
  * Git

Just install either NGINX or Apache, run passenger-install-nginx-module or passenger-install-apache-module, upload your app, point your vhost config to your apps public dir and go!

Please note: If you are running on a super slow connection your sudo session may timeout and you'll have to enter your password again. If you're running this on an EC2 or RS instance it shouldn't be problem.

# 
####Sinatra Ready now supports a "plugin" type system. The distro is detected and a corresponding "recipe" file is pulled down to run the distro specific setup steps. Check the recipes dir to see if your distro is supported. If you would like to add support for a system fork the repo, write a recipe, and submit a pull request. Take a look at recipes/ubuntu.sh for an idea of what to model your recipe after.

If you use this or have any suggestions let me know david@digitalronin.com
