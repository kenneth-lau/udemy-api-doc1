# Exercise 4

## Part 1

XML Data

```xml
<recordTV>
 <date>2015-06-01</date>
 <time format="24">18:00</time>
 <duration>1.5</duration>
 <channel>54</channel>
</recordTV>
```

| Element | Description | Type | Required | Notes |
| ---- | --- | ---- | ---- | ----- | --- |
| recordTV | Date of when the program should be recorded | data object | Required ||
| `date` | Date of the program | string | Optional | YYYY-MM-DD. Default is today's date |
| `time` | Time the program begins | string | Required | Attributes: * format has values "24" or "12" for 24 or 12 hour formats. |
| `duration` | Length of the program in hours | number | Required | |
| `channel`| Channel to record | number | Required | &nbsp; |

## Part 2

XML Data

```xml
<recordTV>
 <when date="2015-06-01" time="18:00" format="24"/>
 <duration hours="1.5"/>
 <station channel="54"/>
</recordTV>
```

| Element | Attribute | Description | Type | Required | Notes |
| ---- | --- | --- | ---- | ---- | ----- | --- |
| recordTV || Date of when the program should be recorded | data object | Required ||
| `when` || Date and time of the program | string | Optional ||
|| date | Date of the program | string | Optional | YYYY-MM-DD. Default is today's date |
|| time | Time the program begins | string | Required ||
|| format | Format of the time | string | Required | "12" or "24" |
| `duration` | hours | Length of the program | number | Required | |
| `station` | channel| Channel to record | number | Required |||

## Part 3

XML Data

```xml
<dailyData>
 <date>2015-06-01</date>
 <hourlyData>
 <time>10:00</time>
 <device>
 <id>34</id>
 <temperature>70</temperature>
 <humidity>11</humidity>
 </device>
 <device>
 <id>35</id>
 <temperature>72</temperature>
 <humidity>12</humidity>
 </device>
 ...
 </hourlyData>
 <hourlyData>
 <time>11:00</time>
 <device>
 <id>34</id>
 <temperature>71</temperature>
 <humidity>10</humidity>
 </device>
 ...
 </hourlyData>
 ...
</dailyData>
```

| Element | Description | Type |
| ---- | --- | ---- |
| dailyData | Temperature and humidity data for one day | dailyData element |

dailyData: Represents temperature and humidity for one day

| Element | Description | Type | Notes |
| ---- | --- | ---- | --- |
| date | Date of data | string | YYYY-MM-DD |
| hourlyData | Temperature and humidity data for one hour | hourlyData element | &nbsp; |

hourlyData: Represents temperature and humidity for one hour

| Element | Description | Type | Notes |
| ---- | --- | ---- | --- |
| time | Local time that the temperature was taken | string | HH:MM |
| device | One or more device objects | device element | &nbsp;|

device: Contains temperature and humidity data from device

| Element | Description | Type |
| ---- | --- | ---- |
| id | The device's ID | number |
| temperature | Temperature in Fahrenheit | number |
| humidity | Humidity in percentage | number |
