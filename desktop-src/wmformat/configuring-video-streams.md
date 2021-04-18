---
title: Configurazione dei flussi video
description: Configurazione dei flussi video
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- flussi, configurazione di flussi video
- codec, configurazione dei flussi video
- flussi video, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d2389026dc1061064c5e687da60c3350ad94a4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299384"
---
# <a name="configuring-video-streams"></a><span data-ttu-id="a36d2-106">Configurazione dei flussi video</span><span class="sxs-lookup"><span data-stu-id="a36d2-106">Configuring Video Streams</span></span>

<span data-ttu-id="a36d2-107">La configurazione dei flussi video è più flessibile rispetto ai flussi audio.</span><span class="sxs-lookup"><span data-stu-id="a36d2-107">Video streams are more flexible in their configuration than audio streams.</span></span> <span data-ttu-id="a36d2-108">Questo perché le proprietà dei frame che compongono il video possono variare notevolmente da un file a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="a36d2-108">This is because the properties of the frames that make up the video can vary widely from one file to the next.</span></span> <span data-ttu-id="a36d2-109">Quando si recupera il formato di codec per il codec in uso, è necessario impostare i valori seguenti per gli oggetti di configurazione del flusso video.</span><span class="sxs-lookup"><span data-stu-id="a36d2-109">When you retrieve the codec format for the codec you are using, you must set the following values for video stream configuration objects.</span></span>



| <span data-ttu-id="a36d2-110">Valore</span><span class="sxs-lookup"><span data-stu-id="a36d2-110">Value</span></span>                                 | <span data-ttu-id="a36d2-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a36d2-111">Description</span></span>                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a36d2-112">Velocità in bit</span><span class="sxs-lookup"><span data-stu-id="a36d2-112">Bit rate</span></span>                              | <span data-ttu-id="a36d2-113">Chiamare [**IWMStreamConfig:: bitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) per impostare sul valore desiderato.</span><span class="sxs-lookup"><span data-stu-id="a36d2-113">Call [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) to set to the desired value.</span></span> <span data-ttu-id="a36d2-114">Il codec video tenterà di comprimere il supporto per soddisfare le specifiche.</span><span class="sxs-lookup"><span data-stu-id="a36d2-114">The video codec will try to compress the media to meet your specifications.</span></span> <span data-ttu-id="a36d2-115">Se i valori sono troppo bassi, il video compresso risultante sarà molto degradato.</span><span class="sxs-lookup"><span data-stu-id="a36d2-115">If your values are too low, the resulting compressed video will be very degraded.</span></span>           |
| <span data-ttu-id="a36d2-116">Finestra buffer</span><span class="sxs-lookup"><span data-stu-id="a36d2-116">Buffer window</span></span>                         | <span data-ttu-id="a36d2-117">Chiamare [**IWMStreamConfig:: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) per impostare sul valore desiderato.</span><span class="sxs-lookup"><span data-stu-id="a36d2-117">Call [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) to set to the desired value.</span></span> <span data-ttu-id="a36d2-118">Il codec video tenterà di comprimere il supporto per soddisfare le specifiche.</span><span class="sxs-lookup"><span data-stu-id="a36d2-118">The video codec will try to compress the media to meet your specifications.</span></span> <span data-ttu-id="a36d2-119">Se i valori sono troppo bassi, il video compresso risultante sarà molto degradato.</span><span class="sxs-lookup"><span data-stu-id="a36d2-119">If your values are too low, the resulting compressed video will be very degraded.</span></span> |
| <span data-ttu-id="a36d2-120">**WMVIDEOINFOHEADER.rcSource**</span><span class="sxs-lookup"><span data-stu-id="a36d2-120">**WMVIDEOINFOHEADER.rcSource**</span></span>        | <span data-ttu-id="a36d2-121">L'angolo superiore sinistro deve essere impostato su 0, 0.</span><span class="sxs-lookup"><span data-stu-id="a36d2-121">The upper left corner must be set to 0,0.</span></span> <span data-ttu-id="a36d2-122">È necessario impostare l'angolo inferiore destro sulle dimensioni del frame.</span><span class="sxs-lookup"><span data-stu-id="a36d2-122">The lower right corner must be set to the frame dimensions.</span></span> <span data-ttu-id="a36d2-123">Ad esempio, in un flusso 640x480 queste impostazioni saranno pari a 0, 0640480.</span><span class="sxs-lookup"><span data-stu-id="a36d2-123">For example, in a 640x480 stream, these settings would be 0,0,640,480.</span></span>                                                                                                |
| <span data-ttu-id="a36d2-124">**WMVIDEOINFOHEADER.rcTarget**</span><span class="sxs-lookup"><span data-stu-id="a36d2-124">**WMVIDEOINFOHEADER.rcTarget**</span></span>        | <span data-ttu-id="a36d2-125">Deve corrispondere a **rcSource**.</span><span class="sxs-lookup"><span data-stu-id="a36d2-125">Must match **rcSource**.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="a36d2-126">**WMVIDEOINFOHEADER.dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="a36d2-126">**WMVIDEOINFOHEADER.dwBitRate**</span></span>       | <span data-ttu-id="a36d2-127">Deve corrispondere alla velocità in bit impostata per il flusso.</span><span class="sxs-lookup"><span data-stu-id="a36d2-127">Must match the bit rate set for the stream.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="a36d2-128">**WMVIDEOINFOHEADER. AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="a36d2-128">**WMVIDEOINFOHEADER.AvgTimePerFrame**</span></span> | <span data-ttu-id="a36d2-129">Impostare sull'ora approssimativa per fotogramma.</span><span class="sxs-lookup"><span data-stu-id="a36d2-129">Set to the approximate time per frame.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="a36d2-130">**BITMAPINFOHEADER. biWidth**</span><span class="sxs-lookup"><span data-stu-id="a36d2-130">**BITMAPINFOHEADER.biWidth**</span></span>          | <span data-ttu-id="a36d2-131">Impostare sulla larghezza, in pixel, della dimensione del fotogramma desiderata.</span><span class="sxs-lookup"><span data-stu-id="a36d2-131">Set to the width, in pixels, of the desired frame size.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="a36d2-132">**BITMAPINFOHEADER. biHeight**</span><span class="sxs-lookup"><span data-stu-id="a36d2-132">**BITMAPINFOHEADER.biHeight**</span></span>         | <span data-ttu-id="a36d2-133">Impostare sull'altezza, in pixel, della dimensione del fotogramma desiderata.</span><span class="sxs-lookup"><span data-stu-id="a36d2-133">Set to the height, in pixels, of the desired frame size.</span></span>                                                                                                                                                                                                                    |



 

