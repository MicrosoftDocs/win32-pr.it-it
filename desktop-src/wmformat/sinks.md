---
title: Sink
description: Sink
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- Windows Media Format SDK, sink
- Windows Media Format SDK, sink di file
- ASF (Advanced Systems Format), sink
- ASF (formato avanzato dei sistemi), sink
- ASF (Advanced Systems Format), sink di file
- ASF (formato avanzato dei sistemi), sink di file
- Windows Media Format SDK, sink di rete
- Windows Media Format SDK, sink di push
- ASF (Advanced Systems Format), sink di rete
- ASF (formato avanzato dei sistemi), sink di rete
- ASF (Advanced Systems Format), sink di push
- ASF (formato avanzato dei sistemi), sink di push
- sink, informazioni
- sink di file, informazioni
- sink di rete
- sink di push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62548f159172f58d4f52b0289c5adbfef02f55
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046332"
---
# <a name="sinks"></a><span data-ttu-id="a0f5e-119">Sink</span><span class="sxs-lookup"><span data-stu-id="a0f5e-119">Sinks</span></span>

<span data-ttu-id="a0f5e-120">L'oggetto writer di Windows Media Format SDK recapita contenuto elaborato a sink.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-120">The writer object of the Windows Media Format SDK delivers processed content to sinks.</span></span> <span data-ttu-id="a0f5e-121">Ogni sink è un oggetto che recapita i dati.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-121">Each sink is an object that delivers data.</span></span> <span data-ttu-id="a0f5e-122">Il punto di distribuzione dipende dal tipo di sink.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-122">The point of delivery depends upon the type of sink.</span></span> <span data-ttu-id="a0f5e-123">Sono disponibili tre tipi di sink: sink di file, sink di rete e sink di push.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-123">There are three types of sinks: file sinks, network sinks, and push sinks.</span></span>

## <a name="file-sinks"></a><span data-ttu-id="a0f5e-124">Sink di file</span><span class="sxs-lookup"><span data-stu-id="a0f5e-124">File Sinks</span></span>

<span data-ttu-id="a0f5e-125">I sink di file scrivono contenuto ASF in un file in un'unità locale o di rete.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-125">File sinks write ASF content to a file on a local or network drive.</span></span> <span data-ttu-id="a0f5e-126">Quando si usa l'oggetto writer per scrivere un file senza aggiungere esplicitamente un sink di file, il writer ne creerà uno usando il nome passato a [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).</span><span class="sxs-lookup"><span data-stu-id="a0f5e-126">When you use the writer object to write a file without explicitly adding a file sink, the writer will create one for you using the name you pass to [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).</span></span> <span data-ttu-id="a0f5e-127">È possibile assegnare più sink di file a un oggetto writer per scrivere il contenuto in più file contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-127">You can assign multiple file sinks to a writer object to write the content in several files at once.</span></span>

<span data-ttu-id="a0f5e-128">Utilizzando un sink di file, è possibile controllare molti aspetti del file.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-128">By using a file sink, you can control many aspects of the file.</span></span> <span data-ttu-id="a0f5e-129">Le funzionalità seguenti sono disponibili tramite un sink di file.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-129">The following features are available through a file sink.</span></span>

-   <span data-ttu-id="a0f5e-130">Monitoraggio delle statistiche di file.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-130">File statistics monitoring.</span></span> <span data-ttu-id="a0f5e-131">È possibile monitorare le dimensioni e la durata del file durante la creazione.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-131">You can monitor the file size and duration as it is being created.</span></span>
-   <span data-ttu-id="a0f5e-132">Creazione di file di contenuto parziale.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-132">Partial content file creation.</span></span> <span data-ttu-id="a0f5e-133">I sink di file possono essere configurati per iniziare a scrivere contenuto in un momento specifico e terminare la scrittura in un momento specifico.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-133">File sinks can be configured to begin writing content at a specific time and to end writing at a specific time.</span></span> <span data-ttu-id="a0f5e-134">In questo modo è possibile creare più file contenenti sezioni diverse dello stesso contenuto nello stesso passaggio di scrittura.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-134">This enables you to create multiple files containing different sections of the same content in the same writing pass.</span></span>

## <a name="network-sinks"></a><span data-ttu-id="a0f5e-135">Sink di rete</span><span class="sxs-lookup"><span data-stu-id="a0f5e-135">Network Sinks</span></span>

<span data-ttu-id="a0f5e-136">I sink di rete trasmettono contenuto a un indirizzo di rete.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-136">Network sinks broadcast content to a network address.</span></span> <span data-ttu-id="a0f5e-137">La lettura dei client può connettersi all'indirizzo per ricevere la trasmissione.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-137">Reading clients can connect to the address to receive the broadcast.</span></span>

## <a name="push-sinks"></a><span data-ttu-id="a0f5e-138">Sink di push</span><span class="sxs-lookup"><span data-stu-id="a0f5e-138">Push Sinks</span></span>

<span data-ttu-id="a0f5e-139">I sink di push recapitano il contenuto dal writer a un server che esegue Servizi Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-139">Push sinks deliver content from the writer to a server running Windows Media Services.</span></span> <span data-ttu-id="a0f5e-140">I sink di push vengono in genere utilizzati negli scenari in cui un computer codifica contenuto Live e lo recapita a uno o più server per la distribuzione estesa.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-140">Push sinks are typically used in scenarios where one computer encodes live content and delivers it to one or more servers for wide distribution.</span></span> <span data-ttu-id="a0f5e-141">L'uso di un sink di push consente di dedicare i computer a attività specifiche, risparmiando la larghezza di banda e la potenza di elaborazione in ogni server.</span><span class="sxs-lookup"><span data-stu-id="a0f5e-141">Using a push sink enables you to dedicate computers to specific tasks, saving bandwidth and processing power on each server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0f5e-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0f5e-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0f5e-143">**Funzionalità di scrittura di file**</span><span class="sxs-lookup"><span data-stu-id="a0f5e-143">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="a0f5e-144">**Utilizzo dei sink di writer**</span><span class="sxs-lookup"><span data-stu-id="a0f5e-144">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




