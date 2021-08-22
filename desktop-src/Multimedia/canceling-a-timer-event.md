---
title: Annullamento di un evento timer
description: Annullamento di un evento timer
ms.assetid: 4c1be031-e3d5-4d7c-b197-c40c61fc4e2f
keywords:
- timer multimediali, eventi
- timer, eventi
- Funzione timeKillEvent
- annullamento di eventi timer
- timer multimediali, annullamento di eventi
- timer, annullamento di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab4e9a92a02dca8ffd4723685fc96cdb0f82fc34a0fa2e3481a71a51997c316
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691792"
---
# <a name="canceling-a-timer-event"></a>Annullamento di un evento timer

> [!Note]  
> In questo argomento viene descritta una funzione obsoleta. Le nuove applicazioni devono usare [**la funzione CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) per creare timer.

 

Per ogni timer periodico creato chiamando [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)), l'applicazione deve annullare il timer chiamando la funzione [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) prima di liberare la memoria che contiene la funzione di callback. Per annullare un evento timer, potrebbe chiamare la funzione seguente.


```C++
void DestroyTimer(NPSEQ npSeq)
{
    if(npSeq->wTimerID) {                // is timer event pending?
        timeKillEvent(npSeq->wTimerID);  // cancel the event
        npSeq->wTimerID = 0;
    }
} 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di timer multimediali](using-multimedia-timers.md)
</dt> </dl>

 

 