<span data-ttu-id="a36d2-134">Il contenuto video non viene eseguito correttamente a meno che non sia codificato con una dimensione che rappresenta un multiplo di quattro per larghezza e altezza.</span><span class="sxs-lookup"><span data-stu-id="a36d2-134">Video content does not play correctly unless it is encoded to a size that is a multiple of four for both width and height.</span></span> <span data-ttu-id="a36d2-135">L'eccezione è il video non compresso [*RGB*](wmformat-glossary.md) , che può essere qualsiasi dimensione.</span><span class="sxs-lookup"><span data-stu-id="a36d2-135">The exception is [*RGB*](wmformat-glossary.md) uncompressed video, which can be any size.</span></span> <span data-ttu-id="a36d2-136">Se si tenta di impostare una dimensione che non è un multiplo di quattro, uno degli errori seguenti verrà restituito dal writer:</span><span class="sxs-lookup"><span data-stu-id="a36d2-136">If you try to set a size that is not a multiple of four, one of the following errors will be returned by the writer:</span></span>

-   <span data-ttu-id="a36d2-137">\_formato di input NS E \_ non valido \_ \_</span><span class="sxs-lookup"><span data-stu-id="a36d2-137">NS\_E\_INVALID\_INPUT\_FORMAT</span></span>
-   <span data-ttu-id="a36d2-138">\_formato di output NS E \_ non valido \_ \_</span><span class="sxs-lookup"><span data-stu-id="a36d2-138">NS\_E\_INVALID\_OUTPUT\_FORMAT</span></span>
-   <span data-ttu-id="a36d2-139">NS \_ E \_ INVALIDPROFILE</span><span class="sxs-lookup"><span data-stu-id="a36d2-139">NS\_E\_INVALIDPROFILE</span></span>

