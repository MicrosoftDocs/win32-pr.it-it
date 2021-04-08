---
description: Creazione di composizioni e tracce di gruppi
ms.assetid: c3bef3cd-5e3c-42c5-850f-b4cb00c414bd
title: Creazione di composizioni e tracce di gruppi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2808c2d096b52ad73da7d518d703bc25103751d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103877025"
---
# <a name="creating-groups-compositions-and-tracks"></a><span data-ttu-id="1727c-103">Creazione di composizioni e tracce di gruppi</span><span class="sxs-lookup"><span data-stu-id="1727c-103">Creating Groups Compositions and Tracks</span></span>

<span data-ttu-id="1727c-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="1727c-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="1727c-105">Gruppi, composizioni e tracce sono i livelli intermedi tra la sequenza temporale e i clip di origine.</span><span class="sxs-lookup"><span data-stu-id="1727c-105">Groups, compositions, and tracks are the intermediate layers between the timeline and the source clips.</span></span> <span data-ttu-id="1727c-106">Sono distinti dal tipo di oggetto che possono contenere.</span><span class="sxs-lookup"><span data-stu-id="1727c-106">They are distinguished by the type of object they can contain.</span></span>

-   <span data-ttu-id="1727c-107">Le tracce contengono oggetti di origine.</span><span class="sxs-lookup"><span data-stu-id="1727c-107">Tracks contain source objects.</span></span>
-   <span data-ttu-id="1727c-108">Le composizioni contengono tracce e altre composizioni, ma non oggetti di origine.</span><span class="sxs-lookup"><span data-stu-id="1727c-108">Compositions contain tracks and other compositions, but not source objects.</span></span>
-   <span data-ttu-id="1727c-109">I gruppi sono composizioni di primo livello.</span><span class="sxs-lookup"><span data-stu-id="1727c-109">Groups are top-level compositions.</span></span> <span data-ttu-id="1727c-110">I gruppi contengono composizioni e tracce, ma le composizioni non possono contenere gruppi.</span><span class="sxs-lookup"><span data-stu-id="1727c-110">Groups contain compositions and tracks, but compositions cannot contain groups.</span></span>
-   <span data-ttu-id="1727c-111">Una *traccia virtuale* è qualsiasi oggetto che può risiedere all'interno di una composizione o di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="1727c-111">A *virtual track* is any object that can reside inside a composition or a group.</span></span> <span data-ttu-id="1727c-112">Sono incluse le tracce e le composizioni.</span><span class="sxs-lookup"><span data-stu-id="1727c-112">This includes tracks and compositions.</span></span>

<span data-ttu-id="1727c-113">Questi oggetti espongono le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="1727c-113">These objects expose the following interfaces:</span></span>



| <span data-ttu-id="1727c-114">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="1727c-114">Interface</span></span>                                                  | <span data-ttu-id="1727c-115">Esposto da</span><span class="sxs-lookup"><span data-stu-id="1727c-115">Exposed By</span></span>           |
|------------------------------------------------------------|----------------------|
| [<span data-ttu-id="1727c-116">**IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="1727c-116">**IAMTimelineTrack**</span></span>](iamtimelinetrack.md)               | <span data-ttu-id="1727c-117">Brani</span><span class="sxs-lookup"><span data-stu-id="1727c-117">Tracks</span></span>               |
| [<span data-ttu-id="1727c-118">**IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="1727c-118">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md) | <span data-ttu-id="1727c-119">Tracce, composizioni</span><span class="sxs-lookup"><span data-stu-id="1727c-119">Tracks, Compositions</span></span> |
| [<span data-ttu-id="1727c-120">**IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="1727c-120">**IAMTimelineComp**</span></span>](iamtimelinecomp.md)                 | <span data-ttu-id="1727c-121">Composizioni, gruppi</span><span class="sxs-lookup"><span data-stu-id="1727c-121">Compositions, Groups</span></span> |
| [<span data-ttu-id="1727c-122">**IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="1727c-122">**IAMTimelineGroup**</span></span>](iamtimelinegroup.md)               | <span data-ttu-id="1727c-123">Gruppi</span><span class="sxs-lookup"><span data-stu-id="1727c-123">Groups</span></span>               |



 

<span data-ttu-id="1727c-124">Queste interfacce contengono i metodi per l'aggiunta di oggetti alla sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="1727c-124">These interfaces contain the methods for adding objects to the timeline.</span></span>

