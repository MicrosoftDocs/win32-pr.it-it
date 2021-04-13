---
title: Lettura di file con il lettore asincrono
description: Lettura di file con il lettore asincrono
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- Windows Media Format SDK, lettura di file
- Windows Media Format SDK, Reader asincroni
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- Formato di sistemi avanzati (ASF), lettura di file
- ASF (Advanced Systems Format), lettura di file
- Reader asincroni, interfaccia IWMReaderCallback
- IWMReaderCallback, lettori asincroni
- Reader asincroni, lettura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0807c0701dd596f943010ad613b08ef9fe2c415c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398555"
---
# <a name="reading-files-with-the-asynchronous-reader"></a><span data-ttu-id="7e278-112">Lettura di file con il lettore asincrono</span><span class="sxs-lookup"><span data-stu-id="7e278-112">Reading Files with the Asynchronous Reader</span></span>

<span data-ttu-id="7e278-113">Il lettore asincrono legge il contenuto dai file ASF usando più thread e chiamate asincrone.</span><span class="sxs-lookup"><span data-stu-id="7e278-113">The asynchronous reader reads the content from ASF files using multiple threads and asynchronous calls.</span></span> <span data-ttu-id="7e278-114">Le funzionalità supportate dal reader asincrono lo rendono particolarmente adatto per le applicazioni che eseguono il rendering del contenuto agli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="7e278-114">The features supported by the asynchronous reader make it well suited for applications that render content to end users.</span></span>

<span data-ttu-id="7e278-115">La maggior parte delle funzionalità di base dell'oggetto Reader può essere suddivisa nei passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="7e278-115">The most basic functionality of the reader object can be broken down into the following steps.</span></span> <span data-ttu-id="7e278-116">In questa procedura "l'applicazione" si riferisce al programma scritto usando Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="7e278-116">In these steps "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="7e278-117">L'applicazione implementa l'interfaccia [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) per gestire i messaggi dal reader.</span><span class="sxs-lookup"><span data-stu-id="7e278-117">The application implements the [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) interface to handle messages from the reader.</span></span> <span data-ttu-id="7e278-118">Sono inclusi due metodi di callback: **OnStatus**, che riceve i messaggi relativi allo stato di diversi aspetti del Reader e **OnSample**, che riceve campioni non compressi dal reader.</span><span class="sxs-lookup"><span data-stu-id="7e278-118">This includes two callback methods: **OnStatus**, which receives messages relating to the status of various aspects of the reader and **OnSample**, which receives uncompressed samples from the reader.</span></span>
2.  <span data-ttu-id="7e278-119">L'applicazione passa al lettore il nome di un file da leggere.</span><span class="sxs-lookup"><span data-stu-id="7e278-119">The application passes to the reader the name of a file to read.</span></span> <span data-ttu-id="7e278-120">Quando il lettore apre il file, assegna un numero di output a ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="7e278-120">When the reader opens the file, it assigns an output number to each stream.</span></span> <span data-ttu-id="7e278-121">Se il file usa l'esclusione reciproca, il lettore assegna un singolo output per tutti i flussi che si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="7e278-121">If the file uses mutual exclusion, the reader assigns a single output for all of the mutually exclusive streams.</span></span>
3.  <span data-ttu-id="7e278-122">L'applicazione ottiene informazioni sulla configurazione dei vari output dal reader.</span><span class="sxs-lookup"><span data-stu-id="7e278-122">The application gets information about the configuration of the various outputs from the reader.</span></span> <span data-ttu-id="7e278-123">Le informazioni raccolte consentiranno all'applicazione di eseguire correttamente il rendering degli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="7e278-123">The information gathered will enable the application to properly render media samples.</span></span>
4.  <span data-ttu-id="7e278-124">L'applicazione indica al lettore di iniziare a leggere i dati dal file.</span><span class="sxs-lookup"><span data-stu-id="7e278-124">The application instructs the reader to begin reading data from the file.</span></span> <span data-ttu-id="7e278-125">Il lettore inizia a inviare campioni non compressi al callback **OnSample** uno alla volta nei buffer racchiusi tra oggetti buffer.</span><span class="sxs-lookup"><span data-stu-id="7e278-125">The reader begins delivering uncompressed samples to the **OnSample** callback one at a time in buffers wrapped in buffer objects.</span></span> <span data-ttu-id="7e278-126">Gli esempi recapitati dal reader sono ordinati in base alla fase di presentazione.</span><span class="sxs-lookup"><span data-stu-id="7e278-126">The samples delivered by the reader are in presentation-time order.</span></span> <span data-ttu-id="7e278-127">Il lettore continuerà a consegnare gli esempi fino a quando non verrà interrotto dall'applicazione o fino al raggiungimento della fine del file.</span><span class="sxs-lookup"><span data-stu-id="7e278-127">The reader will continue delivering samples until stopped by the application or until the end of the file is reached.</span></span>
5.  <span data-ttu-id="7e278-128">L'applicazione è responsabile del rendering dei dati dopo che sono stati recapitati dal lettore.</span><span class="sxs-lookup"><span data-stu-id="7e278-128">The application is responsible for rendering data after it is delivered by the reader.</span></span> <span data-ttu-id="7e278-129">Windows Media Format SDK non fornisce routine di rendering.</span><span class="sxs-lookup"><span data-stu-id="7e278-129">The Windows Media Format SDK does not provide any rendering routines.</span></span> <span data-ttu-id="7e278-130">In genere, le applicazioni utilizzeranno altri SDK per eseguire il rendering dei dati, ad esempio Microsoft DirectX® SDK, o le funzioni multimediali di Microsoft Windows Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="7e278-130">Typically, applications will use other SDKs to render data, such as the Microsoft DirectX® SDK, or the multimedia functions of the Microsoft Windows Platform SDK.</span></span>
6.  <span data-ttu-id="7e278-131">Al termine della lettura, l'applicazione indica al lettore di chiudere il file.</span><span class="sxs-lookup"><span data-stu-id="7e278-131">When reading is complete, the application instructs the reader to close the file.</span></span>

