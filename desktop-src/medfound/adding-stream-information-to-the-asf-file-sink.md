---
description: Il sink di file ASF è un'implementazione di IMFMediaSink fornita da Media Foundation che un'applicazione può usare per archiviare i dati del supporto ASF in un file. Per informazioni sul modello a oggetti dei sink multimediali ASF e sull'utilizzo generale, vedere la pagina relativa ai sink di supporto ASF.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Aggiunta di informazioni sul flusso al sink di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e08c6997d9c77836f379d4ca7b75720ddea245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306759"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a><span data-ttu-id="9b36d-104">Aggiunta di informazioni sul flusso al sink di file ASF</span><span class="sxs-lookup"><span data-stu-id="9b36d-104">Adding Stream Information to the ASF File Sink</span></span>

<span data-ttu-id="9b36d-105">Il sink di file ASF è un'implementazione di [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornita da Media Foundation che un'applicazione può usare per archiviare i dati del supporto ASF in un file.</span><span class="sxs-lookup"><span data-stu-id="9b36d-105">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="9b36d-106">Per informazioni sul modello a oggetti dei sink multimediali ASF e sull'utilizzo generale, vedere la pagina relativa ai [sink di supporto ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="9b36d-106">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="9b36d-107">Dopo aver creato un'istanza del sink di file, è necessario configurarlo prima di compilare la topologia.</span><span class="sxs-lookup"><span data-stu-id="9b36d-107">After instantiating the file sink, it must be configured before building the topology.</span></span> <span data-ttu-id="9b36d-108">Il sink di file deve conoscere i flussi nel file di output, le informazioni sulla modalità di codifica e i metadati.</span><span class="sxs-lookup"><span data-stu-id="9b36d-108">The file sink needs to know about the streams in the output file, the encoding mode information, and the metadata.</span></span> <span data-ttu-id="9b36d-109">In questo argomento viene descritto il processo di aggiunta di un flusso nel sink di file.</span><span class="sxs-lookup"><span data-stu-id="9b36d-109">This topic describes the process of adding stream in the file sink.</span></span>

