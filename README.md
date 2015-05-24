
# Install

### Zabbix Server

```
cd /usr/lib/zabbix/alertscripts
wget https://raw.githubusercontent.com/bageljp/zabbix-slack/master/slack.sh
chmod a+x slack.sh
vi slack.sh
```

<table>
  <tr>
    <td><tt>slack_url</tt></td>
	<td>slack integration url.</td>
  </tr>
  <tr>
    <td><tt>slack_username</tt></td>
    <td>slack username.</td>
  </tr>
  <tr>
    <td><tt>emoji</tt></td>
    <td>slack emoji.</td>
  </tr>
</table>

### Zabbix Server settings

* Administration MediaType
<table>
  <tr>
    <td><tt>Name</tt></td>
	<td>Slack</td>
  </tr>
  <tr>
    <td><tt>Type</tt></td>
    <td>script</td>
  </tr>
  <tr>
    <td><tt>Script name</tt></td>
    <td>slack.sh</td>
  </tr>
</table>

* Action settings ``default message``
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

