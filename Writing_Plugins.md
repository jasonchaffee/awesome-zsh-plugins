# Writing Plugins

Try and keep your plugins as cross-framework compatible as possible. Here are some suggestions to make using your plugin as simple as possible, no matter what framework someone is using.

1. Make it easier for everyone and put the plugin file at the root level of your plugin repository instead of in a subdirectory. This will let [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) users install it with a simple `git clone git@github.com:you/yourplugin.git` in the `custom/plugins` directory. [Antigen](https://github.com/zsh-users/antigen) and [zgen](https://github.com/tarjoilija/zgen) users will be able to automatically clone the repository without having to specify subdirectories.

2. Don't assume `${ZSH_CUSTOM}` is going to be set. `$(dirname $0)` will also tell you what directory your plugin is installed in.

3. Use `yourplugin.plugin.zsh` for the main plugin file. This is what [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) uses, and [antigen](https://github.com/zsh-users/antigen), [zgen](https://github.com/tarjoilija/zgen) and most other frameworks support it as well.
