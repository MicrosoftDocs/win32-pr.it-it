---
title: Esclusione reciproca
description: Esclusione reciproca
ms.assetid: 3a3f6763-a241-4bbd-a6e8-62041b05622d
keywords:
- Windows Media Format SDK, esclusione reciproca
- Formato di sistemi avanzati (ASF), esclusione reciproca
- ASF (formato avanzato dei sistemi), esclusione reciproca
- Windows Media Format SDK, l'esclusione reciproca MBR
- ASF (Advanced Systems Format), esclusione reciproca MBR
- ASF (formato avanzato dei sistemi), esclusione reciproca MBR
- Windows Media Format SDK, frequenza a più bit (MBR)
- ASF (Advanced Systems Format), velocità in bit multipla (MBR)
- ASF (formato avanzato dei sistemi), velocità in bit multipla (MBR)
- esclusione reciproca, informazioni
- velocità in bit multipla (MBR), esclusione reciproca
- MBR (frequenza a più bit), esclusione reciproca
- esclusione reciproca, velocità in bit
- esclusione reciproca, lingua
- esclusione reciproca, presentazione
- esclusione reciproca, sconosciuta
- esclusione reciproca, funzionalità
- esclusione reciproca, funzionalità avanzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd00bf5bcb544d2541a6bc5465171fe9bacc1b9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856889"
---
# <a name="mutual-exclusion"></a><span data-ttu-id="3f0b6-121">Esclusione reciproca</span><span class="sxs-lookup"><span data-stu-id="3f0b6-121">Mutual Exclusion</span></span>

<span data-ttu-id="3f0b6-122">Ogni file ASF contiene uno o più flussi, ognuno dei quali contiene dati multimediali digitali.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-122">Every ASF file contains one or more streams, each containing digital media data.</span></span> <span data-ttu-id="3f0b6-123">In circostanze normali, ogni flusso è associato a un singolo output.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-123">Under normal circumstances, each stream is associated with a single output.</span></span> <span data-ttu-id="3f0b6-124">Durante la riproduzione, l'oggetto Reader recapita esempi per ogni output.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-124">On playback, the reader object delivers samples for each output.</span></span> <span data-ttu-id="3f0b6-125">Pertanto, per impostazione predefinita, ogni flusso in un file ASF viene recapitato dal lettore durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-125">So, as a default, every stream in an ASF file is delivered by the reader on playback.</span></span>

<span data-ttu-id="3f0b6-126">Esistono situazioni in cui non si desidera che ogni flusso venga recapitato al client.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-126">There are situations where you do not want every stream delivered to the client.</span></span> <span data-ttu-id="3f0b6-127">Se, ad esempio, si crea un file video con cinque flussi audio, uno per ogni cinque lingue, è necessario recapitarne solo uno alla volta.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-127">For example, if you create a video file with five audio streams, one for each of five languages, you want only one of them to be delivered at a time.</span></span> <span data-ttu-id="3f0b6-128">L'esclusione reciproca è una funzionalità di Windows Media Format SDK che consente di specificare un numero di flussi che si escludono a vicenda che equivalgono allo stesso output.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-128">Mutual exclusion is a feature of the Windows Media Format SDK that enables you to specify a number of mutually exclusive streams that all equate to the same output.</span></span>

<span data-ttu-id="3f0b6-129">L'esclusione reciproca viene definita nel profilo utilizzato per creare un file.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-129">Mutual exclusion is defined in the profile used to create a file.</span></span> <span data-ttu-id="3f0b6-130">È possibile configurare l'esclusione reciproca in un profilo utilizzando oggetti di esclusione reciproca.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-130">You configure mutual exclusion in a profile by using mutual exclusion objects.</span></span> <span data-ttu-id="3f0b6-131">Si aggiungono i flussi uno alla volta all'oggetto di esclusione reciproca, si imposta il tipo e si include l'oggetto nel profilo.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-131">You add streams one at a time to the mutual exclusion object, set the type, and include the object in the profile.</span></span>

<span data-ttu-id="3f0b6-132">Windows Media Format SDK riconosce quattro tipi di esclusione reciproca:</span><span class="sxs-lookup"><span data-stu-id="3f0b6-132">The Windows Media Format SDK recognizes four types of mutual exclusion:</span></span>

-   <span data-ttu-id="3f0b6-133">Velocità in bit</span><span class="sxs-lookup"><span data-stu-id="3f0b6-133">Bit rate</span></span>
-   <span data-ttu-id="3f0b6-134">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="3f0b6-134">Language</span></span>
-   <span data-ttu-id="3f0b6-135">Presentazione</span><span class="sxs-lookup"><span data-stu-id="3f0b6-135">Presentation</span></span>
-   <span data-ttu-id="3f0b6-136">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="3f0b6-136">Unknown</span></span>

## <a name="mutual-exclusion-by-bit-rate"></a><span data-ttu-id="3f0b6-137">Esclusione reciproca per velocità in bit</span><span class="sxs-lookup"><span data-stu-id="3f0b6-137">Mutual Exclusion by Bit Rate</span></span>

