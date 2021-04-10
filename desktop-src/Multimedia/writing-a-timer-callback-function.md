---
title: Scrittura di una funzione di callback timer
description: Scrittura di una funzione di callback timer
ms.assetid: 85260b6b-42de-43f4-83b7-94edbf660006
keywords:
- timer multimediali, funzioni di callback
- timer, funzioni di callback
- scrittura di funzioni di callback timer
- timer multimediali, scrittura di funzioni di callback
- timer, scrittura di funzioni di callback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609cf2dda455897fb6cae0f3c48252016ba54cb9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956405"
---
# <a name="writing-a-timer-callback-function"></a>Scrittura di una funzione di callback timer

> [!Note]  
> In questo argomento viene descritta una funzione obsoleta. Per creare i timer, le nuove applicazioni devono usare la funzione [**CreateTimerQueueTimer ha provocato**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) .

 

La funzione di callback seguente, OneShotTimer, invalida l'identificatore per l'evento del timer singolo e chiama una routine timer per gestire le attività specifiche dell'applicazione. Per ulteriori informazioni, vedere [**TimeProc**](/previous-versions//dd757631(v=vs.85)).


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

 

 