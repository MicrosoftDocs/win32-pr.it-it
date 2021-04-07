---
description: Aggiunta di oggetti Effect e Transition
ms.assetid: fe82392f-33e2-432a-a6e3-710e475547b3
title: Aggiunta di oggetti Effect e Transition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6d33ed27faa0c69a755a17c72d9c5b136a4670
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048948"
---
# <a name="adding-effect-and-transition-objects"></a><span data-ttu-id="4e6d9-103">Aggiunta di oggetti Effect e Transition</span><span class="sxs-lookup"><span data-stu-id="4e6d9-103">Adding Effect and Transition Objects</span></span>

<span data-ttu-id="4e6d9-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="4e6d9-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="4e6d9-105">In DES un effetto o una transizione viene rappresentato con due oggetti:</span><span class="sxs-lookup"><span data-stu-id="4e6d9-105">In DES, an effect or transition is represented with two objects:</span></span>

-   <span data-ttu-id="4e6d9-106">Un *oggetto Timeline* rappresenta l'effetto o la transizione all'interno della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-106">A *timeline object* represents the effect or transition within the timeline.</span></span> <span data-ttu-id="4e6d9-107">Per gli effetti, l'oggetto Timeline supporta l'interfaccia [**IAMTimelineEffect**](iamtimelineeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="4e6d9-107">For effects, the timeline object supports the [**IAMTimelineEffect**](iamtimelineeffect.md) interface.</span></span> <span data-ttu-id="4e6d9-108">Per le transizioni, supporta l'interfaccia [**IAMTimelineTrans**](iamtimelinetrans.md) .</span><span class="sxs-lookup"><span data-stu-id="4e6d9-108">For transitions, it supports the [**IAMTimelineTrans**](iamtimelinetrans.md) interface.</span></span> <span data-ttu-id="4e6d9-109">Entrambi i tipi supportano l'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) .</span><span class="sxs-lookup"><span data-stu-id="4e6d9-109">Both types support the [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>
-   <span data-ttu-id="4e6d9-110">Il *sottooggetto* è un oggetto che implementa l'elaborazione dei dati per l'effetto o la transizione.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-110">The *subobject* is an object that implements the data processing for the effect or transition.</span></span> <span data-ttu-id="4e6d9-111">L'oggetto sequenza temporale include un puntatore all'oggetto SubObject.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-111">The timeline object holds a pointer to the subobject.</span></span>

<span data-ttu-id="4e6d9-112">Per aggiungere un effetto o una transizione, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-112">To add an effect or transition, perform the following steps.</span></span>

<span data-ttu-id="4e6d9-113">**1. creare l'oggetto sequenza temporale**</span><span class="sxs-lookup"><span data-stu-id="4e6d9-113">**1. Create the Timeline Object**</span></span>

<span data-ttu-id="4e6d9-114">Per creare l'oggetto sequenza temporale, chiamare il metodo [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="4e6d9-114">To create the timeline object, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="4e6d9-115">Impostare il tipo su un **\_ effetto del \_ tipo \_ principale della sequenza temporale** per un effetto o una **\_ \_ \_ transizione di tipo principale della sequenza temporale** per una transizione.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-115">Set the type equal to **TIMELINE\_MAJOR\_TYPE\_EFFECT** for an effect, or **TIMELINE\_MAJOR\_TYPE\_TRANSITION** for a transition.</span></span>

<span data-ttu-id="4e6d9-116">Nell'esempio seguente viene creato un oggetto di transizione:</span><span class="sxs-lookup"><span data-stu-id="4e6d9-116">The following example creates a transition object:</span></span>


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



<span data-ttu-id="4e6d9-117">**2. specificare l'oggetto SubObject**</span><span class="sxs-lookup"><span data-stu-id="4e6d9-117">**2. Specify the Subobject**</span></span>

<span data-ttu-id="4e6d9-118">L'oggetto sequenza temporale funge da wrapper per un altro oggetto, denominato *sottooggetto*, che esegue le operazioni effettive.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-118">The timeline object acts as a wrapper for another object, called the *subobject*, which does the real work.</span></span> <span data-ttu-id="4e6d9-119">L'oggetto SubObject implementa una trasformazione dei dati che produce l'effetto o la transizione desiderata.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-119">The subobject implements a data transform that produces the desired effect or transition.</span></span> <span data-ttu-id="4e6d9-120">Per un elenco delle transizioni e degli effetti forniti con DES, vedere [transizioni ed effetti](transitions-and-effects.md).</span><span class="sxs-lookup"><span data-stu-id="4e6d9-120">For a list of transitions and effects supplied with DES, see [Transitions and Effects](transitions-and-effects.md).</span></span>