<span data-ttu-id="3f0b6-138">L'esclusione reciproca della velocità in bit è un tipo speciale di esclusione reciproca ed è più comunemente indicata come esclusione reciproca a più bit (MBR).</span><span class="sxs-lookup"><span data-stu-id="3f0b6-138">Bit rate mutual exclusion is a special type of mutual exclusion and is more commonly referred to as multiple bit rate (MBR) mutual exclusion.</span></span> <span data-ttu-id="3f0b6-139">Un'esclusione reciproca MBR contiene un numero di flussi che provengono tutti dallo stesso input, ma sono codificati a velocità in bit diverse.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-139">An MBR mutual exclusion contains a number of streams that all originate from the same input, but are encoded at different bit rates.</span></span> <span data-ttu-id="3f0b6-140">Quando si riproduce un file con MBR, il lettore determina il flusso migliore da usare in base alla larghezza di banda disponibile.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-140">When playing a file with MBR, the reader determines the best stream to use based on the available bandwidth.</span></span>

<span data-ttu-id="3f0b6-141">Windows Media Format SDK supporta MBR per flussi audio e video.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-141">The Windows Media Format SDK supports MBR for audio and video streams.</span></span> <span data-ttu-id="3f0b6-142">L'SDK supporta anche un tipo speciale di video MBR denominato più dimensioni video MBR.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-142">The SDK also supports a special type of MBR video called multiple video size MBR.</span></span> <span data-ttu-id="3f0b6-143">Questo è analogo al normale video MBR, tranne per il fatto che i singoli flussi possono avere dimensioni di frame differenti.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-143">This is like normal MBR video except that the individual streams can have different frame sizes.</span></span> <span data-ttu-id="3f0b6-144">Ad esempio, è possibile che siano presenti alcuni flussi alla dimensione del video predefinita 320 x 240 e altre con velocità in bit superiori e 640 x 480 di dimensioni del video.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-144">For example, you might have some streams at the default 320 x 240 video size and some others with higher bit rates and 640 x 480 video size.</span></span>

## <a name="mutual-exclusion-by-language"></a><span data-ttu-id="3f0b6-145">Esclusione reciproca per lingua</span><span class="sxs-lookup"><span data-stu-id="3f0b6-145">Mutual Exclusion by Language</span></span>

<span data-ttu-id="3f0b6-146">L'esclusione reciproca basata sulla lingua è progettata per essere usata con contenuto (in genere audio) registrato in più lingue.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-146">Language-based mutual exclusion is designed for use with content (usually audio) recorded in several languages.</span></span> <span data-ttu-id="3f0b6-147">Un'esclusione reciproca basata sul linguaggio include diversi flussi originati da input univoci.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-147">A language-based mutual exclusion includes several streams that originate from unique inputs.</span></span> <span data-ttu-id="3f0b6-148">Ogni input è lo stesso contenuto, ma in una lingua diversa.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-148">Each input is the same content, but in a different language.</span></span>

<span data-ttu-id="3f0b6-149">Per l'esclusione reciproca in base al linguaggio, l'applicazione di lettura deve includere la logica per selezionare la lingua appropriata.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-149">For mutual exclusion by language to work, the reading application must include logic to select the appropriate language.</span></span> <span data-ttu-id="3f0b6-150">Se si scrive un'applicazione per riprodurre file ASF e si desidera supportare i file con esclusione reciproca basata sulla lingua, è necessario selezionare il flusso appropriato prima di iniziare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-150">If you write an application to play ASF files, and you want to support files with language-based mutual exclusion, you should select the appropriate stream before beginning playback.</span></span>

## <a name="mutual-exclusion-by-presentation"></a><span data-ttu-id="3f0b6-151">Esclusione reciproca per presentazione</span><span class="sxs-lookup"><span data-stu-id="3f0b6-151">Mutual Exclusion by Presentation</span></span>

<span data-ttu-id="3f0b6-152">Viene fornita l'esclusione reciproca basata sulla presentazione per supportare flussi video contenenti lo stesso contenuto codificato con proporzioni diverse.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-152">Presentation-based mutual exclusion is provided to support video streams that contain the same content encoded with different aspect ratios.</span></span> <span data-ttu-id="3f0b6-153">Viene in genere usato quando si fornisce video in una versione letterbox (proporzioni 16:9) e formattato per le schermate televisive (proporzioni 4:3).</span><span class="sxs-lookup"><span data-stu-id="3f0b6-153">Typically, this is used when providing video in a letterbox version (aspect ratio 16:9) as well as formatted for television screens (aspect ratio 4:3).</span></span>

<span data-ttu-id="3f0b6-154">La selezione di una presentazione per la riproduzione è spesso determinata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-154">The selection of a presentation for playback is most often determined by the user.</span></span> <span data-ttu-id="3f0b6-155">Se si scrive un'applicazione per riprodurre file ASF e si desidera supportare i file con esclusione reciproca basata sulla presentazione, è necessario presentare all'utente la possibilità di selezionare un tipo di presentazione per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-155">If you write an application to play ASF files and want to support files with presentation based mutual exclusion, you should present the user with the option of selecting a presentation type for viewing.</span></span>

