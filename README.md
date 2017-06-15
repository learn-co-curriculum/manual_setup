# Set up Instructions

**Step 1** - Delete the LearnIDE

From this point forward we wont be using the LearnIDE anymore. In a later step we will have you choose an editor of your choice but for now go into your App folder and Delete the IDE. Also make sure you empty your trash afterwards. If the IDE is not in the app folder follow these steps:

1. Use the `cmd + space` to search for the LearnIDE. DO NOT CLICK ANYTHING YET!

2. Scroll all the way down until you see "show all in finder", proceed by clicking it.

3. Now finder should have opened up and the LearnIDE should be one of the first items. Go ahead and Delete it.

4. Now empty your trash.

**Step 2** - Download Xcode
**For In-Person Immersive students, this step must be completed before your first day at Flatiron.**

1. Go to the App Store

2. Search for xcode, it should be the first one on the top-left corner.

3. Click Download!

This will allow you to compile software locally. After installing Xcode, open it and accept the license file when prompted. Note, Xcode is a massive 3 or so GB, so it may take some time to download depending on your internet connection.

**Step 3** - Open your Terminal

Open up your terminal. This is where we are going to be doing most of our installation steps! On Mac, you can open up your terminal by going to Applications > Utilities > Terminal, or by using the quick launch (`cmd + space`) and just start typing "Terminal".

**Step 4** - Install Homebrew

Install the Homebrew package manager. You can do this by entering the following command into your terminal:

`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

Note, this is all one line in the terminal even if it is broken up into two lines here in your browser.

**Step 5** - Get git and set it up

1. Make sure you have [git](http://git-scm.com/downloads "Github's download page").
It generally comes pre-installed with most operating systems, but you can check by running `git version` on terminal. If you do not already have git installed, you can get it by typing `brew install git` on your terminal.

2. Run `ssh-keygen` to create a new SSH key. If you do not already have an SSH key setup, you'll be asked to select a location and a passphrase. Just leave everything blank and press enter for default location and no passphrase. If you're asked if you want to overwrite, then you already have an SSH key and you do not want to overwrite it.

3. `cat ~/.ssh/id_rsa.pub`
This will display your SSH key to your terminal. You want to then copy this and add this SSH key to your github by following the
[instructions posted on github](href="https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/").

You're also going to want to let the git that is running on your machine to know you you are. You can set this up by running:
`git config --global user.email "you@example.com"` and
`config --global user.name "Your Name"`

**Step 6** - Support Libraries

Next we're going to add a few support libraries with the following lines: `brew install gmp` and `brew install gnupg` Note: If you get the following error: `Warning: gnupg-1.4.19` already installed, it's just not linked simply run: `brew link gnupg`.

 **Step 7** - Install Ruby Version Manager

[RVM](http://rvm.io/) is a great tool that lets you run different versions of Ruby on your computer. This is really useful because if you know one project your working on works with Ruby version 2.1.0 and another needs 2.3.1, you can easily switch between the two versions when you switch between projects. You can install it and set it up with the following commands:

1. Run `curl -sSL https://get.rvm.io | bash` -make sure you do not use `sudo`

2. ONCE THIS STEP COMPLETES, CLOSE AND RE-OPEN YOUR TERMINAL. Skipping this step will cause RVM to not work.

3. Run `rvm install 2.3.1`

4. Run rvm use 2.3.1 --default

5. Check that everything worked by running `ruby -v` and `rvm list`. This should output the version of ruby you're using (2.3.1) and the list of versions available with your RVM install.

**Step 8** - Install some ruby gems

Ruby gems are pre written, stand alone, chunks of code that have been written and made easily accessible to you.

1. First, lets update our system gems with: `gem update --system`

2. Install the Learn gems. Do this with: `gem install learn-co` (if you get a permissions error use the Need Help button above).

3. Install the gem bundler. This gem takes care of installing all the other gems you need for projects: `gem install bundler`

**Step 9** - Setup the Learn gem

Now we need to setup the Learn gem. Type the following into your terminal: `learn whoami`

This will prompt you to set up the Learn gem. Note: When the gem asks you to go to learn.co/your-github-username, you must be logged in to be able to retrieve your token.

**Step 10** - Get a Text Editor

