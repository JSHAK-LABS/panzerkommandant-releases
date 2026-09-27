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
One of you hosts, the other joins. The host needs the better PC and the
better internet upload speed, because the whole battle runs on the host.

The host:
1. Main menu > Skirmish. Set up the battle, then press "Host online".
2. The game asks your router to open UDP port 27015 automatically (UPnP).
   The banner at the top says what happened:
   - "over the internet they join at 1.2.3.4" -> send that address to your
     friend. The launcher also shows your internet address, with a Copy
     button.
   - "the router did not open it" -> open the port by hand (see below), then
     host again.
3. The first time you host, Windows Firewall asks whether to allow
   panzerkommandant.exe. Tick both "Private" and "Public" and click Allow.
   If you clicked Cancel by mistake: Start > "Allow an app through Windows
   Firewall" > Change settings > tick panzerkommandant.exe on both columns.

The joiner:
1. Main menu > Skirmish > "Join online".
2. Type the host's address and press Connect. Nothing to set up on your side.


IF THE ROUTER DID NOT OPEN THE PORT
Log in to your router (usually http://192.168.0.1 or http://192.168.1.1; the
password is often on a sticker on the router) and find "Port forwarding"
(sometimes called "Virtual servers" or "NAT"). Add a rule:
   Protocol: UDP     External port: 27015     Internal port: 27015
   Device / internal IP: the hosting PC (the game shows it in the banner)
Or switch on "UPnP" in the router's settings and host again.

STILL CANNOT CONNECT?
- Swap roles: let the other player host.
- Some internet providers put customers behind a shared address ("CGNAT"),
  and nobody behind one can host. If the address the launcher shows is
  different from the WAN address on your router's status page, that is you:
  let the other player host, or ask your provider for a public IP.
- As a last resort, both install a free virtual LAN such as Tailscale or
  ZeroTier and join with the address it gives the host.


LAG
- Company and Battalion battles play best online. A Kampfgruppe is about
  1,000 soldiers and over 100 vehicles, and needs a strong host PC and a
  good upload speed.
- If the host's frame rate drops, the battle slows down for both of you.
```

---
Each release holds only the files that changed; its manifest.json links into earlier releases for the rest, so releases here are never deleted.
