# **How ​​to Switch Between Old and New Right-Click Menu in Windows 11**

This guide shows you how to switch between the **old right-click menu** (Windows 10 style) and the **new right-click menu** (Windows 11's default menu). To make the process easier, we've also included `.bat` files inside the `.zip` file so you can quickly run them.

---

## **Overview**

Windows 11 introduces a cleaner, more modern right-click menu. However, some users may find the old menu more functional and familiar. This guide explains how to switch between the two menus by modifying the Windows Registry.

---

## **Switch to Old Right-Click Menu (Classic Menu)**

To enable the old right-click menu, follow these steps:

1. **Open Command Prompt or PowerShell as Administrator**:
- Open the **Start** menu and type `cmd` or `powershell`.
- Right-click on the application and select **Run as administrator**.

2. **Run the Command**:
```cmd
reg add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /and
```

3. **Restart Your Computer**:
- Restart your computer or log off and back on for the changes to take effect.

After completing these steps, the **classic right-click menu** will be enabled.

---

## **Return to New Right-Click Menu (Default Windows 11 Menu)**

To return to the default right-click menu, follow these steps:

1. **Open Command Prompt or PowerShell as Administrator**:
- Open the terminal as administrator as shown in the previous section.

2. **Run the Command**:
```cmd
reg delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}" /f
```

3. **Restart Your Computer**:
- Restart your computer or log out and back in for the changes to take effect.

After completing these steps, the **modern right-click menu** will be restored.

---

## **Important Notes**

- Editing the Windows Registry can significantly affect your system. Follow the instructions carefully to avoid problems.
- If you get the **"Access Denied"** error, make sure you are running the terminal as an administrator.
- Make sure you only change the specified registry paths, otherwise you may make unwanted changes.

---

## **Alternative Simplified Method**

To make this process even easier, `.bat` files for both operations are included in the `.zip` file. You can extract the files and run the `.bat` file containing the operation you want to perform:

- **`Enable_Classic_Menu.bat`**: Enables the old right-click menu.
- **`Restore_New_Menu.bat`**: Restores the default Windows 11 right-click menu.

The changes will take effect when you run these `.bat` files **as Administrator**.

---

By following the steps in this guide, you can easily enable or disable the right-click menu you want.
