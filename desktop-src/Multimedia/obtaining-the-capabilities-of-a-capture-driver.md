---
title: Acquisizione delle funzionalità di un driver di acquisizione
description: Acquisizione delle funzionalità di un driver di acquisizione
ms.assetid: 17e90ca6-3646-41cb-8d7a-a2102bc16cc5
keywords:
- Messaggio WM_CAP_DRIVER_GET_CAPS
- capDriverGetCaps (macro)
- Struttura CAPDRIVERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d15a3b1e01ccff738494f287126b7e1ab033056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298997"
---
# <a name="obtaining-the-capabilities-of-a-capture-driver"></a><span data-ttu-id="65c85-106">Acquisizione delle funzionalità di un driver di acquisizione</span><span class="sxs-lookup"><span data-stu-id="65c85-106">Obtaining the Capabilities of a Capture Driver</span></span>

<span data-ttu-id="65c85-107">Il messaggio [**WM \_ Cap \_ driver \_ get \_ Caps**](wm-cap-driver-get-caps.md) restituisce le funzionalità del driver di acquisizione e dell'hardware sottostante nella struttura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="65c85-107">The [**WM\_CAP\_DRIVER\_GET\_CAPS**](wm-cap-driver-get-caps.md) message returns the capabilities of the capture driver and underlying hardware in the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span> <span data-ttu-id="65c85-108">Ogni volta che un'applicazione connette un nuovo driver di acquisizione alla finestra di acquisizione, deve aggiornare la struttura **CAPDRIVERCAPS** .</span><span class="sxs-lookup"><span data-stu-id="65c85-108">Each time an application connects a new capture driver to the capture window, it should update the **CAPDRIVERCAPS** structure.</span></span> <span data-ttu-id="65c85-109">Nell'esempio seguente viene usata la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) per ottenere le funzionalità del driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="65c85-109">The following example uses the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro to obtain the capture driver capabilities.</span></span>


```C++
CAPDRIVERCAPS CapDrvCaps; 

SendMessage (hWndC, WM_CAP_DRIVER_GET_CAPS, 
    sizeof (CAPDRIVERCAPS), (LONG) (LPVOID) &CapDrvCaps); 

// Or, use the macro to retrieve the driver capabilities. 
// capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 
```



## <a name="related-topics"></a><span data-ttu-id="65c85-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65c85-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65c85-111">Uso di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="65c85-111">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




