---
title: "Zorya Renderer"
summary: "A DX11 real-time renderer developed as a way to experiment with interesting rendering and engine features. Uses a **Render Graph** to ease the implemenentation of new features by automatically managing transient resources. One of the main features is the presence of multiple **subsurface scattering** techniques. Planning to also integrate a DX12 backend."
date: 2024-09-18T23:57:05+02:00
draft: false
weight: 1 
tags: ["C/C++","DX11","Rendering"]
---

{{< alert icon="link">}}
[Github Repository](https://github.com/nagard98/zorya-renderer)
{{< /alert >}}

A DX11 real-time renderer developed as a way to experiment with interesting rendering and engine features. Uses a **Render Graph** to ease the implemenentation of new features by automatically managing transient resources (currently only textures, not constant buffers). One of the main features is the presence of multiple **subsurface scattering** techniques. Planning to also integrate a DX12 backend.

![image](feature.png)

## Subsurface Scattering

Multiple subsurface scattering techniques are supported, specifically:
- Jimenez Gaussian [[Jim09]](https://doi.org/10.1145/1609967.1609970)
- Jimenez Separable [[Jim15]](https://doi.org/10.1111/cgf.12529)
- Golubev [[Gol18]](https://advances.realtimerendering.com/s2018/Efficient%20screen%20space%20subsurface%20scattering%20Siggraph%202018.pdf)
- Golubev Plus (an extension developed during my [thesis](thesis.pdf) that improves performance)

|![image](gauss_med.png)| ![image](separable_med.png)| ![image](golubev_med.png)|![image](golubev+_med.png)|
|:-:|:-:|:-:|:-:|