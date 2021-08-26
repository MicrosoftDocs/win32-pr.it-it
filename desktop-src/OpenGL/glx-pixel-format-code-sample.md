---
title: Esempio di codice per il formato pixel GLX
description: L'esempio di codice seguente illustra come un programma OpenGL X Window System usa le funzioni di formattazione visiva/pixel GLX.
ms.assetid: f01193a9-c0ff-4399-a86e-06bb4603b3f1
keywords:
- portabilità in OpenGL, pixel
- Portabilità OpenGL, pixel
- Sistema finestra X,pixel
- Funzioni GLX, pixel
- pixel, esempio GLX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312b95fb2ff4719c9ecda863b67ac926905b09d0e4b8aecbcc673a03c18c307a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035388"
---
# <a name="glx-pixel-format-code-sample"></a>Esempio di codice per il formato pixel GLX

L'esempio di codice seguente illustra come un programma OpenGL X Window System usa le funzioni di formattazione visiva/pixel GLX.


```C++
/* X globals, defines, and prototypes */ 
Display *dpy; 
Window glwin; 
static int attributes[] = {GLX_DEPTH_SIZE, 16, GLX_DOUBLEBUFFER, None}; 
        
    /* find an OpenGL-capable Color Index visual with depth buffer */ 
    vi = glXChooseVisual(dpy, DefaultScreen(dpy), attributes); 
    if (vi == NULL) { 
        fprintf(stderr, "could not get visual\n"); 
        exit(1); 
    }
```



L'oggetto Visivo può essere usato per creare una finestra e un contesto di rendering.

 

 




