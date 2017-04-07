Docker PHPUnit commands
=======================

Originally forked from https://github.com/m0nah/SimplePHPUnit-for-Sublime-Text


This plugin allows you the run the PHPUnit on a remote server tests using the Sublime Text interface, without having to open and use the command line.

### Available commands:

- `Docker PHPUnit: Run all`
- `Docker PHPUnit: Run unit tests`
- `Docker PHPUnit: Run functional tests`
- `Docker PHPUnit: Run tests in current file`

### Colouring output

![Colouring output](https://raw.githubusercontent.com/aftabnaveed/Sublime-DockerPHPUnit/master/Tests.png)

### Installation:
Use Package Controller or create a the directory `DockerPHPUnit` in your Sublime Text Packages directory, and you're ready to go.

### Configuration:

The server_address configuration is mandatory.

An example for a Symfony2 Vagrant setup looks as follows:

```
{
	"phpunit_path": "/var/www/html/vendor/bin/phpunit", /*phpunit file mounted on remote server*/
    "phpunit_xml_remote_path": "/var/www/html/phpunit.xml",
    "docker_container": "workspace",
    "phpunit_xml_local_path": ""
}
```
* phpunit_path: Path inside docker container
* phpunit_xml_remote_path: Path to phpunit.xml inside docker container
* phpunit_xml_local_path: This is the relative path to the PHPUnit config file (phpunit.xml or phpunit.xml.dist)


### Usage:
Press Cmd + Shift + P for the dropdown command list, search for `Docker PHPUnit: `, and pick your command. Also you can use `Tools/Docker PHPUnit` menu item

### Notes:
- PHPUnit config file needs to been in the root folder of your structure in the sidebar.
- You need insert in Sublime Text user settings `"show_panel_on_build": true` or use `Tools/Build Results/Show Build Results` menu item for view results.
