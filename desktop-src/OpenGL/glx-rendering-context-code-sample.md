---
title: Esempio di codice del contesto di rendering GLX
description: Nell'esempio di codice seguente viene illustrato come un programma OpenGL del sistema X Window usa le funzioni del contesto di rendering GLX.
ms.assetid: 6cee5e5f-ee2f-4fe4-a988-402802e4a1b8
keywords:
- contesti di rendering
- porting in OpenGL, contesti di rendering
- Porting di OpenGL, contesti di rendering
- Sistema finestra X, contesti di rendering
- Funzioni GLX, contesti di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03259cb9b540db3076a0baa4122906e5aeb3e8f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297758"
---
# <a name="glx-rendering-context-code-sample"></a>Esempio di codice del contesto di rendering GLX

Nell'esempio di codice seguente viene illustrato come un programma OpenGL del sistema X Window usa le funzioni del contesto di rendering GLX.


```C++
Display *dpy;             /* display variable */ 
XVisualInfo *vi;          /* visual variable */ 
Window win;               /* window variable */ 
GLXDrawable drawable;     /* drawable variable */ 
GLXContext cx, cxTemp;    /* rendering context variables */ 
 
/* Code to open a display and get a visual. */ 
        
/* Create a GLX context. */ 
cx = glXCreateContext(dpy, vi, 0, GL_FALSE); 
if (!cx) { 
    fprintf(stderr, "Cannot create context.\n"); 
    exit(-1); 
} 
        
        .    
/* Connect the context to the window. */ 
glXMakeCurrent(dpy, win, cx); 
        
        .    
/* When it's time to destroy the rendering context. . . */ 
cx = glXGetCurrentContext; 
glXDestroyContext(dpy, cx);
```



 

 




