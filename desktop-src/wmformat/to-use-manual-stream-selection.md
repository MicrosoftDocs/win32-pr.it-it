---
title: Per usare la selezione del flusso manuale
description: Per usare la selezione del flusso manuale
ms.assetid: 49ec283f-670a-4a0e-9477-c60a80919a1e
keywords:
- ASF (Advanced Systems Format), selezione del flusso manuale
- ASF (formato avanzato dei sistemi), selezione del flusso manuale
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- ASF (Advanced Systems Format), selezione flusso
- ASF (formato avanzato dei sistemi), selezione flusso
- Formato di sistemi avanzati (ASF), esclusione reciproca
- ASF (formato avanzato dei sistemi), esclusione reciproca
- Reader asincroni, selezione flusso manuale
- Reader asincroni, selezione flusso
- flussi, selezione manuale
- esclusione reciproca, selezione flusso manuale
- flussi, lettori asincroni
- esclusione reciproca, lettori asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c493bc8f41bc2a03ba15832ed402939adbeff
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299424"
---
# <a name="to-use-manual-stream-selection"></a><span data-ttu-id="64c0e-117">Per usare la selezione del flusso manuale</span><span class="sxs-lookup"><span data-stu-id="64c0e-117">To Use Manual Stream Selection</span></span>

<span data-ttu-id="64c0e-118">Quando si recapitano campioni non compressi con l'oggetto Reader, è possibile recapitarli solo in base al numero di output.</span><span class="sxs-lookup"><span data-stu-id="64c0e-118">When delivering uncompressed samples with the reader object, you can deliver them only by output number.</span></span> <span data-ttu-id="64c0e-119">Nel caso di flussi che si escludono a vicenda, ciò significa che è possibile ricevere esempi solo da un flusso nell'esclusione reciproca alla volta.</span><span class="sxs-lookup"><span data-stu-id="64c0e-119">In the case of mutually exclusive streams, this means that you can receive samples only from one stream in the mutual exclusion at a time.</span></span> <span data-ttu-id="64c0e-120">Il processo di scelta del flusso che si escludono reciprocamente per la distribuzione è denominato selezione dei flussi.</span><span class="sxs-lookup"><span data-stu-id="64c0e-120">The process of choosing which mutually exclusive stream to deliver is called stream selection.</span></span>

<span data-ttu-id="64c0e-121">Per l'esclusione reciproca della velocità in bit, il lettore esegue automaticamente le selezioni del flusso in base alle condizioni nel computer host durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="64c0e-121">For bit-rate mutual exclusion, the reader makes stream selections automatically based on the conditions on the host machine at playback.</span></span> <span data-ttu-id="64c0e-122">Per altri tipi di esclusione reciproca, il lettore fornirà esempi dal flusso predefinito a meno che non si selezioni manualmente un flusso diverso.</span><span class="sxs-lookup"><span data-stu-id="64c0e-122">For other types of mutual exclusion, the reader will deliver samples from the default stream unless you manually select a different stream yourself.</span></span> <span data-ttu-id="64c0e-123">Potrebbero inoltre essere presenti istanze in cui si desidera selezionare un flusso manualmente da un'esclusione reciproca con frequenza di bit.</span><span class="sxs-lookup"><span data-stu-id="64c0e-123">There may also be instances when you want to select a stream manually from a bit-rate mutual exclusion.</span></span>

<span data-ttu-id="64c0e-124">La selezione del flusso manuale è attiva o disattiva per l'intero file.</span><span class="sxs-lookup"><span data-stu-id="64c0e-124">Manual stream selection is either on or off for the entire file.</span></span> <span data-ttu-id="64c0e-125">Se un file contiene l'esclusione reciproca con velocità in bit e un altro tipo di esclusione reciproca, è necessario selezionare manualmente i flussi basati sulla velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="64c0e-125">If a file contains bit-rate mutual exclusion and some other mutual exclusion type, you must select the bit rate based streams manually.</span></span>

<span data-ttu-id="64c0e-126">Per selezionare un flusso a esclusione reciproca manualmente, è necessario eseguire i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="64c0e-126">To select a mutually exclusive stream manually, you must perform the following steps.</span></span>

1.  <span data-ttu-id="64c0e-127">Recuperare un puntatore all'interfaccia [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) dell'oggetto Reader chiamando **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="64c0e-127">Retrieve a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="64c0e-128">Abilitare la selezione del flusso manuale chiamando [**IWMReaderAdvanced:: SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).</span><span class="sxs-lookup"><span data-stu-id="64c0e-128">Enable manual stream selection by calling [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).</span></span>
3.  <span data-ttu-id="64c0e-129">Per sapere se è selezionato un determinato flusso, chiamare [**IWMReaderAdvanced:: GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected).</span><span class="sxs-lookup"><span data-stu-id="64c0e-129">To find out if a particular stream is selected, call [**IWMReaderAdvanced::GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected).</span></span> <span data-ttu-id="64c0e-130">È necessario passare un puntatore a una variabile del tipo di enumerazione di [**\_ \_ selezione del flusso WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) .</span><span class="sxs-lookup"><span data-stu-id="64c0e-130">You must pass a pointer to a variable of the [**WMT\_STREAM\_SELECTION**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) enumeration type.</span></span> <span data-ttu-id="64c0e-131">Quando la chiamata viene restituita, il valore nella variabile descrive il tipo di selezione corrente del flusso.</span><span class="sxs-lookup"><span data-stu-id="64c0e-131">When the call returns, the value in the variable will describe the current selection type of the stream.</span></span>
4.  <span data-ttu-id="64c0e-132">Per selezionare un flusso, chiamare [**IWMReaderAdvanced:: SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected).</span><span class="sxs-lookup"><span data-stu-id="64c0e-132">To select a stream, call [**IWMReaderAdvanced::SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected).</span></span> <span data-ttu-id="64c0e-133">Questo metodo consente di specificare più flussi contemporaneamente per il cambio di flusso sincronizzato.</span><span class="sxs-lookup"><span data-stu-id="64c0e-133">This method enables you to specify multiple streams at the same time for synchronized stream switching.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64c0e-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="64c0e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64c0e-135">**Lettura di file con il lettore asincrono**</span><span class="sxs-lookup"><span data-stu-id="64c0e-135">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




