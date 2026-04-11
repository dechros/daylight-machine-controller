# daylight-machine-controller

WPF desktop application for remotely controlling a machine over TCP. Shows a splash and license window on startup and a main window with hamburger navigation between Home, Control, Connection, Favorites, Details, Update and Settings pages.

## Platform

- Windows, .NET Framework 4.7.2, WPF
- NuGet packages: `DeviceId` 6.0.0, `Extended.Wpf.Toolkit` 4.1.0

## Layout

```
App.xaml / App.xaml.cs         application entry (Main)
View/
  SplashWindow.xaml            startup splash
  LicenseWindow.xaml           license entry
  MainWindow.xaml              main window with navigation
  MainWindowPages/             Home, Control, Connection, Favorites,
                               Details, Update, Settings pages
Utility/
  FileHandler.cs               license file read/write
  LicenseHandler.cs            license encode/decode against machine id
  RandomNumberGenerator.cs
  StringHelper.cs
Properties/                    AssemblyInfo, Settings, Resources
Resources/                     images and assets
DayLightMachineController.sln
DayLightMachineController.csproj
```

## Build

Open `DayLightMachineController.sln` in Visual Studio (with .NET Framework 4.7.2 targeting pack installed) and build, or from the command line:

```
msbuild DayLightMachineController.sln /p:Configuration=Release
```

NuGet restore is required before the first build.