<span data-ttu-id="4e6d9-121">Per impostare il sottooggetto, chiamare il metodo [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) sull'oggetto Timeline, passandogli l'identificatore di classe (CLSID) dell'oggetto SubObject.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-121">To set the subobject, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method on the timeline object, passing it the class identifier (CLSID) of the subobject.</span></span> <span data-ttu-id="4e6d9-122">DirectShow fornisce un enumeratore per gli effetti video e le transizioni video, che è possibile usare per ottenere il CLSID.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-122">DirectShow provides an enumerator for video effects and video transitions, which you can use to obtain the CLSID.</span></span> <span data-ttu-id="4e6d9-123">Per ulteriori informazioni, vedere [enumerazione degli effetti e delle transizioni](enumerating-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="4e6d9-123">For more information, see [Enumerating Effects and Transitions](enumerating-effects-and-transitions.md).</span></span>

<span data-ttu-id="4e6d9-124">Nell'esempio seguente viene impostata la [transizione di cancellazione SMPTE](smpte-wipe-transition.md) come oggetto SubObject:</span><span class="sxs-lookup"><span data-stu-id="4e6d9-124">The following example sets the [SMPTE Wipe Transition](smpte-wipe-transition.md) as the subobject :</span></span>


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



<span data-ttu-id="4e6d9-125">**3. impostare l'ora di inizio e di fine**</span><span class="sxs-lookup"><span data-stu-id="4e6d9-125">**3. Set the Start and Stop Times**</span></span>

<span data-ttu-id="4e6d9-126">Per impostare l'ora di inizio e di fine, chiamare il metodo [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) .</span><span class="sxs-lookup"><span data-stu-id="4e6d9-126">To set the start and stop times, call the [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) method.</span></span> <span data-ttu-id="4e6d9-127">Questi orari sono relativi all'ora di inizio dell'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-127">These times are relative to the start time of the parent object.</span></span> <span data-ttu-id="4e6d9-128">Gli effetti possono sovrapporsi all'interno dello stesso oggetto, ma le transizioni non possono.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-128">Effects can overlap within the same object, but transitions cannot.</span></span>

<span data-ttu-id="4e6d9-129">L'esempio seguente imposta l'ora di inizio su 5 secondi e l'ora di arresto su 10 secondi:</span><span class="sxs-lookup"><span data-stu-id="4e6d9-129">The following example sets the start time to 5 seconds and the stop time to 10 seconds:</span></span>


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



<span data-ttu-id="4e6d9-130">Quando viene eseguito il rendering di una transizione, lo stato di avanzamento della transizione in ogni frame viene calcolato in base a una proprietà **Progress** , che viene normalizzata in un intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-130">When a transition is rendered, the progress of the transition at each frame is calculated based on a **Progress** property, which is normalized to a range of 0.0 to 1.0.</span></span> <span data-ttu-id="4e6d9-131">DES usa l'ora di inizio di ogni frame per calcolare il valore di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-131">DES uses the start time of each frame to calculate the progress value.</span></span> <span data-ttu-id="4e6d9-132">Ciò significa che se l'ora di arresto della transizione è uguale all'ora di arresto dell'origine, il valore di **avanzamento** non raggiungerà mai esattamente 1,0, perché l'ora di inizio dell'ultimo frame è leggermente diversa dall'ora di arresto.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-132">This means if the transition stop time is equal to the source stop time, the **Progress** value will never reach exactly 1.0, because the start time of the last frame is slightly than the stop time.</span></span> <span data-ttu-id="4e6d9-133">Per raggiungere il 1,0 della transizione, impostare l'ora di arresto della transizione su almeno un frame prima dell'ora di arresto dell'origine.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-133">To make the transition reach 1.0, set the transition stop time to be at least one frame earlier than the source stop time.</span></span>

<span data-ttu-id="4e6d9-134">**4. Inserire l'oggetto nella sequenza temporale**</span><span class="sxs-lookup"><span data-stu-id="4e6d9-134">**4. Insert the Object into the Timeline**</span></span>

<span data-ttu-id="4e6d9-135">Per inserire l'oggetto nella sequenza temporale, chiamare uno dei metodi seguenti sull'elemento padre, a seconda del tipo di oggetto:</span><span class="sxs-lookup"><span data-stu-id="4e6d9-135">To insert the object into the timeline, call one of the following methods on the parent, depending on the object type:</span></span>