<span data-ttu-id="7e278-132">Questi passaggi sono illustrati nell'applicazione di esempio AudioPlayer, tra gli altri.</span><span class="sxs-lookup"><span data-stu-id="7e278-132">These steps are illustrated in the AudioPlayer sample application, among others.</span></span> <span data-ttu-id="7e278-133">Per altre informazioni, vedere [applicazioni di esempio](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="7e278-133">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="7e278-134">Il lettore supporta inoltre funzionalità più avanzate.</span><span class="sxs-lookup"><span data-stu-id="7e278-134">The reader also supports more advanced functionality.</span></span> <span data-ttu-id="7e278-135">Il lettore consente di eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7e278-135">The reader enables you to do the following:</span></span>

-   <span data-ttu-id="7e278-136">Sospendere la riproduzione di un file.</span><span class="sxs-lookup"><span data-stu-id="7e278-136">Pause playback of a file.</span></span>
-   <span data-ttu-id="7e278-137">Recuperare le statistiche sulle prestazioni del lettore.</span><span class="sxs-lookup"><span data-stu-id="7e278-137">Retrieve reader performance statistics.</span></span>
-   <span data-ttu-id="7e278-138">Controllare la selezione del flusso per i flussi che si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="7e278-138">Control stream selection for mutually exclusive streams.</span></span>
-   <span data-ttu-id="7e278-139">Allocare manualmente i buffer per l'output.</span><span class="sxs-lookup"><span data-stu-id="7e278-139">Manually allocate buffers for output.</span></span>
-   <span data-ttu-id="7e278-140">Fornire il proprio clock.</span><span class="sxs-lookup"><span data-stu-id="7e278-140">Provide your own clock.</span></span>
-   <span data-ttu-id="7e278-141">Recuperare lo stato delle operazioni su file (memorizzazione nel buffer, download o salvataggio).</span><span class="sxs-lookup"><span data-stu-id="7e278-141">Retrieve the status of file operations (buffering, download, or save).</span></span>
-   <span data-ttu-id="7e278-142">Aprire un file utilizzando l'interfaccia COM standard, **IStream**.</span><span class="sxs-lookup"><span data-stu-id="7e278-142">Open a file using the standard COM interface, **IStream**.</span></span>
-   <span data-ttu-id="7e278-143">Consente di cercare punti specifici in un file ASF.</span><span class="sxs-lookup"><span data-stu-id="7e278-143">Seek to specific points in an ASF file.</span></span>
-   <span data-ttu-id="7e278-144">Leggere i dati di profilo dall'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="7e278-144">Read profile data from the header of the file.</span></span>