-   <span data-ttu-id="1727c-125">[**IAMTimeline:: addgroup**](iamtimeline-addgroup.md): inserisce un gruppo nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="1727c-125">[**IAMTimeline::AddGroup**](iamtimeline-addgroup.md): Inserts a group into the timeline.</span></span>
-   <span data-ttu-id="1727c-126">[**IAMTimelineComp:: VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md): inserisce una traccia virtuale in una composizione o un gruppo.</span><span class="sxs-lookup"><span data-stu-id="1727c-126">[**IAMTimelineComp::VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md): Inserts a virtual track into a composition or group.</span></span>
-   <span data-ttu-id="1727c-127">[**IAMTimelineTrack:: SrcAdd**](iamtimelinetrack-srcadd.md): inserisce un'origine in una traccia.</span><span class="sxs-lookup"><span data-stu-id="1727c-127">[**IAMTimelineTrack::SrcAdd**](iamtimelinetrack-srcadd.md): Inserts a source into a track.</span></span>

<span data-ttu-id="1727c-128">Il codice seguente, ad esempio, inserisce una nuova traccia in un gruppo.</span><span class="sxs-lookup"><span data-stu-id="1727c-128">For example, the following code inserts a new track into a group.</span></span> <span data-ttu-id="1727c-129">Come illustrato nella tabella precedente, un gruppo è considerato un tipo di composizione e una traccia è un tipo di traccia virtuale. Pertanto, per inserire la traccia nel gruppo, è necessario eseguire una query sul gruppo per la relativa interfaccia **IAMTimelineComp** e chiamare il metodo **IAMTimelineComp:: VTrackInsBefore** .</span><span class="sxs-lookup"><span data-stu-id="1727c-129">As shown in the previous table, a group is considered a kind of composition, and a track is a kind of virtual track. Therefore, to insert the track into the group, you must query the group for its **IAMTimelineComp** interface and call the **IAMTimelineComp::VTrackInsBefore** method.</span></span>


```C++
IAMTimelineGroup    *pGroup;
// Create a new group (not shown). 

IAMTimelineComp     *pComp = NULL;
IAMTimelineObj      *pTrackObj = NULL;

pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
pComp->VTrackInsBefore(pTrackObj, 0);
```



<span data-ttu-id="1727c-130">Il secondo parametro di **VTrackInsBefore** specifica la priorità della traccia virtuale. I livelli di priorità iniziano da zero.</span><span class="sxs-lookup"><span data-stu-id="1727c-130">The second parameter to **VTrackInsBefore** specifies the priority of the virtual track. Priority levels start at zero.</span></span> <span data-ttu-id="1727c-131">Se si specifica il valore-1, la traccia virtuale viene inserita alla fine dell'elenco di priorità.</span><span class="sxs-lookup"><span data-stu-id="1727c-131">If you specify the value –1, the virtual track is inserted at the end of the priority list.</span></span> <span data-ttu-id="1727c-132">Se si specifica un valore in cui è già presente una traccia virtuale, tutti gli elementi da quel punto in poi spostano verso il basso l'elenco in base a un livello di priorità.</span><span class="sxs-lookup"><span data-stu-id="1727c-132">If you specify a value where there is already a virtual track, everything from that point on moves down the list by one priority level.</span></span> <span data-ttu-id="1727c-133">Non inserire una traccia virtuale con una priorità maggiore del numero di tracce virtuali, perché provocherà un comportamento non definito.</span><span class="sxs-lookup"><span data-stu-id="1727c-133">Do not insert a virtual track at a priority greater than the number of virtual tracks, because it will cause undefined behavior.</span></span>

<span data-ttu-id="1727c-134">Per eliminare un oggetto in modo permanente dalla sequenza temporale, chiamare [**IAMTimelineObj:: RemoveAll**](iamtimelineobj-removeall.md) sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1727c-134">To delete an object permanently from the timeline, call [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md) on the object.</span></span> <span data-ttu-id="1727c-135">Questo metodo rimuove l'oggetto e tutti i relativi elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="1727c-135">This method removes the object and all its children.</span></span> <span data-ttu-id="1727c-136">Per rimuovere un oggetto per inserirlo in un'altra posizione nella sequenza temporale, chiamare invece [**IAMTimelineObj:: Remove**](iamtimelineobj-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="1727c-136">To remove an object for the purpose of reinserting it elsewhere in the timeline, call [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md) instead.</span></span> <span data-ttu-id="1727c-137">Diversamente da **RemoveAll**, questo metodo non elimina gli elementi figlio dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1727c-137">Unlike **RemoveAll**, this method does not delete the object's children.</span></span> <span data-ttu-id="1727c-138">Per rimuovere tutti gli elementi dalla sequenza temporale, chiamare [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md).</span><span class="sxs-lookup"><span data-stu-id="1727c-138">To remove everything from the timeline, call [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1727c-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1727c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1727c-140">Creazione di una sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="1727c-140">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