-   [<span data-ttu-id="9b36d-110">Aggiunta di flussi nel sink di file ASF</span><span class="sxs-lookup"><span data-stu-id="9b36d-110">Adding Streams in the ASF File Sink</span></span>](#adding-streams-in-the-asf-file-sink)
-   [<span data-ttu-id="9b36d-111">Enumerazione dei sink di flusso</span><span class="sxs-lookup"><span data-stu-id="9b36d-111">Enumerating Stream Sinks</span></span>](#enumerating-stream-sinks)
-   [<span data-ttu-id="9b36d-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b36d-112">Related topics</span></span>](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a><span data-ttu-id="9b36d-113">Aggiunta di flussi nel sink di file ASF</span><span class="sxs-lookup"><span data-stu-id="9b36d-113">Adding Streams in the ASF File Sink</span></span>

<span data-ttu-id="9b36d-114">Il sink di file deve essere a conoscenza dei flussi di output e delle relative proprietà in modo che sia in grado di generare gli esempi di output di conseguenza e di aggiungerli al file ASF di output.</span><span class="sxs-lookup"><span data-stu-id="9b36d-114">The file sink must know of the output streams and their properties so that it can generate output samples accordingly and add them to the output ASF file.</span></span> <span data-ttu-id="9b36d-115">Queste impostazioni vengono scritte nell'oggetto intestazione ASF finale.</span><span class="sxs-lookup"><span data-stu-id="9b36d-115">These settings are written to the final ASF Header Object.</span></span>

<span data-ttu-id="9b36d-116">Per impostare le informazioni sul flusso, è necessario avere un riferimento all'oggetto ASF di sink di file.</span><span class="sxs-lookup"><span data-stu-id="9b36d-116">To set stream information, you must have a reference to the file sink's ASF ContentInfo object.</span></span> <span data-ttu-id="9b36d-117">Per informazioni, vedere [creazione del sink di file ASF](creating-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="9b36d-117">For information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="9b36d-118">Nella procedura riportata di seguito vengono riepilogati i passaggi generali per la configurazione di Stream utilizzando l'oggetto profilo ASF.</span><span class="sxs-lookup"><span data-stu-id="9b36d-118">The following procedure summarizes the general steps for configuring stream by using the ASF profile object.</span></span>

<span data-ttu-id="9b36d-119">**Per configurare le informazioni sul flusso nel sink di file ASF**</span><span class="sxs-lookup"><span data-stu-id="9b36d-119">**To configure stream information in the ASF file sink**</span></span>

1.  <span data-ttu-id="9b36d-120">Creare un oggetto profilo ASF chiamando [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span><span class="sxs-lookup"><span data-stu-id="9b36d-120">Create an ASF profile object by calling [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span></span>
2.  <span data-ttu-id="9b36d-121">Per ogni flusso nel file di output, creare un tipo di supporto per il flusso di destinazione da aggiungere nel sink di file.</span><span class="sxs-lookup"><span data-stu-id="9b36d-121">For each stream in the output file, create a media type for the target stream to be added in the file sink.</span></span> <span data-ttu-id="9b36d-122">Il tipo di supporto deve essere compatibile con i tipi di output supportati dai codificatori Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9b36d-122">The media type must be compatible with the output types supported by the Windows Media encoders.</span></span>

    <span data-ttu-id="9b36d-123">Per informazioni sull'aggiunta di flussi audio al profilo, vedere Creazione di flussi audio per la codifica ASF.</span><span class="sxs-lookup"><span data-stu-id="9b36d-123">For information about adding audio streams to the profile, see Creating Audio Streams for ASF Encoding.</span></span>

    <span data-ttu-id="9b36d-124">Per informazioni sull'aggiunta di flussi video al profilo, vedere Creazione di flussi video per la codifica ASF.</span><span class="sxs-lookup"><span data-stu-id="9b36d-124">For information about adding video streams to the profile, see Creating Video Streams for ASF Encoding.</span></span>

3.  <span data-ttu-id="9b36d-125">Creare flussi in base ai tipi di supporti creati nel passaggio 2 chiamando [**IMFASFProfile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span><span class="sxs-lookup"><span data-stu-id="9b36d-125">Create streams based on the media types created in step 2 by calling [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span></span>
4.  <span data-ttu-id="9b36d-126">Assegnare un numero di flusso per il flusso appena creato chiamando il puntatore all'interfaccia [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) ricevuto nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="9b36d-126">Assign a stream number for the newly created stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface pointer received in step 3.</span></span>
5.  <span data-ttu-id="9b36d-127">Facoltativamente, configurare il flusso con le seguenti informazioni:</span><span class="sxs-lookup"><span data-stu-id="9b36d-127">Optionally configure the stream with the following information:</span></span>
    -   <span data-ttu-id="9b36d-128">Parametri bucket a perdita di parametri impostando gli attributi: [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) o [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="9b36d-128">Leaky bucket parameters by setting the attributes: [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) or [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span></span>
    -   <span data-ttu-id="9b36d-129">Estensione del payload, esclusione reciproca chiamando i metodi [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="9b36d-129">Payload extension, mutual exclusion by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods.</span></span>
6.  <span data-ttu-id="9b36d-130">Facoltativamente, impostare le dimensioni del pacchetto di dati per il profilo impostando gli attributi [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) e [**MF \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="9b36d-130">Optionally set data packet size for the profile by setting [**MF\_ASFPROFILE\_MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) and [**MF\_ASFPROFILE\_MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) attributes.</span></span> <span data-ttu-id="9b36d-131">Il profilo ASF espone l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , a cui un'applicazione può fare riferimento chiamando **IMFASFProfile:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="9b36d-131">The ASF profile exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, which an application can get reference to by calling **IMFASFProfile::QueryInterface**.</span></span>
7.  <span data-ttu-id="9b36d-132">Impostare le informazioni di codifica per il flusso nel sink di file.</span><span class="sxs-lookup"><span data-stu-id="9b36d-132">Set encoding information for the stream in the file sink.</span></span> <span data-ttu-id="9b36d-133">Descritto in [impostazione delle proprietà nel sink di file](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="9b36d-133">Discussed in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
8.  <span data-ttu-id="9b36d-134">Aggiungere il flusso al profilo chiamando [**IMFASFProfile:: sestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span><span class="sxs-lookup"><span data-stu-id="9b36d-134">Add the stream to the profile by calling [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span></span>
9.  <span data-ttu-id="9b36d-135">Associare il profilo all'oggetto ContentInfo chiamando [**IMFASFContentInfo:: seprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span><span class="sxs-lookup"><span data-stu-id="9b36d-135">Associate the profile with the ContentInfo object by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span>

<span data-ttu-id="9b36d-136">Per modificare un flusso esistente, l'applicazione può ottenere un riferimento all'interfaccia [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) del flusso e riconfigurarla in base ai requisiti.</span><span class="sxs-lookup"><span data-stu-id="9b36d-136">To modify an existing stream, the application can get a reference to the stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface and reconfigure it according to the requirements.</span></span> <span data-ttu-id="9b36d-137">Per aggiungere o rimuovere flussi, l'applicazione deve chiamare [**IMFASFProfile:: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span><span class="sxs-lookup"><span data-stu-id="9b36d-137">To add or remove streams, the application must call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span></span> <span data-ttu-id="9b36d-138">Per applicare queste modifiche, modificare o rimuovere i flussi, è necessario impostare di nuovo il profilo nell'oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="9b36d-138">To apply these changes, stream modifications or removal, you must set the profile again in the ContentInfo object.</span></span> <span data-ttu-id="9b36d-139">Viene sovrascritto il profilo esistente già associato all'oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="9b36d-139">This overwrites the existing profile that is already associated with the ContentInfo object.</span></span>


```C++
//-------------------------------------------------------------------
//  CreateVideoStream
//  Create an video stream and add it to the profile.
//
//  pProfile: A pointer to the ASF profile.
//  wStreamNumber: Stream number to assign for the new stream.
//    pType: A pointer to the source's video media type.
//-------------------------------------------------------------------

HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
{
    if (!pProfile)
    {
        return E_INVALIDARG;
    }
    if (wStreamNumber < 1 || wStreamNumber > 127 )
    {
        return MF_E_INVALIDSTREAMNUMBER;
    }

    HRESULT hr = S_OK;

    
    IMFMediaType* pVideoType = NULL;
    IMFASFStreamConfig* pVideoStream = NULL;

    UINT32 dwBitRate = 0;
        
    //Create a new video type from the source type
    hr = CreateCompressedVideoType(pType, &pVideoType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create a new stream with the video type
    hr = pProfile->CreateStream(pVideoType, &pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }
    

    //Set a valid stream number
    hr = pVideoStream->SetStreamNumber(wStreamNumber);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile
    hr = pProfile->SetStream(pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }

    wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

done:

    SafeRelease(&pVideoStream);
    SafeRelease(&pVideoType);

    return hr;
}
```



## <a name="enumerating-stream-sinks"></a><span data-ttu-id="9b36d-140">Enumerazione dei sink di flusso</span><span class="sxs-lookup"><span data-stu-id="9b36d-140">Enumerating Stream Sinks</span></span>

<span data-ttu-id="9b36d-141">Per ogni flusso del profilo che l'oggetto ContentInfo è in grado di riconoscere, il sink di file ASF crea e aggiunge un sink del flusso che contiene tutte le proprietà del flusso codificato.</span><span class="sxs-lookup"><span data-stu-id="9b36d-141">For each stream in the profile that the ContentInfo object is aware of, the ASF file sink creates and adds a stream sink that contains all the properties of the encoded stream.</span></span> <span data-ttu-id="9b36d-142">Il sink di file ASF è progettato per contenere flussi fissi.</span><span class="sxs-lookup"><span data-stu-id="9b36d-142">The ASF file sink is designed to contain fixed streams.</span></span> <span data-ttu-id="9b36d-143">Ciò significa che non è possibile aggiungere o rimuovere flussi chiamando [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) o [**IMFMediaSink:: RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span><span class="sxs-lookup"><span data-stu-id="9b36d-143">This means that you cannot add or remove streams by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) or [**IMFMediaSink::RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span></span> <span data-ttu-id="9b36d-144">Queste chiamate al sink di file hanno esito negativo con il \_ \_ codice di errore fisso MF E STREAMSINKS \_ .</span><span class="sxs-lookup"><span data-stu-id="9b36d-144">These calls on the file sink fail with the MF\_E\_STREAMSINKS\_FIXED error code.</span></span> <span data-ttu-id="9b36d-145">L'aggiunta o la rimozione di flussi nel profilo non comporta l'aggiunta o la rimozione automatica dei sink di flusso nel sink di file.</span><span class="sxs-lookup"><span data-stu-id="9b36d-145">Adding or removing streams in the profile does not automatically add or remove the stream sinks in the file sink.</span></span> <span data-ttu-id="9b36d-146">È necessario eliminare l'istanza esistente del file e ricrearla con le nuove informazioni sul flusso se i flussi nel profilo sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="9b36d-146">You must discard the existing instance of the file and recreate it with new stream information if your streams in the profile have changed.</span></span>

<span data-ttu-id="9b36d-147">Nella procedura riportata di seguito vengono riepilogati i passaggi generali per l'enumerazione dei sink di flusso nel sink di file ASF.</span><span class="sxs-lookup"><span data-stu-id="9b36d-147">The following procedure summarizes the general steps for enumerating stream sinks in the ASF file sink.</span></span>

<span data-ttu-id="9b36d-148">**Per enumerare i sink di flusso**</span><span class="sxs-lookup"><span data-stu-id="9b36d-148">**To enumerate stream sinks**</span></span>

1.  <span data-ttu-id="9b36d-149">Chiamare [**IMFMediaSink:: GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) per ottenere il numero totale di sink di flusso nel sink di file ASF.</span><span class="sxs-lookup"><span data-stu-id="9b36d-149">Call [**IMFMediaSink::GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) to get the total number of stream sinks in the ASF file sink.</span></span>
2.  <span data-ttu-id="9b36d-150">Loop through the Stream sinks ang ottenere un riferimento all'interfaccia [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) del sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="9b36d-150">Loop through the stream sinks ang get a reference to the stream sink's [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) interface.</span></span>

    <span data-ttu-id="9b36d-151">-oppure-</span><span class="sxs-lookup"><span data-stu-id="9b36d-151">-or-</span></span>

    <span data-ttu-id="9b36d-152">Chiamare [**IMFMediaSink:: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) per ottenere il sink del flusso specificando il numero del flusso.</span><span class="sxs-lookup"><span data-stu-id="9b36d-152">Call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) to get the stream sink by specifying the stream number.</span></span> <span data-ttu-id="9b36d-153">Ogni sink di flusso viene identificato con il numero di flusso impostato durante la creazione del flusso nel profilo.</span><span class="sxs-lookup"><span data-stu-id="9b36d-153">Each stream sink is identified with the stream number you set while creating the stream in the profile.</span></span>

<span data-ttu-id="9b36d-154">Se si compila una topologia parziale per la codifica di un file multimediale, è necessario aggiungere il sink di file alla topologia come nodo della topologia di output.</span><span class="sxs-lookup"><span data-stu-id="9b36d-154">If you are building a partial topology for encoding a media file, you must add the file sink to the topology as an output topology node.</span></span> <span data-ttu-id="9b36d-155">Questa operazione può essere eseguita specificando ogni sink di vapore nel sink di file o impostando l'oggetto di attivazione del sink di file e gli identificatori di sink del flusso.</span><span class="sxs-lookup"><span data-stu-id="9b36d-155">You can do so either by specifying each steam sink in the file sink or by setting the file sink activation object and the stream sink identifiers.</span></span> <span data-ttu-id="9b36d-156">Per ulteriori informazioni ed esempi di codice, vedere [creazione di nodi di output](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="9b36d-156">For more information and code example, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b36d-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b36d-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b36d-158">Sink di supporti ASF</span><span class="sxs-lookup"><span data-stu-id="9b36d-158">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="9b36d-159">Supporto ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9b36d-159">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



