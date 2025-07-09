# ms-gamebar-missing-fix
The script ensures that, if the preinstalled Gamebar had previously been removed, those pesky "couldn't open gamebar" pop ups disappear.

# ms-gamebar-missing-fix

## SYNOPSIS
Gets rid of the Windows pop-up saying the "ms-gamebar" link is missing and one is to search the Microsoft App Store.

---

## DESCRIPTION
The script remedies the cause of the nuisance by modifying the "ms-gamebar" keys in the registry and replacing them with a configuration placates Windows. 
If a Controller is connected, ms-gamebar is called and the script sees to it that the call both finds its target, and appears to be answered; it forwards it to "cmd.exe /c 'rem'", effectively a dud, which obligatorily does something, which is to say run a cmd command that does absolutely nothing. This effort will do its part to advance humanity in the ultimate aim of successfully experiencing a debloated Windows 11 with impunity.

**Beware:** The script itself does not uninstall the Gamebar (there are specific Windows debloat tools for that), it just ensures that an uninstallation has no side effects.
Furthermore, A Windows update, or an update of the Xbox (GamePass) app, could necessitate the tool having a go at it again.

The script itself can perform an automatic self-elevation and relaunchs itself with admin rights – AI be praised! Though that feature becomes irrelevant when launching the script through the provided bat file.
Going further, the script will also create .reg file on the Desktop which one can  use to conveniently revert the previous registry configuration, should one, for any reason, wish to do that.

The script's works like this:
1.  **BACKUP**: It first backs up any existing 'ms-gamebar' keys to a file on the Desktop.
2.  **PURGE**: It deletes any pre-existing 'ms-gamebar' keys from where they would usually be located, just to be safe.
3.  **REBUILD**: Creates the registry keys necessary, in HKEY_LOCAL_MACHINE, to satisfy the system's checks.

---

## USAGE

There are two options for running the script (it's not rocket science):

**Option 1: Direct Powershell Execution**

1.  **Download and extract** from the [Releases page](https://github.com/GrandiloquentSoliloquies/ms-gamebar-fix/releases).
2.  On the ".ps1" file: **Right click** and, inside the context menu, click **"Run with Powershell":** (Alternatively, open powershell in Admin and do "& {Parameters} {PathToScript}" alongside the parameters of your choice.)
3.  If there is an issue with someone's PowerShell execution policy being too restrictive, shift to Option 2.

**Option 2: Just launch the included bat file**

1.  **Download and extract**
2.  **Double Click on the .bat file**

**Fun Fact:** *You can replace `cmd.exe /c "rem"`, in the powershell script, with something like an application path "C:\Users\Julian\Documents\{Emulate Xbox360 Controller Software}". Then, whenever the ms-gamepar pop up would usually occur, the exe in the path is executed instead. However, the ms-gamebar pop up can be a bit capricious in their occurence and you wouldn't want to always have another instance of the app opening whenever the gamebar-missing pop up what have appeared; therefore some intermediary script might be necessary.*

## NOTES
* **Author**: GrandiloquentSoliloquies
* **Version**: 1.1

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
