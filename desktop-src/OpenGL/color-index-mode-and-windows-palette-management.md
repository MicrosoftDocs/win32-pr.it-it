---
title: Modalità Color-Index e gestione tavolozza Windows
description: La modalità di indicizzazione dei colori specifica i colori in una tavolozza logica con un indice per una specifica voce della tavolozza logica.
ms.assetid: 8cf07c3e-8a8b-4f28-a363-34d3c0d33890
keywords:
- OpenGL per Windows, gestione tavolozza
- OpenGL per Windows, modalità indice colori
- OpenGL modalità di indice colore
- gestione tavolozza OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873308c4ac64d496e344b1c71d440d4dc8321418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044992"
---
# <a name="color-index-mode-and-windows-palette-management"></a><span data-ttu-id="60f18-107">Modalità Color-Index e gestione tavolozza Windows</span><span class="sxs-lookup"><span data-stu-id="60f18-107">Color-Index Mode and Windows Palette Management</span></span>

<span data-ttu-id="60f18-108">La modalità di indicizzazione dei colori specifica i colori in una tavolozza logica con un indice per una specifica voce della tavolozza logica.</span><span class="sxs-lookup"><span data-stu-id="60f18-108">The color-index mode specifies colors in a logical palette with an index to a specific logical-palette entry.</span></span> <span data-ttu-id="60f18-109">La maggior parte dei programmi GDI USA le tavolozze degli indici colore, ma la modalità RGBA funziona meglio per OpenGL per diversi effetti, ad esempio ombreggiatura, illuminazione, nebbia e mapping di trama.</span><span class="sxs-lookup"><span data-stu-id="60f18-109">Most GDI programs use color-index palettes, but the RGBA mode works better for OpenGL for several effects, such as shading, lighting, fog, and texture mapping.</span></span> <span data-ttu-id="60f18-110">Se il colore più vero non è cruciale per l'applicazione OpenGL, è possibile scegliere di usare la modalità di indice dei colori, ad esempio per una mappa topografica che usa "false color" per evidenziare la sfumatura di elevazione dei privilegi.</span><span class="sxs-lookup"><span data-stu-id="60f18-110">If having the truest color isn't critical for your OpenGL application, you might choose to use the color-index mode (for example, for a topographic map that uses "false color" to emphasize the elevation gradient).</span></span>

## <a name="color-index-mode-palette-sample"></a><span data-ttu-id="60f18-111">Esempio di tavolozza modalità Color-Index</span><span class="sxs-lookup"><span data-stu-id="60f18-111">Color-Index Mode Palette Sample</span></span>

<span data-ttu-id="60f18-112">Il codice seguente configura una struttura [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) che imposta il flag del membro **iPixelType** su PFD di \_ tipo \_ ColorIndex.</span><span class="sxs-lookup"><span data-stu-id="60f18-112">The following code sets up a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) structure that sets the flag of the **iPixelType** member to PFD\_TYPE\_COLORINDEX.</span></span> <span data-ttu-id="60f18-113">Questa operazione specifica che l'applicazione usa una tavolozza con indice dei colori.</span><span class="sxs-lookup"><span data-stu-id="60f18-113">This specifies that the application use a color-index palette.</span></span>


```C++
BOOL bSetupPixelFormat(HDC hdc) 
{ 
    PIXELFORMATDESCRIPTOR pfd, *ppfd; 
    int pixelformat; 
 
    ppfd = &pfd; 
 
    ppfd->nSize = sizeof(PIXELFORMATDESCRIPTOR); 
    ppfd->nVersion = 1; 
    ppfd->dwFlags = PFD_DRAW_TO_WINDOW | PFD_SUPPORT_OPENGL |  
                        PFD_DOUBLEBUFFER; 
    ppfd->dwLayerMask = PFD_MAIN_PLANE; 
 
    /* Set to color-index mode and use the default color palette. */ 
    ppfd->iPixelType = PFD_TYPE_COLORINDEX;  
 
    ppfd->cColorBits = 8; 
    ppfd->cDepthBits = 16; 
    ppfd->cAccumBits = 0; 
    ppfd->cStencilBits = 0; 
 
    pixelformat = ChoosePixelFormat(hdc, ppfd); 
 
    if ( (pixelformat = ChoosePixelFormat(hdc, ppfd)) == 0 ) 
    { 
        MessageBox(NULL, "ChoosePixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    if (SetPixelFormat(hdc, pixelformat, ppfd) == FALSE) 
    { 
        MessageBox(NULL, "SetPixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    return TRUE; 
}
```



 

 




