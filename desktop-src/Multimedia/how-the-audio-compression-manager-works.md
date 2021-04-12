---
title: Funzionamento di Gestione compressione audio
description: Funzionamento di Gestione compressione audio
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- audio multimediale, Gestione compressione audio (ACM)
- audio, Gestione compressione audio (ACM)
- Gestione compressione audio (ACM), informazioni
- ACM (Gestione compressione audio), informazioni
- Gestione compressione audio (ACM), driver di codec
- ACM (Gestione compressione audio), driver di codec
- Gestione compressione audio (ACM), driver del convertitore di formato
- ACM (Gestione compressione audio), driver del convertitore di formato
- Gestione compressione audio (ACM), driver di filtro
- ACM (Gestione compressione audio), driver di filtro
- Gestione compressione audio (ACM), driver compressore
- ACM (Gestione compressione audio), driver del compressore
- Gestione compressione audio (ACM), driver di decompressione
- ACM (Gestione compressione audio), driver di decompressione
- driver di codec
- driver del convertitore di formato
- filtrare i driver
- driver compressore
- driver di decompressione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b861d381dfc28307c090dbb71b93db8e58e90a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330599"
---
# <a name="how-the-audio-compression-manager-works"></a><span data-ttu-id="12a71-122">Funzionamento di Gestione compressione audio</span><span class="sxs-lookup"><span data-stu-id="12a71-122">How the Audio Compression Manager Works</span></span>

<span data-ttu-id="12a71-123">L'ACM utilizza gli hook di interfaccia del driver esistenti per eseguire l'override dell'algoritmo di mapping predefinito per i dispositivi audio waveform.</span><span class="sxs-lookup"><span data-stu-id="12a71-123">The ACM uses existing driver interface hooks to override the default mapping algorithm for waveform-audio devices.</span></span> <span data-ttu-id="12a71-124">In questo modo, l'ACM può intercettare le chiamate a dispositivi aperti.</span><span class="sxs-lookup"><span data-stu-id="12a71-124">This allows the ACM to intercept device-open calls.</span></span> <span data-ttu-id="12a71-125">Dopo l'intercettazione di una chiamata, l'ACM può eseguire una serie di attività per elaborare i dati audio, ad esempio l'inserimento di un compressore esterno o un decompressore nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="12a71-125">After a call has been intercepted, the ACM can perform a variety of tasks to process the audio data, such as inserting an external compressor or decompressor into the sequence.</span></span>

<span data-ttu-id="12a71-126">L'ACM gestisce i tipi di driver seguenti:</span><span class="sxs-lookup"><span data-stu-id="12a71-126">The ACM manages the following types of drivers:</span></span>

-   <span data-ttu-id="12a71-127">Driver Compressor e decompressore (codec)</span><span class="sxs-lookup"><span data-stu-id="12a71-127">Compressor and decompressor (codec) drivers</span></span>
-   <span data-ttu-id="12a71-128">Driver del convertitore di formato</span><span class="sxs-lookup"><span data-stu-id="12a71-128">Format converter drivers</span></span>
-   <span data-ttu-id="12a71-129">Filtrare i driver</span><span class="sxs-lookup"><span data-stu-id="12a71-129">Filter drivers</span></span>

<span data-ttu-id="12a71-130">I commutatori e i decompressori cambiano un tipo di formato in un altro.</span><span class="sxs-lookup"><span data-stu-id="12a71-130">Compressors and decompressors change one format type to another.</span></span> <span data-ttu-id="12a71-131">Ad esempio, un commutatore o un decompressore può modificare un file PCM (Pulse Code Modulation) in un file ADPCM (modulazione del codice Pulse differenziale).</span><span class="sxs-lookup"><span data-stu-id="12a71-131">For example, a compressor or decompressor can change a PCM (Pulse Code Modulation) file to an ADPCM (Adaptive Differential Pulse Code Modulation) file.</span></span> <span data-ttu-id="12a71-132">I convertitori di formato cambiano il formato, ma non il tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="12a71-132">Format converters change the format, but not the data type.</span></span> <span data-ttu-id="12a71-133">Un convertitore può, ad esempio, modificare i dati 44-kHz, a 16 bit a 44-kHz, a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="12a71-133">For example, a converter can change 44-kHz, 16-bit data to 44-kHz, 8-bit data.</span></span> <span data-ttu-id="12a71-134">I filtri non modificano affatto il formato dati, ma cambiano in qualche modo i dati dell'audio della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="12a71-134">Filters do not change the data format at all, but they change the waveform-audio data in some manner.</span></span> <span data-ttu-id="12a71-135">Un filtro può ad esempio combinare un flusso di dati e un echo di se stesso.</span><span class="sxs-lookup"><span data-stu-id="12a71-135">For example, a filter could combine a data stream and an echo of itself.</span></span> <span data-ttu-id="12a71-136">Un driver ACM singolo, o un tag di filtro o di formato all'interno di un driver, potrebbe supportare anche combinazioni dei tipi precedenti.</span><span class="sxs-lookup"><span data-stu-id="12a71-136">A single ACM driver, or a filter tag or format tag within a driver, might also support combinations of the preceding types.</span></span>

<span data-ttu-id="12a71-137">Per l'output dell'audio della forma d'onda, l'ACM passa ogni buffer di dati al convertitore mentre arriva.</span><span class="sxs-lookup"><span data-stu-id="12a71-137">For waveform-audio output, the ACM passes each buffer of data to the converter as it arrives.</span></span> <span data-ttu-id="12a71-138">Il convertitore decomprime i dati e restituisce i dati decompressi in ACM in un buffer "Shadow".</span><span class="sxs-lookup"><span data-stu-id="12a71-138">The converter decompresses the data and returns the decompressed data to the ACM in a "shadow" buffer.</span></span> <span data-ttu-id="12a71-139">Il modulo ACM passa quindi il buffer di ombreggiatura decompresso al driver audio della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="12a71-139">The ACM then passes the decompressed shadow buffer to the waveform-audio driver.</span></span> <span data-ttu-id="12a71-140">L'ACM alloca i buffer Shadow ogni volta che viene ricevuto un messaggio di preparazione.</span><span class="sxs-lookup"><span data-stu-id="12a71-140">The ACM allocates the shadow buffers whenever it receives a prepare message.</span></span>

<span data-ttu-id="12a71-141">Per l'input audio della forma d'onda, l'ACM passa i buffer di ombreggiatura vuoti al driver.</span><span class="sxs-lookup"><span data-stu-id="12a71-141">For waveform-audio input, the ACM passes empty shadow buffers to the driver.</span></span> <span data-ttu-id="12a71-142">Usa un'attività in background per ricevere una notifica dopo che il driver ha riempito il buffer di ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="12a71-142">It uses a background task to receive a notification after the driver has filled the shadow buffer.</span></span> <span data-ttu-id="12a71-143">L'ACM passa quindi i buffer al driver per la compressione.</span><span class="sxs-lookup"><span data-stu-id="12a71-143">The ACM then passes the buffers to the driver for compression.</span></span> <span data-ttu-id="12a71-144">Al termine della compressione, il driver passa i dati all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="12a71-144">After compression is finished, the driver passes the data to the application.</span></span>

 

 




