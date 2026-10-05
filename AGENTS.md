# Agent instructions: admin

The admin is the restricted application for running the store. Read the root
[`AGENTS.md`](../AGENTS.md) as well; this file wins where the two conflict.

## Boundaries

- Hiding a button is not authorization. The backend enforces every permission; the UI only mirrors
  it.
- Talk to the rest of the platform only through public interfaces: the API, through the generated
  SDK, and real-time events.

## Rules

- Sensitive actions, such as refunds, role changes, inventory edits and cancellations, must go
  through backend operations that write audit records.
- Treat staff and customer data as sensitive. Show each role what it needs and nothing more.
