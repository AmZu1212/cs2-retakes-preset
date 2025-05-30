<p align="center">
  <img src="https://github.com/user-attachments/assets/6d5549f3-7fdc-4f4f-a26d-739863f46055" alt="cs2"/>
</p>

![Top Banner](https://github.com/user-attachments/assets/7fda2d74-d90f-4a15-a4f0-2e73835bf580)
# cs2-retakes-preset

This is a pre-made Retakes server for CS2. All you need to do is port forward port 27015 on your router, and follow these steps to get a working Retakes server with no hassle. Recommended only for tech-savvy players. requires enough disk space for another cs2 installation (about 60GB).

## Used Plugin List:
- [Metamod (stable)](https://www.sourcemm.net/downloads.php?branch=stable)
- [CounterStrikeSharp v1.0.318](https://github.com/roflmuffin/CounterStrikeSharp/releases/tag/v1.0.318)
- [DeleteBuyZones](https://github.com/ItsChase88/deleteBuyZones)
- [InstaDefuse](https://github.com/B3none/cs2-instadefuse)
- [InstaPlant](https://github.com/B3none/cs2-instaplant)
- [MenuManager](https://github.com/NickFox007/MenuManagerCS2)
- [PlayerSettings](https://github.com/NickFox007/PlayerSettingsCS2)
- [RetakesAllocator](https://github.com/yonilerner/cs2-retakes-allocator)
- [AnyBaseLibCS2](https://github.com/NickFox007/AnyBaseLibCS2)
- [RetakesPlugin](https://github.com/B3none/cs2-retakes)
- [RockTheVote (my version)](https://github.com/AmZu1212/cs2-RTV-Fixed)
- [WeaponPaints](https://github.com/Nereziel/cs2-WeaponPaints)
---

## Step 1: Download CS2 Server Files

1. Download and extract [SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD#Downloading_SteamCMD).
2. Open a command prompt in the SteamCMD folder.
3. Run these commands:
    ```sh
    steamcmd
    login anonymous
    force_install_dir ./cs2-server
    app_update 730 validate
    quit
    ```
4. Your server files will be in the `cs2-server` folder.

---

## Step 2: Place Addons Folder

- Copy the entire `addons` folder from this repository into: `cs2-server/game/csgo/`
- Overwrite if prompted.

---

## Step 3: Download and Setup SQL Server (Windows) *(for skins, optional)*

- Download and install [MySQL Community Server](https://dev.mysql.com/downloads/mysql/).
- Follow the installer instructions, set a root password, and finish the installation.
- *(If you don’t want skins, you can skip this and the next step.)*

---

## Step 4: Update WeaponPaints Config *(for skins, optional)*

- Edit the file: `addons\counterstrikesharp\configs\plugins\WeaponPaints\WeaponPaints.json`
- Enter your MySQL server address, username, password, and database name in the .json file.

---

## Step 5: Change Server Config

- Copy your `server.cfg` file to:
- Edit it as needed (hostname, rcon password, etc.).

---

## Step 6: Get a Steam Game Server Login Token (GSLT)

1. Go to [https://steamcommunity.com/dev/managegameservers](https://steamcommunity.com/dev/managegameservers)
2. Enter **App ID:** `730`
3. Enter any memo.
4. Click **Create** and copy the generated token.

---

## Step 7: Fill .bat File With Your Token and cs2.exe Path

- Open `RunServer.bat` in a text editor.
- Replace `YOUR_TOKEN_HERE` with your Steam token.
- Update the path to your `cs2.exe` (inside your `cs2-server` folder).

---

## Step 8: Port Forward Port 27015

- Log in to your router settings.
- Port forward **UDP 27015** to your PC’s local IP address.

---

## Step 9: Run the .bat File

- Double-click `Run Server.bat`.
- Your server should now be online and visible in the CS2 community server browser.

---

**Done. Enjoy your Retakes server!**  
If you have issues, double-check each step and your port forwarding.

![Bottom Banner](https://github.com/user-attachments/assets/37fdd0cc-1e97-464d-82f6-6b3a6e116ac4)
