
# NowGUI for NowDeploy

The NowGUI project is meant to sit on with the AppBuild and CatalogMgr binaries for those using NowDeploy.  It's purpose is to give a graphical user interface to these applications.

![NowGUI Screen Shot](https://raw.githubusercontent.com/NowDeploy/NowGUI/master/NowDeploy.png)

## Setup

1) Download either the binary (NowGUI.exe) or the PowerShell script (NowGUI.ps1) into the same folder that you keep AppBuild.exe and CatalogMgr.exe.
1) Add or edit any settings that were pulled from the Windows registry under *Configuration* and then click *Save Changes*.  You can elect to save your configuration to either HKLM or HKCU.
1) If you already have a catalog.xml file, point to it where prompted.  Your existing catalog settings will be shown.  If you do not already have an XML, enter the path where you would like one to be saved.
1) Click *Download/Update Catalog* to sync with the NowDeploy cloud server.

## Usage

Once setup, you can manipulate your catalog.xml within the GUI and then click "Update Catalog XML".  Once you've made all of your changes and you're ready to import your application(s) into your Configuration Manager environment, click *Load into ConfigMgr*.

## More Information
For more information on how NowDeploy works and what each specific setting means, please visit the [NowDeploy Documentation](https://docs.nowdeploy.com).

## GUI Sections

### Configuration
This is where you'll configure NowDeploy.  These settings use the save registry keys that are used by NowDeploy's AppBuild and CatalogMgr binaries.

* License Key: Enter your NowDeploy license key.
* SCCM Server: Enter the FQDN to your SCCM Server.
* Site Code: Enter the three character site code of your SCCM environment.
* Package Source Directory: This is the UNC path where your packages will be stored.
* Log File Name: The full path to a log file that AppBuild should use.
* Catalog File: The XML file that will store your catalog settings.

### Catalog Application List

This will list all applications within your catalog XML file.  You can update the path (where the applications are stored within SCCM), as well as determine if it should be excluded or not, and if it should supersede previous versions that are already in your SCCM environment.

### Catalog Action List

The AppBuild application allows for a script to run once the import of applications is complete.  For more information, see [this post](https://support.nowdeploy.com/threads/release-notes-for-beta-builds.14/) until the documentation is complete.

## Contributing
If you'd like to contribute to the NowGUI project, pull requests are welcome.  The [NowGUI.ps1](https://github.com/NowDeploy/NowGUI/blob/master/NowGUI.ps1 "NowGUI.ps1") file should be considered read-only.  All changes should be made within the sources folder.