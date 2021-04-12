---
title: Avvio di un singolo evento timer
description: Avvio di un singolo evento timer
ms.assetid: 56010877-1a02-4a7b-b58c-9f96b169acb2
keywords:
- timer multimediali, eventi
- timer, eventi
- timer multimediali, eventi di avvio
- timer, eventi di avvio
- Funzione timeSetEvent (funzione)
- avvio di eventi timer
- eventi timer singolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9d0024e3dfa9b0bda79f209abd9b81e89ad11c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398903"
---
# <a name="starting-a-single-timer-event"></a>Avvio di un singolo evento timer

> [!Note]  
> In questo argomento viene descritta una funzione obsoleta. Per creare i timer, le nuove applicazioni devono usare la funzione [**CreateTimerQueueTimer ha provocato**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) .

 

Per avviare un singolo evento del timer, chiamare la funzione [**funzione timeSetEvent**](/previous-versions//dd757634(v=vs.85)) , specificando la quantità di tempo prima che si verifichi il callback, la risoluzione, l'indirizzo della funzione di callback (vedere [**TimeProc**](/previous-versions//dd757631(v=vs.85))) e i dati utente da fornire con la funzione di callback. Un'applicazione può utilizzare una funzione come la seguente per avviare un singolo evento del timer.


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



Per un esempio della funzione di callback OneShotCallback, vedere [scrittura di una funzione di callback del timer](writing-a-timer-callback-function.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di timer multimediali](using-multimedia-timers.md)
</dt> </dl>

 

 