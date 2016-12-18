### mysql
`$ brew install mysql`


### MariaDB
	$ brew unlink mysql
	$ brew info mariadb # Verify MariaDB Version in Homebrew Repo
	$ brew install mariadb # Install MariaDB

	# mysql setup auto start and start the database
	$ ln -sfv /usr/local/opt/mysql/*.plist ~/Library/LaunchAgents
	$ launchctl load ~/Library/LaunchAgents/homebrew.mxcl.mysql.plist

	# Run the Database Installer
	$ unset TMPDIR
	$ cd /usr/local/Cellar/mariadb/{VERSION}
	$ mysql_install_db

	# if mysql_install_db gives you errors and such, possible conflicting and multiple "mysqld" processes could be causing the sql server instance not to launch.
	# open up activity monitor and search for mysqld, and quit those processes
	# then try to start up mariadb with the code below

	$ mysql.server start # Start MariaDB
	$ mysql_secure_installation # Secure the Installation
	$ mysql -u root -p # Connect to MariaDB

*mysql issues on 10.5.5, reference this link http://stackoverflow.com/questions/34345726/brew-install-mysql-on-mac-os-el-capitan*

### SequelPro
SequelPro is installed via apps.sh if you're running the init.sh script with a few other apps. To use with MariaDB/MySql, add new Favorite in SequelPro sidebar, and set the host to 127.0.0.1 with the username 'root' and whatever password you set above in the MariaDB setup. Test connection, and save it. Now you can easily connect to all your local databases!

### Git
	$ brew install git

	# Write settings to ~/.gitconfig
	$ git config --global user.name '{YOUR NAME}'
	$ git config --global user.email {YOUR EMAIL}

	# a global git ignore file:
	$ git config --global core.excludesfile '~/.gitignore'
	$ echo '.DS_Store' >> ~/.gitignore

	# use keychain for storing passwords
	$ git config --global credential.helper osxkeychain

	# you might not see colors without this
	$ git config --global color.ui true

	# more useful settings: https://github.com/glebm/dotfiles/blob/master/.gitconfig

	# ssh keys - probably can skip this since github app auto adds it for you which is nice
	$ ls -al ~/.ssh # Lists the files in your .ssh directory, if they exist
	$ ssh-keygen -t rsa -C "your_email@example.com" # Creates a new ssh key, using the provided email as a label
	$ eval "$(ssh-agent -s)" # start the ssh-agent in the background
	$ ssh-add ~/.ssh/id_rsa
	$ pbcopy < ~/.ssh/id_rsa.pub # Copies the contents of the id_rsa.pub file to your clipboard to paste in github or w/e

### Node
	$ brew update
	$ brew install node
  
  ### composer
	$ brew update
	$ brew install composer
### bower
	$ npm install -g bower
### bundler
	$ gem install bundler
	# now you can use guard within projects
### Grunt
	$ npm install -g grunt-cli
### gulp
	$ npm install --global gulp
  
  ### Cask
	$ brew install caskroom/cask/brew-cask
		// If you want to install beta versions of things like Chrome Canary or Sublime Text 3,
	$ brew tap caskroom/versions
	$ brew cask install google-chrome # per app
	$ brew update && brew upgrade brew-cask && brew cleanup && brew cask cleanup # when done

	// fonts
	$ brew tap caskroom/fonts

	// apps
	# bash script to install apps -> apps.sh
	$ chmod u+x apps.sh # make it executable
	$ apps.sh # run it

### Sublime Text 3
#### install package installer
1. ctrl+` # opens console in sublime, paste below into console.
2. `import urllib.request,os,hashlib; h = '2915d1851351e5ee549c20394736b442' + '8bc59f460fa1548d1514676163dafc88'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)`

#### ST3 Packages
1. theme-default
2. brogrammer
3. sidebar-enhnacemnets
4. sidebar-folders
5. tabs-extra
6. alignment
7. codekit (.kit)
8. emmet
9. angularjs
10. sass
11. scss
12. docblocker
13. editorconfig
14. html-css-js-prettify
15. js hint
16. move tab
17. origami
18. markdown
19. movetab
20. unsplash
21. wordpress
22. sublimecodeintel
23. jekyll
24. trimmer
25. syncedSidebar


### Sketc 2
``
https://sketchapp.com``

### PHPStorm

### Parallels
