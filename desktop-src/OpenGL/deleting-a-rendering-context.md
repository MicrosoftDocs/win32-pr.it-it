---
title: Eliminazione di un contesto di rendering
description: L'esempio di codice seguente illustra come eliminare un contesto di rendering OpenGL quando viene chiusa una finestra OpenGL. Si tratta di una continuazione dello scenario usato in Creazione di un contesto di rendering e Come renderlo corrente.
ms.assetid: 562c4698-f5bb-418a-8479-0df07e9834e5
keywords:
- OpenGL in Windows,contesti di rendering
- contesti di rendering OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efd6821e51ad2493bc2ec3ce1c3ce9b448faee1079ae3771cf3290874fcb9e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889241"
---
# <a name="deleting-a-rendering-context"></a>Eliminazione di un contesto di rendering

L'esempio di codice seguente illustra come eliminare un contesto di rendering OpenGL quando viene chiusa una finestra OpenGL. Si tratta di una continuazione dello scenario usato in [Creazione di un contesto di rendering e Come renderlo corrente.](creating-a-rendering-context-and-making-it-current.md)


```C++
// a window is about to be destroyed  
case WM_DESTROY: 
    { 
    // local variables  
    HGLRC    hglrc; 
    HDC      hdc ; 
 
    // if the thread has a current rendering context ...  
    if(hglrc = wglGetCurrentContext()) { 
 
        // obtain its associated device context  
        hdc = wglGetCurrentDC() ; 
 
        // make the rendering context not current  
        wglMakeCurrent(NULL, NULL) ; 
 
        // release the device context  
        ReleaseDC (hwnd, hdc) ; 
 
        // delete the rendering context  
        wglDeleteContext(hglrc); 
 
        }
```



 

 




