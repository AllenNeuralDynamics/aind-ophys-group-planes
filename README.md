# aind-ophys-group-planes 

Uses the coupled_fov_index from the session.json to determine which planes are paired together.

## Input

`session.json` at the root directory of the `data` folder.

## Output

`pairN.txt` files with the location in the `data` directory of the coupled timeseries. For example, this is what is within a TEXT file called `pair0.txt`:

`/data/VISp_0`
`/data/VISp_1`

The text files are then sent to the `aind-ophys-decrosstalk-roi-images` capsule in parallel. `aind-ophys-decrosstalk-roi-images` can then process the image pairs within the TEXT file. 