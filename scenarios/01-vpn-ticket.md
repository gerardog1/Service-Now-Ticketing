## Scenario 1: Remote VPN Connectivity Issue (Tier 1 Incident)

**Goal:** Log, triage, claim, and resolve a basic VPN issue from start to finish using standard ITIL ticket workflows.

### 1. Creating & Prioritizing the Ticket
* Opened a new incident under **Network > VPN** and routed it to the **Service Desk** group.
* Since this only affected one remote user rather than the whole office, I set **Impact** to `2 - Medium` and **Urgency** to `2 - Medium`. ServiceNow automatically calculated the priority as **3 - Moderate**.


### 2. Fixing Assignment Permissions & Claiming the Ticket
* When I tried to assign the ticket to my own account (`System Administrator`), my name wouldn't show up in the **Assigned to** search list.
* To fix this, I added `System Administrator` to the **Service Desk** group members list and assigned the `itil` role to my user profile so ServiceNow would recognize me as an active support technician.
* After refreshing the form, I assigned the ticket to myself and changed the state to **In Progress**.


### 3. Troubleshooting & User Updates
* **Internal Work Note (Yellow):** Logged basic troubleshooting steps for the IT team—checked that the user had active internet and an unexpired password, then had them restart the VPN app and turn their Wi-Fi off and on.
* **Customer Comment (White):** Sent a short, non-technical message asking the user to close and reopen their VPN client and try connecting again.



### 4. Resolving the Ticket
* Once the connection worked, I changed the ticket state to **Resolved**, selected **Solution provided** as the resolution code, and wrote a brief summary of what fixed the issue.

## Screenshots
[See Screenshots Here](..screenshots/01-screenshots.md)

## Key Takeaways

* **How ServiceNow Calculates Priority:** Before doing this lab, I thought techs just manually picked whether a ticket was "High" or "Low." Seeing how **Impact** (how many people are affected) and **Urgency** (how fast it needs to be fixed) automatically determine the **Priority** made a lot of sense.
* **Permissions Behind the Scenes:** Getting stuck when my own account wouldn't show up under **Assigned to** taught me how ServiceNow controls access. Even as an admin, a user needs to be added to the right **Assignment Group** and have the **`itil` role** before they can actually work tickets.
* **Two Different Ways to Document:** Learning the difference between **Work Notes** (yellow, for other IT techs to see what I checked) and **Additional Comments** (white, for talking to the user without confusing tech jargon) is a habit I'll definitely use in a real help desk role.
* **Why Clean Resolution Notes Matter:** Writing down the actual fix at the end instead of just clicking "Resolved" helps the next tech who runs into the same VPN issue solve it faster.
