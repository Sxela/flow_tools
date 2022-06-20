# Flow Tools wrapper
Flow Tools is a simple python CLI tool for creating consistency maps from optical flow maps.

Based on the awesome [implementation](https://github.com/maua-maua-maua/maua/blob/44485c745c65cf9d83cb1b1c792a177588e9c9fc/maua/flow/consistency.py) by Hans Brouwer and Henry Rachootin from [maua](https://github.com/maua-maua-maua/maua/)

# Usage
The script takes flow files as numpy float arrays of shape [H,W,2] and outputs a numpy float array of shape [H,W] in range (0,1).\
It can optionally output a jpeg image (for sanity check or direct use for its smaller size)

The list of arguments is pretty straightforward: specify required paths (forward and backward flows and an output filename)
```usage: 
check_consistency.py [-h] --flow_fwd FLOW_FWD --flow_bwd FLOW_BWD
                            --output OUTPUT [--image_output] [--blur BLUR]
                            [--bottom_clamp BOTTOM_CLAMP] [--edges_reliable]

optional arguments:
  -h, --help            show this help message and exit
  --flow_fwd FLOW_FWD   Forward flow path
  --flow_bwd FLOW_BWD   Backward flow path
  --output OUTPUT       Output consistency map path
  --image_output        Output consistency map as b\w image path
  --blur BLUR           Gaussian blur kernel size (0 for no blur)
  --bottom_clamp BOTTOM_CLAMP
                        Clamp lower values
  --edges_reliable      Consider edges reliable
 ```

wrapper by [Alex Spirin](https://linktr.ee/sxela)
