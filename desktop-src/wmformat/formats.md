---
title: Formati
description: Formati
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- Windows Media Format SDK, input
- Windows Media Format SDK, flussi
- Windows Media Format SDK, output
- Windows Media Format SDK, formati
- Advanced Systems Format (ASF), input
- ASF (formato avanzato dei sistemi), input
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- ASF (Advanced Systems Format), output
- ASF (formato avanzato dei sistemi), output
- Formato ASF (Advanced Systems Format), formati
- ASF (formato avanzato dei sistemi), formati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e7895c27af3eb99e96d7009b79ea8df0011208
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331487"
---
# <a name="formats"></a><span data-ttu-id="49d5d-115">Formati</span><span class="sxs-lookup"><span data-stu-id="49d5d-115">Formats</span></span>

<span data-ttu-id="49d5d-116">Le informazioni in un formato descrivono tutti gli elementi necessari per conoscere un particolare tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="49d5d-116">The information in a format describes everything you need to know about a particular type of media.</span></span> <span data-ttu-id="49d5d-117">Ogni formato ha un tipo principale, ad esempio audio o video, e può avere un sottotipo.</span><span class="sxs-lookup"><span data-stu-id="49d5d-117">Every format has a major type, like audio or video, and may have a subtype.</span></span> <span data-ttu-id="49d5d-118">I formati contengono informazioni diverse in base al tipo principale.</span><span class="sxs-lookup"><span data-stu-id="49d5d-118">Formats contain different information based on major type.</span></span> <span data-ttu-id="49d5d-119">I formati audio e video richiedono molto più informazioni rispetto ad altri tipi.</span><span class="sxs-lookup"><span data-stu-id="49d5d-119">Audio and video formats require much more information than other types.</span></span>

<span data-ttu-id="49d5d-120">Proprio come gli oggetti di Windows Media Format SDK distinguono tra i numeri di input, i numeri di flusso e i numeri di output (vedere [input, flussi e](inputs-streams-and-outputs.md)output), esistono differenze importanti tra i formati di input, i formati di flusso e i formati di output.</span><span class="sxs-lookup"><span data-stu-id="49d5d-120">Just as the objects of the Windows Media Format SDK differentiate between input numbers, stream numbers, and output numbers (see [Inputs, Streams and Outputs](inputs-streams-and-outputs.md)), there are important distinctions between input formats, stream formats, and output formats.</span></span> <span data-ttu-id="49d5d-121">Queste differenze sono descritte di seguito:</span><span class="sxs-lookup"><span data-stu-id="49d5d-121">These differences are described here:</span></span>

## <a name="input-formats"></a><span data-ttu-id="49d5d-122">Formati di input</span><span class="sxs-lookup"><span data-stu-id="49d5d-122">Input Formats</span></span>

<span data-ttu-id="49d5d-123">Un formato di input descrive i supporti digitali passati all'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="49d5d-123">An input format describes the digital media that you pass to the writer object.</span></span> <span data-ttu-id="49d5d-124">Se un flusso in un file ASF viene compresso con un codec, il codec supporterà solo determinati formati di input.</span><span class="sxs-lookup"><span data-stu-id="49d5d-124">If a stream in an ASF file is compressed with a codec, the codec will support only certain input formats.</span></span> <span data-ttu-id="49d5d-125">Quando si utilizzano i codec Windows Media Audio e video, è possibile enumerare i formati di input supportati utilizzando l'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="49d5d-125">When using the Windows Media Audio and Video codecs, you can enumerate the supported input formats using the writer object.</span></span> <span data-ttu-id="49d5d-126">Quando si scrive un file, si è responsabili della selezione di un formato di input corrispondente al supporto di input.</span><span class="sxs-lookup"><span data-stu-id="49d5d-126">When writing a file, you are responsible for selecting an input format that matches your input media.</span></span>

<span data-ttu-id="49d5d-127">Sebbene il formato dei supporti di input debba essere supportato dal codec che comprimerà i dati, alcune impostazioni del formato di input non devono corrispondere al formato del flusso.</span><span class="sxs-lookup"><span data-stu-id="49d5d-127">Although the input media format must be supported by the codec that will compress the data, some input format settings need not match the stream format.</span></span> <span data-ttu-id="49d5d-128">Il formato di input per un flusso video, ad esempio, può avere dimensioni del frame diverse da quelle definite nel formato del flusso.</span><span class="sxs-lookup"><span data-stu-id="49d5d-128">For example, the input format for a video stream may have a frame size that is different from that defined in the stream format.</span></span> <span data-ttu-id="49d5d-129">In questi casi, il codec eseguirà le conversioni.</span><span class="sxs-lookup"><span data-stu-id="49d5d-129">The codec will perform conversions in these cases.</span></span>

