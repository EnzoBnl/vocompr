# VoCompr, a VOCabulary-based COMPRession algorithm
[![Actions Status](https://github.com/enzobnl/vocompr/workflows/test/badge.svg)](https://github.com/enzobnl/pycout/actions) [![Actions Status](https://github.com/enzobnl/vocompr/workflows/PyPI/badge.svg)](https://github.com/enzobnl/pycout/actions)

*Specialized in the compression of texts having a small characters set.*

## Install
`pip install vocompr` (or `pip install git+https://github.com/enzobnl/vocompr.git`)
## Usage
This
```python
from vocompr import vocompr, unvocompr

with open("path/vopress_input.txt", "r") as input_file:
    input_str = input_file.read()

with open("path/vopress_output", "wb") as output_bytes_file:
    output_bytes_file.write(vocompr(input_str))

with open("path/vopress_output", "rb") as input_bytes_file:
    print("original text:", unvocompr(input_bytes_file.read()))
```
