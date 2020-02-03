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

## VS Code

Ensure VS Code's default shell is also set to ZSH otherwise these changes won't affect
it. The default out of the box is Bash, but it's hard to miss, because macOS Catalina
Bash is set up so that opening it notifies you to switch to ZSH.

Restart VS Code (not just the integrated terminal) in order to make it source anew.