## <a name="stream-formats"></a><span data-ttu-id="49d5d-130">Formati di flusso</span><span class="sxs-lookup"><span data-stu-id="49d5d-130">Stream Formats</span></span>

<span data-ttu-id="49d5d-131">Un formato di flusso descrive il formato del supporto archiviato nel file ASF.</span><span class="sxs-lookup"><span data-stu-id="49d5d-131">A stream format describes the form of the media as it is stored in the ASF file.</span></span> <span data-ttu-id="49d5d-132">Il formato del flusso è il formato descritto nel profilo e può essere uguale o meno al formato di input e di output.</span><span class="sxs-lookup"><span data-stu-id="49d5d-132">The stream format is the format described in the profile, and may or may not be the same as the input format and output format.</span></span> <span data-ttu-id="49d5d-133">Se viene usato un codec per comprimere i dati in un flusso, il formato del flusso sarà diverso dai formati di input e di output.</span><span class="sxs-lookup"><span data-stu-id="49d5d-133">If a codec is used to compress the data in a stream, the stream format will be different than the input and output formats.</span></span>

<span data-ttu-id="49d5d-134">Quando si usano i codec Windows Media Audio e video, è necessario ottenere un elenco di formati di flusso supportati dal codec per assicurarsi che non si stia tentando di specificare un formato non supportato dal codice.</span><span class="sxs-lookup"><span data-stu-id="49d5d-134">When using the Windows Media Audio and Video codecs, you must obtain a list of supported stream formats from the codec to ensure that you are not attempting to specify a format that the code does not support.</span></span> <span data-ttu-id="49d5d-135">Alcune impostazioni di formato, ad esempio le dimensioni e la profondità dei colori di un frame video, devono essere configurate manualmente dopo aver recuperato il formato del codec.</span><span class="sxs-lookup"><span data-stu-id="49d5d-135">Some format settings, such as the size and color depth of a video frame, must be configured manually after the codec format is retrieved.</span></span>

## <a name="output-formats"></a><span data-ttu-id="49d5d-136">Formati di output</span><span class="sxs-lookup"><span data-stu-id="49d5d-136">Output Formats</span></span>

<span data-ttu-id="49d5d-137">Un formato di output descrive i supporti digitali che il lettore (o il lettore sincrono) recapita alla propria applicazione.</span><span class="sxs-lookup"><span data-stu-id="49d5d-137">An output format describes the digital media that the reader (or synchronous reader) delivers to your application.</span></span> <span data-ttu-id="49d5d-138">Se un flusso in un file ASF viene compresso con un codec, il codec supporterà solo determinati formati di output.</span><span class="sxs-lookup"><span data-stu-id="49d5d-138">If a stream in an ASF file is compressed with a codec, the codec will support only certain output formats.</span></span> <span data-ttu-id="49d5d-139">Quando si usano i codec Windows Media Audio e video, è possibile enumerare i formati di output supportati usando l'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="49d5d-139">When using the Windows Media Audio and Video codecs, you can enumerate the supported output formats by using the reader object.</span></span> <span data-ttu-id="49d5d-140">Ogni codec Windows Media ha un formato di output predefinito, ma è possibile selezionare qualsiasi formato di output supportato per il recapito di esempio.</span><span class="sxs-lookup"><span data-stu-id="49d5d-140">Each of the Windows Media codecs has a default output format, but you can select any supported output format for sample delivery.</span></span>

<span data-ttu-id="49d5d-141">Sebbene il formato dei supporti di output debba essere supportato dal codec che ha compresso i dati, alcune impostazioni del formato di output non devono corrispondere al formato del flusso.</span><span class="sxs-lookup"><span data-stu-id="49d5d-141">Although the output media format must be supported by the codec that compressed the data, some output format settings need not match the stream format.</span></span> <span data-ttu-id="49d5d-142">Ad esempio, il formato di output per un flusso video potrebbe avere dimensioni del frame diverse da quelle definite nel formato del flusso.</span><span class="sxs-lookup"><span data-stu-id="49d5d-142">For example, the output format for a video stream may have a frame size that is different from that defined in the stream format.</span></span> <span data-ttu-id="49d5d-143">In questi casi, il codec eseguirà le conversioni.</span><span class="sxs-lookup"><span data-stu-id="49d5d-143">The codec will perform conversions in these cases.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49d5d-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="49d5d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49d5d-145">**Concetti**</span><span class="sxs-lookup"><span data-stu-id="49d5d-145">**Concepts**</span></span>](concepts.md)
</dt> </dl>

 

 




