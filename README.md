# cs2-retakes-preset

This is a pre-made Retakes server for CS2. All you need to do is port forward port 27015 on your router, and follow these steps to get a working Retakes server with no hassle. Recommended only for tech-savvy players. requires enough disk space for another cs2 installation (about 60GB).

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

## Step 3: Get a Steam Game Server Login Token (GSLT)

1. Go to [https://steamcommunity.com/dev/managegameservers](https://steamcommunity.com/dev/managegameservers)
2. Enter **App ID:** `730`
3. Enter any memo.
4. Click **Create** and copy the generated token.

---

## Step 4: Download and Setup SQL Server (Windows) *(for skins, optional)*

- Download and install [MySQL Community Server](https://dev.mysql.com/downloads/mysql/).
- Follow the installer instructions, set a root password, and finish the installation.
- *(If you don’t want skins, you can skip this and the next step.)*

---

## Step 5: Update WeaponPaints Config *(for skins, optional)*

- Edit the file: `addons\counterstrikesharp\configs\plugins\WeaponPaints\WeaponPaints.json`
- Enter your MySQL server address, username, password, and database name in the .json file.

---

## Step 6: Change Server Config

- Copy your `server.cfg` file to:
- Edit it as needed (hostname, rcon password, etc.).

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
