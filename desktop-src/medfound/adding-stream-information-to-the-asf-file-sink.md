---
description: Informazioni sull'aggiunta di informazioni di flusso al sink di file ASF, che un'applicazione può usare per archiviare i dati multimediali asf in un file.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Aggiunta di informazioni sul flusso al sink di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8202de8da5cb8e17534c334e3d39dddb3c4f99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404359"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a><span data-ttu-id="9d637-103">Aggiunta di informazioni sul flusso al sink di file ASF</span><span class="sxs-lookup"><span data-stu-id="9d637-103">Adding Stream Information to the ASF File Sink</span></span>

<span data-ttu-id="9d637-104">Il sink di file ASF è un'implementazione di [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornita da Media Foundation che un'applicazione può usare per archiviare i dati multimediali asf in un file.</span><span class="sxs-lookup"><span data-stu-id="9d637-104">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="9d637-105">Per informazioni sul modello a oggetti di ASF Media Sinks e sull'utilizzo generale, vedere [ASF Media Sinks](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="9d637-105">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="9d637-106">Dopo la creazione di un'istanza del sink di file, è necessario configurarlo prima di compilare la topologia.</span><span class="sxs-lookup"><span data-stu-id="9d637-106">After instantiating the file sink, it must be configured before building the topology.</span></span> <span data-ttu-id="9d637-107">Il sink di file deve conoscere i flussi nel file di output, le informazioni sulla modalità di codifica e i metadati.</span><span class="sxs-lookup"><span data-stu-id="9d637-107">The file sink needs to know about the streams in the output file, the encoding mode information, and the metadata.</span></span> <span data-ttu-id="9d637-108">Questo argomento descrive il processo di aggiunta del flusso nel sink di file.</span><span class="sxs-lookup"><span data-stu-id="9d637-108">This topic describes the process of adding stream in the file sink.</span></span>

