# GitHub Upload Guide

Use this guide to upload the FSAE Vehicle Data Acquisition System project to GitHub.

## Recommended Repository Name

```text
FSAE-Vehicle-Data-Acquisition-System
```

## Upload Through GitHub Website

1. Create a new GitHub repository.
2. Name it `FSAE-Vehicle-Data-Acquisition-System`.
3. Upload all README files.
4. Upload the `images/` folder.
5. Commit the files.

## Upload Through Git Command Line

```bash
mkdir FSAE-Vehicle-Data-Acquisition-System
cd FSAE-Vehicle-Data-Acquisition-System

# Copy all README files and images folder here

git init
git add README*.md images/
git commit -m "Add FSAE vehicle data acquisition documentation"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/FSAE-Vehicle-Data-Acquisition-System.git
git push -u origin main
```

## Suggested GitHub Description

```text
Custom FSAE vehicle data acquisition system with embedded C firmware, Python CSV logging, KiCad PCB design, analog signal conditioning, current sensing, and real track validation.
```

## Suggested Topics

```text
fsae
embedded-systems
data-acquisition
automotive-electronics
python
kicad
matlab
embedded-c
sensor-fusion
vehicle-dynamics
pcb-design
```

## Important Note

Do not upload copyrighted PDF papers into your public repository unless you have permission. Upload your own README documentation, diagrams you created, code, schematics, and images you are allowed to share.
