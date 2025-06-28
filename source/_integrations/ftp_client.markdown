---
title: FTP Client
description: Instructions on how to use  FTP Client in Home Assistant.
ha_category:
  - Backup
ha_iot_class: Local Polling
ha_release: '2025.8'
ha_config_flow: true
ha_domain: ftp_client
ha_codeowners:
  - '@cyr-ius'
ha_integration_type: service
ha_quality_scale: gold
related:
  - docs: /common-tasks/general/#backups
    title: Creating backups in Home Assistant
---

The **FTP Client** {% term integration %} allows you to perform Home Assistant backups to a server via <abbr title="file transfer protocol">FTP</abbr>. Once this integration is configured, your server contains a new folder called backup where all backups will be stored. If you delete the folder, it will be automatically recreated as long as the {% term integration %} is enabled.

{% include integrations/config_flow.md %}

## Known limitations

- The integration can only access files that it creates in the Home Assistant folder. It cannot access or modify any other files.

## Removing the integration

{% include integrations/remove_device_service.md %}

If you remove the integration, the Home Assistant folder on your server is not automatically deleted. You must delete it manually.

