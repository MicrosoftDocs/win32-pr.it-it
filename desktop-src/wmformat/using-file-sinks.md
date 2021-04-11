---
title: Uso di file sink
description: Uso di file sink
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- ASF (Advanced Systems Format), sink di file
- ASF (formato avanzato dei sistemi), sink di file
- ASF (Advanced Systems Format), sink
- ASF (formato avanzato dei sistemi), sink
- sink, sink di file
- sink di file, informazioni
- sink di file, creazione
- sink di file, arresto
- sink di file, avvio
- sink di file, chiusura
- sink, statistiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7a7f09a08788128719ea80a2a06d339f6398e6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104117454"
---
# <a name="using-file-sinks"></a><span data-ttu-id="cce0a-114">Uso di file sink</span><span class="sxs-lookup"><span data-stu-id="cce0a-114">Using File Sinks</span></span>

<span data-ttu-id="cce0a-115">In circostanze normali, è possibile passare semplicemente il writer a un nome di file di output usando il metodo [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) e l'oggetto writer scriverà il file su disco automaticamente.</span><span class="sxs-lookup"><span data-stu-id="cce0a-115">Under normal circumstances, you can simply pass the writer an output file name using the [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) method, and the writer object will write the file to disk automatically.</span></span> <span data-ttu-id="cce0a-116">In questo caso, il writer sta effettivamente creando e controllando un oggetto sink di file del writer che gestisce la scrittura del file su disco.</span><span class="sxs-lookup"><span data-stu-id="cce0a-116">In this case, the writer is actually creating and controlling a writer file sink object that handles writing the file to disk.</span></span> <span data-ttu-id="cce0a-117">Un oggetto sink di file writer controlla il flusso di dati dall'oggetto writer a un singolo file.</span><span class="sxs-lookup"><span data-stu-id="cce0a-117">A writer file sink object controls the flow of data from the writer object to a single file.</span></span>

<span data-ttu-id="cce0a-118">È possibile creare sink di file personalizzati per ottenere un maggiore controllo sulla modalità di scrittura del file da parte del sink.</span><span class="sxs-lookup"><span data-stu-id="cce0a-118">You can create your own file sinks to get more control over how the sink writes the file.</span></span> <span data-ttu-id="cce0a-119">È anche possibile accedere al sink di file del writer predefinito creato dal writer in risposta a una chiamata a **SetOutputFilename**.</span><span class="sxs-lookup"><span data-stu-id="cce0a-119">You can also access the default writer file sink created by the writer in response to a call to **SetOutputFilename**.</span></span>

## <a name="creating-file-sinks"></a><span data-ttu-id="cce0a-120">Creazione di sink di file</span><span class="sxs-lookup"><span data-stu-id="cce0a-120">Creating File Sinks</span></span>

<span data-ttu-id="cce0a-121">Per creare un sink di file e aggiungerlo al writer, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="cce0a-121">To create a file sink and add it to the writer, perform the following steps.</span></span>

1.  <span data-ttu-id="cce0a-122">Creare un nuovo sink chiamando la funzione [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) .</span><span class="sxs-lookup"><span data-stu-id="cce0a-122">Create a new sink by calling the [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) function.</span></span>
2.  <span data-ttu-id="cce0a-123">Specificare un nome file per il sink chiamando [**IWMWriterFileSink:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).</span><span class="sxs-lookup"><span data-stu-id="cce0a-123">Supply a file name for the sink by calling [**IWMWriterFileSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).</span></span>
3.  <span data-ttu-id="cce0a-124">Aggiungere il sink di file al writer chiamando [**IWMWriterAdvanced:: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).</span><span class="sxs-lookup"><span data-stu-id="cce0a-124">Add the file sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).</span></span>
4.  <span data-ttu-id="cce0a-125">Eseguire la scrittura nel modo consueto.</span><span class="sxs-lookup"><span data-stu-id="cce0a-125">Perform writing in the usual way.</span></span>
5.  <span data-ttu-id="cce0a-126">Al termine della scrittura, il sink chiuderà automaticamente il file.</span><span class="sxs-lookup"><span data-stu-id="cce0a-126">After writing is completed, the sink will close the file automatically.</span></span>

## <a name="stopping-and-starting-file-sinks"></a><span data-ttu-id="cce0a-127">Arresto e avvio di sink di file</span><span class="sxs-lookup"><span data-stu-id="cce0a-127">Stopping and Starting File Sinks</span></span>

