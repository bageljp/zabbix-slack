
# About

Zabbix Server Action to Slack.com

![Zabbix Server to Slack.com](https://raw.githubusercontent.com/bageljp/zabbix-slack/master/img/zabbix_slack.png "Zabbix Server to Slack.com")

# Installation

### Slack.com settings

[Slak.com Incoming Webhooks](https://api.slack.com/incoming-webhooks)

### Script settings in Zabbix Server

```
cd /usr/lib/zabbix/alertscripts    # AlertScriptsPath
wget https://raw.githubusercontent.com/bageljp/zabbix-slack/master/slack.sh
chmod a+x slack.sh
vi slack.sh
```

<table>
  <tr>
    <td><tt>slack_url</tt></td>
	<td>slack integration url. (ex. https://hooks.slack.com/services/XXX/XXXX/XXXXX)</td>
  </tr>
  <tr>
    <td><tt>slack_username</tt></td>
    <td>slack post username.</td>
  </tr>
  <tr>
    <td><tt>emoji</tt></td>
    <td>slack emoji.</td>
  </tr>
</table>

### Zabbix Server Web Interface settings

* Administration MediaType

![Zabbix Server MediaType settings](https://raw.githubusercontent.com/bageljp/zabbix-slack/master/img/zabbix_mediatype.png "Zabbix Server MediaType settings.")

* Action settings ``default message``

![Zabbix Server Action settings](https://raw.githubusercontent.com/bageljp/zabbix-slack/master/img/zabbix_action.png "Zabbix Server Action settings.")

* copy and paste.
```
HOST: {HOST.NAME}
TRIGGER_NAME: {TRIGGER.NAME}
TRIGGER_STATUS: {TRIGGER.STATUS}
TRIGGER_SEVERITY: {TRIGGER.SEVERITY}
DATETIME: {DATE} / {TIME}
ITEM_NAME: {ITEM.NAME1}
ITEM_KEY: {ITEM.KEY1}
ITEM_VALUE: {ITEM.VALUE1}
EVENT_ID: {EVENT.ID}
TRIGGER_URL: {TRIGGER.URL}
```

