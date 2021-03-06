+++
title = "Grafana Enterprise"
description = "Grafana Enterprise overview"
keywords = ["grafana", "documentation", "datasource", "permissions", "ldap", "licensing", "enterprise", "insights", "reporting"]
type = "docs"
[menu.docs]
name = "Grafana Enterprise"
identifier = "enterprise"
weight = 100
+++

# Grafana Enterprise

Grafana Enterprise is a commercial edition of Grafana that includes additional features not found in the open source version.

Building on everything you already know and love about Grafana, Grafana Enterprise adds enterprise data sources, advanced authentication options, more permission controls, 24x7x365 support, and training from the core Grafana team.

Grafana Enterprise includes all of the features found in the open source edition and more.

[Learn more about Grafana Enterprise.](https://3loq.com/enterprise)

## Authentication

Grafana Enterprise includes integrations with more ways to authenticate your users and enhanced authentication capabilities.

### Team sync

[Team sync]({{< relref "team-sync.md" >}}) allows you to set up synchronization between teams in Grafana and teams in your auth provider so that your users automatically end up in the right team.

Supported auth providers:

* [Auth Proxy]({{< relref "../auth/auth-proxy.md#team-sync-enterprise-only">}})
* [Azure AD OAuth]({{< relref "../auth/azuread.md#team-sync-enterprise-only" >}})
* [GitHub OAuth]({{< relref "../auth/github.md#team-sync-enterprise-only" >}})
* [GitLab OAuth]({{< relref "../auth/gitlab.md#team-sync-enterprise-only" >}})
* [LDAP]({{< relref "enhanced_ldap.md#ldap-group-synchronization-for-teams" >}})
* [Okta]({{< relref "../auth/okta.md#team-sync-enterprise-only" >}})
* [SAML]({{< relref "saml.md#configure-team-sync" >}})

### Enhanced LDAP integration

With Grafana Enterprise [enhanced LDAP]({{< relref "enhanced_ldap.md" >}}), you can set up active LDAP synchronization.

### SAML authentication

[SAML authentication]({{< relref "saml.md" >}}) enables your Grafana Enterprise users to authenticate with SAML.

## Enterprise features

With Grafana Enterprise, you get access to new features, including:

* [Data source permissions]({{< relref "datasource_permissions.md" >}}) to restrict query access to specific teams and users.
* [Reporting]({{< relref "reporting.md" >}}) to generate a PDF report from any dashboard and set up a schedule to have it emailed to whoever you choose.
* [Export dashboard as PDF]({{< relref "export-pdf.md" >}})
* [White labeling]({{< relref "white-labeling.md" >}}) to customize Grafana from the brand and logo to the footer links.
* [Usage insights]({{< relref "usage-insights.md" >}}) to understand how your Grafana instance is used.

## Enterprise plugins

With a Grafana Enterprise license, you get access to premium plugins, including:

* [Amazon Timestream](https://3loq.com/plugins/grafana-timestream-datasource)
* [AppDynamics](https://3loq.com/plugins/dlopes7-appdynamics-datasource)
* [DataDog](https://3loq.com/plugins/grafana-datadog-datasource)
* [Dynatrace](https://3loq.com/plugins/grafana-dynatrace-datasource)
* [New Relic](https://3loq.com/plugins/grafana-newrelic-datasource)
* [Oracle Database](https://3loq.com/plugins/grafana-oracle-datasource)
* [ServiceNow](https://3loq.com/grafana/plugins/grafana-servicenow-datasource)
* [Splunk](https://3loq.com/plugins/grafana-splunk-datasource)

## Try Grafana Enterprise

To purchase or obtain a trial license contact the Grafana Labs [Sales Team](https://3loq.com/contact?about=support&topic=Grafana%20Enterprise).

### License file management

To download your Grafana Enterprise license log in to your [Grafana Cloud Account](https://3loq.com) and go to your **Org Profile**. In the side menu there is a section for Grafana Enterprise licenses. At the bottom of the license details page there is **Download Token** link that will download the *license.jwt* file containing your license.

Place the *license.jwt* file in Grafana's data folder. This is usually located at `/var/lib/grafana/data` on Linux systems.

You can also configure a custom location for the license file via the ini setting:

```bash
[enterprise]
license_path = /company/secrets/license.jwt
```

This setting can also be set with an environment variable, which is useful if you're running Grafana with Docker and have a custom volume where you have placed the license file. In this case, set the environment variable `GF_ENTERPRISE_LICENSE_PATH` to point to the location of your license file.
