---
description: Ore di clock
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Ore di clock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0639fd2b38e312f30f932fcf508427cd71c054
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401101"
---
# <a name="clock-times"></a><span data-ttu-id="71591-103">Ore di clock</span><span class="sxs-lookup"><span data-stu-id="71591-103">Clock Times</span></span>

<span data-ttu-id="71591-104">DirectShow definisce due ore di clock correlate: ora di riferimento e tempo di flusso.</span><span class="sxs-lookup"><span data-stu-id="71591-104">DirectShow defines two related clock times: reference time and stream time.</span></span>

-   <span data-ttu-id="71591-105">L' *ora di riferimento* è il tempo assoluto restituito dall'orologio di riferimento.</span><span class="sxs-lookup"><span data-stu-id="71591-105">*Reference time* is the absolute time returned by the reference clock.</span></span> <span data-ttu-id="71591-106">Vedere [clock di riferimento](reference-clocks.md).</span><span class="sxs-lookup"><span data-stu-id="71591-106">(See [Reference Clocks](reference-clocks.md).)</span></span>
-   <span data-ttu-id="71591-107">Il *tempo di flusso* viene definito rispetto al momento in cui è stata avviata l'ultima esecuzione del grafico.</span><span class="sxs-lookup"><span data-stu-id="71591-107">*Stream time* is defined relative to when the graph last started running.</span></span>
    -   <span data-ttu-id="71591-108">Mentre il grafico è in esecuzione, l'ora del flusso è uguale all'ora di riferimento meno l'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="71591-108">While the graph is running, stream time equals reference time minus start time.</span></span>
    -   <span data-ttu-id="71591-109">Quando il grafico è sospeso, il tempo di flusso rimane in corrispondenza dell'ora del flusso in cui è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="71591-109">While the graph is paused, stream time remains at the stream time when it was paused.</span></span>
    -   <span data-ttu-id="71591-110">Dopo un'operazione di ricerca, l'ora del flusso viene reimpostata su zero.</span><span class="sxs-lookup"><span data-stu-id="71591-110">After a seek operation, stream time resets to zero.</span></span>
    -   <span data-ttu-id="71591-111">Quando il grafico viene arrestato, il tempo di flusso non è definito.</span><span class="sxs-lookup"><span data-stu-id="71591-111">While the graph is stopped, stream time is undefined.</span></span>

<span data-ttu-id="71591-112">Quando un esempio di supporto presenta un timestamp *t*, significa che è necessario eseguire il rendering dell'esempio in corrispondenza del tempo di flusso *t*.</span><span class="sxs-lookup"><span data-stu-id="71591-112">When a media sample has a time stamp *t*, it means the sample should be rendered at stream time *t*.</span></span> <span data-ttu-id="71591-113">Per questo motivo, il tempo di flusso viene definito anche *tempo di presentazione*.</span><span class="sxs-lookup"><span data-stu-id="71591-113">For this reason, stream time is also called *presentation time*.</span></span>

<span data-ttu-id="71591-114">Quando un'applicazione chiama [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) per eseguire il grafico dei filtri, il gestore del grafo del filtro chiama [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) in ogni filtro.</span><span class="sxs-lookup"><span data-stu-id="71591-114">When an application calls [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the filter graph, the Filter Graph Manager calls [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) on each filter.</span></span> <span data-ttu-id="71591-115">Per compensare la lieve quantità di tempo necessaria per l'avvio dell'esecuzione dei filtri, il gestore del grafico del filtro specifica un'ora di inizio leggermente in futuro.</span><span class="sxs-lookup"><span data-stu-id="71591-115">To compensate for the slight amount of time it takes for the filters to start running, the Filter Graph Manager specifies a start time slightly in the future.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71591-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71591-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71591-117">Time and Clocks in DirectShow</span><span class="sxs-lookup"><span data-stu-id="71591-117">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="71591-118">Timestamp</span><span class="sxs-lookup"><span data-stu-id="71591-118">Time Stamps</span></span>](time-stamps.md)
</dt> </dl>

 

 



