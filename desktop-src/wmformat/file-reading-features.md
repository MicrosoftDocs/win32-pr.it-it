---
title: Funzionalità di lettura file
description: Funzionalità di lettura file
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- Windows Media Format SDK, funzionalità di lettura file
- Windows Media Format SDK, lettura asincrona dei file
- Windows Media Format SDK, lettura di file sincroni
- ASF (Advanced Systems Format), funzionalità di lettura dei file
- ASF (Advanced Systems Format), funzionalità di lettura dei file
- ASF (Advanced Systems Format), lettura asincrona dei file
- ASF (formato avanzato dei sistemi), lettura asincrona dei file
- ASF (Advanced Systems Format), lettura di file sincroni
- ASF (formato avanzato dei sistemi), lettura sincrona dei file
- lettura asincrona di file
- lettura di file sincroni
- lettori sincroni, funzionalità di lettura file
- lettura file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83d3ce112d0d9e47626b4f7850f760da5c6583e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332319"
---
# <a name="file-reading-features"></a><span data-ttu-id="cb50d-116">Funzionalità di lettura file</span><span class="sxs-lookup"><span data-stu-id="cb50d-116">File Reading Features</span></span>

<span data-ttu-id="cb50d-117">La lettura dei file ASF è una delle funzionalità principali di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="cb50d-117">Reading ASF files is one of the primary features of the Windows Media Format SDK.</span></span> <span data-ttu-id="cb50d-118">Sono supportati due tipi di lettura: asincrono e sincrono.</span><span class="sxs-lookup"><span data-stu-id="cb50d-118">Two types of reading are supported: asynchronous and synchronous.</span></span> <span data-ttu-id="cb50d-119">La lettura asincrona dei file viene gestita dall'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="cb50d-119">Asynchronous file reading is handled by the reader object.</span></span> <span data-ttu-id="cb50d-120">L'oggetto Reader sincrono viene utilizzato per leggere i file in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="cb50d-120">The synchronous reader object is used to read files synchronously.</span></span> <span data-ttu-id="cb50d-121">Per ulteriori informazioni sui diversi oggetti di lettura, vedere [oggetto Reader](reader-object.md) e [oggetto Reader sincrono](synchronous-reader-object.md).</span><span class="sxs-lookup"><span data-stu-id="cb50d-121">For more information about the different reading objects, see [Reader Object](reader-object.md) and [Synchronous Reader Object](synchronous-reader-object.md).</span></span>

<span data-ttu-id="cb50d-122">Nello scenario di lettura del file asincrono più semplice, è necessario implementare un metodo di callback che l'oggetto Reader chiamerà quando gli esempi sono pronti.</span><span class="sxs-lookup"><span data-stu-id="cb50d-122">In the most basic asynchronous file reading scenario, you must implement a callback method that the reader object will call when samples are ready.</span></span> <span data-ttu-id="cb50d-123">Una volta iniziata la lettura di un file, l'applicazione attende che gli esempi vengano recapitati al metodo di callback.</span><span class="sxs-lookup"><span data-stu-id="cb50d-123">After you begin reading a file, your application waits for the samples to be delivered to your callback method.</span></span> <span data-ttu-id="cb50d-124">La lettura asincrona è utile per le applicazioni del lettore e supporta le funzionalità non disponibili con la lettura sincrona.</span><span class="sxs-lookup"><span data-stu-id="cb50d-124">Asynchronous reading is useful for player applications, and supports features not available with synchronous reading.</span></span> <span data-ttu-id="cb50d-125">Se l'applicazione deve leggere i file da un percorso di rete o interagire con un server che esegue Servizi Windows Media, è necessario usare l'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="cb50d-125">If your application needs to read files from a network location, or interact with a server running Windows Media Services, you must use the reader object.</span></span> <span data-ttu-id="cb50d-126">Lo svantaggio dell'oggetto Reader è che per ogni output fornito viene utilizzato un thread separato.</span><span class="sxs-lookup"><span data-stu-id="cb50d-126">The disadvantage of the reader object is that a separate thread is used for each output delivered.</span></span> <span data-ttu-id="cb50d-127">Inoltre, l'oggetto Reader non è flessibile come il lettore sincrono in come può fornire esempi.</span><span class="sxs-lookup"><span data-stu-id="cb50d-127">Additionally, the reader object is not as flexible as the synchronous reader in how it can deliver samples.</span></span>

