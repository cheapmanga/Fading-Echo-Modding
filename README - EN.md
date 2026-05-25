# Fading-Echo-Modding - EN
## Complete Guide: Modifying Localization Text in Fading Echo Demo

### Prerequisites
- FModel installed
- UnrealPak tool downloaded
- A .locres editor (choose one from the options below)

### Step 1: Extract the Localization File
1. Open FModel
2. Navigate to: `UE_YGRO/Content/Localization/Game/fr/Game.locres`
3. Right-click on `Game.locres` and extract it to your computer

### Step 2: Edit the Localization File

Choose one of these editors to modify the .locres file:

**Option A - Unreal Locres Editor (GUI - Recommended):**
- Download: https://github.com/snoozeds/UnrealLocresEditor

**Option B - LocresStudio:**
- Download: https://github.com/AcTePuKc/LocresStudio

**Option C - UE4-locres-Online-Editor:**
- Access: https://github.com/klimaleksus/UE4-locres-Online-Editor

**Option D - UEExtractor (Command-line):**
- Download: https://github.com/SolicenTEAM/UEExtractor

Open your extracted `Game.locres` file in the editor, find the text you want to modify, change it, and save the file.

### Step 3: Create the Mod Folder Structure

Create a folder with this exact structure (the folder name must end with `_P`):

```
CustomLocres_P/
└── UE_YGRO/
    └── Content/
        └── Localization/
            └── Game/
                └── fr/
                    └── Game.locres (your modified file)
```

Place your modified `Game.locres` file in the `fr` folder.

### Step 4: Download UnrealPak

Download the standalone UnrealPak tool:
- Download: https://github.com/Dmgvol/UE_Modding/raw/main/Tools/UnrealPak.zip

Extract it to a folder. You should see:
- `UnrealPak-With-compression.bat`
- `UnrealPak.exe`
- Other support files

### Step 5: Create the .pak File

**Method A - Using the Batch File (Easiest):**
- Drag and drop your `CustomLocres_P` folder onto `UnrealPak-With-compression.bat`
- This will automatically create `CustomLocres_P.pak`

**Method B - Using Command Line:**
1. Open Command Prompt in the UnrealPak folder
2. Create a filelist.txt file with the path to your mod folder
3. Execute:
```
UnrealPak.exe "C:\path\to\CustomLocres_P.pak" -create=filelist.txt -compress
```

### Step 6: Install the Mod

1. Navigate to the game's Paks folder:
```
Steam\steamapps\common\Fading Echo Demo\UE_YGRO\Content\Paks
```

2. Copy your `CustomLocres_P.pak` file into this folder

### Step 7: Create IoStore Files (Required for UE5 games with .ucas/.utoc)

Since your game uses the IoStore format (you have `.ucas` and `.utoc` files):

1. In the Paks folder, locate `global.ucas` and `global.utoc`
2. Copy `global.ucas` and rename the copy to `CustomLocres_P.ucas`
3. Copy `global.utoc` and rename the copy to `CustomLocres_P.utoc`

Your Paks folder should now contain:
- global.ucas
- global.utoc
- UE_YGRO-Windows.pak
- UE_YGRO-Windows.ucas
- UE_YGRO-Windows.utoc
- CustomLocres_P.pak
- CustomLocres_P.ucas
- CustomLocres_P.utoc

### Step 8: Test the Game

Launch Fading Echo Demo and verify that your modified text appears.

### Troubleshooting

If the changes don't appear:
- Verify that the folder structure matches exactly
- Make sure the folder name ends with `_P`
- Check that the .locres file is in the correct language folder (`fr` for French)
- The text might be in another .locres file (like `Engine.locres`)
- The text might be hardcoded in a widget or blueprint

### Additional Resources

- Unreal Engine Localization Documentation: https://docs.unrealengine.com/
- FModel GitHub: https://github.com/4sval/FModel
- UE Modding Community: https://www.nexusmods.com/
- UE Modding Tools Collection: https://github.com/Dmgvol/UE_Modding

### Credits

- UnrealPak Tool: https://github.com/Dmgvol/UE_Modding
- Guides and tutorials from the Unreal Engine modding community

---

This guide was tested on Fading Echo Demo.  
Note that the procedure may vary for modifications other than this one.  

This guide was entirely written with artificial intelligence.  
