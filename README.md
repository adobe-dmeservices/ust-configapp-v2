# Adobe User Sync Tool Configuration Wizard
This is User Sync tool configuration wizard. It helps configure the User Sync tool with User Management API (Adobe.io), Enterprise Directory (LDAP) and sync settings.

The User Sync Tool is a command-line tool that sync users and group information from an organization's Enterprise directory system to the Adobe Admin Console. The key goals of the User Sync Tool are to streamline the process of named user deployment and automate user management for all Enterprise customers.

Overview: https://spark.adobe.com/page/E3hSsLq3G1iVz/

User Sync Tool: https://github.com/adobe-apiplatform/user-sync.py

<img src="https://user-images.githubusercontent.com/63472846/123971247-7ca20900-d97f-11eb-8c04-9911b6f3b6fa.PNG" height = "250" width = "300"> <img src="https://user-images.githubusercontent.com/63472846/123971258-80359000-d97f-11eb-8df2-8acbea12a68d.PNG" height = "250" width = "300">
<img src="https://user-images.githubusercontent.com/63472846/123971653-db678280-d97f-11eb-8c9b-419d36e187ae.PNG" height = "250" width = "300">


## Supported Features
The wizard supports:

* Configuration of Adobe User Management API (UMAPI) token
* Configuration of Enterprise Directory information (including username format login settings)
* Configuration new user identity, group mappings and logging information
* Dropdown selection for Enterprise Directory specific group filter (AD/OpenLDAP)
* Exclude adobe-side identity types/groups from sync
* Enable reading nested group information
* Enable secure password storage for ldap password

## New Features
* Updated user interface using React Spectrum components
* Main config file is now autoloaded on startup
* Support for configuration of Additional Group Options (Dynamic Grouping)
* Adobe limit now accepts percentages in addition to integers
* Supports configuration of old UMAPI connector files (api_key, tech_acct)

You can still add additional keys/edit current key values manually in the configuration files.

Please note, any yml comments and keys order will not be saved during round-trip save, however, the wizard creates a initial backup of config before it updates the configurations.

## Installation
Setup developement enviornment:

    npm install --global yarn

    yarn install
Run in developement-mode:

    yarn start
Build application for production:

    yarn dist
    .\dist\ustapp 0.1.0.exe
## Dev Notes
Developement require NodeJS. Current release is tested and working for Windows. Other operating systems support will be added soon.