<span data-ttu-id="cb50d-128">Con il lettore sincrono non è necessario utilizzare alcun metodo di callback.</span><span class="sxs-lookup"><span data-stu-id="cb50d-128">With the synchronous reader you do not need to use any callback methods.</span></span> <span data-ttu-id="cb50d-129">Al contrario, è possibile selezionare una parte del file per leggere e recuperare gli esempi uno alla volta con le chiamate al metodo.</span><span class="sxs-lookup"><span data-stu-id="cb50d-129">Instead, you select a portion of the file to read and retrieve the samples one at a time with method calls.</span></span> <span data-ttu-id="cb50d-130">Il lettore sincrono è particolarmente adatto alle esigenze delle applicazioni di modifica del contenuto, in cui l'accesso rapido a specifici esempi è essenziale.</span><span class="sxs-lookup"><span data-stu-id="cb50d-130">The synchronous reader is well suited to the needs of content-editing applications, where quick access to specific samples is essential.</span></span> <span data-ttu-id="cb50d-131">Poiché nessun metodo di callback viene utilizzato dal lettore sincrono, è possibile creare applicazioni per leggere i file ASF con un sovraccarico di codifica minimo.</span><span class="sxs-lookup"><span data-stu-id="cb50d-131">Because no callback methods are used by the synchronous reader, you can create applications to read ASF files with a minimum of coding overhead.</span></span> <span data-ttu-id="cb50d-132">Tuttavia, il lettore sincrono non è in grado di aprire un file da un percorso di rete o interagire con un server che esegue Servizi Windows Media oppure leggere file protetti con [*DRM*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="cb50d-132">However, the synchronous reader cannot open a file from a network location, or interact with a server running Windows Media Services, or read files protected with [*DRM*](wmformat-glossary.md).</span></span>

<span data-ttu-id="cb50d-133">Negli argomenti seguenti vengono illustrate le funzionalità del lettore e del lettore sincrono.</span><span class="sxs-lookup"><span data-stu-id="cb50d-133">The following topics discuss the features of the reader and the synchronous reader.</span></span>



| <span data-ttu-id="cb50d-134">Argomento</span><span class="sxs-lookup"><span data-stu-id="cb50d-134">Topic</span></span>                                                              | <span data-ttu-id="cb50d-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb50d-135">Description</span></span>                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb50d-136">Supporto di esempio allocato dall'utente</span><span class="sxs-lookup"><span data-stu-id="cb50d-136">User Allocated Sample Support</span></span>](user-allocated-sample-support.md) | <span data-ttu-id="cb50d-137">Viene descritta l'allocazione del buffer nel Reader e nel lettore sincrono e il modo in cui l'allocazione utente può migliorare le prestazioni</span><span class="sxs-lookup"><span data-stu-id="cb50d-137">Discusses buffer allocation in the reader and synchronous reader, and how user allocation can improve performance.</span></span> |
| [<span data-ttu-id="cb50d-138">Enumerazione del formato di output</span><span class="sxs-lookup"><span data-stu-id="cb50d-138">Output Format Enumeration</span></span>](output-format-enumeration.md)         | <span data-ttu-id="cb50d-139">Descrive l'enumerazione del formato di output.</span><span class="sxs-lookup"><span data-stu-id="cb50d-139">Discusses output format enumeration.</span></span>                                                                               |



 

<span data-ttu-id="cb50d-140">Inoltre, gli argomenti seguenti della sezione relativa alla scrittura di funzionalità si applicano anche alla lettura di file:</span><span class="sxs-lookup"><span data-stu-id="cb50d-140">In addition, the following topics from the writing features section also apply to file reading:</span></span>

-   [<span data-ttu-id="cb50d-141">Ridimensionamento video</span><span class="sxs-lookup"><span data-stu-id="cb50d-141">Video Resizing</span></span>](video-resizing.md)
-   [<span data-ttu-id="cb50d-142">Conversione dello spazio colore</span><span class="sxs-lookup"><span data-stu-id="cb50d-142">Color Space Conversion</span></span>](color-space-conversion.md)
-   [<span data-ttu-id="cb50d-143">Ricampionamento audio</span><span class="sxs-lookup"><span data-stu-id="cb50d-143">Audio Resampling</span></span>](audio-resampling.md)

## <a name="related-topics"></a><span data-ttu-id="cb50d-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cb50d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb50d-145">**Funzionalità**</span><span class="sxs-lookup"><span data-stu-id="cb50d-145">**Features**</span></span>](features.md)
</dt> <dt>

[<span data-ttu-id="cb50d-146">**Lettura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="cb50d-146">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




