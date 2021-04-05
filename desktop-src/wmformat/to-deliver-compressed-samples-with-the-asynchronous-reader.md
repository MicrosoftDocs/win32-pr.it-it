---
title: Per recapitare esempi compressi con il lettore asincrono
description: Per recapitare esempi compressi con il lettore asincrono
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- Advanced Systems Format (ASF), distribuzione di esempi compressi
- ASF (Advanced Systems Format), distribuzione di esempi compressi
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- ASF (Advanced Systems Format), esempi compressi
- ASF (Advanced Systems Format), esempi compressi
- Reader asincroni, distribuzione di esempi compressi
- Reader asincroni, esempi compressi
- esempi compressi, distribuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ce835075f5bd760014a3b1b776ba3627adb076
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723535"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a><span data-ttu-id="7c4a7-112">Per recapitare esempi compressi con il lettore asincrono</span><span class="sxs-lookup"><span data-stu-id="7c4a7-112">To Deliver Compressed Samples with the Asynchronous Reader</span></span>

<span data-ttu-id="7c4a7-113">Il lettore asincrono può recapitare esempi compressi dai flussi nei file ASF.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-113">The asynchronous reader can deliver compressed samples from streams in ASF files.</span></span> <span data-ttu-id="7c4a7-114">Le applicazioni in genere inviano esempi compressi quando si copia un flusso da un file a un altro.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-114">Applications usually deliver compressed samples when copying a stream from one file to another.</span></span> <span data-ttu-id="7c4a7-115">Non è consigliabile ricomprimere i dati ricostruiti da un flusso compresso, perché i dati vengono persi nel processo di codifica.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-115">It is not advisable to recompress data that has been reconstructed from a compressed stream, because data is lost in the encoding process.</span></span> <span data-ttu-id="7c4a7-116">I file multimediali digitali compressi più di una volta avranno una notevole riduzione della qualità.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-116">Digital media that has been compressed more than once will have a noticeable decrease in quality.</span></span>

<span data-ttu-id="7c4a7-117">Windows Media Format SDK non fornisce alcun metodo per la decodifica dei dati dopo che è stato Estratto da un file ASF.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-117">The Windows Media Format SDK does not provide any methods for decoding data after it has been extracted from an ASF file.</span></span> <span data-ttu-id="7c4a7-118">Se si ricevono esempi compressi e successivamente si desidera decomprimerli, sarà necessario fornire il proprio codice a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-118">If you receive compressed samples and later want to decompress them, you will have to provide your own code to do so.</span></span> <span data-ttu-id="7c4a7-119">Per aggirare questa limitazione, è possibile scrivere gli esempi compressi in un nuovo file ASF e quindi leggerli nuovamente in campioni normali non compressi.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-119">One way to get around this limitation is to write the compressed samples to a new ASF file and then re-read them into normal, uncompressed samples.</span></span>

<span data-ttu-id="7c4a7-120">Per ricevere esempi compressi con il lettore asincrono, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-120">To receive compressed samples with the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="7c4a7-121">Implementare il callback [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) .</span><span class="sxs-lookup"><span data-stu-id="7c4a7-121">Implement the [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback.</span></span> <span data-ttu-id="7c4a7-122">Questo callback è sostanzialmente identico nella funzione di [**IWMReaderCallback:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) con la differenza che fornisce esempi in base al numero di flusso e gli esempi sono ancora compressi.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-122">This callback is basically identical in function to [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) except that it delivers samples by stream number and the samples are still compressed.</span></span>
2.  <span data-ttu-id="7c4a7-123">Prima di avviare la riproduzione, ottenere un puntatore all'interfaccia [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) dell'oggetto Reader chiamando **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-123">Before starting playback, obtain a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
3.  <span data-ttu-id="7c4a7-124">Configurare il Reader per il recapito di esempi compressi per il flusso desiderato chiamando [**IWMReaderAdvanced:: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).</span><span class="sxs-lookup"><span data-stu-id="7c4a7-124">Configure the reader to deliver compressed samples for the desired stream by calling [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).</span></span>
4.  <span data-ttu-id="7c4a7-125">Ripetere il passaggio 3 per ogni flusso per il quale si desidera il recapito di esempio compresso.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-125">Repeat step 3 for each stream for which compressed sample delivery is desired.</span></span>

> [!Note]  
> <span data-ttu-id="7c4a7-126">I flussi di immagini non sono validi per il recapito di flussi compressi.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-126">Image streams are not valid for compressed stream delivery.</span></span> <span data-ttu-id="7c4a7-127">Se si copia un flusso di immagini da un file a un altro, non funzionerà nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-127">If you copy an image stream from one file to another, it will not work in the new file.</span></span> <span data-ttu-id="7c4a7-128">Per copiare un flusso di immagini da un file a un altro, recuperare gli esempi di flusso dell'immagine in base al numero di output e includerli nel nuovo file come se fosse incluso un nuovo flusso di immagine.</span><span class="sxs-lookup"><span data-stu-id="7c4a7-128">To copy an image stream from file to file, retrieve the image stream samples by output number and include them in the new file as if including a new image stream.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7c4a7-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c4a7-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c4a7-130">**Interfaccia IWMReaderCallbackAdvanced**</span><span class="sxs-lookup"><span data-stu-id="7c4a7-130">**IWMReaderCallbackAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[<span data-ttu-id="7c4a7-131">**Lettura di file con il lettore asincrono**</span><span class="sxs-lookup"><span data-stu-id="7c4a7-131">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




