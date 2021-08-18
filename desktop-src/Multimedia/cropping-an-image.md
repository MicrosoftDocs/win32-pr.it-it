---
title: Ritaglio di un'immagine
description: Ritaglio di un'immagine
ms.assetid: 6600751c-d4b6-481d-bf69-be2d34244c05
keywords:
- Macro MCIWndGetSource
- Macro MCIWndPutSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0150962dc85e1e179e52a06c7af6c29193b40b50e9acc7a9feecd0570ab4214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144609"
---
# <a name="cropping-an-image"></a>Ritaglio di un'immagine

L'esempio seguente crea una finestra MCIWnd e carica un file AVI. La finestra include un comando di ritaglio nel menu, che ritaglia un quarto dell'altezza o della larghezza da ognuno dei quattro lati del frame. L'esempio recupera le dimensioni correnti (iniziali) del rettangolo di origine usando la macro [**MCIWndGetSource.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) Il rettangolo di origine modificato è metà dell'altezza e della larghezza originali ed è centrato nel frame originale. La chiamata alla macro [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) ridefinisce le coordinate del rettangolo di origine.


```C++
// extern RECT rSource, rDest; 
 
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE, 
                "sample.avi" ); 
            break; 
        case IDM_CROPIMAGE:                          // crops image 
            MCIWndGetSource(g_hwndMCIWnd, &rSource); // source rectangle
            rDest.left = rSource.left +              // new boundaries
                ((rSource.right - rSource.left) / 4); 
            rDest.right = rSource.right - 
                ((rSource.right - rSource.left) / 4); 
            rDest.top = rSource.top + 
                ((rSource.bottom - rSource.top) / 4); 
            rDest.bottom = rSource.bottom - 
                ((rSource.bottom - rSource.top) / 4); 
 
            MCIWndPutSource(g_hwndMCIWnd, &rDest);   // new source rectangle 
    } 
    break; 

    // Handle other messages here. 
```



 

 




