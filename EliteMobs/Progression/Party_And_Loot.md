# Party system, group loot sharing #

##  Creating and Joining a Party ## 

* **`/em party create`** - Creates a party with you as its leader
* **`/em party invite <player>`** - Invites an online player; any current party member can invite
* **`/em party accept`** - Accepts your most recent unexpired invitation
* **`/em party leave`** - Leaves your current party
* **`/em party menu`** - Opens the inventory-based party controls
* **`/em party hideinteractionhint`** - Permanently hides right-click party hints for you

##   Progress and loot ##
### Shared kill progress ###
When any party member earns kill credit, nearby members recieve credit for any objective which required that kill. To trigger this, members must be within the same world, within 128 blocks of the kill.

### Group Loot ### 
When at least two party members are nearby, normal Elite equipment, special Elite gear, and eligible custom items enter a shared Need / Greed vote. Nearby party members do not have to land the killing hit to participate. Coins and Elite Scrolls remain personal.

#### Voting on loot ####

You can open the vote using /em loot. The GUI is presented as such :

- Greed (left) — the default state. Items sit here until someone claims them. If you only want an item should nobody else need it, leave it on the greed side.
- Need (right) — click an item to move it to your Need list. Everyone in the group is notified when you mark or unmark an item as Need.

**How items are distributed**

When the timer runs out, each item is rolled independently:
- If one or more players marked it as Need, the item is randomly awarded to one of those players.
- If nobody needed it, it is randomly awarded among all currently online players eligible for that item (the greed roll).

The winner receives the item directly into their inventory (it drops at their feet if the inventory is full), the item is soulbound to them, and everyone still active in that vote sees a message announcing who got it. A player who logs out or leaves the party is removed from that party's active vote. If nobody eligible remains online, the item drops at the defeated Elite's saved location when that world is still loaded.
