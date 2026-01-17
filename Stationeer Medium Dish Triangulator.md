Stationeer Medium Dish Triangulator

This is an IC10 module that takes three measurements (H/V/Error), and triangulates the H/V setting required to point to the target.

Usage:
- The IC expects no `dx` pins to be set, it doesn't interact with any devices or does any sort of I/O (other than on `db`).
- The IC waits until the housing `Setting` is non-zero, at which point the following MUST have been done:
    - Three triplets of (H, V, E) values have been pushed onto the stack in that order.
- The IC computes the triangulated H/V angles, and writes them to the stack at `db 0` and `db 1` respectively.
- The IC then clears the housing `Setting` to zero to indicate calculation completion.

Notes: 
- It is recommended for the measurements to be taken in a "triangular" pattern, additionally measurements must NOT be taken close to vertical 0 (upwards).
  A minimum of 5~10 degrees Vertical is recommended for accurate results.
- The script requires minification to fit within IC10 size limits, source code can be found in the repository.

License & credits
Use, modify, and republish freely *with credit*!


Made by Doggo