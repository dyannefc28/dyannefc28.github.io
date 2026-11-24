---
layout: post
title: Image Manipulation
image: "/posts/camaro.jpg"
tags: [Python, Numpy]
---

In this post I'm going to run through a function in Python that 

---



```ruby
import numpy as np
from skimage import io
import matplotlib.pyplot as plt
```
Let's get this image to generate

```ruby
camaro = io.imread("camaro.jpg")
print(camaro)

```

![alt text](/img/posts/camaro-show.jpg")



