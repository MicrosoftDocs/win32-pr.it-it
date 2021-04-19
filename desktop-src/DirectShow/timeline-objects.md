---
description: Oggetti Timeline
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: Oggetti Timeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580286b31afd77f064411dd29d60a62b80bfb51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319541"
---
# <a name="timeline-objects"></a><span data-ttu-id="aa9ea-103">Oggetti Timeline</span><span class="sxs-lookup"><span data-stu-id="aa9ea-103">Timeline Objects</span></span>

<span data-ttu-id="aa9ea-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="aa9ea-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="aa9ea-105">Ogni tipo di oggetto nella sequenza temporale, ovvero origine, traccia, effetto e così via, è un oggetto COM distinto.</span><span class="sxs-lookup"><span data-stu-id="aa9ea-105">Each type of object in the timeline—source, track, effect, and so forth—is a distinct COM object.</span></span> <span data-ttu-id="aa9ea-106">Tuttavia, un'applicazione non li crea utilizzando la funzione **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="aa9ea-106">However, an application does not create them using the **CoCreateInstance** function.</span></span> <span data-ttu-id="aa9ea-107">Chiama invece il metodo [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="aa9ea-107">Instead, it calls the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="aa9ea-108">Questo metodo crea un oggetto del tipo richiesto, lo inizializza e restituisce un puntatore all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aa9ea-108">This method creates an object of the requested type, initializes it, and returns a pointer to the object.</span></span> <span data-ttu-id="aa9ea-109">Per informazioni dettagliate, vedere [creazione di una sequenza temporale](constructing-a-timeline.md).</span><span class="sxs-lookup"><span data-stu-id="aa9ea-109">For details, see [Constructing a Timeline](constructing-a-timeline.md).</span></span>

<span data-ttu-id="aa9ea-110">Ogni oggetto sequenza temporale espone l'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) .</span><span class="sxs-lookup"><span data-stu-id="aa9ea-110">Every timeline object exposes the [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span> <span data-ttu-id="aa9ea-111">Inoltre, i vari tipi di oggetto supportano le proprie interfacce specializzate:</span><span class="sxs-lookup"><span data-stu-id="aa9ea-111">In addition, the various object types support their own specialized interfaces:</span></span>

-   <span data-ttu-id="aa9ea-112">Origine: [ **IAMTimelineSrc**](iamtimelinesrc.md)</span><span class="sxs-lookup"><span data-stu-id="aa9ea-112">Source: [**IAMTimelineSrc**](iamtimelinesrc.md)</span></span>
-   <span data-ttu-id="aa9ea-113">Traccia: [ **IAMTimelineTrack**](iamtimelinetrack.md)</span><span class="sxs-lookup"><span data-stu-id="aa9ea-113">Track: [**IAMTimelineTrack**](iamtimelinetrack.md)</span></span>
-   <span data-ttu-id="aa9ea-114">Composizione: [ **IAMTimelineComp**](iamtimelinecomp.md)</span><span class="sxs-lookup"><span data-stu-id="aa9ea-114">Composition: [**IAMTimelineComp**](iamtimelinecomp.md)</span></span>
-   <span data-ttu-id="aa9ea-115">Gruppo: [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)</span><span class="sxs-lookup"><span data-stu-id="aa9ea-115">Group: [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)</span></span>
-   <span data-ttu-id="aa9ea-116">Effetto: [ **IAMTimelineEffect**](iamtimelineeffect.md)</span><span class="sxs-lookup"><span data-stu-id="aa9ea-116">Effect: [**IAMTimelineEffect**](iamtimelineeffect.md)</span></span>
-   <span data-ttu-id="aa9ea-117">Transizione: [ **IAMTimelineTrans**](iamtimelinetrans.md)</span><span class="sxs-lookup"><span data-stu-id="aa9ea-117">Transition: [**IAMTimelineTrans**](iamtimelinetrans.md)</span></span>

