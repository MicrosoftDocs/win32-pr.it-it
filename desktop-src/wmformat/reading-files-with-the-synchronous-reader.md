---
title: Lettura di file con il lettore sincrono
description: Lettura di file con il lettore sincrono
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- Windows Media Format SDK, lettura di file
- Windows Media Format SDK, lettori sincroni
- ASF (Advanced Systems Format), lettori sincroni
- ASF (formato avanzato dei sistemi), lettori sincroni
- Formato di sistemi avanzati (ASF), lettura di file
- ASF (Advanced Systems Format), lettura di file
- lettori sincroni, interfaccia IWMReaderCallback
- IWMReaderCallback, lettori sincroni
- lettori sincroni, lettura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893a1bd324cdc91968e423f2084bfdba5ef57c8e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398554"
---
# <a name="reading-files-with-the-synchronous-reader"></a><span data-ttu-id="0cdbf-112">Lettura di file con il lettore sincrono</span><span class="sxs-lookup"><span data-stu-id="0cdbf-112">Reading Files with the Synchronous Reader</span></span>

<span data-ttu-id="0cdbf-113">È possibile utilizzare il lettore sincrono per leggere un file ASF utilizzando chiamate sincrone anziché i metodi asincroni nell'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-113">You can use the synchronous reader to read an ASF file using synchronous calls instead of the asynchronous methods in the reader object.</span></span> <span data-ttu-id="0cdbf-114">L'utilizzo di chiamate sincrone riduce il numero di thread necessari per la lettura di un file.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-114">Using synchronous calls reduces the number of threads required to read a file.</span></span> <span data-ttu-id="0cdbf-115">Il lettore asincrono usa più thread per l'elaborazione dei flussi.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-115">The asynchronous reader uses multiple threads for processing streams.</span></span> <span data-ttu-id="0cdbf-116">Per i file con più flussi, il numero di thread usati può diventare molto grande.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-116">For files with multiple streams, the number of threads used can become very large.</span></span> <span data-ttu-id="0cdbf-117">Il lettore sincrono utilizza un solo thread.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-117">The synchronous reader uses only one thread.</span></span>

<span data-ttu-id="0cdbf-118">Il lettore sincrono è stato progettato per soddisfare le esigenze di creazione di contenuti e di applicazioni di modifica di file.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-118">The synchronous reader was designed to meet the needs of content creation and file editing applications.</span></span> <span data-ttu-id="0cdbf-119">È possibile utilizzare il lettore sincrono per altre applicazioni, ma la sua funzionalità è limitata.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-119">You can use the synchronous reader for other applications, but its functionality is limited.</span></span>

<span data-ttu-id="0cdbf-120">Il lettore sincrono può aprire file locali o file in una rete usando il nome del percorso UNC (ad esempio " \\ \\ someshare \\ somedirectory \\ somefile. wmv").</span><span class="sxs-lookup"><span data-stu-id="0cdbf-120">The synchronous reader can open files that are local, or files on a network using the UNC path name (such as "\\\\someshare\\somedirectory\\somefile.wmv").</span></span> <span data-ttu-id="0cdbf-121">Non è possibile trasmettere file al lettore sincrono o aprire file da un percorso Internet.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-121">You cannot stream files to the synchronous reader, or open files from an Internet location.</span></span> <span data-ttu-id="0cdbf-122">Il lettore sincrono fornisce inoltre supporto per l'utilizzo dell'interfaccia com **IStream** come origine.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-122">The synchronous reader also provides support for using the **IStream** COM interface as a source.</span></span>

<span data-ttu-id="0cdbf-123">Il lettore sincrono offre maggiore versatilità per il recupero di esempi da un file ASF rispetto al lettore asincrono.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-123">The synchronous reader provides more versatility for retrieving samples from an ASF file than the asynchronous reader.</span></span> <span data-ttu-id="0cdbf-124">Il lettore sincrono può recapitare campioni per numero di flusso e per output.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-124">The synchronous reader can deliver samples by stream number as well as by output.</span></span> <span data-ttu-id="0cdbf-125">Gli esempi recapitati dal numero di flusso possono essere compressi o decompressi.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-125">Samples delivered by stream number can be compressed or uncompressed.</span></span> <span data-ttu-id="0cdbf-126">Il lettore sincrono può anche passare da un recapito compresso a quello non compresso durante la riproduzione. Questa funzionalità è nota come "modifica rapida".</span><span class="sxs-lookup"><span data-stu-id="0cdbf-126">The synchronous reader can also switch between compressed and uncompressed delivery during playback; this feature is known as "fast editing."</span></span> <span data-ttu-id="0cdbf-127">Questa funzionalità consente a un'applicazione di modifica di leggere contenuto basato su Windows Media e passarlo direttamente al writer fino a quando non viene raggiunto un frame desiderato.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-127">This feature enables an editing application to read Windows Media-based content and pass it directly through to the writer until a desired frame is reached.</span></span> <span data-ttu-id="0cdbf-128">A questo punto, l'applicazione può indicare al lettore di iniziare a consegnare contenuto non compresso, che l'applicazione può quindi modificare e passare al writer per la ricompressione.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-128">At that point the application can tell the reader to start delivering uncompressed content, which the application can then modify and pass to the writer for recompression.</span></span> <span data-ttu-id="0cdbf-129">Quando l'applicazione ha terminato di modificare i frame specificati, può indicare al lettore di iniziare a consegnare nuovamente i frame compressi.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-129">When the application has finished modifying the specified frames, it can tell the reader to start delivering compressed frames again.</span></span>

