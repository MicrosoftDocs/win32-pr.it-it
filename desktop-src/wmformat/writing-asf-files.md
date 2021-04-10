---
title: Scrittura di file ASF
description: Scrittura di file ASF
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- Windows Media Format SDK, scrittura di file ASF
- Windows Media Format SDK, creazione di file ASF
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Formato di sistemi avanzati (ASF), scrittura di file
- ASF (Advanced Systems Format), scrittura di file
- ASF (Advanced Systems Format), creazione di file
- ASF (Advanced Systems Format), creazione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c13c1af0d3699c89d26f007e00675ea563639c4e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858006"
---
# <a name="writing-asf-files"></a><span data-ttu-id="6d2a0-110">Scrittura di file ASF</span><span class="sxs-lookup"><span data-stu-id="6d2a0-110">Writing ASF Files</span></span>

<span data-ttu-id="6d2a0-111">È possibile utilizzare l'oggetto writer di Windows Media Format SDK per creare file ASF da dati multimediali digitali.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-111">You can use the writer object of the Windows Media Format SDK to create ASF files from digital media data.</span></span> <span data-ttu-id="6d2a0-112">Per creare un'istanza dell'oggetto writer, chiamare la funzione [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) .</span><span class="sxs-lookup"><span data-stu-id="6d2a0-112">To create an instance of the writer object, call the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function.</span></span> <span data-ttu-id="6d2a0-113">L'oggetto writer coordina la funzionalità di un numero di componenti, inclusi i codec, che sono esterni a Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-113">The writer object coordinates the functionality of a number of components, including codecs, which are external to the Windows Media Format SDK.</span></span>

<span data-ttu-id="6d2a0-114">La funzionalità di base dell'oggetto writer può essere suddivisa nei passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-114">The basic functionality of the writer object can be broken down into the following steps.</span></span> <span data-ttu-id="6d2a0-115">In questa procedura, "l'applicazione" si riferisce al programma scritto utilizzando Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-115">In these steps, "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="6d2a0-116">L'applicazione fornisce al writer un profilo da utilizzare per la creazione del file ASF.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-116">The application supplies the writer with a profile to use in creating the ASF file.</span></span> <span data-ttu-id="6d2a0-117">Quando il writer carica i dati del profilo, assegna un numero di input a ogni connessione del profilo.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-117">When the writer loads the profile data, it assigns an input number to each connection of the profile.</span></span>
2.  <span data-ttu-id="6d2a0-118">L'applicazione fornisce al writer il nome di un file di output per il file da scrivere.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-118">The application supplies the writer with an output file name for the file to be written.</span></span> <span data-ttu-id="6d2a0-119">Il writer crea un oggetto sink di file del writer per gestire la creazione e l'input del file.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-119">The writer creates a writer file sink object to manage the file creation and input.</span></span> <span data-ttu-id="6d2a0-120">Per altre informazioni, vedere [oggetto sink di file writer](writer-file-sink-object.md).</span><span class="sxs-lookup"><span data-stu-id="6d2a0-120">For more information, see [Writer File Sink Object](writer-file-sink-object.md).</span></span>
3.  <span data-ttu-id="6d2a0-121">Il writer crea un'intestazione per il nuovo file in base alle informazioni contenute nel profilo.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-121">The writer creates a header for the new file based on information in the profile.</span></span>
4.  <span data-ttu-id="6d2a0-122">L'applicazione passa campioni non compressi al writer.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-122">The application passes uncompressed samples to the writer.</span></span> <span data-ttu-id="6d2a0-123">Gli esempi vengono passati uno alla volta nei buffer racchiusi tra oggetti buffer.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-123">Samples are passed one at a time in buffers wrapped in buffer objects.</span></span> <span data-ttu-id="6d2a0-124">L'applicazione deve passare esempi per ogni flusso in modo simultaneo, in modo che il writer riceva tutti gli esempi in ordine di tempo di presentazione.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-124">The application should pass samples for each stream concurrently so that the writer receives all samples in presentation-time order.</span></span>
5.  <span data-ttu-id="6d2a0-125">Il writer passa gli esempi al codec appropriato per la compressione.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-125">The writer passes the samples to the appropriate codec for compression.</span></span> <span data-ttu-id="6d2a0-126">Quando il writer riceve gli esempi compressi, li invia con esempi dagli altri flussi, in modo che i campioni vengano inseriti nel file in base all'ordine dei tempi di presentazione indipendentemente dal flusso.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-126">When the writer receives the compressed samples, it interleaves them with samples from the other streams so that samples go into the file in presentation time order irrespective of stream.</span></span> <span data-ttu-id="6d2a0-127">I dati di esempio vengono quindi creati in pacchetti e scritti nella sezione dati del file.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-127">The sample data is then made into packets and written to the data section of the file.</span></span>
6.  <span data-ttu-id="6d2a0-128">Quando vengono elaborati tutti gli esempi, il writer può aggiungere un indice al file per migliorare le prestazioni di ricerca.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-128">When all samples are processed, the writer can add an index to the file to enhance seeking performance.</span></span>

