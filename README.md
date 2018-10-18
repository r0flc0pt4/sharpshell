# SharpShell

[![Build status](https://ci.appveyor.com/api/projects/status/ebvrjdsjm8ne7sdw/branch/master?svg=true)](https://ci.appveyor.com/project/dwmkerr/sharpshell/branch/master) [![NuGet](https://img.shields.io/nuget/dt/SharpShell.svg)](https://www.nuget.org/packages/SharpShell/) [![GuardRails badge](https://badges.production.guardrails.io/dwmkerr/sharpshell.svg)](https://www.guardrails.io)

SharpShell makes it easy to create Windows Shell Extensions using the .NET Framework.

<!-- vim-markdown-toc GFM -->

* [Official NuGet Packages](#official-nuget-packages)
* [Documentation](#documentation)
* [Deploying SharpShell Servers](#deploying-sharpshell-servers)
* [Supported Shell Extensions](#supported-shell-extensions)
    * [Shell Context Menus](#shell-context-menus)
    * [Icon Handlers](#icon-handlers)
    * [Info Tip Handlers](#info-tip-handlers)
    * [Drop Handlers](#drop-handlers)
    * [Preview Handlers](#preview-handlers)
    * [Icon Overlay Handlers](#icon-overlay-handlers)
    * [Thumbnail Handlers](#thumbnail-handlers)
    * [Property Sheet Extensions](#property-sheet-extensions)
    * [DeskBand Extensions](#deskband-extensions)
* [Useful Resources](#useful-resources)
* [License](#license)
* [Testimonials](#testimonials)
* [Projects that use SharpShell](#projects-that-use-sharpshell)
* [Developer Guide](#developer-guide)
    * [Enabling Logging](#enabling-logging)
    * [CI/CD](#cicd)
    * [Creating a Release](#creating-a-release)
* [Thanks](#thanks)

<!-- vim-markdown-toc -->

## Official NuGet Packages

- [![SharpShell Nuget Package](https://img.shields.io/nuget/v/SharpShell.svg)](https://www.nuget.org/packages/SharpShell)
- [![SharpShellTools NuGet Package](https://img.shields.io/nuget/v/SharpShellTools.svg)](https://www.nuget.org/packages/SharpShellTools)

## Documentation

Documentation is in the process of being moved to:

[`./docs`](./docs)

Please open an issue if there is missing documentation and I will try to prioritise it!

## Deploying SharpShell Servers

There is an article on the CodeProject that describes in detail how you can use the Server Registration Manager tool 
to deploy SharpShell servers:

[Deploying SharpShell Servers](http://www.codeproject.com/Articles/653780/NET-Shell-Extensions-Deploying-SharpShell-Servers)

## Supported Shell Extensions

The following extensions are supported by SharpShell.

### Shell Context Menus

Shell Context Menus allow the context menus used in Windows Explorer to be customised.

![Shell Context Menu Screenshot](https://raw.github.com/dwmkerr/sharpshell/master/Assets/Screenshots/contextmenu.png)

[Step by Step Tutorial on the CodeProject](http://www.codeproject.com/Articles/512956/NET-Shell-Extensions-Shell-Context-Menus).

### Icon Handlers

Shell Icon Handlers are DLLs that are registered in the system to customise the appearance of icons.

![Shell Icon Handler Screenshot](https://raw.github.com/dwmkerr/sharpshell/master/Assets/Screenshots/iconhandler.png)

[Step by Step Tutorial on the CodeProject](http://www.codeproject.com/Articles/522665/NET-Shell-Extensions-Shell-Icon-Handlers).

### Info Tip Handlers

Shell Info Tip Handlers are DLLs that are registered in the system to customise tooltips for items in the shell.

![Shell Info Tip Handler Screenshot](https://raw.github.com/dwmkerr/sharpshell/master/Assets/Screenshots/infotiphandler.png)

[Step by Step Tutorial on the CodeProject](http://www.codeproject.com/Articles/527058/NET-Shell-Extensions-Shell-Info-Tip-Handlers).

### Drop Handlers

Shell Drop  Handlers are DLLs that are registered in the system to extend the drag and drop functionality in the Shell. 

![Shell Drop Handler Screenshot](https://raw.github.com/dwmkerr/sharpshell/master/Assets/Screenshots/dorphandler.png)

[Step by Step Tutorial on the CodeProject](http://www.codeproject.com/Articles/529515/NET-Shell-Extensions-Shell-Drop-Handlers).

### Preview Handlers

Shell PreviewHandlers are dlls that can be registered in the system to allow you to create visually rich previews for items that are displayed directly in Windows Explorer. 

![Shell Preview Handler Screenshot](https://raw.github.com/dwmkerr/sharpshell/master/Assets/Screenshots/previewhandler.png)

[Step by Step Tutorial on the CodeProject](http://www.codeproject.com/Articles/533948/NET-Shell-Extensions-Shell-Preview-Handlers).

### Icon Overlay Handlers

Shell Icon Overlay Handlers can be really useful. They let you display an icon overlay over shell objects to provide extra information. Programs like Dropbox use these overlays to show whether files are synchronised or not.

![Shell Icon Overlay Handler Screenshot](https://raw.github.com/dwmkerr/sharpshell/master/Assets/Screenshots/overlayhandler.png)

[Step by Step Tutorial on the CodeProject](http://www.codeproject.com/Articles/545781/NET-Shell-Extensions-Shell-Icon-Overlay-Handlers).

### Thumbnail Handlers

Shell Thumbnail Handlers (or as they're sometimes known, Shell Thumbnail Providers) are COM servers that you can write to customise the appearance of the thumbnail icons in the Windows Shell. 

![Shell Thumbnail Handler Screenshot](https://raw.github.com/dwmkerr/sharpshell/master/Assets/Screenshots/thumbnailhandler.jpg)

[Step by Step Tutorial on the CodeProject](http://www.codeproject.com/Articles/563114/NET-Shell-Extensions-Shell-Thumbnail-Handlers).

### Property Sheet Extensions

These are extensions that add extra pages to the property sheets shown for shell items such as files, network shares, folders and so on.
 
![Shell Thumbnail Handler Screenshot](https://raw.github.com/dwmkerr/sharpshell/master/Assets/Screenshots/propertysheetextensions.png)

[Step by Step Tutorial on the CodeProject](http://www.codeproject.com/Articles/573392/NET-Shell-Extensions-Shell-Property-Sheets).

### DeskBand Extensions

Useful notes:

* Always include a DisplayName for a deskband extension, otherwise it won't register.
* The UserControl for deskband should specify a minimum size and maximum size - if they're
  not specified the actual size will be used.

## Useful Resources

Below are some resources I've found useful during SharpShell development. Please get in touch if you have suggestions
for more, or just make a pull request with changes to this file.

Namespace Extensions
* [Create Namespace Extensions for Windows Explorer with the .NET Framework](http://msdn.microsoft.com/en-us/magazine/cc188741.aspx)
* [Virtual Junction Points](http://msdn.microsoft.com/en-us/library/windows/desktop/cc144096.aspx)

Desk Bands
* [Shell Extensibility - Explorer Desk Band, Tray Notification Icon et al.](http://www.codeproject.com/Articles/39189/Shell-Extensibility-Explorer-Desk-Band-Tray-Notifi)

## License

SharpShell is licensed under the MIT License - the details are at [LICENSE.md](https://raw.github.com/dwmkerr/sharpshell/master/LICENSE.md)

## Testimonials

If you've used SharpShell and would like to add a testimonial, just send me a message!

> CmisSync, our Dropbox-like client for Enterprise Content Management servers, just switched to SharpShell, 
> and we are extremely pleased with this library. Our previous custom-built Windows Explorer integration 
> was buggy, unreliable and hard to maintain, and SharpShell is really rock-solid in comparison. The best 
> part: It only took 2 days to integrate SharpShell into our software, testing and installer included. 
> Thanks SharpShell!

Nicolas Raoul - [CmisSync.com](http://CmisSync.com)

## Projects that use SharpShell

Send me a message to add a project to this list:

 - [Trello Context Menu](https://github.com/GeorgeHahn/TrelloContextMenu)
 - [REAL Shuffle Player 2.0](http://download.cnet.com/Real-Shuffle-Player/3000-2139_4-75992715.html)
 - [The CmisSync context menu](http://aegif-labo.blogspot.jp/2014/08/the-cmissync-context-menu-check-out.html)
 - [TenClips](http://www.paludour.net/TenClips.html)
 - [Checksum Inspector](https://github.com/XxDeadLiiNexX/Checksum-Inspector/#checksum-inspector)
 - [VSIX PowerToys](https://github.com/hmemcpy/VSIXPowerToys)
 - [FileSystemScanner](https://github.com/sensboston/FileSystemScanner)
 - [Windows Explorer Thumbnails for MagicaVoxel .vox files](https://github.com/Arlorean/Voxels)
 - [Markdown Preview](https://github.com/Atrejoe/MarkdownPreview)

## Developer Guide

### Enabling Logging

A detailed guide explaining how to configure and use logging for SharpShell is at:

[./docs/logging/logging.md](./docs/logging/logging.md)

### CI/CD

CI/CD is currently handled by AppVeyor. AppVeyor will:

1. Build the project
2. Run the tests
3. Create the core SharpShell Nuget Package
4. Publish the package to nuget.org if a version tag is pushed
5. Create a GitHub release with the package if a version tag is pushed

Some work is still needed on the CI/CD side:

- [ ] AppVeyor config should be in the yaml file, not the web UI.
- [ ] Look at handing the changelog more effectively, with somelike like the node release tool used in my other projects.
- [ ] Look into automatic notifications for package publication.
- [ ] Deploy SRM as a NuGet package.
- [ ] There is stale release code in the [`Release`](/Release) folder.

### Creating a Release

To create a release:

1. Update the version number in [`SharedAssemblyInfo.cs`](./SharpShell/SharedAssemblyInfo.cs)
2. Update the [`CHANGELOG.md`](./CHANGELOG.md)
3. Create a new version tag, then push

The AppVeyor build will build a new NuGet package and as long as a new semver tag is pushed.

## Thanks

Many thanks to [JetBrains](https://www.jetbrains.com/) for providing an Open Source License for their products!

![JetBrains](./docs/thanks/jetbrains.png)
