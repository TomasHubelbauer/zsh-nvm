# ZSH NVM

If installed NVM before upgrading to ZSH (for example by upgrading to macOS Catalina),
and you find yourself with `nvm use` versions not sticking, even with using `nvm alias`,
do this:

```sh
nano ~/.zshenv
# In Nano
. $HOME/.nvm/nvm.sh
PATH=$PATH:~/.nvm
# Save using Ctrl+X, Y
# Restart the terminal or source:
. ~/.zshenv
```

Now your NVM-selected version of Node should persist across terminal sessions.
