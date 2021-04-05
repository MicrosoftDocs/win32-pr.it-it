---
title: Risoluzione del timer
description: Risoluzione del timer
ms.assetid: 2e5e94fe-8175-417f-8c59-9d5cf052ea89
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
- timeEndPeriod (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e96f1b410f2e18203af794ea124bb6b83bccce
ms.sourcegitcommit: a0b531d335bc691100149830b256d5af7e136c24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/28/2019
ms.locfileid: "103706991"
---
# <a name="timer-resolution"></a><span data-ttu-id="2d2b3-114">Risoluzione del timer</span><span class="sxs-lookup"><span data-stu-id="2d2b3-114">Timer Resolution</span></span>

<span data-ttu-id="2d2b3-115">Per determinare le risoluzioni del timer minime e massime supportate dai servizi timer, utilizzare la funzione [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="2d2b3-115">To determine the minimum and maximum timer resolutions supported by the timer services, use the [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) function.</span></span> <span data-ttu-id="2d2b3-116">Questa funzione compila i membri **wPeriodMin** e **WPeriodMax** della struttura [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) con le risoluzioni minime e massime.</span><span class="sxs-lookup"><span data-stu-id="2d2b3-116">This function fills the **wPeriodMin** and **wPeriodMax** members of the [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) structure with the minimum and maximum resolutions.</span></span> <span data-ttu-id="2d2b3-117">Questo intervallo può variare tra computer e piattaforme Windows.</span><span class="sxs-lookup"><span data-stu-id="2d2b3-117">This range can vary across computers and Windows platforms.</span></span>

<span data-ttu-id="2d2b3-118">Dopo aver determinato le risoluzioni timer minime e massime disponibili, è necessario stabilire la risoluzione minima che si desidera venga utilizzata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d2b3-118">After you determine the minimum and maximum available timer resolutions, you must establish the minimum resolution you want your application to use.</span></span> <span data-ttu-id="2d2b3-119">Usare le funzioni [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) e [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) per impostare e cancellare questa risoluzione.</span><span class="sxs-lookup"><span data-stu-id="2d2b3-119">Use the [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) functions to set and clear this resolution.</span></span> <span data-ttu-id="2d2b3-120">È necessario associare ogni chiamata a **timeBeginPeriod** con una chiamata a **timeEndPeriod**, specificando la stessa risoluzione minima in entrambe le chiamate.</span><span class="sxs-lookup"><span data-stu-id="2d2b3-120">You must match each call to **timeBeginPeriod** with a call to **timeEndPeriod**, specifying the same minimum resolution in both calls.</span></span> <span data-ttu-id="2d2b3-121">Un'applicazione può effettuare più chiamate **timeBeginPeriod** , purché ogni chiamata corrisponda a una chiamata a **timeEndPeriod**.</span><span class="sxs-lookup"><span data-stu-id="2d2b3-121">An application can make multiple **timeBeginPeriod** calls, as long as each call is matched with a call to **timeEndPeriod**.</span></span>

<span data-ttu-id="2d2b3-122">In [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) e [**TimeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod)il parametro *uPeriod* indica la risoluzione minima del timer, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="2d2b3-122">In both [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod), the *uPeriod* parameter indicates the minimum timer resolution, in milliseconds.</span></span> <span data-ttu-id="2d2b3-123">È possibile specificare qualsiasi valore di risoluzione del timer compreso nell'intervallo supportato dal timer.</span><span class="sxs-lookup"><span data-stu-id="2d2b3-123">You can specify any timer resolution value within the range supported by the timer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d2b3-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d2b3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d2b3-125">Informazioni sui timer multimediali</span><span class="sxs-lookup"><span data-stu-id="2d2b3-125">About Multimedia Timers</span></span>](about-multimedia-timers.md)
</dt> </dl>

 

 