Get a Text Editor. We suggest [Atom Text Editor](https://atom.io/)

Once you have Atom installed, you can set it as your default text editor in the learn-config file. First, open up the config file for your learn gem with `atom ~/.learn-config`

You can then change your editor from `subl` to `atom`

You can also set the default location that Learn will save all your labs. Save and close the file. Note: These settings only trigger when you use the Open button in Learn or when you use the `learn open` command. You can always manually clone your labs to any location you wish and open them with any text editor without having to edit this config file.

**Step 11** - Install some more gems!

If you're going to be doing web development on Learn, you're going to want to install a couple more gems.

1. Phantom JS is a JavasScript library and this ruby gem easily installs it for you: `gem install phantomjs`

2. Nokogiri is a gem that let's us scrape websites and you'll definitely want to be able to use it. Let's install it with: `gem install nokogiri` .If you encounter any errors while install this gem, check out the [Nokogiri support docs for Mac OSX](http://www.nokogiri.org/tutorials/installing_nokogiri.html#mac_os_x) installs. If you check out that page an you still have issues, contact support for help.

**Step 12** - Get some databases

You'll be using a couple of different databases as you move through the web development track. The default database that rails uses is SQLite. We also frequently see that students want to deploy their apps to the free hosting service [Heroku](http://www.heroku.co) To do this though, you'll need to be using Postgres instead. It's best of we just install both of them now so you can use either one.

1. SQLite: `brew install sqlite`

2. Postgres: Install the Postgres app at: [Postgres.app](http://postgresapp.com/)


**Step 13** - Install Rails

Finally, rails! The powerful ruby web framework. We can install that with: `gem install rails`

**Step 14** - Node

Now let's get your node version manager installed. Node is a package manager for JavaScript.

1. run `curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash` on terminal. make sure you do not use `sudo`.

2. then run `echo 'export NVM_DIR="$HOME/.nvm"' >> ~/.bash_profile`.

3. as well as `echo '[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"' >> ~/.bash_profile`

4. lastly run `source ~/.bash_profile`. This will refresh your shell after making all the changes. This way you wont have to quit terminal and open it again.

**Step 15** - Install Java
Next, we'll want to install the latest version of the Java Development Kit. To get that, head on over to the [download page](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) and select the Java SE Development Kit for Mac OSX and install it.

**Step 16** - Dotfiles (Optional)

These dotfiles do a variety of different things and I highly recommend you download them. If when you're trying to back up the files you get the error 'No such file or directory', don't worry. This just means you didn't have one of these files to start with, so there is nothing to backup.

1. Backup your `.irbrc` file with `mv ~/.irbrc{,.bak}`.

2. `curl "https://raw.githubusercontent.com/flatiron-school/dotfiles/master/irbrc" -o "$HOME/.irbrc"` - This file gives you some nice formatting for when you're in IRB (IRB lets you write ruby code in your terminal)

3. Backup your `.gitignore` file with `mv ~/.gitignore{,.bak}`.

4. `curl "https://raw.githubusercontent.com/flatiron-school/dotfiles/master/ubuntu-gitignore" -o "$HOME/.gitignore"` - Global .gitignore rules. When you add a .gitignore file to a project, it let's you specify certain files that you DO NOT want pushed up to github (like API keys...)

5. Backup your `.bash_profile` file with `mv ~/.bash_profile{,.bak}`.

6. `curl "https://raw.githubusercontent.com/flatiron-school/dotfiles/master/bash_profile" -o "$HOME/.bash_profile"` - Your bash profile loads up every time you open a terminal window. The Learn bash_profile is designed to load up a bunch of shortcuts for you as well as make sure that RVM loads up every time you open the terminal. I recommend you take a look at this file and even see if there are any shortcuts of your own that you'd like to add! Note: this will overwrite existing bash profile, so back up if you want to.

7. Backup your `.gitconfig` file with `mv ~/.gitconfig{,.bak}`.

8. `curl "https://raw.githubusercontent.com/flatiron-school/dotfiles/master/gitconfig" -o "$HOME/.gitconfig"` then `atom ~/.gitconfig` (you can access this file with the editor of your choosing) and edit what needs to be edited (github username and github email in a few places).
