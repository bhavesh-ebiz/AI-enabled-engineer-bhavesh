# Implementation Plan

## Default Product Decisions

- Group inactive tabs in the same browser window.
- Use "Inactive Tabs" as the default group name.
- Use 2 hours as the default inactivity threshold.
- Move a tab out of the inactive group when the user opens or interacts with it again.

## Phase 1 - Activity Tracking

- Track the last meaningful user interaction timestamp for each tab.
- Update the timestamp when the tab is selected, focused, navigated, or otherwise interacted with.
- Store tab activity state with tab id, window id, URL, last interaction timestamp, and inactive status.
- Check everytime for gathering the inactive tabs and update it into the inactive group.

## Phase 2 - Tab Group Management

- Look for an existing "Inactive Tabs" group in the same window before creating a new one.
- Create the group if it does not already exist.
- Move inactive tabs into the group without closing.
- Keep the group visually consistent with Chrome's existing tab group design.

## Phase 3 - Reactivation tab handling

- When the user opens or interacts with a tab inside the inactive group, mark it as active.
- Move the tab out of the inactive group.
- Update the tab's last interaction timestamp after reactivation.

## Phase 4 - User Controls

- Allow users to manually remove a tab from the inactive group.
- When tabs are moved into the inactive group notify the user visually.