<span data-ttu-id="0cdbf-130">La maggior parte delle funzionalità di base dell'oggetto Reader sincrono può essere suddivisa nei passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-130">The most basic functionality of the synchronous reader object can be broken down into the following steps.</span></span> <span data-ttu-id="0cdbf-131">In questa procedura "l'applicazione" si riferisce al programma scritto usando Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-131">In these steps "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="0cdbf-132">L'applicazione passa al lettore sincrono il nome di un file da leggere.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-132">The application passes to the synchronous reader the name of a file to read.</span></span> <span data-ttu-id="0cdbf-133">Quando il lettore sincrono apre il file, assegna un numero di output a ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-133">When the synchronous reader opens the file, it assigns an output number to each stream.</span></span> <span data-ttu-id="0cdbf-134">Se il file usa l'esclusione reciproca, il lettore assegna un singolo output per tutti i flussi che si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-134">If the file uses mutual exclusion, the reader assigns a single output for all of the mutually exclusive streams.</span></span>
2.  <span data-ttu-id="0cdbf-135">L'applicazione ottiene informazioni sulla configurazione dei vari output dal reader.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-135">The application gets information about the configuration of the various outputs from the reader.</span></span> <span data-ttu-id="0cdbf-136">Le informazioni raccolte consentiranno all'applicazione di eseguire correttamente il rendering degli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-136">The information gathered will enable the application to properly render media samples.</span></span>
3.  <span data-ttu-id="0cdbf-137">L'applicazione inizia a richiedere gli esempi, uno alla volta, dal lettore sincrono.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-137">The application begins requesting samples, one at a time, from the synchronous reader.</span></span> <span data-ttu-id="0cdbf-138">Il lettore sincrono recapita ogni esempio in un oggetto buffer per il quale viene distribuita l'interfaccia [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) .</span><span class="sxs-lookup"><span data-stu-id="0cdbf-138">The synchronous reader delivers each sample in a buffer object for which it delivers the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface.</span></span>
4.  <span data-ttu-id="0cdbf-139">L'applicazione è responsabile del rendering dei dati dopo che sono stati recapitati dal lettore.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-139">The application is responsible for rendering data after it is delivered by the reader.</span></span> <span data-ttu-id="0cdbf-140">Windows Media Format SDK non fornisce routine di rendering.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-140">The Windows Media Format SDK does not provide any rendering routines.</span></span> <span data-ttu-id="0cdbf-141">In genere, le applicazioni utilizzeranno altri SDK per eseguire il rendering dei dati, ad esempio Microsoft Direct X SDK, o le funzioni multimediali di Microsoft Windows Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-141">Typically, applications will use other SDKs to render data, such as the Microsoft Direct X SDK, or the multimedia functions of the Microsoft Windows Platform SDK.</span></span>

<span data-ttu-id="0cdbf-142">Questi passaggi sono illustrati nell'applicazione di esempio WMSyncReader.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-142">These steps are illustrated in the WMSyncReader sample application.</span></span> <span data-ttu-id="0cdbf-143">Per altre informazioni, vedere [applicazioni di esempio](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="0cdbf-143">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="0cdbf-144">Il lettore sincrono supporta inoltre funzionalità più avanzate.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-144">The synchronous reader also supports more advanced functionality.</span></span> <span data-ttu-id="0cdbf-145">Il lettore sincrono consente di eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0cdbf-145">The synchronous reader enables you to do the following:</span></span>

-   <span data-ttu-id="0cdbf-146">Consente di specificare un intervallo di campioni da recuperare in base all'ora o al numero di frame.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-146">Specify a range of samples to retrieve by time or by frame number.</span></span>
-   <span data-ttu-id="0cdbf-147">Controllare la selezione del flusso per i flussi che si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-147">Control stream selection for mutually exclusive streams.</span></span>
-   <span data-ttu-id="0cdbf-148">Aprire un file utilizzando l'interfaccia COM standard, **IStream**.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-148">Open a file using the standard COM interface, **IStream**.</span></span>
-   <span data-ttu-id="0cdbf-149">Leggere i dati di profilo dall'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-149">Read profile data from the file header.</span></span>
-   <span data-ttu-id="0cdbf-150">Leggere i metadati dall'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-150">Read metadata from the file header.</span></span>
-   <span data-ttu-id="0cdbf-151">Passa tra gli esempi di flusso e di output durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-151">Switch between stream and output samples during playback.</span></span>
-   <span data-ttu-id="0cdbf-152">Passare da un campione compresso a un flusso non compresso durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-152">Switch between compressed and uncompressed stream samples during playback.</span></span>