-   [<span data-ttu-id="9d637-109">Aggiunta di flussi nel sink di file ASF</span><span class="sxs-lookup"><span data-stu-id="9d637-109">Adding Streams in the ASF File Sink</span></span>](#adding-streams-in-the-asf-file-sink)
-   [<span data-ttu-id="9d637-110">Enumerazione dei sink di flusso</span><span class="sxs-lookup"><span data-stu-id="9d637-110">Enumerating Stream Sinks</span></span>](#enumerating-stream-sinks)
-   [<span data-ttu-id="9d637-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d637-111">Related topics</span></span>](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a><span data-ttu-id="9d637-112">Aggiunta di flussi nel sink di file ASF</span><span class="sxs-lookup"><span data-stu-id="9d637-112">Adding Streams in the ASF File Sink</span></span>

<span data-ttu-id="9d637-113">Il sink di file deve conoscere i flussi di output e le relative proprietà in modo che possa generare di conseguenza gli esempi di output e aggiungerli al file ASF di output.</span><span class="sxs-lookup"><span data-stu-id="9d637-113">The file sink must know of the output streams and their properties so that it can generate output samples accordingly and add them to the output ASF file.</span></span> <span data-ttu-id="9d637-114">Queste impostazioni vengono scritte nell'oggetto intestazione ASF finale.</span><span class="sxs-lookup"><span data-stu-id="9d637-114">These settings are written to the final ASF Header Object.</span></span>

<span data-ttu-id="9d637-115">Per impostare le informazioni sul flusso, è necessario avere un riferimento all'oggetto ContentInfo ASF del sink di file.</span><span class="sxs-lookup"><span data-stu-id="9d637-115">To set stream information, you must have a reference to the file sink's ASF ContentInfo object.</span></span> <span data-ttu-id="9d637-116">Per informazioni, vedere [Creazione del sink di file ASF.](creating-the-asf-file-sink.md)</span><span class="sxs-lookup"><span data-stu-id="9d637-116">For information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="9d637-117">La procedura seguente riepiloga i passaggi generali per la configurazione del flusso usando l'oggetto profilo ASF.</span><span class="sxs-lookup"><span data-stu-id="9d637-117">The following procedure summarizes the general steps for configuring stream by using the ASF profile object.</span></span>

<span data-ttu-id="9d637-118">**Per configurare le informazioni sul flusso nel sink di file ASF**</span><span class="sxs-lookup"><span data-stu-id="9d637-118">**To configure stream information in the ASF file sink**</span></span>

1.  <span data-ttu-id="9d637-119">Creare un oggetto profilo ASF chiamando [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span><span class="sxs-lookup"><span data-stu-id="9d637-119">Create an ASF profile object by calling [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span></span>
2.  <span data-ttu-id="9d637-120">Per ogni flusso nel file di output, creare un tipo di supporto per il flusso di destinazione da aggiungere nel sink di file.</span><span class="sxs-lookup"><span data-stu-id="9d637-120">For each stream in the output file, create a media type for the target stream to be added in the file sink.</span></span> <span data-ttu-id="9d637-121">Il tipo di supporto deve essere compatibile con i tipi di output supportati dai codificatori di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9d637-121">The media type must be compatible with the output types supported by the Windows Media encoders.</span></span>

    <span data-ttu-id="9d637-122">Per informazioni sull'aggiunta di flussi audio al profilo, vedere Creazione di flussi audio per la codifica ASF.</span><span class="sxs-lookup"><span data-stu-id="9d637-122">For information about adding audio streams to the profile, see Creating Audio Streams for ASF Encoding.</span></span>

    <span data-ttu-id="9d637-123">Per informazioni sull'aggiunta di flussi video al profilo, vedere Creazione di flussi video per la codifica ASF.</span><span class="sxs-lookup"><span data-stu-id="9d637-123">For information about adding video streams to the profile, see Creating Video Streams for ASF Encoding.</span></span>

3.  <span data-ttu-id="9d637-124">Creare flussi basati sui tipi di supporti creati nel passaggio 2 chiamando [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span><span class="sxs-lookup"><span data-stu-id="9d637-124">Create streams based on the media types created in step 2 by calling [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span></span>
4.  <span data-ttu-id="9d637-125">Assegnare un numero di flusso per il flusso appena creato chiamando il puntatore a interfaccia [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) ricevuto nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="9d637-125">Assign a stream number for the newly created stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface pointer received in step 3.</span></span>
5.  <span data-ttu-id="9d637-126">Facoltativamente, configurare il flusso con le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9d637-126">Optionally configure the stream with the following information:</span></span>
    -   <span data-ttu-id="9d637-127">Parametri bucket persi impostando gli [**attributi: MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) o [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="9d637-127">Leaky bucket parameters by setting the attributes: [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) or [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span></span>
    -   <span data-ttu-id="9d637-128">Estensione del payload, esclusione reciproca chiamando i [**metodi IMFASFStreamConfig.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)</span><span class="sxs-lookup"><span data-stu-id="9d637-128">Payload extension, mutual exclusion by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods.</span></span>
6.  <span data-ttu-id="9d637-129">Facoltativamente, impostare le dimensioni del pacchetto di dati per il profilo impostando gli attributi [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) e [**MF \_ ASFPROFILE \_ MAXPACKETSIZE.**](mf-asfprofile-maxpacketsize-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="9d637-129">Optionally set data packet size for the profile by setting [**MF\_ASFPROFILE\_MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) and [**MF\_ASFPROFILE\_MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) attributes.</span></span> <span data-ttu-id="9d637-130">Il profilo ASF espone [**l'interfaccia IMFAttributes,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) a cui un'applicazione può ottenere riferimento chiamando **IMFASFProfile::QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="9d637-130">The ASF profile exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, which an application can get reference to by calling **IMFASFProfile::QueryInterface**.</span></span>
7.  <span data-ttu-id="9d637-131">Impostare le informazioni di codifica per il flusso nel sink di file.</span><span class="sxs-lookup"><span data-stu-id="9d637-131">Set encoding information for the stream in the file sink.</span></span> <span data-ttu-id="9d637-132">Descritto in [Impostazione delle proprietà nel sink di file](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="9d637-132">Discussed in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
8.  <span data-ttu-id="9d637-133">Aggiungere il flusso al profilo chiamando [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span><span class="sxs-lookup"><span data-stu-id="9d637-133">Add the stream to the profile by calling [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span></span>
9.  <span data-ttu-id="9d637-134">Associare il profilo all'oggetto ContentInfo chiamando [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span><span class="sxs-lookup"><span data-stu-id="9d637-134">Associate the profile with the ContentInfo object by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span>

<span data-ttu-id="9d637-135">Per modificare un flusso esistente, l'applicazione può ottenere un riferimento [**all'interfaccia IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) del flusso e riconfigurarla in base ai requisiti.</span><span class="sxs-lookup"><span data-stu-id="9d637-135">To modify an existing stream, the application can get a reference to the stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface and reconfigure it according to the requirements.</span></span> <span data-ttu-id="9d637-136">Per aggiungere o rimuovere flussi, l'applicazione deve chiamare [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span><span class="sxs-lookup"><span data-stu-id="9d637-136">To add or remove streams, the application must call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span></span> <span data-ttu-id="9d637-137">Per applicare queste modifiche, apportare modifiche al flusso o rimuovere il flusso, è necessario impostare nuovamente il profilo nell'oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="9d637-137">To apply these changes, stream modifications or removal, you must set the profile again in the ContentInfo object.</span></span> <span data-ttu-id="9d637-138">Verrà sovrascritto il profilo esistente già associato all'oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="9d637-138">This overwrites the existing profile that is already associated with the ContentInfo object.</span></span>


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



## <a name="enumerating-stream-sinks"></a><span data-ttu-id="9d637-139">Enumerazione dei sink di flusso</span><span class="sxs-lookup"><span data-stu-id="9d637-139">Enumerating Stream Sinks</span></span>

<span data-ttu-id="9d637-140">Per ogni flusso nel profilo di cui l'oggetto ContentInfo è a conoscenza, il sink di file ASF crea e aggiunge un sink di flusso che contiene tutte le proprietà del flusso codificato.</span><span class="sxs-lookup"><span data-stu-id="9d637-140">For each stream in the profile that the ContentInfo object is aware of, the ASF file sink creates and adds a stream sink that contains all the properties of the encoded stream.</span></span> <span data-ttu-id="9d637-141">Il sink di file ASF è progettato per contenere flussi fissi.</span><span class="sxs-lookup"><span data-stu-id="9d637-141">The ASF file sink is designed to contain fixed streams.</span></span> <span data-ttu-id="9d637-142">Ciò significa che non è possibile aggiungere o rimuovere flussi chiamando [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) o [**IMFMediaSink::RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span><span class="sxs-lookup"><span data-stu-id="9d637-142">This means that you cannot add or remove streams by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) or [**IMFMediaSink::RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span></span> <span data-ttu-id="9d637-143">Queste chiamate sul sink di file hanno esito negativo con il codice di errore MF \_ E \_ STREAMSINKS \_ FIXED.</span><span class="sxs-lookup"><span data-stu-id="9d637-143">These calls on the file sink fail with the MF\_E\_STREAMSINKS\_FIXED error code.</span></span> <span data-ttu-id="9d637-144">L'aggiunta o la rimozione di flussi nel profilo non aggiunge o rimuove automaticamente i sink di flusso nel sink di file.</span><span class="sxs-lookup"><span data-stu-id="9d637-144">Adding or removing streams in the profile does not automatically add or remove the stream sinks in the file sink.</span></span> <span data-ttu-id="9d637-145">È necessario rimuovere l'istanza esistente del file e ricrearla con nuove informazioni sul flusso se i flussi nel profilo sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="9d637-145">You must discard the existing instance of the file and recreate it with new stream information if your streams in the profile have changed.</span></span>

<span data-ttu-id="9d637-146">La procedura seguente riepiloga i passaggi generali per l'enumerazione dei sink di flusso nel sink di file ASF.</span><span class="sxs-lookup"><span data-stu-id="9d637-146">The following procedure summarizes the general steps for enumerating stream sinks in the ASF file sink.</span></span>

<span data-ttu-id="9d637-147">**Per enumerare i sink di flusso**</span><span class="sxs-lookup"><span data-stu-id="9d637-147">**To enumerate stream sinks**</span></span>

1.  <span data-ttu-id="9d637-148">Chiamare [**IMFMediaSink::GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) per ottenere il numero totale di sink di flusso nel sink di file ASF.</span><span class="sxs-lookup"><span data-stu-id="9d637-148">Call [**IMFMediaSink::GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) to get the total number of stream sinks in the ASF file sink.</span></span>
2.  <span data-ttu-id="9d637-149">Scorrere i sink di flusso ang ottenere un riferimento [**all'interfaccia GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) del sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="9d637-149">Loop through the stream sinks ang get a reference to the stream sink's [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) interface.</span></span>

    <span data-ttu-id="9d637-150">-oppure-</span><span class="sxs-lookup"><span data-stu-id="9d637-150">-or-</span></span>

    <span data-ttu-id="9d637-151">Chiamare [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) per ottenere il sink di flusso specificando il numero di flusso.</span><span class="sxs-lookup"><span data-stu-id="9d637-151">Call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) to get the stream sink by specifying the stream number.</span></span> <span data-ttu-id="9d637-152">Ogni sink di flusso viene identificato con il numero di flusso impostato durante la creazione del flusso nel profilo.</span><span class="sxs-lookup"><span data-stu-id="9d637-152">Each stream sink is identified with the stream number you set while creating the stream in the profile.</span></span>

<span data-ttu-id="9d637-153">Se si sta creando una topologia parziale per la codifica di un file multimediale, è necessario aggiungere il sink di file alla topologia come nodo della topologia di output.</span><span class="sxs-lookup"><span data-stu-id="9d637-153">If you are building a partial topology for encoding a media file, you must add the file sink to the topology as an output topology node.</span></span> <span data-ttu-id="9d637-154">A tale scopo, è possibile specificare ogni sink di flusso nel sink di file o impostando l'oggetto di attivazione del sink di file e gli identificatori del sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="9d637-154">You can do so either by specifying each steam sink in the file sink or by setting the file sink activation object and the stream sink identifiers.</span></span> <span data-ttu-id="9d637-155">Per altre informazioni ed esempio di codice, vedere [Creazione di nodi di output](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="9d637-155">For more information and code example, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d637-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d637-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d637-157">Sink di supporti ASF</span><span class="sxs-lookup"><span data-stu-id="9d637-157">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="9d637-158">Supporto di ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9d637-158">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



