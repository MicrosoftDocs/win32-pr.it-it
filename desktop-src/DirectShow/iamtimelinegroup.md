---
description: "L'interfaccia IAMTimelineGroup imposta e recupera le proprietà sui gruppi in servizi di modifica DirectShow (DES). Un gruppo contiene una o più tracce e possibilmente una o più composizioni, che a loro volta contengono clip di origine di un tipo uniforme, ad esempio video o audio. I gruppi sono le composizioni più in alto in una sequenza temporale ed espongono anche l'interfaccia IAMTimelineComp. Una sequenza temporale può contenere più gruppi. Ogni gruppo ha gli attributi seguenti. Tipo di supporto associato. Frequenza dei fotogrammi a cui viene eseguito il rendering del gruppo, in frame al secondo (FPS). Tutte le modifiche vengono eseguite in un momento arrotondato al limite di frame più vicino, come definito dall'impostazione FPS del gruppo. Un livello di priorità, per la scrittura di file con più flussi dello stesso tipo di supporto (ad esempio, un file AVI con due flussi video). Per creare un oggetto gruppo, chiamare IAMTimeline:: CreateEmptyNode con il gruppo di tipi principali della sequenza temporale del valore \\_ \\_ \\_ . È possibile eseguire una query sul puntatore IAMTimelineObj restituito per l'interfaccia IAMTimelineGroup."
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: Interfaccia IAMTimelineGroup (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e82a11db65183e343048f594a7457c0a8febf8bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333597"
---
# <a name="iamtimelinegroup-interface"></a><span data-ttu-id="5b08a-107">Interfaccia IAMTimelineGroup</span><span class="sxs-lookup"><span data-stu-id="5b08a-107">IAMTimelineGroup interface</span></span>

> [!Note]  
> <span data-ttu-id="5b08a-108">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5b08a-108">\[Deprecated.</span></span> <span data-ttu-id="5b08a-109">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5b08a-109">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5b08a-110">L' `IAMTimelineGroup` interfaccia imposta e recupera le proprietà sui gruppi in [servizi di modifica DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="5b08a-110">The `IAMTimelineGroup` interface sets and retrieves properties on groups in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="5b08a-111">Un gruppo contiene una o più tracce e possibilmente una o più composizioni, che a loro volta contengono clip di origine di un tipo uniforme, ad esempio video o audio.</span><span class="sxs-lookup"><span data-stu-id="5b08a-111">A group contains one or more tracks, and possibly one or more compositions, which in turn contain source clips of a uniform type, such as video or audio.</span></span> <span data-ttu-id="5b08a-112">I gruppi sono le composizioni più in alto in una sequenza temporale ed espongono anche l'interfaccia [**IAMTimelineComp**](iamtimelinecomp.md) .</span><span class="sxs-lookup"><span data-stu-id="5b08a-112">Groups are the topmost compositions in a timeline, and also expose the [**IAMTimelineComp**](iamtimelinecomp.md) interface.</span></span> <span data-ttu-id="5b08a-113">Una sequenza temporale può contenere più gruppi.</span><span class="sxs-lookup"><span data-stu-id="5b08a-113">A timeline can contain multiple groups.</span></span>

<span data-ttu-id="5b08a-114">Ogni gruppo ha gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5b08a-114">Each group has the following attributes.</span></span>

-   <span data-ttu-id="5b08a-115">Tipo di supporto associato.</span><span class="sxs-lookup"><span data-stu-id="5b08a-115">An associated media type.</span></span>
-   <span data-ttu-id="5b08a-116">Frequenza dei fotogrammi a cui viene eseguito il rendering del gruppo, in frame al secondo (FPS).</span><span class="sxs-lookup"><span data-stu-id="5b08a-116">The frame rate at which the group renders, in frames per second (FPS).</span></span> <span data-ttu-id="5b08a-117">Tutte le modifiche vengono eseguite in un momento arrotondato al limite di frame più vicino, come definito dall'impostazione FPS del gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b08a-117">All edits occur at a time rounded to the nearest frame boundary, as defined by the group's FPS setting.</span></span>
-   <span data-ttu-id="5b08a-118">Un livello di priorità, per la scrittura di file con più flussi dello stesso tipo di supporto (ad esempio, un file AVI con due flussi video).</span><span class="sxs-lookup"><span data-stu-id="5b08a-118">A priority level, for writing files with multiple streams of the same media type (for example, a two-video-stream AVI file).</span></span>

<span data-ttu-id="5b08a-119">Per creare un oggetto gruppo, chiamare [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con il gruppo di tipi principali della sequenza temporale del valore \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5b08a-119">To create a group object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_GROUP.</span></span> <span data-ttu-id="5b08a-120">È possibile eseguire una query sul puntatore [**IAMTimelineObj**](iamtimelineobj.md) restituito per l'interfaccia **IAMTimelineGroup** .</span><span class="sxs-lookup"><span data-stu-id="5b08a-120">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the **IAMTimelineGroup** interface.</span></span>

## <a name="members"></a><span data-ttu-id="5b08a-121">Membri</span><span class="sxs-lookup"><span data-stu-id="5b08a-121">Members</span></span>

<span data-ttu-id="5b08a-122">L'interfaccia **IAMTimelineGroup** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5b08a-122">The **IAMTimelineGroup** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5b08a-123">**IAMTimelineGroup** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5b08a-123">**IAMTimelineGroup** also has these types of members:</span></span>

-   [<span data-ttu-id="5b08a-124">Metodi</span><span class="sxs-lookup"><span data-stu-id="5b08a-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5b08a-125">Metodi</span><span class="sxs-lookup"><span data-stu-id="5b08a-125">Methods</span></span>

<span data-ttu-id="5b08a-126">L'interfaccia **IAMTimelineGroup** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5b08a-126">The **IAMTimelineGroup** interface has these methods.</span></span>



| <span data-ttu-id="5b08a-127">Metodo</span><span class="sxs-lookup"><span data-stu-id="5b08a-127">Method</span></span>                                                                            | <span data-ttu-id="5b08a-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b08a-128">Description</span></span>                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b08a-129">**ClearRecompressFormatDirty**</span><span class="sxs-lookup"><span data-stu-id="5b08a-129">**ClearRecompressFormatDirty**</span></span>](iamtimelinegroup-clearrecompressformatdirty.md) | <span data-ttu-id="5b08a-130">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="5b08a-130">Not supported.</span></span><br/>                                                                       |
| [<span data-ttu-id="5b08a-131">**GetGroupName**</span><span class="sxs-lookup"><span data-stu-id="5b08a-131">**GetGroupName**</span></span>](iamtimelinegroup-getgroupname.md)                             | <span data-ttu-id="5b08a-132">Recupera il nome definito dall'applicazione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b08a-132">Retrieves the application-defined name of the group.</span></span><br/>                                 |
| [<span data-ttu-id="5b08a-133">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="5b08a-133">**GetMediaType**</span></span>](iamtimelinegroup-getmediatype.md)                             | <span data-ttu-id="5b08a-134">Recupera il tipo di supporto non compresso per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b08a-134">Retrieves the uncompressed media type for the group.</span></span><br/>                                 |
| [<span data-ttu-id="5b08a-135">**GetOutputBuffering**</span><span class="sxs-lookup"><span data-stu-id="5b08a-135">**GetOutputBuffering**</span></span>](iamtimelinegroup-getoutputbuffering.md)                 | <span data-ttu-id="5b08a-136">Recupera il numero di frame di cui è stato eseguito il rendering in anticipo durante l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="5b08a-136">Retrieves the number of frames rendered in advance during preview.</span></span><br/>                   |
| [<span data-ttu-id="5b08a-137">**GetOutputFPS**</span><span class="sxs-lookup"><span data-stu-id="5b08a-137">**GetOutputFPS**</span></span>](iamtimelinegroup-getoutputfps.md)                             | <span data-ttu-id="5b08a-138">Recupera la frequenza dei fotogrammi di output di questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b08a-138">Retrieves the output frame rate of this group.</span></span><br/>                                       |
| [<span data-ttu-id="5b08a-139">**GetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="5b08a-139">**GetPreviewMode**</span></span>](iamtimelinegroup-getpreviewmode.md)                         | <span data-ttu-id="5b08a-140">Recupera la modalità di anteprima per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b08a-140">Retrieves the preview mode for the group.</span></span><br/>                                            |
| [<span data-ttu-id="5b08a-141">**GetPriority**</span><span class="sxs-lookup"><span data-stu-id="5b08a-141">**GetPriority**</span></span>](iamtimelinegroup-getpriority.md)                               | <span data-ttu-id="5b08a-142">Recupera la priorità del gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b08a-142">Retrieves the group's priority.</span></span><br/>                                                      |
| [<span data-ttu-id="5b08a-143">**GetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="5b08a-143">**GetSmartRecompressFormat**</span></span>](iamtimelinegroup-getsmartrecompressformat.md)     | <span data-ttu-id="5b08a-144">Recupera il formato di compressione corrente per la ricompressione intelligente.</span><span class="sxs-lookup"><span data-stu-id="5b08a-144">Retrieves the current compression format for smart recompression.</span></span><br/>                    |
| [<span data-ttu-id="5b08a-145">**GetTimeline**</span><span class="sxs-lookup"><span data-stu-id="5b08a-145">**GetTimeline**</span></span>](iamtimelinegroup-gettimeline.md)                               | <span data-ttu-id="5b08a-146">Recupera la sequenza temporale a cui appartiene il gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b08a-146">Retrieves the timeline to which this group belongs.</span></span><br/>                                  |
| [<span data-ttu-id="5b08a-147">**IsRecompressFormatDirty**</span><span class="sxs-lookup"><span data-stu-id="5b08a-147">**IsRecompressFormatDirty**</span></span>](iamtimelinegroup-isrecompressformatdirty.md)       | <span data-ttu-id="5b08a-148">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="5b08a-148">Not supported.</span></span><br/>                                                                       |
| [<span data-ttu-id="5b08a-149">**IsSmartRecompressFormatSet**</span><span class="sxs-lookup"><span data-stu-id="5b08a-149">**IsSmartRecompressFormatSet**</span></span>](iamtimelinegroup-issmartrecompressformatset.md) | <span data-ttu-id="5b08a-150">Determina se è stato impostato un formato di compressione intelligente per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b08a-150">Determines whether a smart compression format was set for the group.</span></span><br/>                 |
| [<span data-ttu-id="5b08a-151">**Segroupname**</span><span class="sxs-lookup"><span data-stu-id="5b08a-151">**SetGroupName**</span></span>](iamtimelinegroup-setgroupname.md)                             | <span data-ttu-id="5b08a-152">Imposta il nome definito dall'applicazione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b08a-152">Sets the application-defined name of the group.</span></span><br/>                                      |
| [<span data-ttu-id="5b08a-153">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="5b08a-153">**SetMediaType**</span></span>](iamtimelinegroup-setmediatype.md)                             | <span data-ttu-id="5b08a-154">Imposta il tipo di supporto non compresso per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b08a-154">Sets the uncompressed media type for the group.</span></span><br/>                                      |
| [<span data-ttu-id="5b08a-155">**SetMediaTypeForVB**</span><span class="sxs-lookup"><span data-stu-id="5b08a-155">**SetMediaTypeForVB**</span></span>](iamtimelinegroup-setmediatypeforvb.md)                   | <span data-ttu-id="5b08a-156">Specifica il tipo di supporto di gruppo per i client di automazione.</span><span class="sxs-lookup"><span data-stu-id="5b08a-156">Specifies the group media type, for Automation clients.</span></span><br/>                              |
| [<span data-ttu-id="5b08a-157">**SetOutputBuffering**</span><span class="sxs-lookup"><span data-stu-id="5b08a-157">**SetOutputBuffering**</span></span>](iamtimelinegroup-setoutputbuffering.md)                 | <span data-ttu-id="5b08a-158">Specifica il numero di frame di cui è stato eseguito il rendering in anticipo durante l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="5b08a-158">Specifies the number of frames rendered in advance during preview.</span></span><br/>                   |
| [<span data-ttu-id="5b08a-159">**SetOutputFPS**</span><span class="sxs-lookup"><span data-stu-id="5b08a-159">**SetOutputFPS**</span></span>](iamtimelinegroup-setoutputfps.md)                             | <span data-ttu-id="5b08a-160">Imposta la frequenza dei fotogrammi di output non compressi per questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b08a-160">Sets the uncompressed output frame rate for this group.</span></span><br/>                              |
| [<span data-ttu-id="5b08a-161">**SetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="5b08a-161">**SetPreviewMode**</span></span>](iamtimelinegroup-setpreviewmode.md)                         | <span data-ttu-id="5b08a-162">Imposta la modalità di anteprima per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b08a-162">Sets the preview mode for the group.</span></span><br/>                                                 |
| [<span data-ttu-id="5b08a-163">**SetRecompFormatFromSource**</span><span class="sxs-lookup"><span data-stu-id="5b08a-163">**SetRecompFormatFromSource**</span></span>](iamtimelinegroup-setrecompformatfromsource.md)   | <span data-ttu-id="5b08a-164">Imposta il formato di ricompressione video usando il formato di compressione da un file di origine.</span><span class="sxs-lookup"><span data-stu-id="5b08a-164">Sets the video recompression format using the compression format from a source file.</span></span><br/> |
| [<span data-ttu-id="5b08a-165">**SetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="5b08a-165">**SetSmartRecompressFormat**</span></span>](iamtimelinegroup-setsmartrecompressformat.md)     | <span data-ttu-id="5b08a-166">Specifica un formato di compressione da utilizzare per la ricompressione intelligente.</span><span class="sxs-lookup"><span data-stu-id="5b08a-166">Specifies a compression format to use for smart recompression.</span></span><br/>                       |
| [<span data-ttu-id="5b08a-167">**Sequenza temporale**</span><span class="sxs-lookup"><span data-stu-id="5b08a-167">**SetTimeline**</span></span>](iamtimelinegroup-settimeline.md)                               | <span data-ttu-id="5b08a-168">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="5b08a-168">Not supported.</span></span><br/>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="5b08a-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b08a-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5b08a-170">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="5b08a-170">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5b08a-171">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5b08a-171">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5b08a-172">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5b08a-172">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5b08a-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b08a-173">Requirements</span></span>



| <span data-ttu-id="5b08a-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b08a-174">Requirement</span></span> | <span data-ttu-id="5b08a-175">Valore</span><span class="sxs-lookup"><span data-stu-id="5b08a-175">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b08a-176">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b08a-176">Header</span></span><br/>  | <dl> <span data-ttu-id="5b08a-177"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b08a-177"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5b08a-178">Libreria</span><span class="sxs-lookup"><span data-stu-id="5b08a-178">Library</span></span><br/> | <dl> <span data-ttu-id="5b08a-179"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b08a-179"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
