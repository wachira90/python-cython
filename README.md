# Example cython

## file example_original.py
```
def test(x):
    y = 0
    for i in range(x):
        y += i
    return y
```

## How do we prepare this file to be passed through Cython? Simple, rather than .py, we do .pyx

## example_cython.pyx
```
def test(x):
    y = 0
    for i in range(x):
        y += i
    return y
```

We obviously don't have any typing information yet. We'll add that in later, but, for now, we'll stick with this.

Once you have a .pyx, you're ready to build. To do this, we're going to make a 

## setup.py file:

```
from distutils.core import setup
from Cython.Build import cythonize

setup(ext_modules = cythonize('example_cython.pyx'))
```
## Next, in your terminal, do:

```
python setup.py build_ext --inplace
```



Visual Studio 2010 (VS10): 
```
SET VS90COMNTOOLS=%VS100COMNTOOLS%
```

Visual Studio 2012 (VS11): 
```
SET VS90COMNTOOLS=%VS110COMNTOOLS%
```

Visual Studio 2013 (VS12): 
```
SET VS90COMNTOOLS=%VS120COMNTOOLS%
```

Visual Studio 2015 (VS14): 
```
SET VS90COMNTOOLS=%VS140COMNTOOLS%
```

```
C:\Users\admin>python
Python 3.8.1 (tags/v3.8.1:1b293b6, Dec 18 2019, 23:11:46) [MSC v.1916 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
MSC v.1000 -> Visual C++ 4.x        
MSC v.1100 -> Visual C++ 5          
MSC v.1200 -> Visual C++ 6          
MSC v.1300 -> Visual C++ .NET       
MSC v.1310 -> Visual C++ .NET 2003  
MSC v.1400 -> Visual C++ 2005  (8.0)
MSC v.1500 -> Visual C++ 2008  (9.0)
MSC v.1600 -> Visual C++ 2010 (10.0)
MSC v.1700 -> Visual C++ 2012 (11.0)
MSC v.1800 -> Visual C++ 2013 (12.0)
MSC v.1900 -> Visual C++ 2015 (14.0)
MSC v.1910 -> Visual C++ 2017 (15.0)
MSC v.1911 -> Visual C++ 2017 (15.3)
MSC v.1912 -> Visual C++ 2017 (15.5)
MSC v.1913 -> Visual C++ 2017 (15.6)
MSC v.1914 -> Visual C++ 2017 (15.7)
MSC v.1915 -> Visual C++ 2017 (15.8)
MSC v.1916 -> Visual C++ 2017 (15.9) 
```


Execute:

32-bit Compilers:

Note: 32-bit Windows installs will only have C:\Program Files\ as expected

```
"C:\Program Files (x86)\Microsoft Visual Studio 9.0\Common7\Tools\vsvars32.bat"
```

64-bit Compilers:

```
"C:\Program Files (x86)\Microsoft Visual Studio 9.0\Common7\Tools\vsvars64.bat"
```

## login-download

```
https://my.visualstudio.com/Downloads?q=Build%20Tools%20for%20Visual%20Studio%202017%20(version%2015.9)&pgroup=
```
