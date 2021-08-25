---
title: Creazione di un contesto di rendering e renderlo corrente
description: L'esempio di codice seguente illustra come creare un contesto di rendering OpenGL in risposta a un messaggio WM \_ CREATE.
ms.assetid: eacf0475-6845-48f9-b016-7f0150679419
keywords:
- OpenGL in Windows,contesti di rendering
- contesti di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1768506eba506506a7198fbccc7dfefc0491adc96dd1e7bd03d2ec2aa5df8eb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868791"
---
# <a name="creating-a-rendering-context-and-making-it-current"></a>Creazione di un contesto di rendering e renderlo corrente

L'esempio di codice seguente illustra come creare un contesto di rendering OpenGL in risposta a un messaggio WM \_ CREATE. Si noti che è stato configurato il formato pixel prima di creare il contesto di rendering. Si noti anche che in questo scenario il contesto del dispositivo non viene rilasciato in locale. viene rilasciata quando la finestra viene chiusa, dopo aver fatto in modo che il contesto di rendering non sia corrente. Per altre informazioni, vedere [Eliminazione di un contesto di rendering.](deleting-a-rendering-context.md) Si noti infine che è possibile usare variabili locali per il contesto di dispositivo e gli handle del contesto di rendering, perché con le funzioni [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) e [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) è possibile ottenere gli handle per tali contesti in base alle esigenze.

``` syntax
// a window has been created, but is not yet visible  
case WM_CREATE: 
    { 
    // local variables  
    HDC      hdc ; 
    HGLRC    hglrc ; 
 
    // obtain a device context for the window  
    hdc = GetDC(hWnd); 
     
    // set an appropriate pixel format   
    myPixelFormatSetupFunction(hdc); 
 
    // if we can create a rendering context ...   
    if (hglrc = wglCreateContext( hdc ) ) { 
 
        // try to make it the thread's current rendering context  
        bHaveCurrentRC = wglMakeCurrent(hdc, hglrc) ; 
 
        } 
 
    // perform miscellaneous other WM_CREATE chores ...  
 
    }  
    break;
```

 

 




