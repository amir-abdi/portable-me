# Portable Me
This is how I make myself (Amir H. Abdi, aka. AHA) a portable developer as I move across orgs.
If you landed here by accident, you might enjoy learning about [my working style](./working-with-me.md)
more than my technical setup.

# Mac

## Tools

- Windows manager: [Rectangle](https://rectangleapp.com/)
- Multiscreen Agent: [Display Link Manager](https://www.synaptics.com/products/displaylink-graphics/downloads/macos)
- IDE: [PyCharm](https://www.jetbrains.com/pycharm/)
  - Set the [settings](./ide/pycharm_settings.zip)
- Offline Password Manager: [KeepassXC](https://keepassxc.org/)

## OS Settings
- Set the default screenshot directory:
  ```bash
  defaults write com.apple.screencapture /Users/`whoami`/Screenshots
  ```

# Shell/Terminal
The following are better be installed in the same order:
- Terminal: [iterm2](https://iterm2.com/)
  - Set the [profile](./terminal/iterm_profile.json)
- Package Manager: [Brew](https://docs.brew.sh/Installation)
- Shell: [zsh](https://formulae.brew.sh/formula/zsh)
  - [oh my zsh](https://github.com/ohmyzsh/ohmyzsh)
    - [auto-suggestions](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md#oh-my-zsh)
  - [Syntax highlighting](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)
  - Set the [profile](./terminal/zshrc)
  - Prompt helper: [Starship](https://starship.rs/)
- Git
  - [Git Quick Stats](https://github.com/arzzen/git-quick-stats)
- Acronym Util: [WTF](https://formulae.brew.sh/formula/wtf)
  - Delete offensive acronyms: `/usr/local/Cellar/wtf/$VERSION/share/misc/acronyms-o` 
  - Set `ACRONYMDB=/path/to/cystom/acronym/file`
  


### Other
- Email signature: *P.S. My working day may not be your working day. 
  Please don’t feel obliged to reply outside of your normal working hours.*

 