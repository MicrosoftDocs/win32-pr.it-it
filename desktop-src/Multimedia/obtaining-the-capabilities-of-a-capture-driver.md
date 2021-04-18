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
# <a name="obtaining-the-capabilities-of-a-capture-driver"></a>Acquisizione delle funzionalità di un driver di acquisizione

Il messaggio [**WM \_ Cap \_ driver \_ get \_ Caps**](wm-cap-driver-get-caps.md) restituisce le funzionalità del driver di acquisizione e dell'hardware sottostante nella struttura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) . Ogni volta che un'applicazione connette un nuovo driver di acquisizione alla finestra di acquisizione, deve aggiornare la struttura **CAPDRIVERCAPS** . Nell'esempio seguente viene usata la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) per ottenere le funzionalità del driver di acquisizione.


```C++
CAPDRIVERCAPS CapDrvCaps; 

SendMessage (hWndC, WM_CAP_DRIVER_GET_CAPS, 
    sizeof (CAPDRIVERCAPS), (LONG) (LPVOID) &CapDrvCaps); 

// Or, use the macro to retrieve the driver capabilities. 
// capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




