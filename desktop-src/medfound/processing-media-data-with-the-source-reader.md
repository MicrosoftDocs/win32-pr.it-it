---
description: In questo argomento viene descritto come utilizzare il lettore di origine per elaborare i dati multimediali.
ms.assetid: 583f5736-f767-47c5-8fdc-b3645aed59f6
title: Utilizzo del lettore di origine per l'elaborazione dei dati multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b19bce4d83298693825037aef92a220d78ed7c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351181"
---
# <a name="using-the-source-reader-to-process-media-data"></a><span data-ttu-id="2545d-103">Utilizzo del lettore di origine per l'elaborazione dei dati multimediali</span><span class="sxs-lookup"><span data-stu-id="2545d-103">Using the Source Reader to Process Media Data</span></span>

<span data-ttu-id="2545d-104">In questo argomento viene descritto come utilizzare il [lettore di origine](source-reader.md) per elaborare i dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="2545d-104">This topic describes how to use the [Source Reader](source-reader.md) to process media data.</span></span>

<span data-ttu-id="2545d-105">Per usare il lettore di origine, seguire questa procedura di base:</span><span class="sxs-lookup"><span data-stu-id="2545d-105">To use the Source Reader, follow these basic steps:</span></span>

1.  <span data-ttu-id="2545d-106">Creare un'istanza del lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="2545d-106">Create an instance of the Source Reader.</span></span>
2.  <span data-ttu-id="2545d-107">Enumerare i formati di output possibili.</span><span class="sxs-lookup"><span data-stu-id="2545d-107">Enumerate the possible output formats.</span></span>
3.  <span data-ttu-id="2545d-108">Imposta il formato di output effettivo per ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="2545d-108">Set the actual output format for each stream.</span></span>
4.  <span data-ttu-id="2545d-109">Elaborare i dati dall'origine.</span><span class="sxs-lookup"><span data-stu-id="2545d-109">Process data from the source.</span></span>

<span data-ttu-id="2545d-110">Nella parte restante di questo argomento vengono descritti in dettaglio questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="2545d-110">The remainder of this topic describes these steps in detail.</span></span>

