# VoCompr, a VOCabulary-based COMPRession algorithm
[![Actions Status](https://github.com/enzobnl/vocompr/workflows/test/badge.svg)](https://github.com/enzobnl/pycout/actions) [![Actions Status](https://github.com/enzobnl/vocompr/workflows/PyPI/badge.svg)](https://github.com/enzobnl/pycout/actions)

## Install
`pip install vocompr` (or `pip install git+https://github.com/enzobnl/vocompr.git`)
## Usage
This
```python
from vocompr import vocompr, unvocompr

with open("path/vopress_input.txt", "r") as input_file: # 163,9 kB(wiki), 23.7kB(bits)
    input_str = input_file.read()

with open("path/vopress_output", "wb") as output_bytes_file: # 147,2 kB, 6.1kB
    output_bytes_file.write(vocompr(input_str))

with open("path/vopress_output", "rb") as input_bytes_file:
    print("original text:", unvocompr(input_bytes_file.read()))
```
