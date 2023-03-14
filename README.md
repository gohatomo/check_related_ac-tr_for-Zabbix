# check_related_ac-tr for Zabbix

## Description
This is a script that outputs a list of actions associated with the trigger for Zabbix 6.0.
This script is coding by php.

## Require
* Zabbix: 6.0
* OS: RHEL 8
* PHP: 7.2
* Package: php-cli, php-pdo, php-zip, php-json, php-mbstring

## Config Settings
Modify the configuration file (check_related_ac-tr.conf) according to the operating environment.
1. API
* $api_url: Describe the URL of Zabbix frontend URL that executes API. 
* $api_user: Zabbix user that executes API.
* $api_pass: Zabbix user password.

2. Encoding
* $encoding: Character code of output file.(SJIS-win, UTF-8, etc.)

3. Timezone
* $timezone: Execution environment time zone.

4. Directory
* $base_dir: Script expansion directory.
* $export_dir: Output directory of export file.
* $tmp_dir: Temporary directory for script processing.

## Usage
1. List the target hostids in hostid_list.csv.
```
[Example]
10084
10051
```
2. Modify the config file according to the environment.See Config Settings.
3. Run the php script(check_related_ac-tr).
```
./check_related_ac-tr
 or
/full_path/check_related_ac-tr
```
4. Download export file and check.
