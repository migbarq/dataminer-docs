---
uid: Discovery
---

# Discovery

On the *Discovery* subtab of the *Admin* tab, you can verify and configure the discovery profiles and scan ranges for device discovery. The tab consists of three pages:

- **Discovery Profiles**: Lists the available discovery profiles.

  - Select a profile in the table to view detailed information below.

  - To load a discovery profile, click the *Import* button above the table listing the current discovery profiles. A section will then become available below the table where you can import a single discovery profile or all available discovery profiles. The profiles must be placed in the DataMiner Documents folder *Skyline IDP Discovery* > *Discovery*.

    > [!NOTE]
    > To be able to load a discovery profile, you must ensure that it uses the correct format. See [Discovery profiles](xref:Discovery_profiles).

  - If a discovery profile is not referenced in any CI Type, it can be removed. To do so, select the discovery profile in the table and click the *Delete* button above the table.

- **Scan Ranges**: Lists the available scan ranges.

  - To view additional information on a scan range, select it in the table. Two additional tables will then be displayed below, listing the IP addresses included in the scan range and the CI Types or discovery profiles included in the scan range.

  - To add a scan range, click the *New* button above the table listing the currently configured scan ranges.

  - To remove a scan range, select it in the table and click the *Delete* button. However, if a scan range has ongoing activities, these will need to be stopped before the scan range can be removed.

  - To edit a scan range, select it in the table and click the *Edit* button. This will open a wizard in a pop-up window. In the first step of the wizard, you can adjust the IP ranges. In the next step, you can select whether discovery should happen by CI Type or by discovery profile, specify the CI Types or discovery profile, and select whether *Ping First* should be enabled. If that option is enabled, a ping command is sent before the discovery.

  - If IDP is used with Process Automation, every hour the scan ranges are automatically synchronized with the profile instances used by Process Automation. If you want to trigger this synchronization immediately, use the *Sync* button on this page.

  > [!NOTE]
  > - Both IPv4 and IPV6 ranges are supported. Both types of ranges can be combined in the same request.
  > - If a discovery is done based on the *Ping* discovery profile, devices can be discovered based on ping discovery only. The *Ping First* option will not be available in this case. As the CI Type for devices discovered using a ping discovery is unknown, these will only be displayed in the IDP app if the setting *Identify Unknown Devices* is enabled.

- **Settings**: Contains the following settings:

  - **Timeout of a Single Command**: The number of milliseconds after which a discovery operation is considered to be in timeout.

  - **Number of Retries**: The number of times the system will retry a discovery operation if it goes in timeout.

  - **Request Maximum Duration**: Determines the maximum total duration of a discovery request. If the discovery takes longer than this maximum duration, it will be stopped and DataMiner IDP will report that the discovery has timed out.

  - **Identify Unknown Devices**: Determines whether the app shows devices that have been discovered but for which no matching CI Type is found.

  - **Identify All Matching CI Types**: Determines whether the discovery process will try to match all possible CI Types configured in the scan range. If the setting is disabled, the process will stop trying to match a device with other CI Types once a CI Type has been identified for it. By default, it is disabled.

  - **DNS Lookup**: Determines whether IP addresses of discovered elements are resolved to the corresponding names. If this option is enabled and a discovery is run, the name corresponding with the IP address will be displayed in the *Name* column of the *Discovered Elements* table. If the option is disabled, this column will not be displayed.

  > [!NOTE]
  > If these settings are modified, the changes are only applied to discovery requests that are started after the changes to the settings have been saved.
  >
