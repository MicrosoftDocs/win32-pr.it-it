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
# <a name="creating-a-rendering-context-and-making-it-current"></a><span data-ttu-id="e433e-105">Creazione di un contesto di rendering e resa corrente</span><span class="sxs-lookup"><span data-stu-id="e433e-105">Creating a Rendering Context and Making It Current</span></span>

<span data-ttu-id="e433e-106">Nell'esempio di codice seguente viene illustrato come creare un contesto di rendering OpenGL in risposta a un \_ messaggio WM create.</span><span class="sxs-lookup"><span data-stu-id="e433e-106">The following code sample shows how to create an OpenGL rendering context in response to a WM\_CREATE message.</span></span> <span data-ttu-id="e433e-107">Si noti che è necessario configurare il formato pixel prima di creare il contesto di rendering.</span><span class="sxs-lookup"><span data-stu-id="e433e-107">Notice that you set up the pixel format before creating the rendering context.</span></span> <span data-ttu-id="e433e-108">Si noti inoltre che in questo scenario il contesto di dispositivo non viene rilasciato localmente; viene rilasciata quando la finestra viene chiusa, dopo aver reso il contesto di rendering non aggiornato.</span><span class="sxs-lookup"><span data-stu-id="e433e-108">Also notice that in this scenario the device context is not released locally; you release it when the window is closed, after making the rendering context not current.</span></span> <span data-ttu-id="e433e-109">Per ulteriori informazioni, vedere [eliminazione di un contesto di rendering](deleting-a-rendering-context.md).</span><span class="sxs-lookup"><span data-stu-id="e433e-109">For more information, see [Deleting a Rendering Context](deleting-a-rendering-context.md).</span></span> <span data-ttu-id="e433e-110">Si noti infine che è possibile usare le variabili locali per il contesto di dispositivo e gli handle del contesto di rendering, perché con le funzioni [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) e [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) è possibile ottenere gli handle per tali contesti in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="e433e-110">Finally, notice that you can use local variables for the device context and rendering context handles, because with the [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) and [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) functions you can obtain handles to those contexts as needed.</span></span>

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

 

 




