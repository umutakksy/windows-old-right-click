Here’s how the content can be formatted for a GitHub `README.md` file:

```markdown
# **Guide to Switch Between Old and New Right-Click Menu in Windows 11**

This guide explains how to switch between the default Windows 11 right-click menu (new context menu) and the classic right-click menu. Since this involves modifying the Windows Registry, you will need to run the terminal as an administrator.

---

## **1. Switch to the Old Right-Click Menu (Classic Context Menu)**

### **Steps:**
1. **Open Command Prompt (CMD) or PowerShell as Administrator**:
   - Open the **Start** menu, type `cmd` or `powershell`.
   - Right-click on the result and select **Run as Administrator**.

2. **Run the Following Command**:
   ```cmd
   reg add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
   ```

3. **Press Enter**:
   - This command creates the necessary registry key to enable the old right-click menu.

4. **Restart Your Computer**:
   - Restart your computer or sign out and back in for the changes to take effect.

---

## **2. Switch Back to the New Right-Click Menu (Default Windows 11 Menu)**

### **Steps:**
1. **Open Command Prompt (CMD) or PowerShell as Administrator**:
   - Open the terminal with administrator privileges, just like before.

2. **Run the Following Command**:
   ```cmd
   reg delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}" /f
   ```

3. **Press Enter**:
   - This command removes the registry key, reverting back to the default new right-click menu.

4. **Restart Your Computer**:
   - Restart your computer or sign out and back in for the changes to take effect.

---

## **Important Notes**
- Modifying the Windows Registry can have a significant impact on your system. Use these commands with care.
- If you encounter an **"Access Denied"** error, ensure the terminal is running in administrator mode.
- Only modify the paths mentioned in this guide to avoid unintended issues.

---

## **Simplified Alternative**
To make this process easier, `.bat` files for both commands are included in the `.zip` file. Simply extract the files and run the one that matches your needs:  
- `Enable_Classic_Menu.bat` to enable the old menu.  
- `Restore_New_Menu.bat` to restore the default Windows 11 menu.  

Run these `.bat` files as an administrator for convenience.
``` 

Copy and paste this content into a `README.md` file in your GitHub repository. It will be formatted and displayed correctly.
