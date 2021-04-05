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
# <a name="canceling-a-timer-event"></a><span data-ttu-id="e7107-109">Annullamento di un evento timer</span><span class="sxs-lookup"><span data-stu-id="e7107-109">Canceling a Timer Event</span></span>

> [!Note]  
> <span data-ttu-id="e7107-110">In questo argomento viene descritta una funzione obsoleta.</span><span class="sxs-lookup"><span data-stu-id="e7107-110">This topic describes an obsolete function.</span></span> <span data-ttu-id="e7107-111">Per creare i timer, le nuove applicazioni devono usare la funzione [**CreateTimerQueueTimer ha provocato**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="e7107-111">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="e7107-112">Per ogni timer periodico che crea chiamando [**funzione timeSetEvent**](/previous-versions//dd757634(v=vs.85)), l'applicazione deve annullare il timer chiamando la funzione [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) prima di liberare la memoria che contiene la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="e7107-112">For every periodic timer creating by calling [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)), the application must cancel the timer by calling the [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) function before it frees the memory that contains the callback function.</span></span> <span data-ttu-id="e7107-113">Per annullare un evento timer, è possibile che venga chiamata la funzione seguente.</span><span class="sxs-lookup"><span data-stu-id="e7107-113">To cancel a timer event, it might call the following function.</span></span>


```C++
void DestroyTimer(NPSEQ npSeq)
{
    if(npSeq->wTimerID) {                // is timer event pending?
        timeKillEvent(npSeq->wTimerID);  // cancel the event
        npSeq->wTimerID = 0;
    }
} 
```



## <a name="related-topics"></a><span data-ttu-id="e7107-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7107-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7107-115">Uso di timer multimediali</span><span class="sxs-lookup"><span data-stu-id="e7107-115">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 