<span data-ttu-id="cce0a-128">Dopo l'inizio delle operazioni di scrittura, è possibile arrestare la scrittura in un sink di file chiamando [**IWMWriterFileSink2:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).</span><span class="sxs-lookup"><span data-stu-id="cce0a-128">After writing operations begin, you can stop writing to a file sink by calling [**IWMWriterFileSink2::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).</span></span>

<span data-ttu-id="cce0a-129">Esistono molti possibili motivi per cui si vuole interrompere la scrittura in un sink.</span><span class="sxs-lookup"><span data-stu-id="cce0a-129">There are many potential reasons why you would want to stop writing to a sink.</span></span> <span data-ttu-id="cce0a-130">Ad esempio, se si esegue la registrazione da un'origine live, è possibile che si sia interessati solo ad alcuni contenuti.</span><span class="sxs-lookup"><span data-stu-id="cce0a-130">For example, if you are recording from a live source, you may only be interested in some of the content.</span></span>

<span data-ttu-id="cce0a-131">È possibile riprendere la scrittura in un sink di file chiamando [**IWMWriterFileSink2:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start).</span><span class="sxs-lookup"><span data-stu-id="cce0a-131">You can resume writing to a file sink by calling [**IWMWriterFileSink2::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start).</span></span> <span data-ttu-id="cce0a-132">Sia l' **arresto** che l' **avvio** usano i tempi di presentazione per controllare approssimativamente quando viene eseguito il comando.</span><span class="sxs-lookup"><span data-stu-id="cce0a-132">Both **Stop** and **Start** use presentation times to control approximately when the command is executed.</span></span> <span data-ttu-id="cce0a-133">È possibile utilizzare i metodi [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) per ottenere un maggiore controllo sulle ore di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="cce0a-133">You can use the [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) methods to gain more control over start and stop times.</span></span>

## <a name="closing-file-sinks"></a><span data-ttu-id="cce0a-134">Chiusura di sink di file</span><span class="sxs-lookup"><span data-stu-id="cce0a-134">Closing File Sinks</span></span>

<span data-ttu-id="cce0a-135">In genere, un sink di file viene chiuso automaticamente.</span><span class="sxs-lookup"><span data-stu-id="cce0a-135">Normally, a file sink is closed automatically.</span></span> <span data-ttu-id="cce0a-136">Se la scrittura in un sink è stata completata, ma la scrittura di operazioni in altri sink continua, è necessario chiudere in modo esplicito il sink per conservare le risorse.</span><span class="sxs-lookup"><span data-stu-id="cce0a-136">If you are finished writing to a sink, but writing operations to other sinks are continuing, you should explicitly close the sink to conserve resources.</span></span> <span data-ttu-id="cce0a-137">Per chiudere un sink di file, chiamare [**IWMWriterFileSink2:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).</span><span class="sxs-lookup"><span data-stu-id="cce0a-137">To close a file sink, call [**IWMWriterFileSink2::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).</span></span>

## <a name="getting-sink-statistics"></a><span data-ttu-id="cce0a-138">Recupero delle statistiche del sink</span><span class="sxs-lookup"><span data-stu-id="cce0a-138">Getting Sink Statistics</span></span>

<span data-ttu-id="cce0a-139">È possibile ottenere le dimensioni e la durata del file per un sink aperto chiamando [**IWMWriterFileSink2:: Filesize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) e [**IWMWriterFileSink2:: GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="cce0a-139">You can get the file size and duration for an open sink by calling [**IWMWriterFileSink2::GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) and [**IWMWriterFileSink2::GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) respectively.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cce0a-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cce0a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cce0a-141">**Interfaccia IWMWriterFileSink**</span><span class="sxs-lookup"><span data-stu-id="cce0a-141">**IWMWriterFileSink Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[<span data-ttu-id="cce0a-142">**Interfaccia IWMWriterFileSink2**</span><span class="sxs-lookup"><span data-stu-id="cce0a-142">**IWMWriterFileSink2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[<span data-ttu-id="cce0a-143">**Interfaccia IWMWriterFileSink3**</span><span class="sxs-lookup"><span data-stu-id="cce0a-143">**IWMWriterFileSink3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[<span data-ttu-id="cce0a-144">**Oggetto file sink del writer**</span><span class="sxs-lookup"><span data-stu-id="cce0a-144">**Writer File Sink Object**</span></span>](writer-file-sink-object.md)
</dt> <dt>

[<span data-ttu-id="cce0a-145">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="cce0a-145">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




