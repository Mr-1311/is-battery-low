# README

Simple battery checker and notification sender script with very little dependencies.

## Installation

Clone this project and put the script wherever you want then call the script at any intervals you want. You can do that easily with cron.

Sample installation with fcron.

```bash
git clone https://github.com/metinUr/is-battery-low.git
mv is-battery-low/is-battery-low /opt
rm -rf is-battery-low #for cleaning
fcrontab -e
*/1 * * * * env DISPLAY=:0 /opt/is-battery-low #save and exit
```

If your fcrontab works properly this will call the script every minute. You can use any other cron alternatives or systemd/Timers setup.

### note

Make sure `acpi -b` and  `notify-send` commands working before using the script.