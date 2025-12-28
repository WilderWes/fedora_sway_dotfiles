# Fedora Sway DotFiles

Author: Weston Preising

- basic sway config for vim
- kitty terminal with CommitMono and built in Nerd Font Glyphs
  - oh-my-zsh, starship, LazyVim
- yazi
- qutebrowser for opening markdown files and rendering latex
- esp-idf

## Guitar Specific

- Transcribe!
- Download TrueFire appimage, you can download videos locally and play through DAW or other medium
  - appimage requires fuse-libs
- ytdlp
- davinci resolve studio
  - [reddit_link](https://www.reddit.com/r/davinciresolve/comments/1pt8omd/guide_native_davinci_resolve_on_fedora_43/)
    - cd /opt/resolve/libs
    - sudo mkdir disabled-libraries
    - sudo mv libgio*disabled-libraries/
    - sudo mv libglib* disabled-libraries/
    - sudo mv libgmodule* disabled-libraries/
  - also need to install `intel-compute-runtime`
- fix obs-studio droidcam lag
  - [linux-audio-setup](https://wiki.linuxaudio.org/wiki/system_configuration)
  - main change is `realtime-setup` then enabling services and adding user to `realtime` group
- `BitwigStudio` flatpak
- `localsend` flatpak
- `handbrake-gui`
- `vlc`
- workflow
  - export in Avid DNxHR SQ --> convert to H.264 in HandBrake

## Testing / School Specific

- eclipse flatpak
  - GDK_SCALE=2 GDK_DPI_SCALE=0.5
- rars
  - using a custom script from ChatGPT to help with antialiasing
