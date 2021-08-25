---
title: Color-Index e gestione Windows tavolozza
description: La modalità di indicizzazione dei colori specifica i colori in una tavolozza logica con un indice per una voce specifica della tavolozza logica.
ms.assetid: 8cf07c3e-8a8b-4f28-a363-34d3c0d33890
keywords:
- OpenGL in Windows,gestione della tavolozza
- OpenGL in Windows, modalità color-index
- Modalità indice colori OpenGL
- Gestione della tavolozza OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e4d7c9db02a80bdffdef93655e88cc5b2ca8197a58c5ffdb488c2b782f10d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889261"
---
# <a name="color-index-mode-and-windows-palette-management"></a>Color-Index e gestione Windows tavolozza

La modalità di indicizzazione dei colori specifica i colori in una tavolozza logica con un indice per una voce specifica della tavolozza logica. La maggior parte dei programmi GDI usa le tavolozze degli indici di colore, ma la modalità RGBA funziona meglio per OpenGL per diversi effetti, ad esempio ombreggiatura, illuminazione, tinta e mapping di trama. Se il colore più vero non è critico per l'applicazione OpenGL, è possibile scegliere di usare la modalità di indicizzazione dei colori (ad esempio, per una mappa topografica che usa "false color" per evidenziare la sfumatura di elevazione).

## <a name="color-index-mode-palette-sample"></a>esempio Color-Index palette modalità di compatibilità

Nel codice seguente viene impostata [**una struttura PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) che imposta il flag del membro **iPixelType** su PFD \_ TYPE \_ COLORINDEX. Specifica che l'applicazione utilizza una tavolozza dell'indice dei colori.


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



 

 




