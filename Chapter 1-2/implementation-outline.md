# Implementation Outline

## Part 1 – Activity Tracking

- Implement the business logic to identify the inactivity tabs by using last active timestamp.
- Maintain a state to classify tabs as active or inactive based on inactivity threshold.

## Part 2 – Tab Group Management

- Implement the reuse an “Inactive Tabs” group or create the new one.
- Move all inactive tabs into this group automatically.

## Part 3 – Reactivation Handling
- On user interaction with an inactive tab, mark it as active.
- Remove the tab from the inactive group and update its activity state.