---
title: Annullamento di un evento timer
description: Annullamento di un evento timer
ms.assetid: 4c1be031-e3d5-4d7c-b197-c40c61fc4e2f
keywords:
- timer multimediali, eventi
- timer, eventi
- timeKillEvent (funzione)
- annullamento degli eventi del timer
- timer multimediali, annullamento di eventi
- timer, annullamento di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1380b2868596e0177e806f5df5217bb839abe61c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046707"
---
# <a name="canceling-a-timer-event"></a>Annullamento di un evento timer

> [!Note]  
> In questo argomento viene descritta una funzione obsoleta. Per creare i timer, le nuove applicazioni devono usare la funzione [**CreateTimerQueueTimer ha provocato**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) .

 

Per ogni timer periodico che crea chiamando [**funzione timeSetEvent**](/previous-versions//dd757634(v=vs.85)), l'applicazione deve annullare il timer chiamando la funzione [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) prima di liberare la memoria che contiene la funzione di callback. Per annullare un evento timer, è possibile che venga chiamata la funzione seguente.


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

 

 