<span data-ttu-id="6d2a0-129">Questi passaggi sono illustrati nell'applicazione di esempio WMStats, tra gli altri.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-129">These steps are illustrated in the WMStats sample application, among others.</span></span> <span data-ttu-id="6d2a0-130">Per altre informazioni, vedere [applicazioni di esempio](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="6d2a0-130">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="6d2a0-131">Il writer supporta inoltre funzionalità più avanzate che consentono di eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6d2a0-131">The writer also supports more advanced functionality, enabling you to do the following:</span></span>

-   <span data-ttu-id="6d2a0-132">Modificare i metadati nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-132">Edit metadata in the header of the file.</span></span>
-   <span data-ttu-id="6d2a0-133">Scrivere esempi precompressi.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-133">Write precompressed samples.</span></span>
-   <span data-ttu-id="6d2a0-134">Scrivere in sink di rete per lo streaming di dati in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-134">Write to network sinks for streaming live data.</span></span>
-   <span data-ttu-id="6d2a0-135">Scrivi nei sink di file per le opzioni avanzate di controllo file.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-135">Write to file sinks for advanced file control options.</span></span>
-   <span data-ttu-id="6d2a0-136">Scrivere nei sink di push per la distribuzione nei server che forniranno contenuto agli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-136">Write to push sinks for distribution to servers that will deliver content to end users.</span></span>
-   <span data-ttu-id="6d2a0-137">Fornire esempi di PostView per la verifica dell'output.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-137">Deliver postview samples for verification of output.</span></span>
-   <span data-ttu-id="6d2a0-138">Recapitare le statistiche sulle prestazioni del writer.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-138">Deliver writer-performance statistics.</span></span>

<span data-ttu-id="6d2a0-139">Nelle sezioni seguenti viene descritto in dettaglio l'utilizzo dell'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-139">The following sections describe the use of the writer object in detail.</span></span>



