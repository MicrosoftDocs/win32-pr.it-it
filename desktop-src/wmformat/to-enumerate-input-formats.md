---
title: Per enumerare i formati di input
description: Per enumerare i formati di input
ms.assetid: 482adfc4-d9ed-403d-912b-1a5a70baf04c
keywords:
- Formato di sistemi avanzati (ASF), enumerazione dei formati di input
- ASF (Advanced Systems Format), enumerazione dei formati di input
- profili, enumerazione dei formati di input
- codec, enumerazione dei formati di input
- Advanced Systems Format (ASF), enumerazioni del formato di input
- ASF (formato avanzato dei sistemi), enumerazioni del formato di input
- profili, enumerazioni del formato di input
- codec, enumerazioni del formato di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18360d3172af785fd1c00648ba0c9e869fb7fbc6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046439"
---
# <a name="to-enumerate-input-formats"></a><span data-ttu-id="1bc45-111">Per enumerare i formati di input</span><span class="sxs-lookup"><span data-stu-id="1bc45-111">To Enumerate Input Formats</span></span>

<span data-ttu-id="1bc45-112">Ognuno dei codec Windows Media accetta uno o più tipi di supporti di input per la compressione.</span><span class="sxs-lookup"><span data-stu-id="1bc45-112">Each of the Windows Media codecs accepts one or more types of input media for compression.</span></span> <span data-ttu-id="1bc45-113">Windows Media Format SDK consente di immettere una varietà di formati più ampia rispetto a quella supportata dai codec.</span><span class="sxs-lookup"><span data-stu-id="1bc45-113">The Windows Media Format SDK enables you to input a wider variety of formats than those supported by the codecs.</span></span> <span data-ttu-id="1bc45-114">L'SDK esegue questa operazione eseguendo le trasformazioni di pre-elaborazione sugli input quando necessario, ad esempio ridimensionando i frame video o ricampionando l'audio.</span><span class="sxs-lookup"><span data-stu-id="1bc45-114">The SDK does this by performing pre-processing transformations on the inputs when necessary, such as resizing video frames or resampling audio.</span></span> <span data-ttu-id="1bc45-115">In ogni caso, è necessario assicurarsi che i formati di input per i file scritti corrispondano ai dati inviati al writer.</span><span class="sxs-lookup"><span data-stu-id="1bc45-115">In any case, you must ensure that the input formats for the files you write match the data you send to the writer.</span></span> <span data-ttu-id="1bc45-116">Ogni codec dispone di un formato multimediale di input predefinito impostato nel writer quando il profilo viene caricato.</span><span class="sxs-lookup"><span data-stu-id="1bc45-116">Each codec has a default input media format that is set in the writer when the profile is loaded.</span></span> <span data-ttu-id="1bc45-117">È possibile esaminare il formato di input predefinito chiamando [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span><span class="sxs-lookup"><span data-stu-id="1bc45-117">You can examine the default input format by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>

<span data-ttu-id="1bc45-118">I codec video supportano i formati seguenti: IYUV, I420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RGB 555 e RGB 8.</span><span class="sxs-lookup"><span data-stu-id="1bc45-118">The video codecs support the following formats: IYUV, I420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RGB 555, and RGB 8.</span></span> <span data-ttu-id="1bc45-119">I codec audio supportano l'audio PCM.</span><span class="sxs-lookup"><span data-stu-id="1bc45-119">The audio codecs support PCM audio.</span></span>

<span data-ttu-id="1bc45-120">Per enumerare i formati di input supportati da un codec, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="1bc45-120">To enumerate the input formats supported by a codec, perform the following steps:</span></span>

1.  <span data-ttu-id="1bc45-121">Creare un oggetto writer e impostare un profilo da usare.</span><span class="sxs-lookup"><span data-stu-id="1bc45-121">Create a writer object and set a profile to use.</span></span> <span data-ttu-id="1bc45-122">Per ulteriori informazioni sull'impostazione dei profili nel writer, vedere [per utilizzare i profili con il writer](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="1bc45-122">For more information about setting profiles in the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
2.  <span data-ttu-id="1bc45-123">Identificare il numero di input per il quale si desidera controllare i formati.</span><span class="sxs-lookup"><span data-stu-id="1bc45-123">Identify the input number for which you want to check the formats.</span></span> <span data-ttu-id="1bc45-124">Per ulteriori informazioni sull'identificazione dei numeri di input, vedere [per identificare gli input per numero](to-identify-inputs-by-number.md).</span><span class="sxs-lookup"><span data-stu-id="1bc45-124">For more information about identifying input numbers, see [To Identify Inputs By Number](to-identify-inputs-by-number.md).</span></span>
3.  <span data-ttu-id="1bc45-125">Recuperare il numero totale di formati di input supportati dall'input desiderato chiamando [**IWMWriter:: GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).</span><span class="sxs-lookup"><span data-stu-id="1bc45-125">Retrieve the total number of input formats supported by the desired input by calling [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).</span></span>
4.  <span data-ttu-id="1bc45-126">Scorrere tutti i formati di input supportati, eseguendo i passaggi seguenti per ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="1bc45-126">Loop through all of the supported input formats, performing the following steps for each.</span></span>
    -   <span data-ttu-id="1bc45-127">Recuperare l'interfaccia [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) per il formato di input chiamando [**IWMWriter:: GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).</span><span class="sxs-lookup"><span data-stu-id="1bc45-127">Retrieve the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input format by calling [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).</span></span>
    -   <span data-ttu-id="1bc45-128">Recuperare la struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) per il formato di input.</span><span class="sxs-lookup"><span data-stu-id="1bc45-128">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the input format.</span></span> <span data-ttu-id="1bc45-129">Chiamare [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), passando **null** per il parametro *pType* per ottenere la dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="1bc45-129">Call [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), passing **NULL** for the *pType* parameter to get the size of the structure.</span></span> <span data-ttu-id="1bc45-130">Quindi allocare la memoria per conservare la struttura e chiamare di nuovo **GetMediaType** per ottenere la struttura.</span><span class="sxs-lookup"><span data-stu-id="1bc45-130">Then allocate memory to hold the structure and call **GetMediaType** again to get the structure.</span></span> <span data-ttu-id="1bc45-131">[**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) eredita da [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops), quindi è possibile effettuare le chiamate a **GetMediaType** dall'istanza di **IWMInputMediaProps** recuperata nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="1bc45-131">[**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) inherits from [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops), so you can make the calls to **GetMediaType** from the instance of **IWMInputMediaProps** retrieved in the previous step.</span></span>
    -   <span data-ttu-id="1bc45-132">Il formato descritto nella struttura [**del \_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contiene tutte le informazioni pertinenti sul formato di input.</span><span class="sxs-lookup"><span data-stu-id="1bc45-132">The format described in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure contains all of the pertinent information about the input format.</span></span> <span data-ttu-id="1bc45-133">Il formato di base del supporto è identificato da **WM \_ media \_ Type. sottotipo**.</span><span class="sxs-lookup"><span data-stu-id="1bc45-133">The basic format of the media is identified by **WM\_MEDIA\_TYPE.subtype**.</span></span> <span data-ttu-id="1bc45-134">Per i flussi video, il membro **pbFormat** punta a una struttura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) allocata in modo dinamico che contiene ulteriori dettagli sul flusso, incluse le dimensioni del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="1bc45-134">For video streams, the **pbFormat** member points to a dynamically allocated [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure which contains further details about the stream, including rectangle size.</span></span> <span data-ttu-id="1bc45-135">Non è necessario che la dimensione dei frame di input corrisponda esattamente a una dimensione supportata dal codec.</span><span class="sxs-lookup"><span data-stu-id="1bc45-135">The size of the input frames is not required to match exactly a size supported by the codec.</span></span> <span data-ttu-id="1bc45-136">Se non corrispondono, i componenti Runtime SDK, in molti casi, ridimensionano automaticamente i fotogrammi video di input in base a qualcosa che il codec può accettare.</span><span class="sxs-lookup"><span data-stu-id="1bc45-136">If they do not match, the SDK run-time components, in many cases, will automatically resize the input video frames to something the codec can accept.</span></span>

<span data-ttu-id="1bc45-137">Nell'esempio di codice seguente viene trovato il formato di input del sottotipo passato come parametro.</span><span class="sxs-lookup"><span data-stu-id="1bc45-137">The following example code finds the input format of the subtype passed as a parameter.</span></span> <span data-ttu-id="1bc45-138">Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="1bc45-138">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT FindInputFormat(IWMWriter* pWriter, 
                       DWORD dwInput,
                       GUID guidSubType,
                       IWMInputMediaProps** ppProps)
{
    DWORD   cFormats = 0;
    DWORD   cbSize   = 0;

    WM_MEDIA_TYPE*      pType  = NULL;
    IWMInputMediaProps* pProps = NULL;

    // Set the ppProps parameter to point to NULL. This will
    //  be used to check the results of the function later.
    *ppProps = NULL;

    // Find the number of formats supported by this input.
    HRESULT hr = pWriter->GetInputFormatCount(dwInput, &cFormats);
    if (FAILED(hr))
    {
        goto Exit;
    }
    // Loop through all of the supported formats.
    for (DWORD formatIndex = 0; formatIndex < cFormats; formatIndex++)
    {
        // Get the input media properties for the input format.
        hr = pWriter->GetInputFormat(dwInput, formatIndex, &pProps);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Get the size of the media type structure.
        hr = pProps->GetMediaType(NULL, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Allocate memory for the media type structure.
        pType = (WM_MEDIA_TYPE*) new (std::nothrow) BYTE[cbSize];
        if (pType == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }
        
        // Get the media type structure.
        hr = pProps->GetMediaType(pType, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }

        if(pType->subtype == guidSubType)
        {
            *ppProps = pProps;
            (*ppProps)->AddRef();
            goto Exit;
        }

        // Clean up for next iteration.
        delete [] pType;
        pType = NULL;
        SAFE_RELEASE(pProps);
    } // End for formatIndex.

    // If execution made it to this point, no matching format was found.
    hr = NS_E_INVALID_INPUT_FORMAT;

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="1bc45-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1bc45-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bc45-140">**Interfaccia IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="1bc45-140">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="1bc45-141">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="1bc45-141">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




