---
description: L'interfaccia IAMTimelineComp inserisce o recupera tracce virtuali in una composizione in servizi di modifica DirectShow (DES). Una composizione è una raccolta di livelli che funge da singolo tracciato composito.
ms.assetid: b0a47303-9e3c-4b78-ac90-c5d8fce2b727
title: Interfaccia IAMTimelineComp (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 645abbb9c5f61fcfd04e433c3cfc61b926ed403d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333705"
---
# <a name="iamtimelinecomp-interface"></a><span data-ttu-id="09538-103">Interfaccia IAMTimelineComp</span><span class="sxs-lookup"><span data-stu-id="09538-103">IAMTimelineComp interface</span></span>

> [!Note]  
> <span data-ttu-id="09538-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="09538-104">\[Deprecated.</span></span> <span data-ttu-id="09538-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="09538-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="09538-106">L'interfaccia **IAMTimelineComp** inserisce o recupera tracce virtuali in una composizione in [servizi di modifica DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="09538-106">The **IAMTimelineComp** interface inserts or retrieves virtual tracks on a composition in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="09538-107">Una composizione è una raccolta di livelli che funge da singolo *tracciato* composito. Ad esempio, una composizione che contiene due tracce con una transizione tra loro funge da singola traccia con la transizione precomposita.</span><span class="sxs-lookup"><span data-stu-id="09538-107">A composition is a collection of layers that acts as a single, composited *track*. For example, a composition that contains two tracks with a transition between them acts as a single track with the transition precomposited.</span></span> <span data-ttu-id="09538-108">Una composizione deve contenere supporti di un solo tipo, ad esempio audio o video, ma questa limitazione non viene applicata.</span><span class="sxs-lookup"><span data-stu-id="09538-108">A composition should contain media of only one type (such as audio or video), but this limitation is not enforced.</span></span> <span data-ttu-id="09538-109">Una *traccia virtuale* è qualsiasi oggetto che può risiedere in una composizione, incluse le tracce e altre composizioni.</span><span class="sxs-lookup"><span data-stu-id="09538-109">A *virtual track* is any object that can reside in a composition, including tracks and other compositions.</span></span>

<span data-ttu-id="09538-110">I nodi più in alto nella sequenza temporale sono *gruppi*.</span><span class="sxs-lookup"><span data-stu-id="09538-110">The topmost nodes in the timeline are *groups*.</span></span> <span data-ttu-id="09538-111">I gruppi implementano sia l'interfaccia `IAMTimelineComp` che l'interfaccia [**IAMTimelineGroup**](iamtimelinegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="09538-111">Groups implement both the `IAMTimelineComp` interface and the [**IAMTimelineGroup**](iamtimelinegroup.md) interface.</span></span>

<span data-ttu-id="09538-112">Per creare un oggetto Composition, chiamare [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con il tipo principale della sequenza temporale del valore \_ \_ \_ composito.</span><span class="sxs-lookup"><span data-stu-id="09538-112">To create a composition object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_COMPOSITE.</span></span> <span data-ttu-id="09538-113">È possibile eseguire una query sul puntatore [**IAMTimelineObj**](iamtimelineobj.md) restituito per l' `IAMTimelineComp` interfaccia.</span><span class="sxs-lookup"><span data-stu-id="09538-113">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineComp` interface.</span></span> <span data-ttu-id="09538-114">Per ulteriori informazioni, vedere [il modello di sequenza temporale](the-timeline-model.md) e [creazione di una sequenza temporale](constructing-a-timeline.md).</span><span class="sxs-lookup"><span data-stu-id="09538-114">For more information, see [The Timeline Model](the-timeline-model.md) and [Constructing a Timeline](constructing-a-timeline.md).</span></span>

## <a name="members"></a><span data-ttu-id="09538-115">Membri</span><span class="sxs-lookup"><span data-stu-id="09538-115">Members</span></span>

<span data-ttu-id="09538-116">L'interfaccia **IAMTimelineComp** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="09538-116">The **IAMTimelineComp** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="09538-117">**IAMTimelineComp** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="09538-117">**IAMTimelineComp** also has these types of members:</span></span>

-   [<span data-ttu-id="09538-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="09538-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="09538-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="09538-119">Methods</span></span>

<span data-ttu-id="09538-120">L'interfaccia **IAMTimelineComp** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="09538-120">The **IAMTimelineComp** interface has these methods.</span></span>



| <span data-ttu-id="09538-121">Metodo</span><span class="sxs-lookup"><span data-stu-id="09538-121">Method</span></span>                                                                       | <span data-ttu-id="09538-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09538-122">Description</span></span>                                                                                                                                               |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09538-123">**GetCountOfType**</span><span class="sxs-lookup"><span data-stu-id="09538-123">**GetCountOfType**</span></span>](iamtimelinecomp-getcountoftype.md)                     | <span data-ttu-id="09538-124">Recupera il numero di oggetti di un tipo specificato contenuto nella composizione e in tutte le relative tracce virtuali, in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="09538-124">Retrieves the number of objects of a given type contained in this composition and all of its virtual tracks, recursively.</span></span><br/>                      |
| [<span data-ttu-id="09538-125">**GetNextVTrack**</span><span class="sxs-lookup"><span data-stu-id="09538-125">**GetNextVTrack**</span></span>](iamtimelinecomp-getnextvtrack.md)                       | <span data-ttu-id="09538-126">Recupera la traccia virtuale successiva dopo una traccia virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="09538-126">Retrieves the next virtual track after a specified virtual track.</span></span><br/>                                                                              |
| [<span data-ttu-id="09538-127">**GetRecursiveLayerOfType**</span><span class="sxs-lookup"><span data-stu-id="09538-127">**GetRecursiveLayerOfType**</span></span>](iamtimelinecomp-getrecursivelayeroftype.md)   | <span data-ttu-id="09538-128">Esegue un ordine di profondità-primo delle tracce virtuali contenute in questa composizione e recupera la traccia virtuale *n* dall'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="09538-128">Performs a depth-first ordering of the virtual tracks contained in this composition, and retrieves the *n* th virtual track from that ordering.</span></span><br/> |
| [<span data-ttu-id="09538-129">**GetRecursiveLayerOfTypeI**</span><span class="sxs-lookup"><span data-stu-id="09538-129">**GetRecursiveLayerOfTypeI**</span></span>](iamtimelinecomp-getrecursivelayeroftypei.md) | <span data-ttu-id="09538-130">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="09538-130">Not supported.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="09538-131">**GetVTrack**</span><span class="sxs-lookup"><span data-stu-id="09538-131">**GetVTrack**</span></span>](iamtimelinecomp-getvtrack.md)                               | <span data-ttu-id="09538-132">Recupera la traccia virtuale alla priorità specificata.</span><span class="sxs-lookup"><span data-stu-id="09538-132">Retrieves the virtual track at the specified priority.</span></span><br/>                                                                                         |
| [<span data-ttu-id="09538-133">**VTrackGetCount**</span><span class="sxs-lookup"><span data-stu-id="09538-133">**VTrackGetCount**</span></span>](iamtimelinecomp-vtrackgetcount.md)                     | <span data-ttu-id="09538-134">Recupera il numero di tracce virtuali contenute nella composizione.</span><span class="sxs-lookup"><span data-stu-id="09538-134">Retrieves the number of virtual tracks contained in the composition.</span></span><br/>                                                                           |
| [<span data-ttu-id="09538-135">**VTrackInsBefore**</span><span class="sxs-lookup"><span data-stu-id="09538-135">**VTrackInsBefore**</span></span>](iamtimelinecomp-vtrackinsbefore.md)                   | <span data-ttu-id="09538-136">Inserisce una traccia virtuale nella composizione con la priorità specificata.</span><span class="sxs-lookup"><span data-stu-id="09538-136">Inserts a virtual track into the composition at the specified priority.</span></span><br/>                                                                        |
| [<span data-ttu-id="09538-137">**VTrackSwapPriorities**</span><span class="sxs-lookup"><span data-stu-id="09538-137">**VTrackSwapPriorities**</span></span>](iamtimelinecomp-vtrackswappriorities.md)         | <span data-ttu-id="09538-138">Passa i livelli di priorità di due tracce.</span><span class="sxs-lookup"><span data-stu-id="09538-138">Switches the priority levels of two tracks.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="09538-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="09538-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="09538-140">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="09538-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="09538-141">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="09538-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="09538-142">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="09538-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="09538-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09538-143">Requirements</span></span>



| <span data-ttu-id="09538-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="09538-144">Requirement</span></span> | <span data-ttu-id="09538-145">Valore</span><span class="sxs-lookup"><span data-stu-id="09538-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09538-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09538-146">Header</span></span><br/>  | <dl> <span data-ttu-id="09538-147"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="09538-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="09538-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="09538-148">Library</span></span><br/> | <dl> <span data-ttu-id="09538-149"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09538-149"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
