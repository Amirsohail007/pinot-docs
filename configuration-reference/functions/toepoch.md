---
description: This section contains reference documentation for the toEpoch functions.
---

# toEpoch

Convert epoch milliseconds to epoch <Time Unit>.
The following time units are supported:

* SECONDS
* MINUTES
* HOURS
* DAYS

## Signature

> ToEpoch<TIME_UNIT>(timeInMillis)

## Usage Examples

```sql
select ToEpochSeconds(1613472303000) AS epochSeconds
FROM ignoreMe
```

| epochSeconds   |
| ------------- |
| 1613472303 |

```sql
select ToEpochMinutes(1613472303000) AS epochMins
FROM ignoreMe
```

| epochMins   |
| ------------- |
| 26891205 |

```sql
select ToEpochHours(1613472303000) AS epochHours
FROM ignoreMe
```

| epochHours   |
| ------------- |
| 448186 |

```sql
select ToEpochDays(1613472303000) AS epochDays
FROM ignoreMe
```

| epochDays   |
| ------------- |
| 18674 |


