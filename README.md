
# About

Zabbix Server Action to Slack.com

![Zabbix Server to Slack.com](https://raw.githubusercontent.com/bageljp/zabbix-slack/master/img/zabbix_chart.png "Zabbix Server to Slack.com")

# Installation

### Slack.com settings

[Slak.com Incoming Webhooks](https://api.slack.com/incoming-webhooks)

### Script settings in Zabbix Server

```
cd /usr/lib/zabbix/alertscripts    # AlertScriptsPath
wget https://raw.githubusercontent.com/hdkiller/zabbix-slack/master/slack.sh
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
    <td><tt>zabbix_baseurl</tt></td>
    <td>full URL of zabbix mainpage</td>
  </tr>
  <tr>
    <td><tt>zabbix_username</tt></td>
    <td>zabbix username to grab the chart</td>
  </tr>
  <tr>
    <td><tt>zabbix_password</tt></td>
    <td>zabbix password</td>
  </tr>
  <tr>
    <td><tt>chart_period</tt></td>
    <td>how many seconds to be shown on the chart</td>
  </tr>
  <tr>
    <td><tt>chart_width</tt></td>
    <td>width of the chart</td>
  </tr>
  <tr>
    <td><tt>chart_height</tt></td>
    <td>height of the chart</td>
  </tr>
  <tr>
    <td><tt>chart_baseurl</tt></td>
    <td>where the charts will be hosted</td>
  </tr>
  <tr>
    <td><tt>chart_basedir</tt></td>
    <td>charts will be downloaded there</td>
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
ITEM_ID: {ITEM.ID1}
ITEM_NAME: {ITEM.NAME1}
ITEM_KEY: {ITEM.KEY1}
ITEM_VALUE: {ITEM.VALUE1}
EVENT_ID: {EVENT.ID}
TRIGGER_URL: {TRIGGER.URL}
```

