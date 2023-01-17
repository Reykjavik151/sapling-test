My terminal actions are on record:

```bash
brew install sapling

# I had to do this command because of failure previous one
xcode-select --install

# And then again the previous command
brew install sapling

# Configure creds of your account
# You can just change your name/email if you wish :D
sl config --user ui.username "Roman Andreev <reykjavik151@gmail.com>"

# This command failured 
# Because after the previous clone command it was a `.git` folder
# But we need `.sl` folder
sl add .

# So remove the directory and clone it with sapling to create `.sl` folder
sl clone git@github.com:Reykjavik151/sapling-test.git

sl add .
# I have a watchman warning here
# warning: watchman has recently started (pid 1705) - operation will be slower than usual

sl commit
# It opened vim as editor..
# I really want to open only and only VSCode for this purpose

# Googled solution
sl config --user ui.editor "/usr/local/bin/code --wait"

# And then again
sl commit
# Opened VSCode
# But it looks different from our usual git commit template

# Here I realised that I can't see the branch in the VSCode / Terminal
# Its annoying (-)
# I wrote the issue about it here:
# https://github.com/facebook/sapling/issues/472

# I've tried to install Sapling SCM extension for my VSCode
# But seems it doesn't provide any current branch info for my status bar / terminal (even built-in VScode terminal)

sl
# Check the history of commits
# Really nice branch tree (+)

sl push
# Automatic push to `main` branch