| <span data-ttu-id="6d2a0-140">Sezione</span><span class="sxs-lookup"><span data-stu-id="6d2a0-140">Section</span></span>                                                                    | <span data-ttu-id="6d2a0-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d2a0-141">Description</span></span>                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d2a0-142">Per utilizzare profili con il writer</span><span class="sxs-lookup"><span data-stu-id="6d2a0-142">To Use Profiles with the Writer</span></span>](to-use-profiles-with-the-writer.md)     | <span data-ttu-id="6d2a0-143">Viene descritto come specificare un profilo da utilizzare con il writer.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-143">Describes how to specify a profile to use with the writer.</span></span>                                             |
| [<span data-ttu-id="6d2a0-144">Utilizzo degli input</span><span class="sxs-lookup"><span data-stu-id="6d2a0-144">Working with Inputs</span></span>](working-with-inputs.md)                             | <span data-ttu-id="6d2a0-145">Viene descritto come identificare e configurare le impostazioni di input nel writer.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-145">Describes how to identify and configure the input settings in the writer.</span></span>                              |
| [<span data-ttu-id="6d2a0-146">Per modificare i metadati con il writer</span><span class="sxs-lookup"><span data-stu-id="6d2a0-146">To Edit Metadata with the Writer</span></span>](to-edit-metadata-with-the-writer.md)   | <span data-ttu-id="6d2a0-147">Viene descritto come utilizzare il writer per modificare i metadati per un nuovo file.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-147">Describes how to use the writer to edit metadata for a new file.</span></span>                                       |
| [<span data-ttu-id="6d2a0-148">Per scrivere esempi</span><span class="sxs-lookup"><span data-stu-id="6d2a0-148">To Write Samples</span></span>](to-write-samples.md)                                   | <span data-ttu-id="6d2a0-149">Viene descritto come passare campioni al writer.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-149">Describes how to pass samples to the writer.</span></span>                                                           |
| [<span data-ttu-id="6d2a0-150">Impostazione delle estensioni delle unità dati</span><span class="sxs-lookup"><span data-stu-id="6d2a0-150">Setting Data Unit Extensions</span></span>](setting-data-unit-extensions.md)           | <span data-ttu-id="6d2a0-151">Viene descritto come aggiungere dati estesi ad esempi.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-151">Describes how to add extended data to samples.</span></span>                                                         |
| [<span data-ttu-id="6d2a0-152">Scrittura di esempi compressi</span><span class="sxs-lookup"><span data-stu-id="6d2a0-152">Writing Compressed Samples</span></span>](writing-compressed-samples.md)               | <span data-ttu-id="6d2a0-153">Viene descritto come passare gli esempi pre-compressi al writer.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-153">Describes how to pass pre-compressed samples to the writer.</span></span>                                            |
| [<span data-ttu-id="6d2a0-154">Scrittura di flussi di immagini</span><span class="sxs-lookup"><span data-stu-id="6d2a0-154">Writing Image Streams</span></span>](writing-image-streams.md)                         | <span data-ttu-id="6d2a0-155">Viene descritto come configurare un input per un flusso di immagini.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-155">Describes how to configure an input for an image stream.</span></span>                                               |
| [<span data-ttu-id="6d2a0-156">Creazione di esempi di immagini video</span><span class="sxs-lookup"><span data-stu-id="6d2a0-156">Writing Video Image Samples</span></span>](writing-video-image-samples.md)             | <span data-ttu-id="6d2a0-157">Viene descritto come configurare esempi di immagini video.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-157">Describes how to configure Video Image samples.</span></span>                                                        |
| [<span data-ttu-id="6d2a0-158">Scrittura di flussi di velocità in bit variabili</span><span class="sxs-lookup"><span data-stu-id="6d2a0-158">Writing Variable Bit Rate Streams</span></span>](writing-variable-bit-rate-streams.md) | <span data-ttu-id="6d2a0-159">Viene descritto come scrivere flussi di velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="6d2a0-159">Describes how to write variable bit rate (VBR) streams.</span></span>                                                |
| [<span data-ttu-id="6d2a0-160">Uso della codifica Two-Pass</span><span class="sxs-lookup"><span data-stu-id="6d2a0-160">Using Two-Pass Encoding</span></span>](using-two-pass-encoding.md)                     | <span data-ttu-id="6d2a0-161">Viene descritto come fare in modo che il codec esegua un passaggio preliminare prima di scrivere il file.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-161">Describes how to have the codec perform a preliminary pass before writing the file.</span></span>                    |
| [<span data-ttu-id="6d2a0-162">Per forzare l'inserimento di Key-Frame</span><span class="sxs-lookup"><span data-stu-id="6d2a0-162">To Force Key-Frame Insertion</span></span>](to-force-key-frame-insertion.md)           | <span data-ttu-id="6d2a0-163">Viene descritto come forzare manualmente il codec a codificare un campione come fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-163">Describes how to manually force the codec to encode a sample as a key frame.</span></span>                           |
| [<span data-ttu-id="6d2a0-164">Per gestire la latenza del writer</span><span class="sxs-lookup"><span data-stu-id="6d2a0-164">To Manage Writer Latency</span></span>](to-manage-writer-latency.md)                   | <span data-ttu-id="6d2a0-165">Viene descritto come ridurre al minimo il tempo impiegato dal writer per elaborare gli esempi in un file o un sink di output.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-165">Describes how to minimize the time it takes the writer to process samples into an output file or sink.</span></span> |
| [<span data-ttu-id="6d2a0-166">Utilizzo dei sink di writer</span><span class="sxs-lookup"><span data-stu-id="6d2a0-166">Working with Writer Sinks</span></span>](working-with-writer-sinks.md)                 | <span data-ttu-id="6d2a0-167">Viene descritto come usare i sink del writer per distribuire il contenuto a file o percorsi di rete.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-167">Describes how to use writer sinks to deliver your content to files or network locations.</span></span>               |
| [<span data-ttu-id="6d2a0-168">Per ottenere le statistiche del writer</span><span class="sxs-lookup"><span data-stu-id="6d2a0-168">To Get Writer Statistics</span></span>](to-get-writer-statistics.md)                   | <span data-ttu-id="6d2a0-169">Viene descritto come ottenere le statistiche per il writer.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-169">Describes how to get statistics for the writer.</span></span>                                                        |
| [<span data-ttu-id="6d2a0-170">Per utilizzare PostView writer</span><span class="sxs-lookup"><span data-stu-id="6d2a0-170">To Use Writer Postview</span></span>](to-use-writer-postview.md)                       | <span data-ttu-id="6d2a0-171">Viene descritto come ottenere campioni non compressi durante la scrittura di un file per la verifica.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-171">Describes how to get uncompressed samples as you write a file for verification.</span></span>                        |



 

## <a name="related-topics"></a><span data-ttu-id="6d2a0-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6d2a0-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d2a0-173">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="6d2a0-173">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="6d2a0-174">**Oggetto file sink del writer**</span><span class="sxs-lookup"><span data-stu-id="6d2a0-174">**Writer File Sink Object**</span></span>](writer-file-sink-object.md)
</dt> <dt>

[<span data-ttu-id="6d2a0-175">**Oggetto sink di rete writer**</span><span class="sxs-lookup"><span data-stu-id="6d2a0-175">**Writer Network Sink Object**</span></span>](writer-network-sink-object.md)
</dt> <dt>

[<span data-ttu-id="6d2a0-176">**Oggetto writer**</span><span class="sxs-lookup"><span data-stu-id="6d2a0-176">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




