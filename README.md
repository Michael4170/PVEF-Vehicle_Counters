<img width="1920" height="1080" alt="PVEF_Vehicle_Counters_Workshop" src="https://github.com/user-attachments/assets/49d264f2-6039-4b3d-99df-43b1fe990a1d" />



Vehicle counter-attacks designed to work with PVEF - PvE Framework. A crewed USSR vehicle is sent at a base the players are taking, or have just taken.

Built and tested as a PVEF companion, with no hard dependency on it: base game only.

ALPHA, for testing.

TWO TRIGGERS, EACH WITH ITS OWN CHANCE
- When the player faction starts capturing a base. Rolled once per attempt, not once per capture point.
- When a base changes hands to them.

THEY COME FROM SOMEWHERE
- The bearing runs from the objective towards the nearest enemy-held base, so a counter arrives from contested ground instead of a random compass point.
- It spawns on a real road at that bearing, 700-1300 m out, facing the objective. If no road is found the counter is skipped and the log says why.
- Never spawns within 350 m of a player.

MOUNTED UNTIL CONTACT
- The whole crew rides in. No parking short and walking the last stretch.
- Driver and gunners stay aboard for good.
- Cargo dismounts and fights once a player closes inside the engage radius.

ONE CONFIG FILE
- Written to your server profile on first run. Never overwritten after that.
- Vehicle list with pick weights and per-trigger eligibility - add any vehicle by resource name.
- Chances, delays, per-base cooldown, spawn distances, engage radius, lifetime.

IT KNOWS WHEN TO SAY NO
- A cap on how many counters are live across the map.
- Skips while the server is near its active-AI limit.
- HQs are never targeted, including PVEF's offshore OPFOR anchor.
- Cleans up once no player is near. Every skip is logged with the reason.
