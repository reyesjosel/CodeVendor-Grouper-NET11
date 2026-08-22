# CodeVendor.Controls.Grouper

A special custom rounding GroupBox control for Windows Forms with advanced painting features.

## Overview

This is a Windows Forms UserControl that provides a highly customizable GroupBox with:
- **Rounded corners** with adjustable radius
- **Gradient backgrounds** with multiple gradient modes
- **Shadow effects** with customizable color and thickness
- **Custom borders** with adjustable thickness and color
- **Image support** in the title bar
- **Custom painting** of the group title background

## .NET 11 Upgrade

This repository contains the upgraded version of the original CodeVendor Grouper control, migrated from .NET Framework to **.NET 11** (preview).

### Upgrade Changes
- **Target Framework**: Upgraded from .NET 7 to .NET 11
- **Windows Forms Designer**: Added modern designer serialization attributes for .NET 9+ compatibility
- **Platform API Support**: Added `[SupportedOSPlatform("windows")]` attribute for proper Windows-only API declarations
- **Build**: Clean build with zero errors and zero warnings

## Original Author & Credits

**Original Author**: Adam Smith  
**Author Email**: ibulwark@hotmail.com  
**Original Website**: http://www.codevendor.com  
**Original Release**: December 17, 2005 (Version 1.0a - Beta)

This code was originally published at CodeVendor.com and is redistributed here with full credit to the original author. The code has been upgraded to modern .NET to demonstrate the migration path from classic .NET Framework to .NET 11.

## Features

### Appearance Properties

- **BackgroundColor** - Main control background color
- **BackgroundGradientColor** - Secondary color for gradient backgrounds
- **BackgroundGradientMode** - Gradient direction (None, Horizontal, Vertical, ForwardDiagonal, BackwardDiagonal)
- **BorderColor** - Control border color
- **BorderThickness** - Border width (1-3)
- **RoundCorners** - Corner radius (1-25)
- **ShadowControl** - Enable/disable shadow effect
- **ShadowColor** - Shadow color
- **ShadowThickness** - Shadow width (1-10)
- **GroupTitle** - Title text displayed in the group bar
- **GroupImage** - 16x16 image for the title bar
- **PaintGroupBox** - Enable custom title background painting
- **CustomGroupBoxColor** - Custom color for title background

## Requirements

- **.NET 11** (preview) or later
- **Windows** operating system (uses GDI+ APIs)
- **Visual Studio 2026** or compatible IDE with Windows Forms Designer support

## Usage

1. Add the `CodeVendor.Controls.dll` reference to your Windows Forms project
2. The Grouper control will appear in the toolbox
3. Drag and drop onto your form
4. Customize appearance using the Properties window

```csharp
using CodeVendor.Controls;

// Create a Grouper control
Grouper grouper = new Grouper();
grouper.GroupTitle = "My Group";
grouper.RoundCorners = 15;
grouper.BorderColor = Color.Blue;
grouper.BackgroundGradientMode = Grouper.GroupBoxGradientMode.Vertical;
grouper.BackgroundColor = Color.LightBlue;
grouper.BackgroundGradientColor = Color.White;
grouper.ShadowControl = true;
```

## Building

```bash
dotnet build CodeVendor.Controls.sln
```

Or open `CodeVendor.Controls.sln` in Visual Studio and build.

## License

Please refer to the original CodeVendor.com website for license information. This repository exists to preserve and modernize this classic Windows Forms control with full attribution to the original author.

## Version History

- **1.0a** (December 17, 2005) - Original beta version by Adam Smith
- **2.0** (2024) - Upgraded to .NET 11, modern Windows Forms designer support

## Acknowledgments

Special thanks to **Adam Smith** and **CodeVendor.com** for creating and sharing this useful Windows Forms control with the community.
