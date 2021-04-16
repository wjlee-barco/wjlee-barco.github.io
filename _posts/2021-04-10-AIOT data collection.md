---
title:  "AIOT data collection"
metadate: "2021-04-10 21:40:10"
categories: ["BigData", "IOT"]
image: "/assets/images/11.04.2021_19.07.45_REC.png"
visit:
tags: [featured]
featured: true
author: wjlee
---

## AIOT data collection

AIOT is the combination of AI and IOT. Three major steps for AIOT: **data**, **intelligence**, **actions** mean **data collection**, **smart data intelligence**, then **actions** accordingly. For **data collection**, **IOT devices events** and **user behaviorial events** might be collected via several approaches. Here we focus on the approaches of data collections and aggreagration. 

### via InfluxDB

**Data collection**, or IOT devices and user behaviorial events collection, can be formulated as **time series** or **events** and and stored in **times series database** ([TSDB](https://www.influxdata.com/time-series-database/))

a time series or event can be in the form of

```
measurement tag fields timestamp
```
andd an example as
```
temperature,device=device1,buidling=b1 internal=80,external=18 1443782126
```
[![]({{site.url}}{{site.baseurl}}/assets/images/13.04.2021_10.35.03_REC.png)]()

[influxDB](https://www.influxdata.com/) is the top solution for ([TSDB](https://www.influxdata.com/time-series-database/)) as collectors, aggregators and visualizer and its block digram as below.

[![](https://www.influxdata.com/wp-content/uploads/APM-Diagram-1.png)](https://www.influxdata.com/time-series-platform/telegraf/)


## References
* [How To Install InfluxDB Telegraf and Grafana on Docker](https://devconnected.com/how-to-install-influxdb-telegraf-and-grafana-on-docker/)
* [Nextcloud to influxDB (Grafana for display) with telegraf](https://blog.lbdg.me/nextcloud-influxdb-telegraf-grafana/)