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
# <a name="starting-a-single-timer-event"></a><span data-ttu-id="19edf-110">Avvio di un singolo evento timer</span><span class="sxs-lookup"><span data-stu-id="19edf-110">Starting a Single Timer Event</span></span>

> [!Note]  
> <span data-ttu-id="19edf-111">In questo argomento viene descritta una funzione obsoleta.</span><span class="sxs-lookup"><span data-stu-id="19edf-111">This topic describes an obsolete function.</span></span> <span data-ttu-id="19edf-112">Per creare i timer, le nuove applicazioni devono usare la funzione [**CreateTimerQueueTimer ha provocato**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="19edf-112">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="19edf-113">Per avviare un singolo evento del timer, chiamare la funzione [**funzione timeSetEvent**](/previous-versions//dd757634(v=vs.85)) , specificando la quantità di tempo prima che si verifichi il callback, la risoluzione, l'indirizzo della funzione di callback (vedere [**TimeProc**](/previous-versions//dd757631(v=vs.85))) e i dati utente da fornire con la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="19edf-113">To start a single timer event, call the [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) function, specifying the amount of time before the callback occurs, the resolution, the address of the callback function (see [**TimeProc**](/previous-versions//dd757631(v=vs.85))), and the user data to supply with the callback function.</span></span> <span data-ttu-id="19edf-114">Un'applicazione può utilizzare una funzione come la seguente per avviare un singolo evento del timer.</span><span class="sxs-lookup"><span data-stu-id="19edf-114">An application can use a function like the following to start a single timer event.</span></span>


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



<span data-ttu-id="19edf-115">Per un esempio della funzione di callback OneShotCallback, vedere [scrittura di una funzione di callback del timer](writing-a-timer-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="19edf-115">For an example of the callback function OneShotCallback, see [Writing a Timer Callback Function](writing-a-timer-callback-function.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="19edf-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="19edf-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19edf-117">Uso di timer multimediali</span><span class="sxs-lookup"><span data-stu-id="19edf-117">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 