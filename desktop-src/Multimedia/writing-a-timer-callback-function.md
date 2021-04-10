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
# <a name="writing-a-timer-callback-function"></a><span data-ttu-id="3260a-108">Scrittura di una funzione di callback timer</span><span class="sxs-lookup"><span data-stu-id="3260a-108">Writing a Timer Callback Function</span></span>

> [!Note]  
> <span data-ttu-id="3260a-109">In questo argomento viene descritta una funzione obsoleta.</span><span class="sxs-lookup"><span data-stu-id="3260a-109">This topic describes an obsolete function.</span></span> <span data-ttu-id="3260a-110">Per creare i timer, le nuove applicazioni devono usare la funzione [**CreateTimerQueueTimer ha provocato**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="3260a-110">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="3260a-111">La funzione di callback seguente, OneShotTimer, invalida l'identificatore per l'evento del timer singolo e chiama una routine timer per gestire le attività specifiche dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3260a-111">The following callback function, OneShotTimer, invalidates the identifier for the single timer event and calls a timer routine to handle the application-specific tasks.</span></span> <span data-ttu-id="3260a-112">Per ulteriori informazioni, vedere [**TimeProc**](/previous-versions//dd757631(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3260a-112">For more information, see [**TimeProc**](/previous-versions//dd757631(v=vs.85)).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3260a-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3260a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3260a-114">Uso di timer multimediali</span><span class="sxs-lookup"><span data-stu-id="3260a-114">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 