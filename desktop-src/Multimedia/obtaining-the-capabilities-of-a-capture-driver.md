---
title: Recupero delle funzionalità di un driver di acquisizione
description: Recupero delle funzionalità di un driver di acquisizione
ms.assetid: 17e90ca6-3646-41cb-8d7a-a2102bc16cc5
keywords:
- WM_CAP_DRIVER_GET_CAPS messaggio
- Macro capDriverGetCaps
- Struttura CAPDRIVERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6f717f1a7c19878ceeca2cccc2db309be3e62e0febf90dcb23376db73eed17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806571"
---
# <a name="obtaining-the-capabilities-of-a-capture-driver"></a>Recupero delle funzionalità di un driver di acquisizione

Il [**messaggio WM CAP DRIVER GET \_ \_ \_ \_ CAPS**](wm-cap-driver-get-caps.md) restituisce le funzionalità del driver di acquisizione e dell'hardware sottostante nella [**struttura CAPDRIVERCAPS.**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) Ogni volta che un'applicazione connette un nuovo driver di acquisizione alla finestra di acquisizione, deve aggiornare la **struttura CAPDRIVERCAPS.** Nell'esempio seguente viene utilizzata la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) per ottenere le funzionalità del driver di acquisizione.


```C++
CAPDRIVERCAPS CapDrvCaps; 

SendMessage (hWndC, WM_CAP_DRIVER_GET_CAPS, 
    sizeof (CAPDRIVERCAPS), (LONG) (LPVOID) &CapDrvCaps); 

// Or, use the macro to retrieve the driver capabilities. 
// capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




