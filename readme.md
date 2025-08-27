# Amigo

![Amigo Logo](images/icon.png)

**Amigo** is a Visual Studio Code extension that enhances project hygiene by scanning for unused files and providing an intuitive interface to manage them. Keep your workspace clean and organized with fast, lightweight scanning.

---

## Features
- **Scan All Files**: Detects unused files in your project, regardless of file type, respecting `.gitignore` and custom ignore patterns.
- **Tree View**: Displays unused files in the Explorer sidebar with options to open, delete, or ignore them.
- **Progress Indicator**: Shows scan progress for large projects.
- **Context Menus**: Right-click options in the Explorer and Tree View for scanning and file management.
- **Persistent Ignore**: Exclude specific files from future scans, saved across sessions.
- **Lightweight and Fast**: Optimized for quick scans and minimal resource use.

---

## Commands
- **Amigo: Scan**: Scans your workspace and lists unused files in the Output tab and Tree View.
- **Amigo: Status**: Displays “Amigo: Extension active” in the Output tab.
- **Amigo: Version**: Shows the installed extension version (e.g., `v0.0.7`).
- **Amigo: Clean**: Deletes a specific unused file.
- **Amigo: Clean --all**: Removes all unused files after confirmation.
- **Amigo: Open File**: Opens a file from the Tree View.
- **Amigo: Ignore File**: Excludes a file from future scans (persists across sessions).

---

## Configuration
You can customize Amigo via VS Code settings:
- **`amigo.ignorePatterns`**: Additional patterns to ignore during scanning (e.g., `["node_modules", "*.log"]`). Default: `[]`.

Amigo respects `.gitignore` and custom ignore patterns, scanning all file types for unused files.

---

## Usage
1. Install Amigo from the VS Code Marketplace or a `.vsix` file (`Extensions > ... > Install from VSIX`).
2. Open a project folder in VS Code (`File > Open Folder`).
3. Run commands via the **Command Palette** (`Ctrl+Shift+P`) or right-click in the Explorer:
   - Right-click a folder and select `Amigo: Scan` to start a scan.
   - Right-click a file and select `Amigo: Clean` to delete it (if unused).
   - Right-click a folder and select `Amigo: Clean --all` to delete all unused files.
4. View results in:
   - **Output tab** (“Amigo” channel) for a detailed list of unused files.
   - **Amigo: Unused Files** Tree View in the Explorer sidebar.
5. In the Tree View, right-click files to open, delete, or ignore them.

---

## Improvements in Latest Version
### 0.0.7
- Added **Tree View** in the Explorer sidebar to display unused files with actions (open, delete, ignore).
- Added **progress indicator** for scanning large projects.
- Removed file extension filtering, now scanning all files for broader coverage.
- Added **persistent ignore** for files, saved across sessions.
- Enhanced **context menus** in Explorer and Tree View for easier file management.
- Improved async scanning for better performance.

### 0.0.6
- Added project icon (pixel-art retro style).
- Integrated `.gitignore` parsing for faster scanning.
- Improved output handling and cleanup features.

### 0.0.1
- Initial release of Amigo.

---

## Troubleshooting
- **Tree View Missing**:
  - Run `Amigo: Scan` to populate it.
  - Open the Explorer (`Ctrl+Shift+E`) and check `... > Show All`.
  - Use `View: Show Amigo: Unused Files` in the Command Palette.
- **No Unused Files**:
  - Ensure some files are not referenced by others.
  - Check `amigo.ignorePatterns` for overly broad patterns (e.g., `*.*`).
- **Scan Errors**:
  - Verify a project folder is open.
  - Check the Output tab or Developer Console (`Help > Toggle Developer Tools`) for errors.

---

## Feedback
Report issues or suggest features at [https://github.com/ChandanSaroj/amigo/issues](https://github.com/ChandanSaroj/amigo/issues).

Keep your projects clean with Amigo!
