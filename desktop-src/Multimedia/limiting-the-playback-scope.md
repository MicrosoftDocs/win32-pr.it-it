---
title: Limitazione dell'ambito di riproduzione
description: Limitazione dell'ambito di riproduzione
ms.assetid: 080ab96f-1cb5-48d4-ac0a-8fd9ba68a31a
keywords:
- Macro MCIWndPlayFrom
- Macro MCIWndPlayTo
- Macro MCIWndPlayFromTo
- Comandi di riproduzione MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 064f62e913c33bef0582efaa950ee376e31a5b06a54d0e70674192e31a679a9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139484"
---
# <a name="limiting-the-playback-scope"></a>Limitazione dell'ambito di riproduzione

Il controllo della riproduzione inizia con la macro [**MCIWndPlay,**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) che riproduce il contenuto o il file associato a una finestra MCIWnd dalla posizione di riproduzione corrente alla fine del contenuto. Se si vuole limitare la riproduzione a una parte specifica del contenuto o del file, è possibile scegliere tra le altre macro MCIWnd di riproduzione: [**MCIWndPlayFrom,**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)e [**MCIWndPlayFromTo.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)

È anche necessario impostare un formato di ora appropriato. Il formato dell'ora determina se il contenuto viene misurato in fotogrammi, millisecondi, tracce o altre unità.

L'esempio seguente crea una finestra MCIWnd e fornisce comandi di menu per riprodurre l'ultimo terzo, primo terzo o terzo intermedio del contenuto. Questi comandi di menu **usano MCIWndPlayFrom,** **MCIWndPlayTo** e **MCIWndPlayFromTo** per riprodurre i segmenti di contenuto. L'esempio usa anche le macro [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) e [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) per identificare l'inizio e la fine del contenuto e usa la macro [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) per spostare la posizione di riproduzione all'inizio del contenuto.

La funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) usa gli stili WS CAPTION e MCIWNDF SHOWALL oltre agli stili della finestra standard per visualizzare il nome file, la modalità e la posizione di riproduzione corrente nella barra del titolo della \_ \_ finestra MCIWnd.


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE | WS_CAPTION | 
                MCIWNDF_SHOWALL, 
                "sample.avi"); 
            break;
        case IDM_PLAYFROM:                // plays last third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback end position. 
            lPlayStart = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFrom(g_hwndMCIWnd, lPlayStart); 
            break; 
        case IDM_PLAYTO:                  // plays first third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start position. 
            lPlayEnd = (lEnd - lStart) / 3 + lStart;
 
            MCIWndHome(g_hwndMCIWnd); 
            MCIWndPlayTo(g_hwndMCIWnd, lPlayEnd); 
            break; 
        case IDM_PLAYSOME:               // plays middle third of clip 
            MCIWndUseTime(g_hwndMCIWnd); // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start and end positions. 
            lPlayStart = (lEnd - lStart) / 3 + lStart;
            lPlayEnd = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFromTo(g_hwndMCIWnd, lPlayStart, lPlayEnd); 
            break; 
    
    // Handle other commands here. 
    } 
```



 

 