-   [<span data-ttu-id="2545d-111">Creazione del lettore di origine</span><span class="sxs-lookup"><span data-stu-id="2545d-111">Creating the Source Reader</span></span>](#creating-the-source-reader)
-   [<span data-ttu-id="2545d-112">Enumerazione dei formati di output</span><span class="sxs-lookup"><span data-stu-id="2545d-112">Enumerating Output Formats</span></span>](#enumerating-output-formats)
-   [<span data-ttu-id="2545d-113">Impostazione di formati di output</span><span class="sxs-lookup"><span data-stu-id="2545d-113">Setting Output Formats</span></span>](#setting-output-formats)
-   [<span data-ttu-id="2545d-114">Elaborazione dei dati multimediali</span><span class="sxs-lookup"><span data-stu-id="2545d-114">Processing Media Data</span></span>](#using-the-source-reader-to-process-media-data)
-   [<span data-ttu-id="2545d-115">Svuotamento della pipeline di dati</span><span class="sxs-lookup"><span data-stu-id="2545d-115">Draining the Data Pipeline</span></span>](#draining-the-data-pipeline)
-   [<span data-ttu-id="2545d-116">Recupero della durata del file</span><span class="sxs-lookup"><span data-stu-id="2545d-116">Getting the File Duration</span></span>](#getting-the-file-duration)
-   [<span data-ttu-id="2545d-117">La ricerca</span><span class="sxs-lookup"><span data-stu-id="2545d-117">Seeking</span></span>](#seeking)
-   [<span data-ttu-id="2545d-118">Velocità di riproduzione</span><span class="sxs-lookup"><span data-stu-id="2545d-118">Playback Rate</span></span>](#playback-rate)
-   [<span data-ttu-id="2545d-119">Accelerazione hardware</span><span class="sxs-lookup"><span data-stu-id="2545d-119">Hardware Acceleration</span></span>](#hardware-acceleration)
-   [<span data-ttu-id="2545d-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2545d-120">Related topics</span></span>](#related-topics)

## <a name="creating-the-source-reader"></a><span data-ttu-id="2545d-121">Creazione del lettore di origine</span><span class="sxs-lookup"><span data-stu-id="2545d-121">Creating the Source Reader</span></span>

<span data-ttu-id="2545d-122">Per creare un'istanza del lettore di origine, chiamare una delle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2545d-122">To create an instance of the Source Reader, call one of the following functions:</span></span>



| <span data-ttu-id="2545d-123">Funzione</span><span class="sxs-lookup"><span data-stu-id="2545d-123">Function</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="2545d-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2545d-124">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2545d-125"><span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)</span><span class="sxs-lookup"><span data-stu-id="2545d-125"><span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)</span></span><br/>                                         | <span data-ttu-id="2545d-126">Accetta un URL come input.</span><span class="sxs-lookup"><span data-stu-id="2545d-126">Takes a URL as input.</span></span> <span data-ttu-id="2545d-127">Questa funzione usa il [resolver di origine](source-resolver.md) per creare un'origine multimediale dall'URL.</span><span class="sxs-lookup"><span data-stu-id="2545d-127">This function uses the [Source Resolver](source-resolver.md) to create a media source from the URL.</span></span><br/>                                                                       |
| <span data-ttu-id="2545d-128"><span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)</span><span class="sxs-lookup"><span data-stu-id="2545d-128"><span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)</span></span><br/>      | <span data-ttu-id="2545d-129">Accetta un puntatore a un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="2545d-129">Takes a pointer to a byte stream.</span></span> <span data-ttu-id="2545d-130">Questa funzione usa anche il resolver di origine per creare l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="2545d-130">This function also uses the Source Resolver to create the media source.</span></span><br/>                                                                                        |
| <span data-ttu-id="2545d-131"><span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)</span><span class="sxs-lookup"><span data-stu-id="2545d-131"><span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)</span></span><br/> | <span data-ttu-id="2545d-132">Accetta un puntatore a un'origine multimediale che è già stata creata.</span><span class="sxs-lookup"><span data-stu-id="2545d-132">Takes a pointer to a media source that has already been created.</span></span> <span data-ttu-id="2545d-133">Questa funzione è utile per le origini multimediali che il resolver di origine non è in grado di creare, ad esempio dispositivi di acquisizione o origini multimediali personalizzate.</span><span class="sxs-lookup"><span data-stu-id="2545d-133">This function is useful for media sources that the Source Resolver cannot create, such capture devices or custom media sources.</span></span><br/> |



 

<span data-ttu-id="2545d-134">In genere, per i file multimediali, usare [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl).</span><span class="sxs-lookup"><span data-stu-id="2545d-134">Typically, for media files, use [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl).</span></span> <span data-ttu-id="2545d-135">Per i dispositivi, ad esempio le webcam, usare [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource).</span><span class="sxs-lookup"><span data-stu-id="2545d-135">For devices, such as webcams, use [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource).</span></span> <span data-ttu-id="2545d-136">Per ulteriori informazioni sui dispositivi di acquisizione in Microsoft Media Foundation, vedere [acquisizione audio/video](audio-video-capture.md).</span><span class="sxs-lookup"><span data-stu-id="2545d-136">(For more information about capture devices in Microsoft Media Foundation, see [Audio/Video Capture](audio-video-capture.md).)</span></span>

<span data-ttu-id="2545d-137">Ognuna di queste funzioni accetta un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) facoltativo, che viene usato per impostare diverse opzioni nel lettore di origine, come descritto negli argomenti di riferimento per queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="2545d-137">Each of these functions takes an optional [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer, which is used to set various options on the Source Reader, as described in the reference topics for these functions.</span></span> <span data-ttu-id="2545d-138">Per ottenere il comportamento predefinito, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="2545d-138">To get the default behavior, set this parameter to **NULL**.</span></span> <span data-ttu-id="2545d-139">Ogni funzione restituisce un puntatore [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="2545d-139">Each function returns an [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) pointer as an output parameter.</span></span> <span data-ttu-id="2545d-140">Prima di chiamare una di queste funzioni, è necessario chiamare la funzione **CoInitialize (ex)** e [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) .</span><span class="sxs-lookup"><span data-stu-id="2545d-140">You must call **CoInitialize(Ex)** and [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function before calling any of these functions.</span></span>

<span data-ttu-id="2545d-141">Il codice seguente crea il lettore di origine da un URL.</span><span class="sxs-lookup"><span data-stu-id="2545d-141">The following code creates the Source Reader from a URL.</span></span>


```C++
int __cdecl wmain(int argc, __in_ecount(argc) PCWSTR* argv)
{
    if (argc < 2)
    {
        return 1;
    }

    const WCHAR *pszURL = argv[1];

    // Initialize the COM runtime.
    HRESULT hr = CoInitializeEx(0, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        // Initialize the Media Foundation platform.
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            // Create the source reader.
            IMFSourceReader *pReader;
            hr = MFCreateSourceReaderFromURL(pszURL, NULL, &pReader);
            if (SUCCEEDED(hr))
            {
                ReadMediaFile(pReader);
                pReader->Release();
            }
            // Shut down Media Foundation.
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="enumerating-output-formats"></a><span data-ttu-id="2545d-142">Enumerazione dei formati di output</span><span class="sxs-lookup"><span data-stu-id="2545d-142">Enumerating Output Formats</span></span>

<span data-ttu-id="2545d-143">Ogni origine multimediale ha almeno un flusso.</span><span class="sxs-lookup"><span data-stu-id="2545d-143">Every media source has at least one stream.</span></span> <span data-ttu-id="2545d-144">Ad esempio, un file video può contenere un flusso video e un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="2545d-144">For example, a video file might contain a video stream and an audio stream.</span></span> <span data-ttu-id="2545d-145">Il formato di ogni flusso viene descritto usando un tipo di supporto, rappresentato dall'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="2545d-145">The format of each stream is described using a media type, represented by the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="2545d-146">Per ulteriori informazioni sui tipi di supporto, vedere [tipi di supporti](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="2545d-146">For more information about media types, see [Media Types](media-types.md).</span></span> <span data-ttu-id="2545d-147">È necessario esaminare il tipo di supporto per comprendere il formato dei dati che si ottengono dal lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="2545d-147">You must examine the media type to understand the format of the data that you get from the Source Reader.</span></span>

<span data-ttu-id="2545d-148">Inizialmente, ogni flusso ha un formato predefinito, che è possibile trovare chiamando il metodo [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) :</span><span class="sxs-lookup"><span data-stu-id="2545d-148">Initially, every stream has a default format, which you can find by calling the [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) method:</span></span>

<span data-ttu-id="2545d-149">Per ogni flusso, l'origine multimediale offre un elenco di tipi di supporti possibili per quel flusso.</span><span class="sxs-lookup"><span data-stu-id="2545d-149">For each stream, the media source offers a list of possible media types for that stream.</span></span> <span data-ttu-id="2545d-150">Il numero di tipi dipende dall'origine.</span><span class="sxs-lookup"><span data-stu-id="2545d-150">The number of types depends on the source.</span></span> <span data-ttu-id="2545d-151">Se l'origine rappresenta un file multimediale, in genere è presente un solo tipo per ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="2545d-151">If the source represents a media file, there is typically only one type per stream.</span></span> <span data-ttu-id="2545d-152">Una webcam, d'altra parte, potrebbe essere in grado di trasmettere video in formati diversi.</span><span class="sxs-lookup"><span data-stu-id="2545d-152">A webcam, on the other hand, might be able to stream video in several different formats.</span></span> <span data-ttu-id="2545d-153">In tal caso, l'applicazione può selezionare il formato da usare dall'elenco dei tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="2545d-153">In that case, the application can select which format to use from the list of media types.</span></span>

<span data-ttu-id="2545d-154">Per ottenere uno dei tipi di supporto per un flusso, chiamare il metodo [**IMFSourceReader:: GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) .</span><span class="sxs-lookup"><span data-stu-id="2545d-154">To get one of the media types for a stream, call the [**IMFSourceReader::GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) method.</span></span> <span data-ttu-id="2545d-155">Questo metodo accetta due parametri di indice, ovvero l'indice del flusso e un indice nell'elenco dei tipi di supporto per il flusso.</span><span class="sxs-lookup"><span data-stu-id="2545d-155">This method takes two index parameters: The index of the stream, and an index into the list of media types for the stream.</span></span> <span data-ttu-id="2545d-156">Per enumerare tutti i tipi per un flusso, incrementare l'indice dell'elenco mantenendo la costante dell'indice del flusso.</span><span class="sxs-lookup"><span data-stu-id="2545d-156">To enumerate all the types for a stream, increment the list index while keeping the stream index constant.</span></span> <span data-ttu-id="2545d-157">Quando l'indice dell'elenco non rientra nei limiti, **GetNativeMediaType** restituisce **MF \_ E \_ non \_ più \_ tipi**.</span><span class="sxs-lookup"><span data-stu-id="2545d-157">When the list index goes out of bounds, **GetNativeMediaType** returns **MF\_E\_NO\_MORE\_TYPES**.</span></span>


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



<span data-ttu-id="2545d-158">Per enumerare i tipi di supporto per ogni flusso, incrementare l'indice del flusso.</span><span class="sxs-lookup"><span data-stu-id="2545d-158">To enumerate the media types for every stream, increment the stream index.</span></span> <span data-ttu-id="2545d-159">Quando l'indice del flusso non rientra nei limiti, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) restituisce **MF \_ E \_ INVALIDSTREAMNUMBER**.</span><span class="sxs-lookup"><span data-stu-id="2545d-159">When the stream index goes out of bounds, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) returns **MF\_E\_INVALIDSTREAMNUMBER**.</span></span>


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



## <a name="setting-output-formats"></a><span data-ttu-id="2545d-160">Impostazione di formati di output</span><span class="sxs-lookup"><span data-stu-id="2545d-160">Setting Output Formats</span></span>

<span data-ttu-id="2545d-161">Per modificare il formato di output, chiamare il metodo [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) .</span><span class="sxs-lookup"><span data-stu-id="2545d-161">To change the output format, call the [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) method.</span></span> <span data-ttu-id="2545d-162">Questo metodo accetta l'indice del flusso e un tipo di supporto:</span><span class="sxs-lookup"><span data-stu-id="2545d-162">This method takes the stream index and a media type:</span></span>

``` syntax
hr = pReader->SetCurrentMediaType(dwStreamIndex, pMediaType);
```

<span data-ttu-id="2545d-163">Per il tipo di supporto, dipende dal fatto che si desideri inserire un decodificatore.</span><span class="sxs-lookup"><span data-stu-id="2545d-163">For the media type, it depends on whether you want to insert a decoder.</span></span>

-   <span data-ttu-id="2545d-164">Per ottenere i dati direttamente dall'origine senza decodificarli, usare uno dei tipi restituiti da [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).</span><span class="sxs-lookup"><span data-stu-id="2545d-164">To get data directly from the source without decoding it, use one of the types returned by [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).</span></span>
-   <span data-ttu-id="2545d-165">Per decodificare il flusso, creare un nuovo tipo di supporto che descriva il formato non compresso desiderato.</span><span class="sxs-lookup"><span data-stu-id="2545d-165">To decode the stream, create a new media type that describes the desired uncompressed format.</span></span>

<span data-ttu-id="2545d-166">Nel caso del decodificatore, creare il tipo di supporto come segue:</span><span class="sxs-lookup"><span data-stu-id="2545d-166">In the case of the decoder, create the media type as follows:</span></span>

1.  <span data-ttu-id="2545d-167">Chiamare [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) per creare un nuovo tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="2545d-167">Call [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) to create a new media type.</span></span>
2.  <span data-ttu-id="2545d-168">Impostare l'attributo di [**\_ \_ \_ tipo principale MF mt**](mf-mt-major-type-attribute.md) per specificare audio o video.</span><span class="sxs-lookup"><span data-stu-id="2545d-168">Set the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute to specify audio or video.</span></span>
3.  <span data-ttu-id="2545d-169">Impostare l'attributo del [**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md) per specificare il sottotipo del formato di decodifica.</span><span class="sxs-lookup"><span data-stu-id="2545d-169">Set the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute to specify the subtype of the decoding format.</span></span> <span data-ttu-id="2545d-170">(Vedere [GUID del sottotipo audio](audio-subtype-guids.md) e [GUID del sottotipo video](video-subtype-guids.md)).</span><span class="sxs-lookup"><span data-stu-id="2545d-170">(See [Audio Subtype GUIDs](audio-subtype-guids.md) and [Video Subtype GUIDs](video-subtype-guids.md).)</span></span>
4.  <span data-ttu-id="2545d-171">Chiamare [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="2545d-171">Call [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span></span>

<span data-ttu-id="2545d-172">Il lettore di origine caricherà automaticamente il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="2545d-172">The Source Reader will automatically load the decoder.</span></span> <span data-ttu-id="2545d-173">Per ottenere i dettagli completi del formato decodificato, chiamare [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) dopo la chiamata a [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)</span><span class="sxs-lookup"><span data-stu-id="2545d-173">To get the complete details of the decoded format, call [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) after the call to [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)</span></span>

<span data-ttu-id="2545d-174">Il codice seguente configura il flusso video per RGB-32 e il flusso audio per l'audio PCM.</span><span class="sxs-lookup"><span data-stu-id="2545d-174">The following code configures the video stream for RGB-32 and the audio stream for PCM audio.</span></span>


```C++
HRESULT ConfigureDecoder(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    IMFMediaType *pNativeType = NULL;
    IMFMediaType *pType = NULL;

    // Find the native format of the stream.
    HRESULT hr = pReader->GetNativeMediaType(dwStreamIndex, 0, &pNativeType);
    if (FAILED(hr))
    {
        return hr;
    }

    GUID majorType, subtype;

    // Find the major type.
    hr = pNativeType->GetGUID(MF_MT_MAJOR_TYPE, &majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Define the output type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Select a subtype.
    if (majorType == MFMediaType_Video)
    {
        subtype= MFVideoFormat_RGB32;
    }
    else if (majorType == MFMediaType_Audio)
    {
        subtype = MFAudioFormat_PCM;
    }
    else
    {
        // Unrecognized type. Skip.
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the uncompressed format.
    hr = pReader->SetCurrentMediaType(dwStreamIndex, NULL, pType);
    if (FAILED(hr))
    {
        goto done;
    }

done:
    SafeRelease(&pNativeType);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="processing-media-data"></a><span data-ttu-id="2545d-175">Elaborazione dei dati multimediali</span><span class="sxs-lookup"><span data-stu-id="2545d-175">Processing Media Data</span></span>

<span data-ttu-id="2545d-176">Per ottenere i dati multimediali dall'origine, chiamare il metodo [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="2545d-176">To get media data from the source, call the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method, as shown in the following code.</span></span>


```C++
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );
```



<span data-ttu-id="2545d-177">Il primo parametro è l'indice del flusso per il quale si desidera ottenere i dati.</span><span class="sxs-lookup"><span data-stu-id="2545d-177">The first parameter is the index of the stream for which you want to get data.</span></span> <span data-ttu-id="2545d-178">È anche possibile specificare **MF \_ source \_ Reader \_ Any \_ Stream** per ottenere i dati disponibili successivi da qualsiasi flusso.</span><span class="sxs-lookup"><span data-stu-id="2545d-178">You can also specify **MF\_SOURCE\_READER\_ANY\_STREAM** to get the next available data from any stream.</span></span> <span data-ttu-id="2545d-179">Il secondo parametro contiene flag facoltativi. per un elenco di questi, vedere il [**flag di controllo del \_ lettore di origine \_ \_ \_ MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) .</span><span class="sxs-lookup"><span data-stu-id="2545d-179">The second parameter contains optional flags; see [**MF\_SOURCE\_READER\_CONTROL\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) for a list of these.</span></span> <span data-ttu-id="2545d-180">Il terzo parametro riceve l'indice del flusso che produce effettivamente i dati.</span><span class="sxs-lookup"><span data-stu-id="2545d-180">The third parameter receives the index of the stream that actually produces the data.</span></span> <span data-ttu-id="2545d-181">Queste informazioni sono necessarie se si imposta il primo parametro su **MF \_ source \_ Reader \_ Any \_ Stream**.</span><span class="sxs-lookup"><span data-stu-id="2545d-181">You will need this information if you set the first parameter to **MF\_SOURCE\_READER\_ANY\_STREAM**.</span></span> <span data-ttu-id="2545d-182">Il quarto parametro riceve i flag di stato, che indicano vari eventi che possono verificarsi durante la lettura dei dati, ad esempio le modifiche al formato nel flusso.</span><span class="sxs-lookup"><span data-stu-id="2545d-182">The fourth parameter receives status flags, indicating various events that can occur while reading the data, such as format changes in the stream.</span></span> <span data-ttu-id="2545d-183">Per un elenco di flag di stato, [**vedere \_ \_ \_ flag di lettura origine MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).</span><span class="sxs-lookup"><span data-stu-id="2545d-183">For a list of status flags, see [**MF\_SOURCE\_READER\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).</span></span>

<span data-ttu-id="2545d-184">Se l'origine del supporto è in grado di produrre dati per il flusso richiesto, l'ultimo parametro di [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) riceve un puntatore all'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) di un oggetto di esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="2545d-184">If the media source is able to produce data for the requested stream, the last parameter of [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) receives a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface of a media sample object.</span></span> <span data-ttu-id="2545d-185">Usare l'esempio di supporto per:</span><span class="sxs-lookup"><span data-stu-id="2545d-185">Use the media sample to:</span></span>

-   <span data-ttu-id="2545d-186">Ottenere un puntatore ai dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="2545d-186">Get a pointer to the media data.</span></span>
-   <span data-ttu-id="2545d-187">Ottenere l'ora di presentazione e la durata del campione.</span><span class="sxs-lookup"><span data-stu-id="2545d-187">Get the presentation time and sample duration.</span></span>
-   <span data-ttu-id="2545d-188">Ottiene gli attributi che descrivono l'interlacciamento, la dominanza dei campi e altri aspetti dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="2545d-188">Get attributes that describe interlacing, field dominance, and other aspects of the sample.</span></span>

<span data-ttu-id="2545d-189">Il contenuto dei dati multimediali dipende dal formato del flusso.</span><span class="sxs-lookup"><span data-stu-id="2545d-189">The contents of the media data depend on the format of the stream.</span></span> <span data-ttu-id="2545d-190">Per un flusso video non compresso, ogni esempio multimediale contiene un singolo frame video.</span><span class="sxs-lookup"><span data-stu-id="2545d-190">For an uncompressed video stream, each media sample contains a single video frame.</span></span> <span data-ttu-id="2545d-191">Per un flusso audio non compresso, ogni esempio di supporto contiene una sequenza di frame audio.</span><span class="sxs-lookup"><span data-stu-id="2545d-191">For an uncompressed audio stream, each media sample contains a sequence of audio frames.</span></span>

<span data-ttu-id="2545d-192">Il metodo [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) può restituire **S \_ OK** e non restituisce ancora un esempio multimediale nel parametro *pSample* .</span><span class="sxs-lookup"><span data-stu-id="2545d-192">The [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method can return **S\_OK** and yet not return a media sample in the *pSample* parameter.</span></span> <span data-ttu-id="2545d-193">Ad esempio, quando si raggiunge la fine del file, **ReadSample** imposta il flag **MF \_ source \_ READERF \_ ENDOFSTREAM** in *dwFlags* e imposta *pSample* su **null**.</span><span class="sxs-lookup"><span data-stu-id="2545d-193">For example, when you reach the end of the file, **ReadSample** sets the **MF\_SOURCE\_READERF\_ENDOFSTREAM** flag in *dwFlags* and sets *pSample* to **NULL**.</span></span> <span data-ttu-id="2545d-194">In questo caso, il metodo **ReadSample** restituisce **S \_ OK** perché non si è verificato alcun errore, anche se il parametro *pSample* è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="2545d-194">In this case, the **ReadSample** method returns **S\_OK** because no error has occurred, even though the *pSample* parameter is set to **NULL**.</span></span> <span data-ttu-id="2545d-195">Quindi, controllare sempre il valore di *pSample* prima di dereferenziarlo.</span><span class="sxs-lookup"><span data-stu-id="2545d-195">Therefore, always check the value of *pSample* before you dereference it.</span></span>

<span data-ttu-id="2545d-196">Il codice seguente illustra come chiamare [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) in un ciclo e controllare le informazioni restituite dal metodo, fino a quando non viene raggiunta la fine del file multimediale.</span><span class="sxs-lookup"><span data-stu-id="2545d-196">The following code shows how to call [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) in a loop and check the information returned by the method, until the end of the media file is reached.</span></span>


```C++
HRESULT ProcessSamples(IMFSourceReader *pReader)
{
    HRESULT hr = S_OK;
    IMFSample *pSample = NULL;
    size_t  cSamples = 0;

    bool quit = false;
    while (!quit)
    {
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );

        if (FAILED(hr))
        {
            break;
        }

        wprintf(L"Stream %d (%I64d)\n", streamIndex, llTimeStamp);
        if (flags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            wprintf(L"\tEnd of stream\n");
            quit = true;
        }
        if (flags & MF_SOURCE_READERF_NEWSTREAM)
        {
            wprintf(L"\tNew stream\n");
        }
        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            wprintf(L"\tNative type changed\n");
        }
        if (flags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            wprintf(L"\tCurrent type changed\n");
        }
        if (flags & MF_SOURCE_READERF_STREAMTICK)
        {
            wprintf(L"\tStream tick\n");
        }

        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            // The format changed. Reconfigure the decoder.
            hr = ConfigureDecoder(pReader, streamIndex);
            if (FAILED(hr))
            {
                break;
            }
        }

        if (pSample)
        {
            ++cSamples;
        }

        SafeRelease(&pSample);
    }

    if (FAILED(hr))
    {
        wprintf(L"ProcessSamples FAILED, hr = 0x%x\n", hr);
    }
    else
    {
        wprintf(L"Processed %d samples\n", cSamples);
    }
    SafeRelease(&pSample);
    return hr;
}
```



## <a name="draining-the-data-pipeline"></a><span data-ttu-id="2545d-197">Svuotamento della pipeline di dati</span><span class="sxs-lookup"><span data-stu-id="2545d-197">Draining the Data Pipeline</span></span>

<span data-ttu-id="2545d-198">Durante l'elaborazione dei dati, un decodificatore o un'altra trasformazione può memorizzare nel buffer esempi di input.</span><span class="sxs-lookup"><span data-stu-id="2545d-198">During data processing, a decoder or other transform might buffer input samples.</span></span> <span data-ttu-id="2545d-199">Nel diagramma seguente l'applicazione chiama [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) e riceve un campione con un'ora di presentazione uguale a *T1*.</span><span class="sxs-lookup"><span data-stu-id="2545d-199">In the following diagram, the application calls [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) and receives a sample with a presentation time equal to *t1*.</span></span> <span data-ttu-id="2545d-200">Il decodificatore contiene esempi per *T2* e *T3*.</span><span class="sxs-lookup"><span data-stu-id="2545d-200">The decoder is holding samples for *t2* and *t3*.</span></span>

![illustrazione che mostra il buffering in un decodificatore.](images/sourcereader02.png)

<span data-ttu-id="2545d-202">Alla successiva chiamata a [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), il lettore di origine potrebbe assegnare *T4* al decodificatore e restituire *T2* all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2545d-202">On the next call to [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), the Source Reader might give *t4* to the decoder and return *t2* to the application.</span></span>

<span data-ttu-id="2545d-203">Se si desidera decodificare tutti gli esempi attualmente memorizzati nel buffer nel decodificatore, senza passare i nuovi esempi al decodificatore, impostare il flag di **\_ \_ \_ \_ svuotamento CONTROLF di MF source Reader** nel parametro *dwControlFlags* di [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span><span class="sxs-lookup"><span data-stu-id="2545d-203">If you want to decode all of the samples that are currently buffered in the decoder, without passing any new samples to the decoder, set the **MF\_SOURCE\_READER\_CONTROLF\_DRAIN** flag in the *dwControlFlags* parameter of [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span></span> <span data-ttu-id="2545d-204">Continuare a eseguire questa operazione in un ciclo fino a quando **ReadSample** non restituisce un puntatore di esempio **null** .</span><span class="sxs-lookup"><span data-stu-id="2545d-204">Continue to do this in a loop until **ReadSample** returns a **NULL** sample pointer.</span></span> <span data-ttu-id="2545d-205">A seconda del modo in cui il decodificatore memorizza nel buffer gli esempi, questo potrebbe verificarsi immediatamente o dopo diverse chiamate a **ReadSample**.</span><span class="sxs-lookup"><span data-stu-id="2545d-205">Depending on how the decoder buffers samples, that might happen immediately or after several calls to **ReadSample**.</span></span>

## <a name="getting-the-file-duration"></a><span data-ttu-id="2545d-206">Recupero della durata del file</span><span class="sxs-lookup"><span data-stu-id="2545d-206">Getting the File Duration</span></span>

<span data-ttu-id="2545d-207">Per ottenere la durata di un file multimediale, chiamare il metodo [**IMFSourceReader:: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) e richiedere l'attributo [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="2545d-207">To get the duration of a media file, call the [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) method and request the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute, as shown in the following code.</span></span>


```C++
HRESULT GetDuration(IMFSourceReader *pReader, LONGLONG *phnsDuration)
{
    PROPVARIANT var;
    HRESULT hr = pReader->GetPresentationAttribute(MF_SOURCE_READER_MEDIASOURCE, 
        MF_PD_DURATION, &var);
    if (SUCCEEDED(hr))
    {
        hr = PropVariantToInt64(var, phnsDuration);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="2545d-208">La funzione illustrata di seguito consente di ottenere la durata in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="2545d-208">The function shown here gets the duration in 100-nanosecond units.</span></span> <span data-ttu-id="2545d-209">Dividere per 10 milioni per ottenere la durata in secondi.</span><span class="sxs-lookup"><span data-stu-id="2545d-209">Divide by 10,000,000 to get the duration in seconds.</span></span>

## <a name="seeking"></a><span data-ttu-id="2545d-210">La ricerca</span><span class="sxs-lookup"><span data-stu-id="2545d-210">Seeking</span></span>

<span data-ttu-id="2545d-211">Un'origine multimediale che ottiene dati da un file locale può in genere eseguire ricerche in posizioni arbitrarie nel file.</span><span class="sxs-lookup"><span data-stu-id="2545d-211">A media source that gets data from a local file can usually seek to arbitrary positions in the file.</span></span> <span data-ttu-id="2545d-212">I dispositivi di acquisizione, ad esempio le webcam, in genere non possono eseguire ricerche, perché i dati sono Live.</span><span class="sxs-lookup"><span data-stu-id="2545d-212">Capture devices such as webcams generally cannot seek, because the data is live.</span></span> <span data-ttu-id="2545d-213">Un'origine che trasmette i dati in una rete potrebbe essere in grado di eseguire ricerche, a seconda del protocollo di streaming di rete.</span><span class="sxs-lookup"><span data-stu-id="2545d-213">A source that streams data over a network might be able to seek, depending on the network streaming protocol.</span></span>

<span data-ttu-id="2545d-214">Per determinare se un'origine multimediale può eseguire ricerche, chiamare [**IMFSourceReader:: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) e richiedere l'attributo delle [ \_ \_ \_ \_ caratteristiche di lettura origine (MF](mf-source-reader-mediasource-characteristics.md) ), come illustrato nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="2545d-214">To find out whether a media source can seek, call [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) and request the [MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS](mf-source-reader-mediasource-characteristics.md) attribute, as shown in the following code:</span></span>


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



<span data-ttu-id="2545d-215">Questa funzione ottiene un set di flag di funzionalità dall'origine.</span><span class="sxs-lookup"><span data-stu-id="2545d-215">This function gets a set of capabilities flags from the source.</span></span> <span data-ttu-id="2545d-216">Questi flag sono definiti nell'enumerazione [**delle \_ caratteristiche MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="2545d-216">These flags are defined in the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span> <span data-ttu-id="2545d-217">Due flag sono correlati alla ricerca:</span><span class="sxs-lookup"><span data-stu-id="2545d-217">Two flags relate to seeking:</span></span>



| <span data-ttu-id="2545d-218">Flag</span><span class="sxs-lookup"><span data-stu-id="2545d-218">Flag</span></span>                                                                                                                                      | <span data-ttu-id="2545d-219">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2545d-219">Description</span></span>                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2545d-220"><span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE \_ può \_ cercare**</span><span class="sxs-lookup"><span data-stu-id="2545d-220"><span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE\_CAN\_SEEK**</span></span><br/>                 | <span data-ttu-id="2545d-221">L'origine è in grado di cercare.</span><span class="sxs-lookup"><span data-stu-id="2545d-221">The source can seek.</span></span><br/>                                                                                                                                                                            |
| <span data-ttu-id="2545d-222"><span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE \_ con \_ \_ ricerca lenta**</span><span class="sxs-lookup"><span data-stu-id="2545d-222"><span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE\_HAS\_SLOW\_SEEK**</span></span><br/> | <span data-ttu-id="2545d-223">Il completamento della ricerca potrebbe richiedere molto tempo.</span><span class="sxs-lookup"><span data-stu-id="2545d-223">Seeking might take a long time to complete.</span></span> <span data-ttu-id="2545d-224">Ad esempio, l'origine potrebbe dover scaricare l'intero file prima che possa essere cercato.</span><span class="sxs-lookup"><span data-stu-id="2545d-224">For example, the source might need to download the entire file before it can seek.</span></span> <span data-ttu-id="2545d-225">Non esistono criteri severi per l'origine per restituire questo flag.</span><span class="sxs-lookup"><span data-stu-id="2545d-225">(There are no strict criteria for a source to return this flag.)</span></span><br/> |



 

<span data-ttu-id="2545d-226">I test di codice seguenti per **MFMEDIASOURCE \_ possono \_ cercare** flag.</span><span class="sxs-lookup"><span data-stu-id="2545d-226">The following code tests for the **MFMEDIASOURCE\_CAN\_SEEK** flag.</span></span>


```C++
BOOL SourceCanSeek(IMFSourceReader *pReader)
{
    BOOL bCanSeek = FALSE;
    ULONG flags;
    if (SUCCEEDED(GetSourceFlags(pReader, &flags)))
    {
        bCanSeek = ((flags & MFMEDIASOURCE_CAN_SEEK) == MFMEDIASOURCE_CAN_SEEK);
    }
    return bCanSeek;
}
```



<span data-ttu-id="2545d-227">Per eseguire la ricerca, chiamare il metodo [**IMFSourceReader:: SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="2545d-227">To seek, call the [**IMFSourceReader::SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) method, as shown in the following code.</span></span>


```C++
HRESULT SetPosition(IMFSourceReader *pReader, const LONGLONG& hnsPosition)
{
    PROPVARIANT var;
    HRESULT hr = InitPropVariantFromInt64(hnsPosition, &var);
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentPosition(GUID_NULL, var);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="2545d-228">Il primo parametro fornisce il formato di ora utilizzato per specificare la posizione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2545d-228">The first parameter gives the time format that you are using to specify the seek position.</span></span> <span data-ttu-id="2545d-229">Tutte le origini multimediali in Media Foundation sono necessarie per supportare unità 100-nanosecondi, indicate dal valore **\_ null GUID**.</span><span class="sxs-lookup"><span data-stu-id="2545d-229">All media sources in Media Foundation are required to support 100-nanosecond units, indicated by the value **GUID\_NULL**.</span></span> <span data-ttu-id="2545d-230">Il secondo parametro è un **PROPVARIANT** che contiene la posizione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2545d-230">The second parameter is a **PROPVARIANT** that contains the seek position.</span></span> <span data-ttu-id="2545d-231">Per le unità di tempo di 100 nanosecondi, il tipo di dati è **LONGLONG**.</span><span class="sxs-lookup"><span data-stu-id="2545d-231">For 100-nanosecond time units, the data type is **LONGLONG**.</span></span>

<span data-ttu-id="2545d-232">Tenere presente che non tutte le origini supporti forniscono la ricerca con precisione del frame.</span><span class="sxs-lookup"><span data-stu-id="2545d-232">Be aware that not every media source provides frame-accurate seeking.</span></span> <span data-ttu-id="2545d-233">L'accuratezza della ricerca dipende da diversi fattori, ad esempio l'intervallo del fotogramma chiave, se il file multimediale contiene un indice e se i dati hanno una velocità in bit costante o variabile.</span><span class="sxs-lookup"><span data-stu-id="2545d-233">The accuracy of seeking depends on several factors, such as the key frame interval, whether the media file contains an index, and whether the data has a constant or variable bit rate.</span></span> <span data-ttu-id="2545d-234">Pertanto, dopo la ricerca in una posizione in un file, non esiste alcuna garanzia che il timestamp del campione successivo corrisponda esattamente alla posizione richiesta.</span><span class="sxs-lookup"><span data-stu-id="2545d-234">Therefore, after you seek to a position in a file, there is no guarantee that the time stamp on the next sample will exactly match the requested position.</span></span> <span data-ttu-id="2545d-235">In genere, la posizione effettiva non sarà successiva alla posizione richiesta, pertanto è possibile rimuovere gli esempi fino a raggiungere il punto desiderato nel flusso.</span><span class="sxs-lookup"><span data-stu-id="2545d-235">Generally, the actual position will not be later than the requested position, so you can discard samples until you reach the desired point in the stream.</span></span>

## <a name="playback-rate"></a><span data-ttu-id="2545d-236">Velocità di riproduzione</span><span class="sxs-lookup"><span data-stu-id="2545d-236">Playback Rate</span></span>

<span data-ttu-id="2545d-237">Sebbene sia possibile impostare la velocità di riproduzione usando il lettore di origine, l'operazione non è in genere molto utile per i motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2545d-237">Although you can set the playback rate using the Source Reader, doing is typically not very useful, for the following reasons:</span></span>

-   <span data-ttu-id="2545d-238">Il lettore di origine non supporta la riproduzione inversa, anche se l'origine multimediale lo esegue.</span><span class="sxs-lookup"><span data-stu-id="2545d-238">The Source Reader does not support reverse playback, even if the media source does.</span></span>
-   <span data-ttu-id="2545d-239">L'applicazione controlla i tempi di presentazione, in modo che l'applicazione possa implementare una riproduzione veloce o lenta senza impostare la frequenza nell'origine.</span><span class="sxs-lookup"><span data-stu-id="2545d-239">The application controls the presentation times, so the application can implement fast or slow play without setting the rate on the source.</span></span>
-   <span data-ttu-id="2545d-240">Alcune origini supporti supportano la modalità di *assottigliamento* , in cui l'origine fornisce un minor numero di campioni, in genere solo i fotogrammi chiave.</span><span class="sxs-lookup"><span data-stu-id="2545d-240">Some media sources support *thinning* mode, where the source delivers fewer samples—typically just the key frames.</span></span> <span data-ttu-id="2545d-241">Tuttavia, se si desidera eliminare i fotogrammi non chiave, è possibile controllare ogni esempio per l' [attributo \_ CleanPoint di MFSampleExtension](mfsampleextension-cleanpoint-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="2545d-241">However, if you want to drop non-key frames, you can check each sample for the [MFSampleExtension\_CleanPoint](mfsampleextension-cleanpoint-attribute.md) attribute.</span></span>

<span data-ttu-id="2545d-242">Per impostare la velocità di riproduzione usando il lettore di origine, chiamare il metodo [**IMFSourceReader:: GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) per ottenere le interfacce [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) e [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) dall'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="2545d-242">To set the playback rate using the Source Reader, call the [**IMFSourceReader::GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) method to get the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) and [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interfaces from the media source.</span></span>

## <a name="hardware-acceleration"></a><span data-ttu-id="2545d-243">Accelerazione hardware</span><span class="sxs-lookup"><span data-stu-id="2545d-243">Hardware Acceleration</span></span>

<span data-ttu-id="2545d-244">Il lettore di origine è compatibile con Microsoft DirectX Video Acceleration (DXVA) 2,0 per la decodifica video con accelerazione hardware.</span><span class="sxs-lookup"><span data-stu-id="2545d-244">The Source Reader is compatible with Microsoft DirectX Video Acceleration (DXVA) 2.0 for hardware accelerated video decoding.</span></span> <span data-ttu-id="2545d-245">Per usare DXVA con il lettore di origine, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="2545d-245">To use DXVA with the Source Reader, perform the following steps.</span></span>

1.  <span data-ttu-id="2545d-246">Creare un dispositivo Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2545d-246">Create a Microsoft Direct3D device.</span></span>
2.  <span data-ttu-id="2545d-247">Chiamare la funzione [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) per creare la gestione dispositivi Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2545d-247">Call the [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) function to create the Direct3D device manager.</span></span> <span data-ttu-id="2545d-248">Questa funzione ottiene un puntatore all'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .</span><span class="sxs-lookup"><span data-stu-id="2545d-248">This function gets a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span>
3.  <span data-ttu-id="2545d-249">Chiamare il metodo [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) con un puntatore al dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2545d-249">Call the [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) method with a pointer to the Direct3D device.</span></span>
4.  <span data-ttu-id="2545d-250">Creare un archivio di attributi chiamando la funzione [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .</span><span class="sxs-lookup"><span data-stu-id="2545d-250">Create an attribute store by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span>
5.  <span data-ttu-id="2545d-251">Creare il lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="2545d-251">Create the Source Reader.</span></span> <span data-ttu-id="2545d-252">Passare l'archivio di attributi nel parametro *pAttributes* della funzione di creazione.</span><span class="sxs-lookup"><span data-stu-id="2545d-252">Pass the attribute store in the *pAttributes* parameter of the creation function.</span></span>

<span data-ttu-id="2545d-253">Quando si fornisce un dispositivo Direct3D, il lettore di origine alloca gli esempi video compatibili con l'API DXVA video processor.</span><span class="sxs-lookup"><span data-stu-id="2545d-253">When you provide a Direct3D device, the Source Reader allocates video samples that are compatible with the DXVA video processor API.</span></span> <span data-ttu-id="2545d-254">È possibile usare l'elaborazione video DXVA per eseguire la deinterlacciamento hardware o la combinazione di video.</span><span class="sxs-lookup"><span data-stu-id="2545d-254">You can use DXVA video processing to perform hardware deinterlacing or video mixing.</span></span> <span data-ttu-id="2545d-255">Per ulteriori informazioni, vedere [DXVA video processing](dxva-video-processing.md).</span><span class="sxs-lookup"><span data-stu-id="2545d-255">For more information, see [DXVA Video Processing](dxva-video-processing.md).</span></span> <span data-ttu-id="2545d-256">Inoltre, se il decodificatore supporta DXVA 2,0, utilizzerà il dispositivo Direct3D per eseguire la decodifica con accelerazione hardware.</span><span class="sxs-lookup"><span data-stu-id="2545d-256">Also, if the decoder supports DXVA 2.0, it will use the Direct3D device to perform hardware-accelerated decoding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2545d-257">A partire da Windows 8, è possibile usare [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) invece di [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9).</span><span class="sxs-lookup"><span data-stu-id="2545d-257">Beginning in Windows 8, [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) can be used instead of the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9).</span></span> <span data-ttu-id="2545d-258">Per le app di Windows Store, è necessario usare **IMFDXGIDeviceManager**.</span><span class="sxs-lookup"><span data-stu-id="2545d-258">For Windows Store apps, you must use **IMFDXGIDeviceManager**.</span></span> <span data-ttu-id="2545d-259">Per altre informazioni, vedere le [API video di Direct3D 11](direct3d-11-video-apis.md).</span><span class="sxs-lookup"><span data-stu-id="2545d-259">For more info, see the [Direct3D 11 Video APIs](direct3d-11-video-apis.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2545d-260">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2545d-260">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2545d-261">Lettore di origine</span><span class="sxs-lookup"><span data-stu-id="2545d-261">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




