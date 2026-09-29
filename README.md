# PANZERKOMMANDANT

A WW2 tank and infantry game: command a battlegroup from the turret of your own tank, against the AI or a friend online.

## Download

**[Download PanzerkommandantLauncher.exe](https://github.com/JSHAK-LABS/panzerkommandant-releases/releases/latest/download/PanzerkommandantLauncher.exe)** (Windows 10/11), run it, press PLAY.

The launcher downloads the game (about 650 MB) and keeps it up to date; always start the game from it, so everyone online is on the same version.

## Installing and playing online

```
INSTALLING
1. Download the launcher:
   https://github.com/JSHAK-LABS/panzerkommandant-releases/releases/latest/download/PanzerkommandantLauncher.exe
2. Run PanzerkommandantLauncher.exe (keep it anywhere, e.g. the Desktop).
   Windows may say "Windows protected your PC", because the launcher is not
   signed by a big publisher. Click "More info", then "Run anyway".
3. The first time it downloads the game (about 650 MB). After that it only
   downloads what changed, and it updates itself too. The game installs to
   %LOCALAPPDATA%\Panzerkommandant\game.
4. Press PLAY. Always start the game from the launcher: that is what keeps
   both of you on exactly the same version.

The version is on the game's title screen and in the launcher, for example
"0.3.0-bf5db624". Both players must show the same one, or the host will turn
the joiner away with a message saying so. The fix is always the same: close
the game and open the launcher on both PCs.


PLAYING TOGETHER OVER THE INTERNET
One of you hosts, the other joins. The whole battle runs on the host's PC,
so the host wants the better PC and the better upload speed.

The host:
1. Main menu > Multiplayer > Host a Skirmish. Set up the battle and press
   "Host online".
2. The banner at the top shows the ONE address to send your friend (press C
   to copy it) and, underneath, whether they can get through:
   - "Your router opened port 27015 for the game" -> good to go.
   - "Your router did not open the port" -> forward UDP port 27015 to your
     PC in the router's settings (see below), then host again.
   - "Your internet provider shares your address with other customers" ->
     your connection cannot host at all (many providers do this). Let the
     other player host, or use Tailscale (below).
3. The first time you host, Windows Firewall asks about panzerkommandant.exe:
   tick both "Private" and "Public" and click Allow.

The joiner:
1. Main menu > Multiplayer > Join a Skirmish.
2. Type the address the host's banner shows and press Connect.

Both of you must have the same version (shown on the title screen): always
start the game from the launcher and it keeps you the same.


IF NEITHER CONNECTION CAN HOST: TAILSCALE
Tailscale (free, tailscale.com) links two PCs as if they were on the same
network, whatever the providers and routers do.
1. Both of you install Tailscale and sign in. The host shares their machine
   with the joiner (in the Tailscale admin page: Share), or you both sign
   in to the same account.
2. Host as usual: the banner then shows the host's Tailscale address
   (100.x.y.z) -- send that one.


IF THE ROUTER DID NOT OPEN THE PORT
Log in to your router (usually http://192.168.0.1 or http://192.168.1.1; the
password is often on a sticker on the router) and find "Port forwarding"
(sometimes "Virtual servers" or "NAT"). Add a rule:
   Protocol: UDP     External port: 27015     Internal port: 27015
   Device / internal IP: the hosting PC (the banner shows it)
Or switch on "UPnP" in the router's settings and host again.


LAG
- Company and Battalion battles play best online. A Kampfgruppe is about
  1,000 soldiers and over 100 vehicles, and needs a strong host PC and a
  good upload speed.
- If the host's frame rate drops, the battle slows down for both of you.
```

---
Each release holds only the files that changed; its manifest.json links into earlier releases for the rest, so releases here are never deleted.
