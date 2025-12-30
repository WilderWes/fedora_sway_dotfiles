# Fedora Sway DotFiles

**Author:** Weston Preising

A minimal Fedora 43 Sway configuration focused on development (I'm currently a MS in CS candidate at Mines) and guitar practice/recording.
Emphasis on vim-based applications when possible since vim is fun. A profound thank you to all open source contributors--thank you for making Linux accessible and enjoyable :).

## To-do

1) update headers on all config files
2) add install commands

## Core Setup

### Terminal & Shell

- [kitty](https://sw.kovidgoyal.net/kitty/) with [CommitMono](https://commitmono.com/) font (includes Nerd Font glyphs)
- [oh-my-zsh](https://ohmyz.sh/) with plugins:
  - [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
  - [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
  - [zsh-completions](https://github.com/zsh-users/zsh-completions)
  - [gradle-completion](https://github.com/gradle/gradle-completion)
- [starship](https://starship.rs/) prompt
- [eza](https://github.com/eza-community/eza) as ls replacement
- [fastfetch](https://github.com/fastfetch-cli/fastfetch) system info

### Editor & File Management

- [Neovim](https://neovim.io/) via [LazyVim](https://www.lazyvim.org/)
- [yazi](https://github.com/sxyazi/yazi) terminal file manager
- [zathura](https://pwmt.org/projects/zathura/) with [zathura-pdf-poppler](https://pwmt.org/projects/zathura-pdf-poppler/) for PDF viewing

### Browsers

- [Firefox Developer Edition](https://copr.fedorainfracloud.org/coprs/the4runner/firefox-dev/) via COPR with [Betterfox](https://github.com/yokoffing/Betterfox) user.js
- [qutebrowser](https://qutebrowser.org/) — keyboard-driven browser, used strictly for [Markdown Preview](https://github.com/iamcco/markdown-preview.nvim)

### Embedded Development

- [esp-idf](https://github.com/espressif/esp-idf) toolchain
  - [NOTE] not using this currently but plan to build out some projects with my ESP32
- [SDKMAN](https://sdkman.io/) for JDK management (gradle)

## Music Production / Guitar

- [Transcribe!](https://www.seventhstring.com/) — slow down audio, loop sections, transcribe by ear
- [yt-dlp](https://github.com/yt-dlp/yt-dlp) — download videos/audio from YouTube
- [DaVinci Resolve Studio](https://www.blackmagicdesign.com/products/davinciresolve) — video editing
  - [Fedora 43 setup guide](https://www.reddit.com/r/davinciresolve/comments/1pt8omd/guide_native_davinci_resolve_on_fedora_43/)
  - Fix library conflicts:

    ```bash
    cd /opt/resolve/libs
    sudo mkdir disabled-libraries
    sudo mv libgio* disabled-libraries/
    sudo mv libglib* disabled-libraries/
    sudo mv libgmodule* disabled-libraries/
    ```

  - Also install `intel-compute-runtime`
- [OBS Studio](https://obsproject.com/) with [DroidCam](https://www.dev47apps.com/)
  - Fix lag via [linux audio realtime setup](https://wiki.linuxaudio.org/wiki/system_configuration)
  - Run `realtime-setup`, enable services, add user to `realtime` group
- [Bitwig Studio](https://www.bitwig.com/) — flatpak
- [Handbrake](https://handbrake.fr/) — video transcoding
- [VLC](https://www.videolan.org/vlc/)
- [LocalSend](https://localsend.org/) — flatpak, cross-platform file sharing

## School / Testing

- [Eclipse](https://eclipseide.org/) — flatpak
  - HiDPI fix: `GDK_SCALE=2 GDK_DPI_SCALE=0.5`
- [RARS](https://github.com/TheThirdOne/rars) — RISC-V assembler and simulator
  - Using custom script for antialiasing

## Communication

- [Discord](https://discord.com/)

## References

### Main Resource

- [Fedora 43 Post Install Guide](https://github.com/devangshekhawat/Fedora-43-Post-Install-Guide) — essential post-install steps

### Terminal & Shell

- [kitty](https://sw.kovidgoyal.net/kitty/) — GPU-accelerated terminal
- [CommitMono](https://commitmono.com/) — neutral programming font
- [oh-my-zsh](https://ohmyz.sh/) — zsh framework
- [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting) — fish-like syntax highlighting
- [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions) — fish-like autosuggestions
- [zsh-completions](https://github.com/zsh-users/zsh-completions) — additional completions
- [gradle-completion](https://github.com/gradle/gradle-completion) — gradle tab completion
- [starship](https://starship.rs/) — cross-shell prompt
- [eza](https://github.com/eza-community/eza) — modern ls replacement
- [fastfetch](https://github.com/fastfetch-cli/fastfetch) — system information tool

### Editor & Tools

- [Neovim](https://neovim.io/) — hyperextensible text editor
- [LazyVim](https://www.lazyvim.org/) — neovim configuration
- [yazi](https://github.com/sxyazi/yazi) — terminal file manager
- [zathura](https://pwmt.org/projects/zathura/) — vim-like PDF viewer
- [zathura-pdf-poppler](https://pwmt.org/projects/zathura-pdf-poppler/) — poppler PDF backend

### Browsers

- [Firefox Developer Edition COPR](https://copr.fedorainfracloud.org/coprs/the4runner/firefox-dev/) — bleeding edge Firefox
- [Betterfox](https://github.com/yokoffing/Betterfox) — Firefox user.js for speed and privacy
- [qutebrowser](https://qutebrowser.org/) — keyboard-driven browser

### Development

- [esp-idf](https://github.com/espressif/esp-idf) — ESP32 development framework
- [SDKMAN](https://sdkman.io/) — SDK version manager for JVM languages

### Fedora Docs

- [Adding New Fonts](https://docs.fedoraproject.org/en-US/quick-docs/fonts/) — install custom fonts
- [Installing Java](https://docs.fedoraproject.org/en-US/quick-docs/installing-java/) — OpenJDK setup
- [LaTeX](https://docs.fedoraproject.org/en-US/neurofedora/latex/) — TeXLive installation
- [Troubleshoot Sound Problems](https://docs.fedoraproject.org/en-US/quick-docs/how-to-troubleshoot-sound-problems/) — PipeWire debugging

### Sway / Wayland

- [Fedora Sway Login Background](https://morph.sh/posts/2024-01-15-fedora-sway-change-background/) — change sddm and swaylock backgrounds
- [Fedora Sway Kanshi Setup](https://blog.sakuragawa.moe/working-on-fedora-sway-spin/) — multi-monitor config
- [Detect Wayland vs XWayland](https://medium.com/@bugaevc/how-to-easily-determine-if-an-app-runs-on-xwayland-or-on-wayland-natively-8191b506ab9a) — use xeyes to check
- [kanshi](https://github.com/emersion/kanshi) — dynamic output configuration
- [gammastep](https://gitlab.com/chinstrap/gammastep) — screen color temperature (Wayland redshift alternative)
- [dunst](https://github.com/dunst-project/dunst) — lightweight notification daemon
- [simple-hyprland](https://github.com/gaurav23b/simple-hyprland) — borrowed dunst config from here

### Audio

- [Linux Audio Config](https://wiki.linuxaudio.org/wiki/system_configuration) — realtime audio setup

### Docker

- [Docker on Fedora](https://docs.docker.com/engine/install/fedora/) — install Docker Engine
- [Docker Post-Install](https://docs.docker.com/engine/install/linux-postinstall/) — non-root user setup
- [Docker Completion](https://docs.docker.com/compose/completion/) — shell autocompletion

### Utilities

- [Clang-Format Options](https://clang.llvm.org/docs/ClangFormatStyleOptions.html) — code formatting config
- [img2pdf](https://pypi.org/project/img2pdf/) — lossless image to PDF
- [cpdf](https://github.com/coherentgraphics/cpdf-binaries) — PDF manipulation from the command line

### Other Acknowledgments

Plenty of small fixes came from random Google searches, Reddit threads, and StackOverflow answers that may not be cited (I should have done a better job organizing this from the get-go).

## AI Usage

- To organize this README
- To convert some default fedora theming to tokyo-night (e.g. Waybar)
- Played around with a few models but been mostly using Claude
- When using AI, I strive to use it as an active learning tool -- not blindly copying and pasting -- and always prioritize active learning whenever possible.
