---
title: Ritaglio di un'immagine
description: Ritaglio di un'immagine
ms.assetid: 6600751c-d4b6-481d-bf69-be2d34244c05
keywords:
- MCIWndGetSource (macro)
- MCIWndPutSource (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d73eb37792c124ad907f660d4b906ca80e715d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471190"
---
# <a name="cropping-an-image"></a>Ritaglio di un'immagine

Nell'esempio seguente viene creata una finestra MCIWnd e viene caricato un file AVI. La finestra include un comando Crop nel menu, che consente di ritagliare un trimestre dell'altezza o della larghezza da ognuno dei quattro lati del frame. Nell'esempio vengono recuperate le dimensioni correnti (iniziali) del rettangolo di origine utilizzando la macro [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) . Il rettangolo di origine modificato è la metà dell'altezza e della larghezza originali e viene centrato nel frame originale. La chiamata alla macro [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) ridefinisce le coordinate del rettangolo di origine.


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



 

 




