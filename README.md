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

<img width="3840" height="2160" alt="Screenshot from 2025-10-15-19-39-53" src="https://github.com/user-attachments/assets/e6608a98-92c2-4e42-a2d3-95aff541ae36" />


## Features


- **Background Manager** - Wallpaper management with thumbnail previews

<img width="3840" height="2160" alt="Screenshot from 2025-10-15-19-44-54" src="https://github.com/user-attachments/assets/de4016d1-9f4a-4870-aa41-ce75e2320324" />

- **Font Manager** - System font management with live preview capabilities

<img width="3840" height="2160" alt="Screenshot from 2025-10-15-19-40-59" src="https://github.com/user-attachments/assets/055b4d59-9c7a-417c-8d62-84736d1d126b" />

- **Cursor Theme Manager** - Advanced cursor theme management with extracted cursor previews

<img width="3840" height="2160" alt="Screenshot from 2025-10-15-19-41-26" src="https://github.com/user-attachments/assets/59409777-160b-4b20-bd36-b22e1d7f2f22" />

- **Application Theme Manager** - Preview and apply GTK themes for applications

<img width="3840" height="2160" alt="Screenshot from 2025-10-15-19-42-24" src="https://github.com/user-attachments/assets/78dbc862-1ae3-4557-8d5f-a3b81b18d139" />

- **Icon Theme Manager** - Browse and switch between icon themes with comprehensive previews

<img width="3840" height="2160" alt="Screenshot from 2025-10-15-19-42-44" src="https://github.com/user-attachments/assets/336f6251-cd16-4442-ad62-8a26dd11f1e5" />

- **Cinnamon Theme Manager** - Preview and apply Cinnamon desktop themes

<img width="3840" height="2160" alt="Screenshot from 2025-10-15-19-43-02" src="https://github.com/user-attachments/assets/a4c289a3-295f-44ad-871d-a23217f2d606" />


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

