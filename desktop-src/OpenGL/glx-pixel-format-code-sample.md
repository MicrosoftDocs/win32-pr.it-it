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
# <a name="glx-pixel-format-code-sample"></a><span data-ttu-id="945df-108">Esempio di codice in formato pixel GLX</span><span class="sxs-lookup"><span data-stu-id="945df-108">GLX Pixel Format Code Sample</span></span>

<span data-ttu-id="945df-109">Nell'esempio di codice riportato di seguito viene illustrato il modo in cui un programma OpenGL di sistema X Window usa le funzioni di formattazione visiva/pixel GLX.</span><span class="sxs-lookup"><span data-stu-id="945df-109">The code sample below shows how an X Window System OpenGL program uses GLX visual/pixel formatting functions.</span></span>


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



<span data-ttu-id="945df-110">L'oggetto visivo può essere utilizzato per creare una finestra e un contesto di rendering.</span><span class="sxs-lookup"><span data-stu-id="945df-110">The Visual can be used to create a window and a rendering context.</span></span>

 

 




