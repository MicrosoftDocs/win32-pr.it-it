---
title: Creazione di un contesto di rendering e resa corrente
description: Nell'esempio di codice seguente viene illustrato come creare un contesto di rendering OpenGL in risposta a un \_ messaggio WM create.
ms.assetid: eacf0475-6845-48f9-b016-7f0150679419
keywords:
- OpenGL per Windows, contesti di rendering
- contesti di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7bcb8eb5a3892aac977f465894808adc19809a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331164"
---
# <a name="creating-a-rendering-context-and-making-it-current"></a>Creazione di un contesto di rendering e resa corrente

Nell'esempio di codice seguente viene illustrato come creare un contesto di rendering OpenGL in risposta a un \_ messaggio WM create. Si noti che è necessario configurare il formato pixel prima di creare il contesto di rendering. Si noti inoltre che in questo scenario il contesto di dispositivo non viene rilasciato localmente; viene rilasciata quando la finestra viene chiusa, dopo aver reso il contesto di rendering non aggiornato. Per ulteriori informazioni, vedere [eliminazione di un contesto di rendering](deleting-a-rendering-context.md). Si noti infine che è possibile usare le variabili locali per il contesto di dispositivo e gli handle del contesto di rendering, perché con le funzioni [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) e [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) è possibile ottenere gli handle per tali contesti in base alle esigenze.

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

 

 




