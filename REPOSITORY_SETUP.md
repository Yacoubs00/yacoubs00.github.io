# Yacoub's Kodi Repository - Setup Complete ✅

## Repository Structure Fixed

The repository now follows Kodi best practices and is properly structured for both GitHub repos.

### What Was Fixed

1. **Directory Structure**
   - Added addon metadata files (addon.xml, icon.png, fanart.jpg, changelog.txt) to `service.subtitles.yacoubs/` directory
   - Previously only had the zip file, now has proper addon structure

2. **URL Consistency**
   - Changed from `raw.githubusercontent.com` to `yacoubs00.github.io`
   - Repository now uses GitHub Pages URLs consistently
   - Rebuilt `repository.yacoubs-1.0.0.zip` with corrected URLs

3. **MD5 Checksum**
   - Updated `addons.xml.md5` to match the corrected `addons.xml`

## How It Works

### Repository: yacoubs00.github.io
**URL:** https://yacoubs00.github.io/

This is the main Kodi repository that users install from. It contains:
- `addons.xml` - List of all available addons
- `addons.xml.md5` - Checksum for verification
- `repository.yacoubs-1.0.0.zip` - The repository addon itself
- `repository.yacoubs.subs/` - Repository addon files
- `service.subtitles.yacoubs/` - Subtitle addon files and zip

### Repository: yacoubs-subtitles
This repo hosts the source code and uses GitHub Releases for version history.

## Installation Instructions for Users

### Method 1: Install Repository (Recommended)
1. Download: https://yacoubs00.github.io/repository.yacoubs-1.0.0.zip
2. In Kodi: Settings → Add-ons → Install from zip file
3. Select the downloaded zip
4. Go to: Install from repository → Yacoub's Repository → Subtitles
5. Install "Yacoub's Subs"

### Method 2: Direct Install
1. Download: https://yacoubs00.github.io/service.subtitles.yacoubs/service.subtitles.yacoubs-1.1.0.zip
2. In Kodi: Settings → Add-ons → Install from zip file
3. Select the downloaded zip
   
*(Note: Direct install won't receive automatic updates)*

## Repository Structure

```
yacoubs00.github.io/
├── addons.xml                              # Addon catalog
├── addons.xml.md5                          # Checksum
├── index.html                              # Web page
├── repository.yacoubs-1.0.0.zip           # Repository installer
├── repository.yacoubs.subs/
│   ├── addon.xml                          # Repository metadata
│   ├── icon.png
│   ├── fanart.jpg
│   └── changelog.txt
└── service.subtitles.yacoubs/
    ├── addon.xml                          # Addon metadata
    ├── icon.png
    ├── fanart.jpg
    ├── changelog.txt
    └── service.subtitles.yacoubs-1.1.0.zip # Addon installer
```

## Updating Addons

When you release a new version:

1. **In yacoubs-subtitles repo:**
   - Update version in `addon.xml`
   - Create GitHub release with new zip

2. **In yacoubs00.github.io repo:**
   - Copy new addon files to `service.subtitles.yacoubs/`
   - Copy new zip to `service.subtitles.yacoubs/`
   - Update version in `addons.xml`
   - Regenerate `addons.xml.md5`: `md5sum addons.xml > addons.xml.md5`
   - Commit and push

3. **Kodi will automatically detect the update** for users who installed via repository!

## URLs Reference

### Live URLs (accessible now)
- Repository: https://yacoubs00.github.io/repository.yacoubs-1.0.0.zip
- Addon: https://yacoubs00.github.io/service.subtitles.yacoubs/service.subtitles.yacoubs-1.1.0.zip
- Metadata: https://yacoubs00.github.io/addons.xml
- Checksum: https://yacoubs00.github.io/addons.xml.md5

### GitHub Repos
- Main Repo: https://github.com/Yacoubs00/yacoubs00.github.io
- Source Code: https://github.com/Yacoubs00/yacoubs-subtitles

## Testing

The "Could not connect to repository" error should now be fixed. Test on 2 different Kodi devices:

1. Remove old repository if installed
2. Install fresh from: https://yacoubs00.github.io/repository.yacoubs-1.0.0.zip
3. Check that repository shows up in: Add-ons → Install from repository
4. Install "Yacoub's Subs" from the repository
5. Verify it works and shows version 1.1.0

## Success Indicators

✅ Repository structure matches Kodi standards
✅ URLs use GitHub Pages (yacoubs00.github.io)
✅ Both addon directories contain metadata files
✅ MD5 checksum is correct
✅ All files are accessible via HTTPS
✅ Changes are committed and pushed

## Current Versions

- **Repository:** v1.0.0
- **Yacoub's Subs:** v1.1.0

---

*Last Updated: December 5, 2025*
*Fixed by: Repository structure standardization*
