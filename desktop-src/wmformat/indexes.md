---
title: Indici
description: Indici
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- Windows Media Format SDK, indici
- ASF (Advanced Systems Format), indici
- ASF (formato avanzato dei sistemi), indici
- Windows Media Format SDK, indici temporali
- ASF (Advanced Systems Format), indici temporali
- ASF (formato avanzato dei sistemi), indici temporali
- Windows Media Format SDK, indici basati su frame
- ASF (Advanced Systems Format), indici basati su frame
- ASF (formato avanzato dei sistemi), indici basati su frame
- Windows Media Format SDK, codici temporali SMPTE
- ASF (Advanced Systems Format), codici temporali SMPTE
- ASF (Advanced Systems Format), codici temporali SMPTE
- indici, informazioni
- indici temporali
- indici basati su frame
- Codici temporali SMPTE, indici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2e5a194f9c495720cbc40ccdb192509723eee0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856697"
---
# <a name="indexes"></a><span data-ttu-id="f2762-119">Indici</span><span class="sxs-lookup"><span data-stu-id="f2762-119">Indexes</span></span>

<span data-ttu-id="f2762-120">Un requisito comune per le applicazioni che leggono i file multimediali digitali è la possibilità di ricercare un punto specifico nel contenuto.</span><span class="sxs-lookup"><span data-stu-id="f2762-120">A common requirement for applications that read digital media files is the ability to seek to a specific point in the content.</span></span> <span data-ttu-id="f2762-121">La ricerca può essere difficile perché non vi è alcuna garanzia che i vari flussi in un file includano campioni con orari di avvio simultanei.</span><span class="sxs-lookup"><span data-stu-id="f2762-121">Seeking can be difficult because there is no guarantee that the various streams in a file have samples with concurrent start times.</span></span> <span data-ttu-id="f2762-122">Questo problema viene risolto con l'uso degli *indici*.</span><span class="sxs-lookup"><span data-stu-id="f2762-122">This problem is addressed with the use of *indexes*.</span></span> <span data-ttu-id="f2762-123">Un indice è un oggetto in un file ASF che equivale ai campioni video con le relative ore di presentazione.</span><span class="sxs-lookup"><span data-stu-id="f2762-123">An index is an object in an ASF file that equates video samples with their presentation times.</span></span> <span data-ttu-id="f2762-124">Per i flussi audio non è richiesto alcun indice perché i dati audio sono strettamente connessi all'ora di presentazione rispetto ai dati video.</span><span class="sxs-lookup"><span data-stu-id="f2762-124">No index is required for audio streams because audio data is more closely connected with presentation time than video data is.</span></span>

<span data-ttu-id="f2762-125">L'oggetto indicizzatore di Windows Media Format SDK può creare tre diversi tipi di indici: indici temporali, indici basati su frame e indici di codice in tempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="f2762-125">The indexer object of the Windows Media Format SDK can create three different types of indexes: temporal indexes, frame-based indexes, and SMPTE time code indexes.</span></span>

<span data-ttu-id="f2762-126">Gli indici temporali sono il tipo più comune.</span><span class="sxs-lookup"><span data-stu-id="f2762-126">Temporal indexes are the most common type.</span></span> <span data-ttu-id="f2762-127">Equivalgono semplicemente agli esempi video con i tempi di presentazione corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="f2762-127">They simply equate video samples with the corresponding presentation times.</span></span>

<span data-ttu-id="f2762-128">Un indice basato su frame equivale a esempi video con numeri di fotogrammi video e tempi di presentazione.</span><span class="sxs-lookup"><span data-stu-id="f2762-128">A frame-based index equates video samples with video frame numbers and presentation times.</span></span> <span data-ttu-id="f2762-129">I numeri di frame sono particolarmente utili nelle applicazioni che modificano il video.</span><span class="sxs-lookup"><span data-stu-id="f2762-129">Frame numbers are particularly useful in applications that edit video.</span></span>

<span data-ttu-id="f2762-130">Un indice del codice ora SMTP è il tipo di indice più raro.</span><span class="sxs-lookup"><span data-stu-id="f2762-130">A SMTPE time code index is the rarest type of index.</span></span> <span data-ttu-id="f2762-131">Usa il codice di ora SMPTE come base dell'indice e può essere usato solo in flussi con timestamp SMPTE inclusi negli esempi.</span><span class="sxs-lookup"><span data-stu-id="f2762-131">It uses SMPTE time code as the basis of the index and can be used only on streams that have SMPTE time stamps included with their samples.</span></span> <span data-ttu-id="f2762-132">Per altre informazioni sul codice ora SMPTE, vedere [supporto del codice ora SMPTE](smpte-time-code-support.md).</span><span class="sxs-lookup"><span data-stu-id="f2762-132">For more information about SMPTE time code, see [SMPTE Time Code Support](smpte-time-code-support.md).</span></span>

<span data-ttu-id="f2762-133">Un file ASF può contenere un indice di ogni tipo per ogni flusso video che contiene.</span><span class="sxs-lookup"><span data-stu-id="f2762-133">An ASF file can contain an index of each type for each video stream it contains.</span></span> <span data-ttu-id="f2762-134">Come impostazione predefinita, viene incluso un indice temporale per ogni flusso video nei file creati dall'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="f2762-134">As a default, a temporal index is included for each video stream in files created by the writer object.</span></span> <span data-ttu-id="f2762-135">È possibile modificare le impostazioni di indicizzazione automatica per i file in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="f2762-135">You can change the automatic indexing settings for your files to suit your needs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2762-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f2762-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2762-137">**Funzionalità file ASF**</span><span class="sxs-lookup"><span data-stu-id="f2762-137">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="f2762-138">**Operazioni con gli indici**</span><span class="sxs-lookup"><span data-stu-id="f2762-138">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> <dt>

[<span data-ttu-id="f2762-139">**Lettura di file con il lettore asincrono**</span><span class="sxs-lookup"><span data-stu-id="f2762-139">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="f2762-140">**Lettura di file con il lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="f2762-140">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




