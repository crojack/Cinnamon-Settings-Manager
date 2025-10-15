# Cinnamon Settings Manager

A modern, comprehensive settings management suite for Linux Mint Cinnamon desktop environment, written in Perl with GTK3.

![Cinnamon Settings Manager](https://img.shields.io/badge/Platform-Linux%20Mint%20Cinnamon-green)
![Language](https://img.shields.io/badge/Language-Perl-blue)
![GUI](https://img.shields.io/badge/GUI-GTK3-orange)
![License](https://img.shields.io/badge/License-MIT-yellow)

## Overview

Cinnamon Settings Manager is a collection of specialized configuration tools that provides an interface for managing various aspects of your Cinnamon desktop environment. It has a slightly different module organization than the original Linux Mint Cinnamon system settings

### **Main Settings Manager**
- Unified interface for all main appearance system settings
- Search functionality
- Organized category-based navigation
- Integration with system configuration tools

<img width="3573" height="2152" alt="Screenshot from 2025-08-24-19-51-21" src="https://github.com/user-attachments/assets/6b138b67-ad39-402f-8c09-9ceb0fa43c0f" />


## Features

- **Cinnamon Theme Manager** - Preview and apply Cinnamon desktop themes
<img width="3565" height="2152" alt="Screenshot from 2025-08-24-19-49-20" src="https://github.com/user-attachments/assets/68b17956-1f7a-4fa3-b097-f37262733a7e" />


- **Application Theme Manager** - Preview and apply GTK themes for applications
<img width="3565" height="2152" alt="Screenshot from 2025-08-24-19-48-14" src="https://github.com/user-attachments/assets/b9de62c9-cbba-4ecb-9d54-cc6758f69155" />


- **Icon Theme Manager** - Browse and switch between icon themes with comprehensive previews
<img width="3565" height="2152" alt="Screenshot from 2025-08-24-19-49-00" src="https://github.com/user-attachments/assets/f6b603f3-6c46-4330-a450-78abed335fc3" />


- **Cursor Theme Manager** - Advanced cursor theme management with extracted cursor previews
<img width="3565" height="2152" alt="Screenshot from 2025-08-24-19-47-12" src="https://github.com/user-attachments/assets/2c78285a-3b0c-4aaf-a23b-fc1add463028" />


- **Background Manager** - Wallpaper management with thumbnail previews
<img width="3565" height="2152" alt="Screenshot from 2025-08-24-19-46-24" src="https://github.com/user-attachments/assets/1deb7dc2-e098-449a-92b6-587b42117560" />


- **Font Manager** - System font management with live preview capabilities
<img width="3565" height="2152" alt="Screenshot from 2025-08-24-19-46-50" src="https://github.com/user-attachments/assets/b6db225e-df44-48ac-8943-ffaa1d2f495e" />


## Usage

### Running the Applications

After installation, you can run the applications in several ways:

**From Command Line:**
```bash
# Main settings manager
cinnamon-settings-manager.pl

# Individual managers
cinnamon-themes-manager.pl
cinnamon-application-themes-manager.pl
cinnamon-icon-themes-manager.pl
cinnamon-cursor-themes-manager.pl
cinnamon-backgrounds-manager.pl
cinnamon-font-manager.pl
```

**From Application Menu:**
Look for the applications in your system's application menu under the "Settings" category.

### Application Features

#### Main Settings Manager
- **Unified Interface**: Access all Cinnamon settings from one place
- **Advanced Search**: Quickly find specific settings
- **Category Organization**: Logical grouping of related settings
- **Custom Module Integration**: Launches specialized theme managers

#### Theme Managers
- **Live Previews**: See themes before applying them
- **Multiple Sources**: Scan system and user theme directories
- **Theme Information**: View theme details and metadata
- **Zoom Control**: Adjustable preview sizes

#### Cursor Theme Manager
- **Advanced Preview**: Extract and display actual cursor shapes
- **Multiple Cursors**: Preview different cursor types (arrow, hand, text, etc.)
- **Cache Management**: Efficient thumbnail caching system
- **Zoom Control**: Adjustable preview sizes

#### Background Manager
- **Thumbnail Grid**: Visual browsing of wallpapers
- **Multiple Formats**: Support for various image formats
- **Custom Directories**: Add your own wallpaper folders
- **Zoom Control**: Adjustable preview sizes

#### Font Manager
- **Live Preview**: See fonts rendered with sample text
- **System Integration**: Works with system font configuration
- **Custom Sample Text**: Use your own preview text
- **Font Information**: Display font family and style details
- **Zoom Control**: Adjustable preview sizes

## Configuration

Each application maintains its configuration in `~/.local/share/cinnamon-settings-manager/`. Configuration files are automatically created and managed by the applications.

### Common Configuration Options

- **Preview Sizes**: Adjustable thumbnail and preview sizes
- **Custom Directories**: Add additional search paths
- **Cache Settings**: Control caching behavior
- **Interface Preferences**: UI customization options

## Technical Details

### Architecture

The suite is built using:
- **Language**: Perl 5 with modern object-oriented features (Moo)
- **GUI Toolkit**: GTK3 via Perl bindings
- **Configuration**: JSON-based configuration files
- **Caching**: MD5-based cache system for performance
- **Binary Component**: C-based xcursor_extractor for cursor preview

### xcursor_extractor

The `xcursor_extractor` is a custom C utility that:
- Reads X11 cursor files using libXcursor
- Extracts individual cursor frames
- Converts to PNG format using libpng
- Handles pre-multiplied alpha transparency
- Provides metadata about cursor animations

