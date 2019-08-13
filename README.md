# Glacier-Front-Classification

This is the code repository for summer research done through the NASA Space Grant Summer 2019 Undergraduate Research Program (SURP).


At the moment, the file path is hard coded into the seg_coast.py script and will need to be edited with the correct file path. The repository contains a "pickled" version of the segmented image which can be accessed by first running the command 
```bash
tar -zxvf seg_pic.tar.gz
``` 
in the terminal, then in your python code adding the following:

```python
import pickle

with open('seg_pic', 'rb') as f:
     img = pickle.load(f)
```
Run `make` in the terminal before running the border removal algorithm in order to compile the required cython code to C. Just for a sanity check, there should be a `.so` file now in the directory.
