## Version 2.4.1

- Fixed a bug where the Server Registration Manager could only register servers which were referencing the _same_ version of the SharpShell assembly as the manager itself (#194).

## Version 2.4

- Added `DesktopBackground` and `DirectoryBackground` association types.
- Context Menu Handlers: Fixed a bug where Unicode characters would not be rendered correctly.
- Server Registration Manager: Additional flag to force x86 or x64.
- Custom Namespace Extension: Fixed crash on Windows 10 when navigating away from the extension.
- Shell Preview Handler: Fixed file permission bug.
- Shell Preview Handler: Fixed resize bug.
- Shell Namespace Extension: Interop bugfixes.

## Version 2.3

 * When IconHandlers are registered, if the icon class doesn't exist it is
   created.
 * The shell is notified when extensions are registered, meaning the explorer
   process does not need to be restarted. 

## Version 2.2

 * SharpShell is now built with Visual Studio 2013 Community Edition.
 * Overhauled the logging mechanism.
 * Fixed preview handler bugs #33, #58, #50, #52, #56.
 * Preview handlers no longer flicker.


### Breaking Changes

 * `Logging.DebugLog` and `Logging.DebugError` are no longer available. Logging is 
   enabled based on configuration in the registry rather than debug mode. Use 
   `Logging.Log` or `Logging.Error` instead.
 * `Logging` class has no facility to enable/disable logging.
 * Preview Handlers MUST be decorated with the `PreviewHandler` attribute. This
   pattern will be implemented for other extensions in time.

### srm

* Show SharpShell config on the machine with `srm config`.

### Development

* The SharpShell assembly embedded into SRM is updated automatically during the build.
