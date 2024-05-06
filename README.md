# GamingOnHackintoshAMD
Guide + Testing of games on a AMD Hackintosh (RX580[Metal 2] | Ryzen 5 3600)
A guide will be released later on how I was able to get the games pictured below running and testing playability
Note: For users with a stronger GPU that supports Metal 3 games will run MUCH better using D3DMetal feature in CrossOver(With moltenVK CXPatcher)

# Steam Issues w/ Crossover 24(and older versions posisbly)
- Steam crashes while downloading
- DO NOT SAVE LOGIN! Causes issue with ram increasing while loading and steam will sometimes instantly crash.
- Most likely due to a ram issue with the way crossover wine runs steam
  - Current fix I am using is to close explorer.exe in the crossover settings(Control Panels setting in the steam settings bottle)
  - Disable GPU accelerated + Smooth scrolling in steam settings
  - Low peformance mode enabled (Steam settings -> Library)
- This fixes steam crashing constantly, but when downloading it may crash after sometime. Usually going into activity monitor(the macOS utility) and closing all the ".exe" and then running steam again in crossover will run again. (Reboot PC if steam still doesn't open). The optional tweaks below are what I used that helped steam/games run slightly better

# Tweaks(OPTIONAL)

## Disable spotlight

```bash
# Disables spotlight but helps with steam crashing.
sudo mdutil -i off -a

# Re-enable spotlight
# sudo mdutil -i on -a

```
  
## Reduce Motion & Transparency

```bash
defaults write com.apple.Accessibility DifferentiateWithoutColor -int 1
defaults write com.apple.Accessibility ReduceMotionEnabled -int 1
defaults write com.apple.universalaccess reduceMotion -int 1
defaults write com.apple.universalaccess reduceTransparency -int 1
```


# W.I.P(Currently tested games so far)

# Genshin Impact

![](http://i.epvpimg.com/339jcab.jpg)

Status: Works! | Uses yet another anime game launcher(look it up) and set wine environment to unstable-bh-1.2 to fix game crashing. Basically native performance using windows

# Sleeping Dogs Definitive Edition

![](http://i.epvpimg.com/DEddaab.jpg)

Status: Works(Mostly with one major bug) | Playable, but when playing with my original screen resolution(1920x1080) caused the textures to be blurry no matter what. Lowering the resolution fixed it and you must set the 3D settings in the game lower. 

# Palworld

![](http://i.epvpimg.com/RPVEeab.jpg)

Status: Works | Loading into the game takes a VERY long time intially. The game will freeze when creating a world for a bit as textures load and when the world loads in as well. After the game runs fine with low/medium settings. So far no major texture issues.