-   <span data-ttu-id="4e6d9-136">Effetti: [ **IAMTimelineEffectable:: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)</span><span class="sxs-lookup"><span data-stu-id="4e6d9-136">Effects: [**IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)</span></span>
-   <span data-ttu-id="4e6d9-137">Transizioni: [ **IAMTimelineTransable:: TransAdd**](iamtimelinetransable-transadd.md)</span><span class="sxs-lookup"><span data-stu-id="4e6d9-137">Transitions: [**IAMTimelineTransable::TransAdd**](iamtimelinetransable-transadd.md)</span></span>

<span data-ttu-id="4e6d9-138">Nel metodo [**IAMTimelineEffectable:: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) è necessario specificare la priorità dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-138">In the [**IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) method, you must specify the priority of the effect.</span></span> <span data-ttu-id="4e6d9-139">Quando gli effetti si sovrappongono allo stesso oggetto, vengono applicati in ordine di priorità.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-139">When effects overlap on the same object, they are applied in order of priority.</span></span> <span data-ttu-id="4e6d9-140">L'effetto audio della busta del volume è un'eccezione. per informazioni dettagliate, vedere la Guida di riferimento all' [effetto envelope del volume](volume-envelope-effect.md) .</span><span class="sxs-lookup"><span data-stu-id="4e6d9-140">The Volume Envelope audio effect is an exception; see the [Volume Envelope Effect](volume-envelope-effect.md) reference for details.</span></span> <span data-ttu-id="4e6d9-141">All'interno di una composizione, tutte le tracce audio vengono combinate prima che vengano applicati gli effetti audio per tale composizione.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-141">Within a composition, all audio tracks are mixed before the audio effects for that composition are applied.</span></span>

<span data-ttu-id="4e6d9-142">Poiché le transizioni non possono sovrapporsi allo stesso oggetto, non hanno un valore di priorità.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-142">Because transitions cannot overlap on the same object, they do not have a priority value.</span></span>

<span data-ttu-id="4e6d9-143">Nell'esempio seguente l'oggetto Transition viene aggiunto a una traccia:</span><span class="sxs-lookup"><span data-stu-id="4e6d9-143">The following example adds the transition object to a track:</span></span>


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



<span data-ttu-id="4e6d9-144">Nell'esempio viene eseguita una query sull'oggetto Track per l'interfaccia [**IAMTimelineTransable**](iamtimelinetransable.md) prima di chiamare AddTrans.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-144">The example queries the track object for the [**IAMTimelineTransable**](iamtimelinetransable.md) interface before calling AddTrans.</span></span>

<span data-ttu-id="4e6d9-145">**5. impostare le proprietà**</span><span class="sxs-lookup"><span data-stu-id="4e6d9-145">**5. Set Properties**</span></span>

<span data-ttu-id="4e6d9-146">Molti effetti e transizioni supportano proprietà personalizzate.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-146">Many effects and transitions support custom properties.</span></span> <span data-ttu-id="4e6d9-147">Per informazioni, vedere [impostazione delle proprietà per gli effetti e le transizioni](setting-properties-on-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="4e6d9-147">For information, see [Setting Properties on Effects and Transitions](setting-properties-on-effects-and-transitions.md).</span></span>

<span data-ttu-id="4e6d9-148">Esempio</span><span class="sxs-lookup"><span data-stu-id="4e6d9-148">Example</span></span>

<span data-ttu-id="4e6d9-149">Nell'esempio di codice seguente viene aggiunta una [transizione di cancellazione SMPTE](smpte-wipe-transition.md) a una traccia. Si presuppone che l'oggetto Track esista già nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4e6d9-149">The following code example adds a [SMPTE Wipe Transition](smpte-wipe-transition.md) to a track. It assumes that the track object already exists in the timeline.</span></span>


```C++
IAMTimeline *pTL;
IAMTimelineTrack *pTrack;

// Create timeline with track (not shown).

// Create the transition object. 
IAMTimelineObj *pTransObj = NULL;
hr = pTL->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);

// Set the subobject. 
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe

// Set the start and stop times. 
hr = pTransObj->SetStartStop(50000000, 100000000);

// Insert the transition object into the timeline. 
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
pTransObj->Release();
```



## <a name="related-topics"></a><span data-ttu-id="4e6d9-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4e6d9-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e6d9-151">Utilizzo degli effetti e delle transizioni</span><span class="sxs-lookup"><span data-stu-id="4e6d9-151">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



