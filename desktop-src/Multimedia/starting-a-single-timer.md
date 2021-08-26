---
title: Avvio di un singolo evento timer
description: Avvio di un singolo evento timer
ms.assetid: 56010877-1a02-4a7b-b58c-9f96b169acb2
keywords:
- timer multimediali, eventi
- timer, eventi
- timer multimediali, eventi di avvio
- timer, eventi di avvio
- Funzione timeSetEvent
- avvio di eventi timer
- eventi timer singoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc3a4c69aefe8df3310c8ff974ef7592b435eabccd661bdbeb1ebbf85dc3c9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037171"
---
# <a name="starting-a-single-timer-event"></a>Avvio di un singolo evento timer

> [!Note]  
> In questo argomento viene descritta una funzione obsoleta. Le nuove applicazioni devono usare [**la funzione CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) per creare timer.

 

Per avviare un singolo evento timer, chiamare la funzione [**timeSetEvent,**](/previous-versions//dd757634(v=vs.85)) specificando l'intervallo di tempo prima che si verifichi il callback, la risoluzione, l'indirizzo della funzione di callback (vedere [**TimeProc**](/previous-versions//dd757631(v=vs.85))) e i dati utente da fornire con la funzione di callback. Un'applicazione può usare una funzione simile alla seguente per avviare un singolo evento timer.


```C++
UINT SetTimerCallback(NPSEQ npSeq,  // sequencer data
    UINT msInterval)                // event interval
{ 
    npSeq->wTimerID = timeSetEvent(
        msInterval,                    // delay
        wTimerRes,                     // resolution (global variable)
        OneShotCallback,               // callback function
        (DWORD)npSeq,                  // user data
        TIME_ONESHOT );                // single timer event
    if(! npSeq->wTimerID)
        return ERR_TIMER;
    else
        return ERR_NOERROR;
} 

```



Per un esempio della funzione di callback OneShotCallback, vedere [Scrittura di una funzione di callback del timer.](writing-a-timer-callback-function.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di timer multimediali](using-multimedia-timers.md)
</dt> </dl>

 

 