## <a name="unknown-mutual-exclusion"></a><span data-ttu-id="3f0b6-156">Esclusione reciproca sconosciuta</span><span class="sxs-lookup"><span data-stu-id="3f0b6-156">Unknown Mutual Exclusion</span></span>

<span data-ttu-id="3f0b6-157">Puoi creare un'esclusione reciproca in base ai criteri che preferisci.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-157">You can create mutual exclusion based on any criteria you like.</span></span> <span data-ttu-id="3f0b6-158">Tutti i tipi di esclusione reciproca personalizzata devono essere creati usando il tipo sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-158">All custom mutual exclusion types should be created using the unknown type.</span></span>

## <a name="advanced-mutual-exclusion-features"></a><span data-ttu-id="3f0b6-159">Funzionalità avanzate di esclusione reciproca</span><span class="sxs-lookup"><span data-stu-id="3f0b6-159">Advanced Mutual Exclusion Features</span></span>

<span data-ttu-id="3f0b6-160">È anche possibile usare l'esclusione reciproca per assegnare flussi a gruppi che si escludono reciprocamente tra loro.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-160">You can also use mutual exclusion to assign streams to groups that are mutually exclusive of one another.</span></span> <span data-ttu-id="3f0b6-161">Ad esempio, potrebbe essere necessario disporre di flussi audio in più lingue e assegnare un flusso video diverso a ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-161">For example, you might want to have audio streams in multiple languages and assign a different video stream to each.</span></span> <span data-ttu-id="3f0b6-162">Si usa l'esclusione reciproca per raggruppare ogni flusso audio con il flusso video corrispondente e rendere tutti i gruppi che si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-162">You use mutual exclusion to group each audio stream with its corresponding video stream and make all groups mutually exclusive.</span></span>

<span data-ttu-id="3f0b6-163">Il Reader seleziona automaticamente i flussi per tutte le esclusioni reciproche.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-163">The reader automatically selects streams for all mutual exclusions.</span></span> <span data-ttu-id="3f0b6-164">Per tutti i tipi di esclusione reciproca tranne MBR ed esclusione reciproca basata sulla lingua, il Reader seleziona sempre il flusso predefinito, ovvero il primo flusso aggiunto all'oggetto di esclusione reciproca nel profilo.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-164">For all types of mutual exclusion except MBR and language-based mutual exclusion, the reader always selects the default stream, which is the first stream added to the mutual exclusion object in the profile.</span></span> <span data-ttu-id="3f0b6-165">Per MBR, il lettore seleziona il flusso che meglio si adatta alla larghezza di banda disponibile al momento della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-165">For MBR, the reader selects the stream that best suits the available bandwidth at the time of playback.</span></span> <span data-ttu-id="3f0b6-166">Se non si vuole usare il flusso predefinito, è possibile impostare la selezione del flusso su manuale prima di iniziare la lettura di un file.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-166">If you do not want to use the default stream, you can set stream selection to manual before starting to read a file.</span></span>

<span data-ttu-id="3f0b6-167">La selezione del flusso manuale si applica all'intero file.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-167">Manual stream selection applies to the entire file.</span></span> <span data-ttu-id="3f0b6-168">Le difficoltà possono verificarsi quando si hanno esclusioni reciproche di tipi diversi nello stesso file.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-168">Difficulties can arise when you have mutual exclusions of different types in the same file.</span></span> <span data-ttu-id="3f0b6-169">Un file può includere, ad esempio, l'esclusione reciproca basata sulla velocità in bit e l'esclusione reciproca personalizzata.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-169">For example, a file can contain both bit-rate-based mutual exclusion and custom mutual exclusion.</span></span> <span data-ttu-id="3f0b6-170">Per selezionare un flusso diverso da quello predefinito nell'esclusione reciproca personalizzata, è necessario usare la selezione del flusso manuale.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-170">To select a stream other than the default in the custom mutual exclusion, you must use manual stream selection.</span></span> <span data-ttu-id="3f0b6-171">Se si usa la selezione del flusso manuale, tuttavia, il lettore non selezionerà automaticamente il flusso a più velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-171">If you use manual stream selection, however, the reader will not automatically select the multiple bit rate stream.</span></span> <span data-ttu-id="3f0b6-172">È necessario pianificare questa eventualità nell'applicazione se si prevede di supportare più tipi di esclusione reciproca in un singolo file.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-172">You must plan for this eventuality in your application if you plan to support multiple types of mutual exclusion in a single file.</span></span> <span data-ttu-id="3f0b6-173">Ciò significa in genere creare routine di selezione dei flussi personalizzati per i tipi di esclusione reciproca normalmente automatici.</span><span class="sxs-lookup"><span data-stu-id="3f0b6-173">Typically this means creating your own stream selection routines for normally automatic types of mutual exclusion.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f0b6-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f0b6-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f0b6-175">**Funzionalità file ASF**</span><span class="sxs-lookup"><span data-stu-id="3f0b6-175">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="3f0b6-176">**Uso dell'esclusione reciproca**</span><span class="sxs-lookup"><span data-stu-id="3f0b6-176">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> </dl>

 

 




