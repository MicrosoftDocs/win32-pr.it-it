---
description: L'interfaccia IMediaDet recupera le informazioni su un file multimediale, ad esempio il numero di flussi e il tipo di supporto, la durata e la frequenza dei fotogrammi di ogni flusso.
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: Interfaccia IMediaDet (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ca5c87a1424872491aba5dcf4e01011872e9ff36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325305"
---
# <a name="imediadet-interface"></a><span data-ttu-id="c9538-103">Interfaccia IMediaDet</span><span class="sxs-lookup"><span data-stu-id="c9538-103">IMediaDet interface</span></span>

> [!Note]  
> <span data-ttu-id="c9538-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c9538-104">\[Deprecated.</span></span> <span data-ttu-id="c9538-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c9538-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c9538-106">L' `IMediaDet` interfaccia recupera le informazioni su un file multimediale, ad esempio il numero di flussi e il tipo di supporto, la durata e la frequenza dei fotogrammi di ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="c9538-106">The `IMediaDet` interface retrieves information about a media file, such as the number of streams, and the media type, duration, and frame rate of each stream.</span></span> <span data-ttu-id="c9538-107">Contiene inoltre metodi per il recupero di singoli frame da un flusso video.</span><span class="sxs-lookup"><span data-stu-id="c9538-107">It also contains methods for retrieving individual frames from a video stream.</span></span> <span data-ttu-id="c9538-108">L'oggetto [mediadet (Media Detector)](media-detector--mediadet.md) espone questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c9538-108">The [Media Detector (MediaDet)](media-detector--mediadet.md) object exposes this interface.</span></span>

<span data-ttu-id="c9538-109">Per ottenere informazioni su un file usando questa interfaccia, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="c9538-109">To obtain information about a file using this interface, perform the following steps:</span></span>

1.  <span data-ttu-id="c9538-110">Creare un'istanza dell'oggetto MediaDet chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="c9538-110">Create an instance of the MediaDet object by calling **CoCreateInstance**.</span></span> <span data-ttu-id="c9538-111">L'ID di classe è CLSID \_ mediadet.</span><span class="sxs-lookup"><span data-stu-id="c9538-111">The class ID is CLSID\_MediaDet.</span></span>
2.  <span data-ttu-id="c9538-112">Chiamare [**IMediaDet::p \_ nome file UT**](imediadet-put-filename.md) per specificare il nome del file di origine.</span><span class="sxs-lookup"><span data-stu-id="c9538-112">Call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to specify the name of the source file.</span></span>
3.  <span data-ttu-id="c9538-113">Chiamare [**IMediaDet:: Get \_ OutputStreams**](imediadet-get-outputstreams.md) per ottenere il numero di flussi di output nell'origine.</span><span class="sxs-lookup"><span data-stu-id="c9538-113">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to obtain the number of output streams in the source.</span></span>
4.  <span data-ttu-id="c9538-114">Chiamare [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md) per specificare un determinato flusso.</span><span class="sxs-lookup"><span data-stu-id="c9538-114">Call [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md) to specify a particular stream.</span></span>
5.  <span data-ttu-id="c9538-115">Chiamare uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9538-115">Call any of the following methods:</span></span>
    -   [<span data-ttu-id="c9538-116">**IMediaDet:: Get \_ framerate**</span><span class="sxs-lookup"><span data-stu-id="c9538-116">**IMediaDet::get\_FrameRate**</span></span>](imediadet-get-framerate.md)
    -   [<span data-ttu-id="c9538-117">**IMediaDet:: Get \_ StreamLength**</span><span class="sxs-lookup"><span data-stu-id="c9538-117">**IMediaDet::get\_StreamLength**</span></span>](imediadet-get-streamlength.md)
    -   [<span data-ttu-id="c9538-118">**IMediaDet:: Get \_ StreamMediaType**</span><span class="sxs-lookup"><span data-stu-id="c9538-118">**IMediaDet::get\_StreamMediaType**</span></span>](imediadet-get-streammediatype.md)
    -   [<span data-ttu-id="c9538-119">**IMediaDet:: Get \_ StreamType**</span><span class="sxs-lookup"><span data-stu-id="c9538-119">**IMediaDet::get\_StreamType**</span></span>](imediadet-get-streamtype.md)

<span data-ttu-id="c9538-120">Per recuperare un frame video, chiamare [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) o [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md).</span><span class="sxs-lookup"><span data-stu-id="c9538-120">To retrieve a video frame, call [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md).</span></span> <span data-ttu-id="c9538-121">Il frame restituito è sempre in formato RGB a 24 bit.</span><span class="sxs-lookup"><span data-stu-id="c9538-121">The returned frame is always in 24-bit RGB format.</span></span>

> [!Note]  
> <span data-ttu-id="c9538-122">Non usare lo stesso oggetto MediaDet con più file.</span><span class="sxs-lookup"><span data-stu-id="c9538-122">Do not use the same MediaDet object with multiple files.</span></span> <span data-ttu-id="c9538-123">Per ottenere informazioni o fotogrammi video da più di un file, usare istanze MediaDet separate.</span><span class="sxs-lookup"><span data-stu-id="c9538-123">To get information or video frames from more than one file, use separate MediaDet instances.</span></span>

 

<span data-ttu-id="c9538-124">L'interfaccia **IMediaDet** non supporta i formati [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , pertanto non è possibile usare questa interfaccia per ottenere campi interlacciati o informazioni sull'interlacciamento.</span><span class="sxs-lookup"><span data-stu-id="c9538-124">The **IMediaDet** interface does not support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats, so you cannot use this interface to get interlaced fields or information about interlacing.</span></span> <span data-ttu-id="c9538-125">Inoltre, se il decodificatore upstream supporta solo **VIDEOINFOHEADER2**, non è possibile utilizzare `IMediaDet` .</span><span class="sxs-lookup"><span data-stu-id="c9538-125">Also, if the upstream decoder supports only **VIDEOINFOHEADER2**, you cannot use `IMediaDet`.</span></span> <span data-ttu-id="c9538-126">Questo potrebbe essere il caso di un decodificatore MPEG-2, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="c9538-126">This might be the case with an MPEG-2 decoder, for example.</span></span> <span data-ttu-id="c9538-127">Inoltre, l' `IMediaDet` interfaccia ignora tutti i flussi nel file che non sono video o audio.</span><span class="sxs-lookup"><span data-stu-id="c9538-127">Also, the `IMediaDet` interface ignores any streams in the file that are not video or audio.</span></span> <span data-ttu-id="c9538-128">Se, ad esempio, il file contiene un flusso audio, un flusso di dati e un flusso video, il metodo **get \_ OutputStreams** segnalerà solo due flussi (audio e video).</span><span class="sxs-lookup"><span data-stu-id="c9538-128">For example, if the file contains an audio stream, a data stream, and a video stream, the **get\_OutputStreams** method will report only two streams (the audio and video).</span></span>

## <a name="members"></a><span data-ttu-id="c9538-129">Membri</span><span class="sxs-lookup"><span data-stu-id="c9538-129">Members</span></span>

<span data-ttu-id="c9538-130">L'interfaccia **IMediaDet** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c9538-130">The **IMediaDet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c9538-131">**IMediaDet** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c9538-131">**IMediaDet** also has these types of members:</span></span>

-   [<span data-ttu-id="c9538-132">Metodi</span><span class="sxs-lookup"><span data-stu-id="c9538-132">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c9538-133">Metodi</span><span class="sxs-lookup"><span data-stu-id="c9538-133">Methods</span></span>

<span data-ttu-id="c9538-134">L'interfaccia **IMediaDet** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c9538-134">The **IMediaDet** interface has these methods.</span></span>



| <span data-ttu-id="c9538-135">Metodo</span><span class="sxs-lookup"><span data-stu-id="c9538-135">Method</span></span>                                                        | <span data-ttu-id="c9538-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9538-136">Description</span></span>                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9538-137">**EnterBitmapGrabMode**</span><span class="sxs-lookup"><span data-stu-id="c9538-137">**EnterBitmapGrabMode**</span></span>](imediadet-enterbitmapgrabmode.md)  | <span data-ttu-id="c9538-138">Passa il rilevatore di contenuti multimediali alla modalità di cattura della bitmap e cerca il grafico del filtro a un orario specificato.</span><span class="sxs-lookup"><span data-stu-id="c9538-138">Switches the media detector to bitmap grab mode and seeks the filter graph to a specified time.</span></span><br/> |
| [<span data-ttu-id="c9538-139">**ottenere \_ CurrentStream**</span><span class="sxs-lookup"><span data-stu-id="c9538-139">**get\_CurrentStream**</span></span>](imediadet-get-currentstream.md)     | <span data-ttu-id="c9538-140">Recupera il numero di flusso attualmente utilizzato dal rilevamento multimediale.</span><span class="sxs-lookup"><span data-stu-id="c9538-140">Retrieves the stream number currently used by the media detector.</span></span><br/>                               |
| [<span data-ttu-id="c9538-141">**Ottieni \_ nome file**</span><span class="sxs-lookup"><span data-stu-id="c9538-141">**get\_Filename**</span></span>](imediadet-get-filename.md)               | <span data-ttu-id="c9538-142">Recupera il nome del file di origine attualmente utilizzato dal rilevamento multimediale.</span><span class="sxs-lookup"><span data-stu-id="c9538-142">Retrieves the name of the source file currently used by the media detector.</span></span><br/>                     |
| [<span data-ttu-id="c9538-143">**Ottieni \_ filtro**</span><span class="sxs-lookup"><span data-stu-id="c9538-143">**get\_Filter**</span></span>](imediadet-get-filter.md)                   | <span data-ttu-id="c9538-144">Recupera un puntatore al filtro di origine attualmente utilizzato dal rilevamento multimediale.</span><span class="sxs-lookup"><span data-stu-id="c9538-144">Retrieves a pointer to the source filter currently used by the media detector.</span></span><br/>                  |
| [<span data-ttu-id="c9538-145">**Ottieni \_ framerate**</span><span class="sxs-lookup"><span data-stu-id="c9538-145">**get\_FrameRate**</span></span>](imediadet-get-framerate.md)             | <span data-ttu-id="c9538-146">Recupera la frequenza dei fotogrammi del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="c9538-146">Retrieves the frame rate of the current stream.</span></span><br/>                                                 |
| [<span data-ttu-id="c9538-147">**ottenere \_ OutputStreams**</span><span class="sxs-lookup"><span data-stu-id="c9538-147">**get\_OutputStreams**</span></span>](imediadet-get-outputstreams.md)     | <span data-ttu-id="c9538-148">Recupera il numero di flussi audio e video contenuti nell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="c9538-148">Retrieves the number of audio and video streams contained in the media source.</span></span><br/>                  |
| [<span data-ttu-id="c9538-149">**ottenere \_ StreamLength**</span><span class="sxs-lookup"><span data-stu-id="c9538-149">**get\_StreamLength**</span></span>](imediadet-get-streamlength.md)       | <span data-ttu-id="c9538-150">Recupera la durata del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="c9538-150">Retrieves the duration of the current stream.</span></span><br/>                                                   |
| [<span data-ttu-id="c9538-151">**ottenere \_ StreamMediaType**</span><span class="sxs-lookup"><span data-stu-id="c9538-151">**get\_StreamMediaType**</span></span>](imediadet-get-streammediatype.md) | <span data-ttu-id="c9538-152">Recupera il tipo di supporto del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="c9538-152">Retrieves the media type of the current stream.</span></span><br/>                                                 |
| [<span data-ttu-id="c9538-153">**ottenere \_ StreamType**</span><span class="sxs-lookup"><span data-stu-id="c9538-153">**get\_StreamType**</span></span>](imediadet-get-streamtype.md)           | <span data-ttu-id="c9538-154">Recupera l'identificatore univoco globale (GUID) per il tipo di supporto del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="c9538-154">Retrieves the globally unique identifier (GUID) for the media type of the current stream.</span></span><br/>       |
| [<span data-ttu-id="c9538-155">**ottenere \_ StreamTypeB**</span><span class="sxs-lookup"><span data-stu-id="c9538-155">**get\_StreamTypeB**</span></span>](imediadet-get-streamtypeb.md)         | <span data-ttu-id="c9538-156">Recupera una stringa che rappresenta il GUID del tipo di supporto per il flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="c9538-156">Retrieves a string representing the GUID of the media type for the current stream.</span></span><br/>              |
| [<span data-ttu-id="c9538-157">**GetBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="c9538-157">**GetBitmapBits**</span></span>](imediadet-getbitmapbits.md)              | <span data-ttu-id="c9538-158">Recupera un frame video al momento del supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="c9538-158">Retrieves a video frame at the specified media time.</span></span><br/>                                            |
| [<span data-ttu-id="c9538-159">**GetSampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="c9538-159">**GetSampleGrabber**</span></span>](imediadet-getsamplegrabber.md)        | <span data-ttu-id="c9538-160">Recupera un puntatore all'interfaccia [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="c9538-160">Retrieves a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span><br/>                  |
| [<span data-ttu-id="c9538-161">**Inserisci \_ CurrentStream**</span><span class="sxs-lookup"><span data-stu-id="c9538-161">**put\_CurrentStream**</span></span>](imediadet-put-currentstream.md)     | <span data-ttu-id="c9538-162">Specifica il numero di flusso per il rilevatore multimediale da usare.</span><span class="sxs-lookup"><span data-stu-id="c9538-162">Specifies the stream number for the media detector to use.</span></span><br/>                                      |
| [<span data-ttu-id="c9538-163">**Inserisci \_ nome file**</span><span class="sxs-lookup"><span data-stu-id="c9538-163">**put\_Filename**</span></span>](imediadet-put-filename.md)               | <span data-ttu-id="c9538-164">Specifica il nome del file di origine per il rilevatore multimediale da usare.</span><span class="sxs-lookup"><span data-stu-id="c9538-164">Specifies the name of the source file for the media detector to use.</span></span><br/>                            |
| [<span data-ttu-id="c9538-165">**Inserisci \_ filtro**</span><span class="sxs-lookup"><span data-stu-id="c9538-165">**put\_Filter**</span></span>](imediadet-put-filter.md)                   | <span data-ttu-id="c9538-166">Specifica un filtro di origine per il rilevatore di contenuti multimediali da usare.</span><span class="sxs-lookup"><span data-stu-id="c9538-166">Specifies a source filter for the media detector to use.</span></span><br/>                                        |
| [<span data-ttu-id="c9538-167">**WriteBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="c9538-167">**WriteBitmapBits**</span></span>](imediadet-writebitmapbits.md)          | <span data-ttu-id="c9538-168">Recupera un frame video nel tempo di supporto specificato e lo scrive in un file.</span><span class="sxs-lookup"><span data-stu-id="c9538-168">Retrieves a video frame at the specified media time and writes it to a file.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="c9538-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9538-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c9538-170">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="c9538-170">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c9538-171">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c9538-171">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c9538-172">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c9538-172">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c9538-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9538-173">Requirements</span></span>



| <span data-ttu-id="c9538-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9538-174">Requirement</span></span> | <span data-ttu-id="c9538-175">Valore</span><span class="sxs-lookup"><span data-stu-id="c9538-175">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9538-176">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9538-176">Header</span></span><br/>  | <dl> <span data-ttu-id="c9538-177"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9538-177"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c9538-178">Libreria</span><span class="sxs-lookup"><span data-stu-id="c9538-178">Library</span></span><br/> | <dl> <span data-ttu-id="c9538-179"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9538-179"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