<span data-ttu-id="a36d2-140">Se si utilizza la codifica della velocità in bit variabile, potrebbe essere necessario apportare altre modifiche.</span><span class="sxs-lookup"><span data-stu-id="a36d2-140">If you are using variable bit rate encoding, you may need to make other adjustments.</span></span> <span data-ttu-id="a36d2-141">Per ulteriori informazioni, vedere [configurazione dei flussi VBR](configuring-vbr-streams.md).</span><span class="sxs-lookup"><span data-stu-id="a36d2-141">For more information, see [Configuring VBR Streams](configuring-vbr-streams.md).</span></span>

<span data-ttu-id="a36d2-142">Alcuni Windows Media Video codec supportano più livelli di complessità.</span><span class="sxs-lookup"><span data-stu-id="a36d2-142">Some Windows Media Video codecs support multiple complexity levels.</span></span> <span data-ttu-id="a36d2-143">I livelli di complessità determinano gli algoritmi che il codec userà per la codifica di un flusso video.</span><span class="sxs-lookup"><span data-stu-id="a36d2-143">Complexity levels determine the algorithms that the codec will use when encoding a video stream.</span></span> <span data-ttu-id="a36d2-144">L'utilizzo di un livello di complessità elevato richiede una maggiore potenza di elaborazione per la codifica e la decodifica.</span><span class="sxs-lookup"><span data-stu-id="a36d2-144">Using a high complexity level will require more processing power for encoding and decoding.</span></span>

<span data-ttu-id="a36d2-145">Ogni codec che supporta le impostazioni di complessità espone le impostazioni seguenti che è possibile recuperare con il metodo [**IWMCodecInfo3:: GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) .</span><span class="sxs-lookup"><span data-stu-id="a36d2-145">Each codec that supports complexity settings exposes the following settings that you can retrieve with the [**IWMCodecInfo3::GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) method.</span></span>



| <span data-ttu-id="a36d2-146">Impostazione</span><span class="sxs-lookup"><span data-stu-id="a36d2-146">Setting</span></span>                 | <span data-ttu-id="a36d2-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a36d2-147">Description</span></span>                                         |
|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="a36d2-148">g \_ wszComplexityMax</span><span class="sxs-lookup"><span data-stu-id="a36d2-148">g\_wszComplexityMax</span></span>     | <span data-ttu-id="a36d2-149">Livello di qualità massimo supportato dal codec.</span><span class="sxs-lookup"><span data-stu-id="a36d2-149">The maximum quality level supported by the codec.</span></span>   |
| <span data-ttu-id="a36d2-150">g \_ wszComplexityOffline</span><span class="sxs-lookup"><span data-stu-id="a36d2-150">g\_wszComplexityOffline</span></span> | <span data-ttu-id="a36d2-151">Livello di qualità suggerito per la riproduzione offline.</span><span class="sxs-lookup"><span data-stu-id="a36d2-151">The suggested quality level for offline playback.</span></span>   |
| <span data-ttu-id="a36d2-152">g \_ wszComplexityLive</span><span class="sxs-lookup"><span data-stu-id="a36d2-152">g\_wszComplexityLive</span></span>    | <span data-ttu-id="a36d2-153">Livello di qualità suggerito per la riproduzione del flusso.</span><span class="sxs-lookup"><span data-stu-id="a36d2-153">The suggested quality level for streaming playback.</span></span> |



 

<span data-ttu-id="a36d2-154">Per impostare la complessità per un flusso video in un profilo, usare il metodo [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) usando la proprietà g \_ wszComplexity.</span><span class="sxs-lookup"><span data-stu-id="a36d2-154">To set the complexity for a video stream in a profile, use the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method using the property g\_wszComplexity.</span></span> <span data-ttu-id="a36d2-155">Il valore impostato deve essere minore o uguale alla complessità massima supportata per il codec.</span><span class="sxs-lookup"><span data-stu-id="a36d2-155">The value you set must be less than or equal to the maximum supported complexity for the codec.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a36d2-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a36d2-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a36d2-157">**Configurazione comune a tutti i flussi**</span><span class="sxs-lookup"><span data-stu-id="a36d2-157">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="a36d2-158">**Configurazione di flussi**</span><span class="sxs-lookup"><span data-stu-id="a36d2-158">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="a36d2-159">**Impostazioni di complessità video**</span><span class="sxs-lookup"><span data-stu-id="a36d2-159">**Video Complexity Settings**</span></span>](video-complexity-settings.md)
</dt> </dl>

 

 