<span data-ttu-id="0cdbf-153">Nelle sezioni seguenti viene descritto in dettaglio l'utilizzo dell'oggetto Reader sincrono.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-153">The following sections describe the use of the synchronous reader object in detail.</span></span>

-   [<span data-ttu-id="0cdbf-154">Per creare un reader sincrono e aprire un file</span><span class="sxs-lookup"><span data-stu-id="0cdbf-154">To Create a Synchronous Reader and Open a File</span></span>](to-create-a-synchronous-reader-and-open-a-file.md)
-   [<span data-ttu-id="0cdbf-155">Per trovare i numeri di flusso e i numeri di output</span><span class="sxs-lookup"><span data-stu-id="0cdbf-155">To Find Stream Numbers and Output Numbers</span></span>](to-find-stream-numbers-and-output-numbers.md)
-   [<span data-ttu-id="0cdbf-156">Per recuperare esempi di supporti con il lettore sincrono</span><span class="sxs-lookup"><span data-stu-id="0cdbf-156">To Retrieve Media Samples with the Synchronous Reader</span></span>](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [<span data-ttu-id="0cdbf-157">Per eseguire ricerche in base al tempo tramite il lettore sincrono</span><span class="sxs-lookup"><span data-stu-id="0cdbf-157">To Seek By Time Using the Synchronous Reader</span></span>](to-seek-by-time-using-the-synchronous-reader.md)
-   [<span data-ttu-id="0cdbf-158">Per eseguire la ricerca in base al numero di frame utilizzando il lettore sincrono</span><span class="sxs-lookup"><span data-stu-id="0cdbf-158">To Seek By Frame Number Using the Synchronous Reader</span></span>](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [<span data-ttu-id="0cdbf-159">Per eseguire la ricerca in base al codice ora SMPTE usando il lettore sincrono</span><span class="sxs-lookup"><span data-stu-id="0cdbf-159">To Seek By SMPTE Time Code Using the Synchronous Reader</span></span>](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [<span data-ttu-id="0cdbf-160">Per recuperare esempi di flusso con il lettore sincrono</span><span class="sxs-lookup"><span data-stu-id="0cdbf-160">To Retrieve Stream Samples with the Synchronous Reader</span></span>](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [<span data-ttu-id="0cdbf-161">Per recuperare esempi compressi con il lettore sincrono</span><span class="sxs-lookup"><span data-stu-id="0cdbf-161">To Retrieve Compressed Samples with the Synchronous Reader</span></span>](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

<span data-ttu-id="0cdbf-162">**Codice di esempio**</span><span class="sxs-lookup"><span data-stu-id="0cdbf-162">**Example Code**</span></span>

<span data-ttu-id="0cdbf-163">Nell'esempio di codice seguente viene illustrato come leggere esempi da un file ASF utilizzando il lettore sincrono.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-163">The following example code shows how to read samples from an ASF file using the synchronous reader.</span></span> <span data-ttu-id="0cdbf-164">Specifica in base al numero di frame un intervallo di campioni da recapitare.</span><span class="sxs-lookup"><span data-stu-id="0cdbf-164">It specifies by frame number a range of samples to deliver.</span></span>


```C++
IWMSyncReader* pSyncReader = NULL;
INSSBuffer*    pMyBuffer   = NULL;

QWORD cnsSampleTime = 0;
QWORD cnsSampleDuration = 0;
DWORD dwFlags = 0;
DWORD dwOutputNumber;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a synchronous reader.
hr = WMCreateSyncReader(NULL, WMT_RIGHT_PLAYBACK, &pSyncReader);

// Open an ASF file.
hr = pSyncReader->Open(L"c:\\somefile.wmv");

// TODO: Identify the properties for each output. This works 
// exactly as it does with the asynchronous reader.

// Specify a playback range from frame number 100 of the video 
// stream to the end of the file. Assume that the video stream 
// is stream number 2.
hr = pSyncReader->SetRangeByFrame(2, 100, 0);

// Loop through all the samples in the specified range.
do
{
   // Get the next sample, regardless of its stream number.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

pSyncReader->Release();
pSyncReader = NULL;

```



## <a name="related-topics"></a><span data-ttu-id="0cdbf-165">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0cdbf-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cdbf-166">**Interfaccia IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="0cdbf-166">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="0cdbf-167">**Lettura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="0cdbf-167">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="0cdbf-168">**Oggetto lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="0cdbf-168">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> </dl>

 

 




