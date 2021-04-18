---
description: L'interfaccia IAMTimelineSrc fornisce metodi per la modifica e l'impostazione delle proprietà negli oggetti di origine nei servizi di modifica DirectShow (DES).
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: Interfaccia IAMTimelineSrc (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 25733b1353bc0cbd92c40335a8d342473b03a806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325178"
---
# <a name="iamtimelinesrc-interface"></a><span data-ttu-id="94595-103">Interfaccia IAMTimelineSrc</span><span class="sxs-lookup"><span data-stu-id="94595-103">IAMTimelineSrc interface</span></span>

> [!Note]  
> <span data-ttu-id="94595-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="94595-104">\[Deprecated.</span></span> <span data-ttu-id="94595-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="94595-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="94595-106">L' `IAMTimelineSrc` interfaccia fornisce metodi per la modifica e l'impostazione delle proprietà negli oggetti di origine nei [servizi di modifica DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="94595-106">The `IAMTimelineSrc` interface provides methods for manipulating and setting properties on source objects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="94595-107">Un oggetto di origine rappresenta un flusso da un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="94595-107">A source object represents one stream from a media source.</span></span>

<span data-ttu-id="94595-108">È possibile usare una parte dei dati all'interno di un file di origine impostando gli orari di inizio e di fine del supporto.</span><span class="sxs-lookup"><span data-stu-id="94595-108">You can use a portion of the data within a source file by setting the media start and media stop times.</span></span> <span data-ttu-id="94595-109">Questi valori specificano l'inizio e la fine dell'oggetto di origine rispetto all'origine del supporto originale.</span><span class="sxs-lookup"><span data-stu-id="94595-109">These values specify the beginning and end of the source object, relative to the original media source.</span></span> <span data-ttu-id="94595-110">I tempi del supporto possono differire dall'ora di inizio e di fine dell'oggetto nella sequenza temporale, consentendo la riproduzione veloce o lenta.</span><span class="sxs-lookup"><span data-stu-id="94595-110">The media times can differ from the object's start and stop times on the timeline, allowing for fast- or slow-motion playback.</span></span> <span data-ttu-id="94595-111">(Con le origini audio, viene eseguito il pitch shift).</span><span class="sxs-lookup"><span data-stu-id="94595-111">(With audio sources, pitch shifting occurs.)</span></span>

<span data-ttu-id="94595-112">Per creare un oggetto di origine, chiamare [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con l' \_ origine del tipo principale della sequenza temporale del valore \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="94595-112">To create a source object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_SOURCE.</span></span> <span data-ttu-id="94595-113">È possibile eseguire una query sul puntatore [**IAMTimelineObj**](iamtimelineobj.md) restituito per l'interfaccia **IAMTimelineSrc** .</span><span class="sxs-lookup"><span data-stu-id="94595-113">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the **IAMTimelineSrc** interface.</span></span> <span data-ttu-id="94595-114">Per ulteriori informazioni, vedere [creazione di una sequenza temporale](constructing-a-timeline.md) e [utilizzo di origini](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="94595-114">For more information, see [Constructing a Timeline](constructing-a-timeline.md) and [Working with Sources](working-with-sources.md).</span></span>

## <a name="members"></a><span data-ttu-id="94595-115">Membri</span><span class="sxs-lookup"><span data-stu-id="94595-115">Members</span></span>

<span data-ttu-id="94595-116">L'interfaccia **IAMTimelineSrc** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="94595-116">The **IAMTimelineSrc** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="94595-117">**IAMTimelineSrc** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="94595-117">**IAMTimelineSrc** also has these types of members:</span></span>

-   [<span data-ttu-id="94595-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="94595-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="94595-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="94595-119">Methods</span></span>

<span data-ttu-id="94595-120">L'interfaccia **IAMTimelineSrc** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="94595-120">The **IAMTimelineSrc** interface has these methods.</span></span>



| <span data-ttu-id="94595-121">Metodo</span><span class="sxs-lookup"><span data-stu-id="94595-121">Method</span></span>                                                    | <span data-ttu-id="94595-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94595-122">Description</span></span>                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94595-123">**FixMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="94595-123">**FixMediaTimes**</span></span>](iamtimelinesrc-fixmediatimes.md)     | <span data-ttu-id="94595-124">Arrotonda i valori temporali specificati al limite del frame più vicino.</span><span class="sxs-lookup"><span data-stu-id="94595-124">Rounds the specified time values to the nearest frame boundary.</span></span><br/>                               |
| [<span data-ttu-id="94595-125">**FixMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="94595-125">**FixMediaTimes2**</span></span>](iamtimelinesrc-fixmediatimes2.md)   | <span data-ttu-id="94595-126">Arrotonda i valori temporali specificati, specificati come valori **REFTIME** , al limite di frame più vicino.</span><span class="sxs-lookup"><span data-stu-id="94595-126">Rounds the specified time values, given as **REFTIME** values, to the nearest frame boundary.</span></span><br/> |
| [<span data-ttu-id="94595-127">**GetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="94595-127">**GetDefaultFPS**</span></span>](iamtimelinesrc-getdefaultfps.md)     | <span data-ttu-id="94595-128">Recupera la frequenza dei fotogrammi predefinita dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="94595-128">Retrieves the source object's default frame rate.</span></span><br/>                                             |
| [<span data-ttu-id="94595-129">**GetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="94595-129">**GetMediaLength**</span></span>](iamtimelinesrc-getmedialength.md)   | <span data-ttu-id="94595-130">Recupera la lunghezza del supporto di questo oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="94595-130">Retrieves the media length of this source object.</span></span><br/>                                             |
| [<span data-ttu-id="94595-131">**GetMediaLength2**</span><span class="sxs-lookup"><span data-stu-id="94595-131">**GetMediaLength2**</span></span>](iamtimelinesrc-getmedialength2.md) | <span data-ttu-id="94595-132">Recupera la lunghezza del supporto di questo oggetto di origine, come valore **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="94595-132">Retrieves the media length of this source object, as a **REFTIME** value.</span></span><br/>                     |
| [<span data-ttu-id="94595-133">**Getmedianame**</span><span class="sxs-lookup"><span data-stu-id="94595-133">**GetMediaName**</span></span>](iamtimelinesrc-getmedianame.md)       | <span data-ttu-id="94595-134">Recupera il nome del file di origine rappresentato da questo oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="94595-134">Retrieves the name of the source file represented by this source object.</span></span><br/>                      |
| [<span data-ttu-id="94595-135">**GetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="94595-135">**GetMediaTimes**</span></span>](iamtimelinesrc-getmediatimes.md)     | <span data-ttu-id="94595-136">Recupera l'ora di inizio e di fine del supporto.</span><span class="sxs-lookup"><span data-stu-id="94595-136">Retrieves the media start and stop times.</span></span><br/>                                                     |
| [<span data-ttu-id="94595-137">**GetMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="94595-137">**GetMediaTimes2**</span></span>](iamtimelinesrc-getmediatimes2.md)   | <span data-ttu-id="94595-138">Recupera le ore di inizio e di fine del supporto, come valori **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="94595-138">Retrieves the media start and stop times, as **REFTIME** values.</span></span><br/>                              |
| [<span data-ttu-id="94595-139">**GetStreamNumber**</span><span class="sxs-lookup"><span data-stu-id="94595-139">**GetStreamNumber**</span></span>](iamtimelinesrc-getstreamnumber.md) | <span data-ttu-id="94595-140">Recupera il numero corrente del flusso per l'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="94595-140">Retrieves the current stream number for the source object.</span></span><br/>                                    |
| [<span data-ttu-id="94595-141">**GetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="94595-141">**GetStretchMode**</span></span>](iamtimelinesrc-getstretchmode.md)   | <span data-ttu-id="94595-142">Recupera la modalità di estensione di un'origine video.</span><span class="sxs-lookup"><span data-stu-id="94595-142">Retrieves the stretch mode of a video source.</span></span><br/>                                                 |
| [<span data-ttu-id="94595-143">**IsNormalRate**</span><span class="sxs-lookup"><span data-stu-id="94595-143">**IsNormalRate**</span></span>](iamtimelinesrc-isnormalrate.md)       | <span data-ttu-id="94595-144">Indica se il clip viene riprodotto alla frequenza di riproduzione normale.</span><span class="sxs-lookup"><span data-stu-id="94595-144">Indicates whether the clip will play at the normal playback rate.</span></span><br/>                             |
| [<span data-ttu-id="94595-145">**ModifyStopTime**</span><span class="sxs-lookup"><span data-stu-id="94595-145">**ModifyStopTime**</span></span>](iamtimelinesrc-modifystoptime.md)   | <span data-ttu-id="94595-146">Imposta l'ora di arresto, relativa alla sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="94595-146">Sets the stop time, relative to the timeline.</span></span><br/>                                                 |
| [<span data-ttu-id="94595-147">**ModifyStopTime2**</span><span class="sxs-lookup"><span data-stu-id="94595-147">**ModifyStopTime2**</span></span>](iamtimelinesrc-modifystoptime2.md) | <span data-ttu-id="94595-148">Imposta l'ora di arresto, come valore di **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="94595-148">Sets the stop time, as a **REFTIME** value.</span></span><br/>                                                   |
| [<span data-ttu-id="94595-149">**SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="94595-149">**SetDefaultFPS**</span></span>](iamtimelinesrc-setdefaultfps.md)     | <span data-ttu-id="94595-150">Imposta la frequenza dei fotogrammi predefinita dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="94595-150">Sets the source object's default frame rate.</span></span><br/>                                                  |
| [<span data-ttu-id="94595-151">**SetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="94595-151">**SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)   | <span data-ttu-id="94595-152">Specifica la durata del file di origine.</span><span class="sxs-lookup"><span data-stu-id="94595-152">Specifies the duration of the source file.</span></span><br/>                                                    |
| [<span data-ttu-id="94595-153">**SetMediaLength2**</span><span class="sxs-lookup"><span data-stu-id="94595-153">**SetMediaLength2**</span></span>](iamtimelinesrc-setmedialength2.md) | <span data-ttu-id="94595-154">Specifica la durata del file di origine, come valore **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="94595-154">Specifies the duration of the source file, as a **REFTIME** value.</span></span><br/>                            |
| [<span data-ttu-id="94595-155">**MEDIANAME**</span><span class="sxs-lookup"><span data-stu-id="94595-155">**SetMediaName**</span></span>](iamtimelinesrc-setmedianame.md)       | <span data-ttu-id="94595-156">Specifica il nome del file di origine rappresentato da questo oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="94595-156">Specifies the name of the source file represented by this source object.</span></span><br/>                      |
| [<span data-ttu-id="94595-157">**SetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="94595-157">**SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)     | <span data-ttu-id="94595-158">Imposta l'ora di inizio e di fine del supporto.</span><span class="sxs-lookup"><span data-stu-id="94595-158">Sets the media stop and start times.</span></span><br/>                                                          |
| [<span data-ttu-id="94595-159">**SetMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="94595-159">**SetMediaTimes2**</span></span>](iamtimelinesrc-setmediatimes2.md)   | <span data-ttu-id="94595-160">Imposta l'ora di inizio e di fine del supporto, come valori **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="94595-160">Sets the media stop and start times, as **REFTIME** values.</span></span><br/>                                   |
| [<span data-ttu-id="94595-161">**SetStreamNumber**</span><span class="sxs-lookup"><span data-stu-id="94595-161">**SetStreamNumber**</span></span>](iamtimelinesrc-setstreamnumber.md) | <span data-ttu-id="94595-162">Specifica il flusso da leggere dal file di origine associato a questo oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="94595-162">Specifies which stream to read from the source file associated with this source object.</span></span><br/>       |
| [<span data-ttu-id="94595-163">**SetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="94595-163">**SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)   | <span data-ttu-id="94595-164">Imposta la modalità di estensione di un'origine video.</span><span class="sxs-lookup"><span data-stu-id="94595-164">Sets the stretch mode of a video source.</span></span><br/>                                                      |
| [<span data-ttu-id="94595-165">**SpliceWithNext**</span><span class="sxs-lookup"><span data-stu-id="94595-165">**SpliceWithNext**</span></span>](iamtimelinesrc-splicewithnext.md)   | <span data-ttu-id="94595-166">Unisce questo oggetto di origine a un altro oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="94595-166">Joins this source object to another source object.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="94595-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="94595-167">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="94595-168">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="94595-168">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="94595-169">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="94595-169">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="94595-170">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="94595-170">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="94595-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94595-171">Requirements</span></span>



| <span data-ttu-id="94595-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="94595-172">Requirement</span></span> | <span data-ttu-id="94595-173">Valore</span><span class="sxs-lookup"><span data-stu-id="94595-173">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94595-174">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94595-174">Header</span></span><br/>  | <dl> <span data-ttu-id="94595-175"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="94595-175"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="94595-176">Libreria</span><span class="sxs-lookup"><span data-stu-id="94595-176">Library</span></span><br/> | <dl> <span data-ttu-id="94595-177"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94595-177"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
