# sprout-wrap

[![Build Status](https://travis-ci.org/pivotal-sprout/sprout-wrap.png?branch=master)](https://travis-ci.org/pivotal-sprout/sprout-wrap)

This project uses [soloist](https://github.com/mkocher/soloist) and [librarian-chef](https://github.com/applicationsonline/librarian-chef)
to run a subset of the recipes in sprout's [cookbooks]((https://github.com/pivotal-sprout/sprout).

[Fork it](https://github.com/pivotal-sprout/sprout-wrap/fork) to 
customize its [attributes](http://docs.opscode.com/chef_overview_attributes.html) in [soloistrc](/soloistrc) and the list of recipes 
you'd like to use for your team. You may also want to add other cookbooks to its [Cheffile](/Cheffile), perhaps one 
of the many [community cookbooks](http://community.opscode.com/cookbooks). By default it configures an OS X 
Mavericks workstation for Ruby development.

Finally, if you've never used Chef before - we highly recommend you buy &amp; watch [this excellent 17 minute screencast](http://railscasts.com/episodes/339-chef-solo-basics) by Ryan Bates. 

## Installation under Mavericks (OS X 10.9)

### 0. Backup you SSH Keys

If you're starting by wiping your machine please be sure to back up your ssh keys so that ops does not have to redeploy the base package.

### 1. Install XCode

[![Xcode - Apple](http://r.mzstatic.com/images/web/linkmaker/badge_macappstore-lrg.gif)](https://itunes.apple.com/us/app/xcode/id497799835?mt=12&uo=4)

Don't forget to start up Xcode once it's installed so that you can agree to the terms&mdash;many commands won't work until the terms have been agreed to.

### 2. Install Command Line Tools
  
    xcode-select --install
  
### 3. Clone this project

    git clone https://github.com/gnip/sprout-wrap.git
    cd sprout-wrap

### 4. Install soloist & and other required gems

    sudo gem install bundler
    sudo bundle

### 5. Set up ssh key for github

Make sure that you're a member of the Gnip organization on github

[Follow these instructions](https://help.github.com/articles/generating-ssh-keys)


### 6. Run soloist

[Note that this should take ~30 minutes or less to complete.  You'll be asked to enter your sudo password a few times along the way.]

    bundle exec soloist

