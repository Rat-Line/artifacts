## 📜 The Complete Collection

This repository contains the canonical set of DOS reserved device names:

| File | Device | Purpose | Windows Accessibility |
|------|--------|---------|----------------------|
| `con.txt` | CON | Console (Keyboard/Screen) | ❌ Redirects to console |
| `nul.txt` | NUL | Null Device (Bit Bucket) | ❌ Redirects to null |
| `aux.txt` | AUX | Auxiliary Port | ❌ Redirects to console |
| `prn.txt` | PRN | Printer (LPT1 alias) | ❌ Redirects to printer |
| `lpt1.txt` | LPT1-9 | Parallel Ports 1-9 | ❌ Redirects to ports |
| `com1.txt` | COM1-9 | Serial Ports 1-9 | ❌ Redirects to ports |

## 🧪 The Experiment
1. **Clone on Linux**: All files are normal `.txt` files.
2. **Clone on Windows**: Files appear in listing but cannot be read, renamed, or deleted.
3. **The Paradox**: These files exist in Git history but not as accessible files on Windows.

## 🔬 The Proof
```powershell
# On Windows:
dir *.txt               # Files appear to exist
type con.txt            # Fails: "File not found"
git add con.txt         # Fails: "unable to index file"
del con.txt            # Fails: "Could not find file"
