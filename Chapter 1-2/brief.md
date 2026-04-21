# Brief:
This is the feature that we can implement in Google Chrome that will help us to orgnize the tabs that we have not interacted for given time period or default time. It will automatically check the interaction time of the tab and assign it to the specificed group or create the separate one (like Inactive).


## Assumptions:
- Inactive tabs will automatically move to the specificed group in the same window.
- User will be able to remove the tab from the group.
- Group name will be the "Inactive" by default.
- For the identifing inactive tabs, the default time will be 2 hours.


## Top Risks:
- User may phase the issue if the tab moves to the group and user is not aware of it.
- We may lost the tab itself that is not inactive at the moment.