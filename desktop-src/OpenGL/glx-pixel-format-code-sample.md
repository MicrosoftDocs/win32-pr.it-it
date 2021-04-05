---
title: Esempio di codice in formato pixel GLX
description: Nell'esempio di codice riportato di seguito viene illustrato il modo in cui un programma OpenGL di sistema X Window usa le funzioni di formattazione visiva/pixel GLX.
ms.assetid: f01193a9-c0ff-4399-a86e-06bb4603b3f1
keywords:
- porting in OpenGL, pixel
- Porting OpenGL, pixel
- Sistema finestra X, pixel
- Funzioni GLX, pixel
- pixel, esempio GLX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0ab6464d54e696c136a6c987b94124f52b0ee2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707816"
---
# <a name="glx-pixel-format-code-sample"></a>Esempio di codice in formato pixel GLX

Nell'esempio di codice riportato di seguito viene illustrato il modo in cui un programma OpenGL di sistema X Window usa le funzioni di formattazione visiva/pixel GLX.


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



L'oggetto visivo può essere utilizzato per creare una finestra e un contesto di rendering.

 

 




