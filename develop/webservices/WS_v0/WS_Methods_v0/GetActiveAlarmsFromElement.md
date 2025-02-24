---
uid: GetActiveAlarmsFromElement
---

# GetActiveAlarmsFromElement

Use this method to request a list of all the alarms of a specific element (referenced by name).

## Input

| Item        | Format | Description                                   |
|-------------|--------|-----------------------------------------------|
| Connection  | String | The connection ID. See [Connect](xref:Connect). |
| ElementName | String | The element name.                             |

## Output

| Item | Format | Description |
|--|--|--|
| GetActiveAlarmsFrom­ElementResult | Array of [AlarmEventMessage](xref:AlarmEventMessage) | All the alarms of the specified element. |
