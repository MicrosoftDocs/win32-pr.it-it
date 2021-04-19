---
description: L'interfaccia IAMTimelineTrack fornisce metodi per la modifica degli oggetti Track nei servizi di modifica DirectShow (DES). Una traccia contiene un elenco di origini di cui viene eseguito il rendering nell'output finale.
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: Interfaccia IAMTimelineTrack (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 71003694d33b33980fb262f06f6b2e7aa55a70d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333267"
---
# <a name="iamtimelinetrack-interface"></a><span data-ttu-id="16b2b-103">Interfaccia IAMTimelineTrack</span><span class="sxs-lookup"><span data-stu-id="16b2b-103">IAMTimelineTrack interface</span></span>

> [!Note]  
> <span data-ttu-id="16b2b-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="16b2b-104">\[Deprecated.</span></span> <span data-ttu-id="16b2b-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="16b2b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="16b2b-106">L' `IAMTimelineTrack` interfaccia fornisce metodi per la modifica degli oggetti *Track* nei [servizi di modifica DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="16b2b-106">The `IAMTimelineTrack` interface provides methods for manipulating *track* objects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="16b2b-107">Una traccia contiene un elenco di origini di cui viene eseguito il rendering nell'output finale.</span><span class="sxs-lookup"><span data-stu-id="16b2b-107">A track contains a list of sources that are rendered in the final output.</span></span> <span data-ttu-id="16b2b-108">Le origini all'interno della stessa traccia potrebbero non sovrapporsi.</span><span class="sxs-lookup"><span data-stu-id="16b2b-108">Sources within the same track may not overlap.</span></span> <span data-ttu-id="16b2b-109">Le tracce video possono avere sia effetti che transizioni.</span><span class="sxs-lookup"><span data-stu-id="16b2b-109">Video tracks can have both effects and transitions.</span></span> <span data-ttu-id="16b2b-110">Il motore di rendering applica gli effetti prima di applicare le transizioni.</span><span class="sxs-lookup"><span data-stu-id="16b2b-110">The render engine applies effects before it applies transitions.</span></span> <span data-ttu-id="16b2b-111">Le tracce audio possono avere effetti, ma non transizioni.</span><span class="sxs-lookup"><span data-stu-id="16b2b-111">Audio tracks can have effects, but not transitions.</span></span> <span data-ttu-id="16b2b-112">Per ulteriori informazioni, vedere [il modello di sequenza temporale](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="16b2b-112">For more information, see [The Timeline Model](the-timeline-model.md).</span></span>

<span data-ttu-id="16b2b-113">Per creare un oggetto Track, chiamare [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con il tipo di sequenza temporale del valore \_ principale \_ \_ Track.</span><span class="sxs-lookup"><span data-stu-id="16b2b-113">To create a track object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_TRACK.</span></span> <span data-ttu-id="16b2b-114">È possibile eseguire una query sul puntatore **IAMTimelineObj** restituito per l' `IAMTimelineTrack` interfaccia.</span><span class="sxs-lookup"><span data-stu-id="16b2b-114">You can query the returned **IAMTimelineObj** pointer for the `IAMTimelineTrack` interface.</span></span>

## <a name="members"></a><span data-ttu-id="16b2b-115">Membri</span><span class="sxs-lookup"><span data-stu-id="16b2b-115">Members</span></span>

<span data-ttu-id="16b2b-116">L'interfaccia **IAMTimelineTrack** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="16b2b-116">The **IAMTimelineTrack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="16b2b-117">**IAMTimelineTrack** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="16b2b-117">**IAMTimelineTrack** also has these types of members:</span></span>

-   [<span data-ttu-id="16b2b-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="16b2b-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="16b2b-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="16b2b-119">Methods</span></span>

<span data-ttu-id="16b2b-120">L'interfaccia **IAMTimelineTrack** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="16b2b-120">The **IAMTimelineTrack** interface has these methods.</span></span>



| <span data-ttu-id="16b2b-121">Metodo</span><span class="sxs-lookup"><span data-stu-id="16b2b-121">Method</span></span>                                                          | <span data-ttu-id="16b2b-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16b2b-122">Description</span></span>                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16b2b-123">**AreYouBlank**</span><span class="sxs-lookup"><span data-stu-id="16b2b-123">**AreYouBlank**</span></span>](iamtimelinetrack-areyoublank.md)             | <span data-ttu-id="16b2b-124">Determina se la traccia è vuota (non contiene oggetti di origine).</span><span class="sxs-lookup"><span data-stu-id="16b2b-124">Determines whether the track is blank (contains no source objects).</span></span><br/>                                                                       |
| [<span data-ttu-id="16b2b-125">**GetNextSrc**</span><span class="sxs-lookup"><span data-stu-id="16b2b-125">**GetNextSrc**</span></span>](iamtimelinetrack-getnextsrc.md)               | <span data-ttu-id="16b2b-126">Esegue la ricerca della successiva origine visualizzata all'ora specificata o successiva.</span><span class="sxs-lookup"><span data-stu-id="16b2b-126">Searches the track for the next source that appears at the specified time or later.</span></span><br/>                                                       |
| [<span data-ttu-id="16b2b-127">**GetNextSrc2**</span><span class="sxs-lookup"><span data-stu-id="16b2b-127">**GetNextSrc2**</span></span>](iamtimelinetrack-getnextsrc2.md)             | <span data-ttu-id="16b2b-128">Esegue la ricerca della successiva origine visualizzata nell'ora specificata o in una versione successiva, con l'oggetto specificato come valore [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="16b2b-128">Searches the track for the next source that appears at the specified time or later, with the given as a [**REFTIME**](reftime.md) value.</span></span><br/> |
| [<span data-ttu-id="16b2b-129">**GetNextSrcEx**</span><span class="sxs-lookup"><span data-stu-id="16b2b-129">**GetNextSrcEx**</span></span>](iamtimelinetrack-getnextsrcex.md)           | <span data-ttu-id="16b2b-130">Recupera l'origine successiva dopo l'origine specificata.</span><span class="sxs-lookup"><span data-stu-id="16b2b-130">Retrieves the next source after the specified source.</span></span><br/>                                                                                     |
| [<span data-ttu-id="16b2b-131">**GetSourcesCount**</span><span class="sxs-lookup"><span data-stu-id="16b2b-131">**GetSourcesCount**</span></span>](iamtimelinetrack-getsourcescount.md)     | <span data-ttu-id="16b2b-132">Recupera il numero di origini nella traccia.</span><span class="sxs-lookup"><span data-stu-id="16b2b-132">Retrieves the number of sources in the track.</span></span><br/>                                                                                             |
| [<span data-ttu-id="16b2b-133">**GetSrcAtTime**</span><span class="sxs-lookup"><span data-stu-id="16b2b-133">**GetSrcAtTime**</span></span>](iamtimelinetrack-getsrcattime.md)           | <span data-ttu-id="16b2b-134">Recupera l'oggetto di origine più vicino al tempo specificato, in base alle condizioni di limite specificate.</span><span class="sxs-lookup"><span data-stu-id="16b2b-134">Retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span><br/>                                |
| [<span data-ttu-id="16b2b-135">**GetSrcAtTime2**</span><span class="sxs-lookup"><span data-stu-id="16b2b-135">**GetSrcAtTime2**</span></span>](iamtimelinetrack-getsrcattime2.md)         | <span data-ttu-id="16b2b-136">Recupera l'oggetto di origine più vicino al tempo specificato, dato come valore [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="16b2b-136">Retrieves the source object nearest to the specified time, given as a [**REFTIME**](reftime.md) value.</span></span><br/>                                   |
| [<span data-ttu-id="16b2b-137">**InsertSpace**</span><span class="sxs-lookup"><span data-stu-id="16b2b-137">**InsertSpace**</span></span>](iamtimelinetrack-insertspace.md)             | <span data-ttu-id="16b2b-138">Suddivide tutti gli oggetti esistenti al momento specificato e inserisce uno spazio tra di essi.</span><span class="sxs-lookup"><span data-stu-id="16b2b-138">Splits any objects that exist at the specified time and inserts space between them.</span></span><br/>                                                       |
| [<span data-ttu-id="16b2b-139">**InsertSpace2**</span><span class="sxs-lookup"><span data-stu-id="16b2b-139">**InsertSpace2**</span></span>](iamtimelinetrack-insertspace2.md)           | <span data-ttu-id="16b2b-140">Suddivide tutti gli oggetti esistenti al momento specificato e inserisce uno spazio tra di essi, usando i valori [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="16b2b-140">Splits any objects that exist at the specified time and inserts space between them, using [**REFTIME**](reftime.md) values.</span></span><br/>              |
| [<span data-ttu-id="16b2b-141">**MoveEverythingBy**</span><span class="sxs-lookup"><span data-stu-id="16b2b-141">**MoveEverythingBy**</span></span>](iamtimelinetrack-moveeverythingby.md)   | <span data-ttu-id="16b2b-142">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="16b2b-142">Not supported.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="16b2b-143">**MoveEverythingBy2**</span><span class="sxs-lookup"><span data-stu-id="16b2b-143">**MoveEverythingBy2**</span></span>](iamtimelinetrack-moveeverythingby2.md) | <span data-ttu-id="16b2b-144">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="16b2b-144">Not supported.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="16b2b-145">**SrcAdd**</span><span class="sxs-lookup"><span data-stu-id="16b2b-145">**SrcAdd**</span></span>](iamtimelinetrack-srcadd.md)                       | <span data-ttu-id="16b2b-146">Aggiunge un'origine alla traccia.</span><span class="sxs-lookup"><span data-stu-id="16b2b-146">Adds a source to the track.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="16b2b-147">**ZeroBetween**</span><span class="sxs-lookup"><span data-stu-id="16b2b-147">**ZeroBetween**</span></span>](iamtimelinetrack-zerobetween.md)             | <span data-ttu-id="16b2b-148">Rimuove tutti gli elementi dalla traccia tra le ore specificate.</span><span class="sxs-lookup"><span data-stu-id="16b2b-148">Removes everything from the track between the specified times.</span></span><br/>                                                                            |
| [<span data-ttu-id="16b2b-149">**ZeroBetween2**</span><span class="sxs-lookup"><span data-stu-id="16b2b-149">**ZeroBetween2**</span></span>](iamtimelinetrack-zerobetween2.md)           | <span data-ttu-id="16b2b-150">Rimuove tutti gli elementi dalla traccia tra gli orari specificati, specificati come valori [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="16b2b-150">Removes everything from the track between the specified times, given as [**REFTIME**](reftime.md) values.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="16b2b-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="16b2b-151">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="16b2b-152">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="16b2b-152">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="16b2b-153">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="16b2b-153">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="16b2b-154">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="16b2b-154">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16b2b-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16b2b-155">Requirements</span></span>



| <span data-ttu-id="16b2b-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="16b2b-156">Requirement</span></span> | <span data-ttu-id="16b2b-157">Valore</span><span class="sxs-lookup"><span data-stu-id="16b2b-157">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16b2b-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16b2b-158">Header</span></span><br/>  | <dl> <span data-ttu-id="16b2b-159"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="16b2b-159"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="16b2b-160">Libreria</span><span class="sxs-lookup"><span data-stu-id="16b2b-160">Library</span></span><br/> | <dl> <span data-ttu-id="16b2b-161"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16b2b-161"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
