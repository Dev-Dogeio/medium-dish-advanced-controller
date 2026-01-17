Stationeers Medium Dish Advanced Controller

This is an IC10 controller that automates sweeping, triangulation, alignment and trader interrogation utilizing a medium dish and the triangulator module.

Usage:
- Setup the following device pins:
    - `d0` - Medium Dish
    - `d1` - Small scan switch (if enabled, will scan the "easy" contacts)
    - `d2` - Big scan switch (if enabled, will scan the "hard" contacts, o3 trader + 6x6/9x9 traders)
    - `d4` - Display device for status output (optional, highly recommended)
    - `d5` - Triangulator IC housing, uploaded as a seperate workshop item
- The controller will continuously sweep the sky, look for contacts, and interrogate them.
- Higher than available power targets are recorded to the blacklist via `put db slotIndex signalID` to avoid repeated interrogation attempts for impossible targets.

Behavior:
- The controller performs layered sweeps: vertical steps with full horizontal rotations between steps.
- The controller will avoid triangulating a signal if it can be scanned without it (enough power reaching target).


Notes:
- Only ~25% of the "big" traders contacts have higher power requirements than medium dishes can handle. (~75% can be scanned)
- The script requires minification to fit within IC10 size limits, source code can be found in the repository.

License & credits
Use, modify, and republish freely *with credit*!

Made by Doggo