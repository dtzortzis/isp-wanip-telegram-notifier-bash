# ISP WAN IP - Telegram Notifier | Bash Script Version
Sends a [Telegram](https://telegram.org/) notification message when your WAN IP address changes.

Uses [ipconfig.io](http://ipconfig.io/) to detect if you WAN IP address changed.

Scripts need to scheduling a new crontab job for every 15 minutes, other wise script cannot check if the WAN IP Address has changed.

## Telegram Guides
* For information how to obtain Telegram BOT API Token check the following [guide](https://core.telegram.org/bots).
* For information about Telegram BOT API usage and configuration check the following [guide](https://core.telegram.org/bots/api).
* For information how to obtain Telegram ChatID check the following [guide](https://docs.influxdata.com/kapacitor/v1.6/event_handlers/telegram/).

## Usage
GIT clone repository
```sh
git clone https://github.com/dtzortzis/isp-wanip-telegram-notifier-bash.git
```
Mark the file script as executable
```sh
chmod +x CheckWANIP.sh
```
Create a custom cron job using your Shell user
```
crontab -e
```
Paste the following command and change the **path_to_script** with the actually location of script file
```
*/15 * * * * /path_to_script/CheckWANIP.sh >/dev/null 2>&1
```

## License
MIT