<span data-ttu-id="7e278-145">Nelle sezioni seguenti viene descritto in dettaglio l'utilizzo dell'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="7e278-145">The following sections describe the use of the reader object in detail.</span></span>

-   [<span data-ttu-id="7e278-146">Per implementare i messaggi del lettore nel callback OnStatus</span><span class="sxs-lookup"><span data-stu-id="7e278-146">To Implement Reader Messages in the OnStatus Callback</span></span>](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [<span data-ttu-id="7e278-147">Per implementare il callback OnSample</span><span class="sxs-lookup"><span data-stu-id="7e278-147">To Implement the OnSample Callback</span></span>](to-implement-the-onsample-callback.md)
-   [<span data-ttu-id="7e278-148">Per creare un reader e aprire un file</span><span class="sxs-lookup"><span data-stu-id="7e278-148">To Create a Reader and Open a File</span></span>](to-create-a-reader-and-open-a-file.md)
-   [<span data-ttu-id="7e278-149">Per recuperare esempi di supporti con il Reader asincrono</span><span class="sxs-lookup"><span data-stu-id="7e278-149">To Retrieve Media Samples with the Asynchronous Reader</span></span>](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [<span data-ttu-id="7e278-150">Per eseguire ricerche in base al tempo tramite il Reader asincrono</span><span class="sxs-lookup"><span data-stu-id="7e278-150">To Seek By Time Using the Asynchronous Reader</span></span>](to-seek-by-time-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="7e278-151">Per eseguire la ricerca in base al numero di frame utilizzando il Reader asincrono</span><span class="sxs-lookup"><span data-stu-id="7e278-151">To Seek By Frame Number Using the Asynchronous Reader</span></span>](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="7e278-152">Per eseguire la ricerca in base al codice ora SMPTE usando il Reader asincrono</span><span class="sxs-lookup"><span data-stu-id="7e278-152">To Seek By SMPTE Time Code Using the Asynchronous Reader</span></span>](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="7e278-153">Per cercare i marcatori</span><span class="sxs-lookup"><span data-stu-id="7e278-153">To Seek to Markers</span></span>](to-seek-to-markers.md)
-   [<span data-ttu-id="7e278-154">Per sospendere o arrestare la riproduzione</span><span class="sxs-lookup"><span data-stu-id="7e278-154">To Pause or Stop Playback</span></span>](to-pause-or-stop-playback.md)
-   [<span data-ttu-id="7e278-155">Per ottenere le statistiche sulle prestazioni del lettore</span><span class="sxs-lookup"><span data-stu-id="7e278-155">To Get Reader Performance Statistics</span></span>](to-get-reader-performance-statistics.md)
-   [<span data-ttu-id="7e278-156">Per usare la selezione del flusso manuale</span><span class="sxs-lookup"><span data-stu-id="7e278-156">To Use Manual Stream Selection</span></span>](to-use-manual-stream-selection.md)
-   [<span data-ttu-id="7e278-157">Per recapitare esempi compressi con il lettore asincrono</span><span class="sxs-lookup"><span data-stu-id="7e278-157">To Deliver Compressed Samples with the Asynchronous Reader</span></span>](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a><span data-ttu-id="7e278-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e278-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e278-159">**Lettura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="7e278-159">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="7e278-160">**Oggetto Lettore**</span><span class="sxs-lookup"><span data-stu-id="7e278-160">**Reader Object**</span></span>](reader-object.md)
</dt> </dl>

 

 




