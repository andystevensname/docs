---
title: "Horizontally Scaling High-Traffic Applications with Observability and Monitoring"
description: "Horizontally scale infrastructure to meet demands of a growing application through HAProxy, and monitor with Prometheus and Grafana."
license: "[CC BY-ND 4.0](http://creativecommons.org/licenses/by-nd/4.0/)"
tab_group_main:
    is_root: true
    title: Overview
    weight: 10
---

## Abstract
This reference architecture demonstrates how developers can horizontally scale their infrastructure using Terraform and Ansible when certain application performance thresholds are met. They can also observe detailed real-time metrics through the Grafana dashboard from Prometheus.

In this example, the main bottleneck is the */notifications* endpoint of a mobile app. When the client pushes notifications to the app, many users check the notifications on their devices, which call back to the server. This creates an overwhelming number of requests that can crash the server. This proposed architecture solves several issues by:

- Allowing the application to grow as the target audience increases by having multiple HAProxy nodes
- Establishing monitoring via Prometheus and Grafana
- Separating the main app and the notification callback to the app
- Scaling the app’s notifications section via configuration management tools
- Implementing network segmentation using Linode VLANs
- Adding resiliency to the database for uptime and reliability

## Technologies Used
- TerraForm
- Ansible
- Prometheus
- Grafana
- HAProxy

## Business Benefits
- Better user experience through scalability
- Proactive maintenance through observability and monitoring
- A high degree of reliability with no single point of failure
- A portable workload that can be deployed anywhere

## Market Applicability
- Small Business
- Mid-Market
- Enterprise
