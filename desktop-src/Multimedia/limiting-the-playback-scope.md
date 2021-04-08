---
title: Limitazione dell'ambito di riproduzione
description: Limitazione dell'ambito di riproduzione
ms.assetid: 080ab96f-1cb5-48d4-ac0a-8fd9ba68a31a
keywords:
- MCIWndPlayFrom (macro)
- MCIWndPlayTo (macro)
- MCIWndPlayFromTo (macro)
- Comandi di riproduzione MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 465bcf7a7b6b5811de8413a1c89f7befcf81037f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855874"
---
# <a name="limiting-the-playback-scope"></a>Limitazione dell'ambito di riproduzione

Il controllo della riproduzione inizia con la macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) , che riproduce il contenuto o il file associato a una finestra di MCIWnd dalla posizione di riproduzione corrente fino alla fine del contenuto. Se si vuole limitare la riproduzione a una parte specifica del contenuto o del file, è possibile scegliere tra le altre macro MCIWnd di riproduzione: [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom), [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)e [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto).

È anche necessario impostare un formato di ora appropriato. Il formato dell'ora determina se il contenuto viene misurato in frame, millisecondi, tracce o altre unità.

Nell'esempio seguente viene creata una finestra MCIWnd e vengono forniti i comandi di menu per riprodurre l'ultimo terzo, il primo terzo o il terzo medio del contenuto. Questi comandi di menu usano **MCIWndPlayFrom**, **MCIWndPlayTo** e **MCIWndPlayFromTo** per riprodurre i segmenti di contenuto. Nell'esempio vengono inoltre utilizzate le macro [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) e [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) per identificare l'inizio e la fine del contenuto e viene utilizzata la macro [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) per spostare la posizione di riproduzione all'inizio del contenuto.

La funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) usa gli stili WS \_ Caption e MCIWNDF \_ ShowAll, oltre agli stili standard della finestra per visualizzare il nome del file, la modalità e la posizione di riproduzione corrente nella barra del titolo della finestra MCIWnd.


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



 

 




