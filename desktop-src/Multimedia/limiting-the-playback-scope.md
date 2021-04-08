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
# <a name="limiting-the-playback-scope"></a><span data-ttu-id="9017f-107">Limitazione dell'ambito di riproduzione</span><span class="sxs-lookup"><span data-stu-id="9017f-107">Limiting the Playback Scope</span></span>

<span data-ttu-id="9017f-108">Il controllo della riproduzione inizia con la macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) , che riproduce il contenuto o il file associato a una finestra di MCIWnd dalla posizione di riproduzione corrente fino alla fine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="9017f-108">Controlling playback begins with the [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) macro, which plays the content or file associated with an MCIWnd window from the current playback position to the end of the content.</span></span> <span data-ttu-id="9017f-109">Se si vuole limitare la riproduzione a una parte specifica del contenuto o del file, è possibile scegliere tra le altre macro MCIWnd di riproduzione: [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom), [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)e [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto).</span><span class="sxs-lookup"><span data-stu-id="9017f-109">If you want to limit playback to a specific portion of the content or file, you can choose from the other playback MCIWnd macros: [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom), [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto), and [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto).</span></span>

<span data-ttu-id="9017f-110">È anche necessario impostare un formato di ora appropriato.</span><span class="sxs-lookup"><span data-stu-id="9017f-110">You also need to set an appropriate time format.</span></span> <span data-ttu-id="9017f-111">Il formato dell'ora determina se il contenuto viene misurato in frame, millisecondi, tracce o altre unità.</span><span class="sxs-lookup"><span data-stu-id="9017f-111">The time format determines whether the content is measured in frames, milliseconds, tracks, or some other units.</span></span>

<span data-ttu-id="9017f-112">Nell'esempio seguente viene creata una finestra MCIWnd e vengono forniti i comandi di menu per riprodurre l'ultimo terzo, il primo terzo o il terzo medio del contenuto.</span><span class="sxs-lookup"><span data-stu-id="9017f-112">The following example creates an MCIWnd window and provides menu commands to play the last third, first third, or middle third of the content.</span></span> <span data-ttu-id="9017f-113">Questi comandi di menu usano **MCIWndPlayFrom**, **MCIWndPlayTo** e **MCIWndPlayFromTo** per riprodurre i segmenti di contenuto.</span><span class="sxs-lookup"><span data-stu-id="9017f-113">These menu commands use **MCIWndPlayFrom**, **MCIWndPlayTo**, and **MCIWndPlayFromTo** to play the content segments.</span></span> <span data-ttu-id="9017f-114">Nell'esempio vengono inoltre utilizzate le macro [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) e [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) per identificare l'inizio e la fine del contenuto e viene utilizzata la macro [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) per spostare la posizione di riproduzione all'inizio del contenuto.</span><span class="sxs-lookup"><span data-stu-id="9017f-114">The example also uses the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) and [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macros to identify the beginning and end of the content, and it uses the [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) macro to move the playback position to the beginning of the content.</span></span>

<span data-ttu-id="9017f-115">La funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) usa gli stili WS \_ Caption e MCIWNDF \_ ShowAll, oltre agli stili standard della finestra per visualizzare il nome del file, la modalità e la posizione di riproduzione corrente nella barra del titolo della finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="9017f-115">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function uses the WS\_CAPTION and MCIWNDF\_SHOWALL styles in addition to the standard window styles to display the filename, mode, and current playback position in the title bar of the MCIWnd window.</span></span>


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



 

 