<span data-ttu-id="aa9ea-118">Si noti che i gruppi sono un tipo di composizione, quindi supportano [**IAMTimelineComp**](iamtimelinecomp.md), nonché la propria interfaccia [**IAMTimelineGroup**](iamtimelinegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="aa9ea-118">Note that groups are a type of composition, so they support [**IAMTimelineComp**](iamtimelinecomp.md), as well as their own [**IAMTimelineGroup**](iamtimelinegroup.md) interface.</span></span>

<span data-ttu-id="aa9ea-119">Oltre alle interfacce elencate in precedenza, gli oggetti sequenza temporale espongono altre interfacce secondarie.</span><span class="sxs-lookup"><span data-stu-id="aa9ea-119">In addition to the interfaces listed previously, timeline objects expose other, secondary interfaces.</span></span> <span data-ttu-id="aa9ea-120">Queste interfacce determinano le relazioni tra i tipi di oggetto.</span><span class="sxs-lookup"><span data-stu-id="aa9ea-120">These interfaces determine the relationships between the object types.</span></span>



| <span data-ttu-id="aa9ea-121">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="aa9ea-121">Interface</span></span>                                                  | <span data-ttu-id="aa9ea-122">Significato</span><span class="sxs-lookup"><span data-stu-id="aa9ea-122">Meaning</span></span>                                                                                                       | <span data-ttu-id="aa9ea-123">Esposto da</span><span class="sxs-lookup"><span data-stu-id="aa9ea-123">Exposed By</span></span>                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [<span data-ttu-id="aa9ea-124">**IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="aa9ea-124">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md) | <span data-ttu-id="aa9ea-125">L'oggetto è una traccia virtuale. Le tracce virtuali possono risiedere all'interno di composizioni e tenere altri oggetti della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="aa9ea-125">The object is a virtual track. Virtual tracks can reside inside compositions and hold other timeline objects.</span></span> | <span data-ttu-id="aa9ea-126">Composizione, traccia</span><span class="sxs-lookup"><span data-stu-id="aa9ea-126">Composition, Track</span></span>                |
| [<span data-ttu-id="aa9ea-127">**IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="aa9ea-127">**IAMTimelineEffectable**</span></span>](iamtimelineeffectable.md)     | <span data-ttu-id="aa9ea-128">L'oggetto può avere effetti.</span><span class="sxs-lookup"><span data-stu-id="aa9ea-128">The object can have effects.</span></span>                                                                                  | <span data-ttu-id="aa9ea-129">Composizione, traccia, origine</span><span class="sxs-lookup"><span data-stu-id="aa9ea-129">Composition, Track, Source</span></span>        |
| [<span data-ttu-id="aa9ea-130">**IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="aa9ea-130">**IAMTimelineTransable**</span></span>](iamtimelinetransable.md)       | <span data-ttu-id="aa9ea-131">L'oggetto può avere transizioni.</span><span class="sxs-lookup"><span data-stu-id="aa9ea-131">The object can have transitions.</span></span>                                                                              | <span data-ttu-id="aa9ea-132">Composizione, traccia</span><span class="sxs-lookup"><span data-stu-id="aa9ea-132">Composition, Track</span></span>                |
| [<span data-ttu-id="aa9ea-133">**IAMTimelineSplittable**</span><span class="sxs-lookup"><span data-stu-id="aa9ea-133">**IAMTimelineSplittable**</span></span>](iamtimelinesplittable.md)     | <span data-ttu-id="aa9ea-134">L'oggetto può essere suddiviso in due oggetti.</span><span class="sxs-lookup"><span data-stu-id="aa9ea-134">The object can be split into two objects.</span></span>                                                                     | <span data-ttu-id="aa9ea-135">Track, source, Effect, Transition</span><span class="sxs-lookup"><span data-stu-id="aa9ea-135">Track, Source, Effect, Transition</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="aa9ea-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa9ea-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa9ea-137">Panoramica dei componenti della sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="aa9ea-137">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



