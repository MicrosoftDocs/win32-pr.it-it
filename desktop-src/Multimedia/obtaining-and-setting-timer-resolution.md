---
title: Recupero e impostazione della risoluzione del timer
description: Recupero e impostazione della risoluzione del timer
ms.assetid: 237a6770-89b9-4922-b9e9-0e0bf3e0c9b6
keywords:
- timer multimediali, risoluzione
- timer, risoluzione
- risoluzione minima del timer
- risoluzione del timer massima
- timer multimediali, risoluzione massima
- timer, risoluzione massima
- timer multimediali, risoluzione minima
- timer, risoluzione minima
- timeGetDevCaps (funzione)
- timeBeginPeriod (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af5feca59e6fb4c528d6042b00eb7aa23263245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298129"
---
# <a name="obtaining-and-setting-timer-resolution"></a>Recupero e impostazione della risoluzione del timer

Nell'esempio seguente viene chiamata la funzione [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) per determinare le risoluzioni del timer minime e massime supportate dai servizi timer. Prima di configurare gli eventi del timer, l'esempio stabilisce la risoluzione minima del timer tramite la funzione [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) .


```C++
#define TARGET_RESOLUTION 1         // 1-millisecond target resolution

TIMECAPS tc;
UINT     wTimerRes;

if (timeGetDevCaps(&tc, sizeof(TIMECAPS)) != TIMERR_NOERROR) 
{
    // Error; application can't continue.
}

wTimerRes = min(max(tc.wPeriodMin, TARGET_RESOLUTION), tc.wPeriodMax);
timeBeginPeriod(wTimerRes); 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di timer multimediali](using-multimedia-timers.md)
</dt> </dl>

 

 




