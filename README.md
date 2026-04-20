# Weekly Airtable Data Rollover from Week 1 to Week 4 and Summary Tables

## Overview

A scheduled weekly data rollover workflow for Airtable. Every Sunday, it cascades data through 4 weekly tables: Week 4 data is archived, Week 3 moves to Week 4, Week 2 moves to Week 3, Week 1 moves to Week 2, and Week 1 is cleared for new data. After the rollover, it aggregates all data to update monthly and master summary tables. This maintains a rolling 4-week window of active data with full historical archiving.

## How It Works

```
Every Sunday -> Configure tables -> Create parent table list -> For each table: Archive Week 4 -> Move Week 3 to Week 4 -> Move Week 2 to Week 3 -> Move Week 1 to Week 2 -> Clear Week 1 -> Aggregate all data -> Update Monthly Summary -> Update Master Summary
```

## Integrations

- **Airtable** - Weekly data tables, archive, and summary tables

## Setup

1. Import `Weekly_Airtable_Data_Rollover_from_Week_1_to_Week_4_and_Summary_Tables.json` into your n8n instance.
2. Configure Airtable credentials and table IDs in the Workflow Configuration node.
3. Activate for weekly Sunday execution.
