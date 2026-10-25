# Assignment 1.3 — Solution: Terminal & Developer Workflow

## Terminal Commands Record

### 1. Open the terminal
- **Windows:** press `Win + R`, type `cmd` (or open **PowerShell** / **Git Bash**), or use `Ctrl + `` in VS Code.
- **macOS/Linux:** open **Terminal**.

### 2. Create the main folder
```bash
mkdir web-development-practice
```

### 3. Create week folders inside it
```bash
cd web-development-practice
mkdir week-1 week-2 week-3
```

### 4. Create an `index.html` file inside each folder
```bash
# macOS / Linux / Git Bash
touch week-1/index.html week-2/index.html week-3/index.html

# Windows Command Prompt
type nul > week-1\index.html
type nul > week-2\index.html
type nul > week-3\index.html

# Windows PowerShell
New-Item week-1/index.html, week-2/index.html, week-3/index.html
```

### 5. Navigate, rename and delete
```bash
pwd                      # show current location (Windows cmd: cd)
ls                       # list contents (Windows cmd: dir)
cd week-1                # go into week-1
cd ..                    # go back one level
cd ~                     # go to home directory (Git Bash/macOS/Linux)

# Rename a folder
mv week-3 week-three     # Windows cmd: ren week-3 week-three
mv week-three week-3     # rename back

# Create a temporary folder and delete it
mkdir temp-folder
rmdir temp-folder        # remove empty folder (Windows cmd: rmdir temp-folder)

# Delete a folder with contents (use carefully)
mkdir -p temp/sub
rm -r temp               # Windows cmd: rmdir /s /q temp
                         # PowerShell: Remove-Item temp -Recurse
```

### 6. Open the project in VS Code from the terminal
```bash
cd ~/web-development-practice    # make sure you are in the project root
code .
```
> If `code` is not recognized: in VS Code press `Ctrl + Shift + P` → **Shell Command: Install 'code' command in PATH** (macOS), or reinstall VS Code with "Add to PATH" checked (Windows).

## Final Folder Structure
Check with `ls -R` (or `tree` / `tree /f` on Windows):

```
web-development-practice/
├── week-1/
│   └── index.html
├── week-2/
│   └── index.html
└── week-3/
    └── index.html
```

## Useful Command Cheat Sheet
| Action | macOS/Linux/Git Bash | Windows CMD |
|--------|----------------------|-------------|
| Current directory | `pwd` | `cd` |
| List files | `ls` / `ls -la` | `dir` |
| Make folder | `mkdir name` | `mkdir name` |
| Create file | `touch file` | `type nul > file` |
| Change directory | `cd name` | `cd name` |
| Rename/move | `mv old new` | `ren old new` / `move` |
| Delete file | `rm file` | `del file` |
| Delete folder | `rm -r name` | `rmdir /s name` |
| Clear screen | `clear` | `cls` |

## Submission
- ✅ Record of terminal commands (above)
- 📸 Screenshot of the final folder structure (run `ls -R` or `tree`, or show the Explorer panel in VS Code)
