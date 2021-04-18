---
title: Scelta e impostazione di un formato Best-Match pixel
description: In questo argomento viene illustrata la procedura per abbinare un contesto di dispositivo a un formato pixel.
ms.assetid: 7b974fb5-e34d-4781-858c-572c4e7754bc
keywords:
- OpenGL per Windows, pixel
- formato pixel con corrispondenza migliore OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 143800a9c43d8c8a7779bb5e6cd119c6737f8129
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298185"
---
# <a name="choosing-and-setting-a-best-match-pixel-format"></a>Scelta e impostazione di un formato Best-Match pixel

In questo argomento viene illustrata la procedura per abbinare un contesto di dispositivo a un formato pixel.

**Per ottenere la migliore corrispondenza del contesto di dispositivo con un formato pixel**

1.  Specificare il formato pixel desiderato in una struttura [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) .
2.  Chiamare [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).

    La funzione **ChoosePixelFormat** restituisce un indice di formato pixel, che è quindi possibile passare a [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) per impostare la corrispondenza del formato pixel migliore come il formato pixel corrente del contesto di dispositivo.

Nell'esempio di codice riportato di seguito viene illustrato come eseguire i passaggi precedenti.


```C++
PIXELFORMATDESCRIPTOR pfd = { 
    sizeof(PIXELFORMATDESCRIPTOR),    // size of this pfd  
    1,                                // version number  
    PFD_DRAW_TO_WINDOW |              // support window  
    PFD_SUPPORT_OPENGL |              // support OpenGL  
    PFD_DOUBLEBUFFER,                 // double buffered  
    PFD_TYPE_RGBA,                    // RGBA type  
    24,                               // 24-bit color depth  
    0, 0, 0, 0, 0, 0,                 // color bits ignored  
    0,                                // no alpha buffer  
    0,                                // shift bit ignored  
    0,                                // no accumulation buffer  
    0, 0, 0, 0,                       // accum bits ignored  
    32,                               // 32-bit z-buffer      
    0,                                // no stencil buffer  
    0,                                // no auxiliary buffer  
    PFD_MAIN_PLANE,                   // main layer  
    0,                                // reserved  
    0, 0, 0                           // layer masks ignored  
}; 
HDC  hdc; 
int  iPixelFormat; 
 
// get the device context's best, available pixel format match  
iPixelFormat = ChoosePixelFormat(hdc, &pfd); 
 
// make that match the device context's current pixel format  
SetPixelFormat(hdc, iPixelFormat, &pfd);
```



 

 




