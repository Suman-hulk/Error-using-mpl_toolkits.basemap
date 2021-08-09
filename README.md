# Error-using-mpl_toolkits.basemap
ImportError: cannot import name 'dedent' from 'matplotlib.cbook' #494

mpl_toolkits.basemap don't work with newer version of matplotlib
So we need to follow the following procedure to make it work:

1) open /home/user/anaconda2/envs/py37/lib/python3.7/site-packages/matplotlib/cbook 
2) go to file __init__.py 
3) go to line no. 519 where dedent_regex = {} ends. 
4) After that go to link : https://matplotlib.org/3.1.1/_modules/matplotlib/cbook.html#dedent 
5) copy the code where dedent is defined and paste it in _init.py after _dedent_regex = {} and save it. 
6) Update the system using sudo apt-get update. 
7) Now run the code it will work.

import matplotlib.pyplot as plt
from mpl_toolkits.basemap import Basemap
