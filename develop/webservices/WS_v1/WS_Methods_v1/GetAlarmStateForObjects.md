---
uid: GetAlarmStateForObjects
---

# GetAlarmStateForObjects

Use this method to retrieve the current alarm state of several specified objects.

## Input

| Item | Format | Description |
|--|--|--|
| Connection | String | The connection ID. See [ConnectApp](xref:ConnectApp). |
| Objects | Array of objects | Array of objects, consisting of \[type, dmaID, ID, index\], where type can be “view”, “element” or “service”. |

## Output

| Item                           | Format          | Description                                        |
|--------------------------------|-----------------|----------------------------------------------------|
| GetAlarmStateFor­ObjectsResult | Array of string | The current alarm states of the specified objects. |
