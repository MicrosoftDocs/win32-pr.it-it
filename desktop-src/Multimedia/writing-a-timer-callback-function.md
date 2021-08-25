---
title: Scrittura di una funzione di callback del timer
description: Scrittura di una funzione di callback del timer
ms.assetid: 85260b6b-42de-43f4-83b7-94edbf660006
keywords:
- timer multimediali, funzioni di callback
- timer, funzioni di callback
- scrittura di funzioni di callback del timer
- timer multimediali, scrittura di funzioni di callback
- timer, scrittura di funzioni di callback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b8680fc4d697c33514276276daaa2a4d75577bfbd78fa3caffc7f426ca9d70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891781"
---
# <a name="writing-a-timer-callback-function"></a>Scrittura di una funzione di callback del timer

> [!Note]  
> Questo argomento descrive una funzione obsoleta. Le nuove applicazioni devono usare [**la funzione CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) per creare timer.

 

La funzione di callback seguente, OneShotTimer, invalida l'identificatore per il singolo evento timer e chiama una routine timer per gestire le attività specifiche dell'applicazione. Per altre informazioni, vedere [**TimeProc**](/previous-versions//dd757631(v=vs.85)).


```C++
void CALLBACK OneShotTimer(UINT wTimerID, UINT msg, 
    DWORD dwUser, DWORD dw1, DWORD dw2) 
{ 
    NPSEQ npSeq;             // pointer to sequencer data 
    npSeq = (NPSEQ)dwUser;
    npSeq->wTimerID = 0;     // invalidate timer ID (no longer in use)
    TimerRoutine(npSeq);     // handle tasks 
} 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di timer multimediali](using-multimedia-timers.md)
</dt> </dl>

 

 