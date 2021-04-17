---
description: Configurazione di profili e altre proprietà dei file ASF
ms.assetid: c43df556-9d8a-4010-9ed6-f84d8ac6d9bc
title: Configurazione di profili e altre proprietà dei file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e26dcbb49cb5ff8309dccafc3f1d8d66397871
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401263"
---
# <a name="configuring-profiles-and-other-asf-file-properties"></a><span data-ttu-id="3d34e-103">Configurazione di profili e altre proprietà dei file ASF</span><span class="sxs-lookup"><span data-stu-id="3d34e-103">Configuring Profiles and Other ASF File Properties</span></span>

<span data-ttu-id="3d34e-104">Gli elementi seguenti descrivono come eseguire diverse attività correlate alla creazione di file ASF.</span><span class="sxs-lookup"><span data-stu-id="3d34e-104">The following items describe how to perform various tasks related to the creation of ASF files.</span></span> <span data-ttu-id="3d34e-105">Alcune delle interfacce indicate in questo argomento sono documentate nella documentazione di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="3d34e-105">Some of the interfaces mentioned in this topic are documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="3d34e-106">Creazione di un profilo</span><span class="sxs-lookup"><span data-stu-id="3d34e-106">Creating a Profile</span></span>

<span data-ttu-id="3d34e-107">I profili ASF sono descritti in dettaglio in Windows Media Format SDK; in sostanza, descrivono gli attributi di un file di formato Windows Media, ad esempio velocità in bit, numero e tipo di flussi e qualità di compressione.</span><span class="sxs-lookup"><span data-stu-id="3d34e-107">ASF profiles are discussed in detail in the Windows Media Format SDK; essentially, they describe attributes of a Windows Media Format file such as bit rate, number and type of streams, and compression quality.</span></span> <span data-ttu-id="3d34e-108">Il filtro usa il profilo per determinare il tipo di file di formato Windows Media da scrivere, il numero di pin di input che deve configurare e i tipi di supporti che possono accettare.</span><span class="sxs-lookup"><span data-stu-id="3d34e-108">The filter uses the profile to determine what kind of Windows Media Format file to write, how many input pins it must set up, and what media types they can accept.</span></span>

<span data-ttu-id="3d34e-109">Per creare un profilo personalizzato, usare direttamente Windows Media Format SDK per creare un oggetto di gestione profili tramite la funzione **WMCreateProfileManager** .</span><span class="sxs-lookup"><span data-stu-id="3d34e-109">To create a custom profile, use the Windows Media Format SDK directly to create a profile manager object by using the **WMCreateProfileManager** function.</span></span> <span data-ttu-id="3d34e-110">Successivamente, creare il profilo e passarlo al [writer ASF WM](wm-asf-writer-filter.md) usando il metodo [**IConfigASFWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) .</span><span class="sxs-lookup"><span data-stu-id="3d34e-110">Next, create the profile, and pass it to the [WM ASF Writer](wm-asf-writer-filter.md) by using the [**IConfigASFWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) method.</span></span> <span data-ttu-id="3d34e-111">Questo è l'unico modo per configurare il filtro con un profilo che usa i codec della serie Windows Media Audio e video 9.</span><span class="sxs-lookup"><span data-stu-id="3d34e-111">This is the only way to configure the filter with a profile that uses the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="3d34e-112">È possibile aggiungere i profili di sistema per le versioni precedenti di questi codec usando il metodo [**IConfigASFWriter:: ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) .</span><span class="sxs-lookup"><span data-stu-id="3d34e-112">System profiles for earlier versions of these codecs can be added by using the [**IConfigASFWriter::ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) method.</span></span>

<span data-ttu-id="3d34e-113">È possibile reimpostare il profilo mentre i pin di input del filtro sono connessi, purché il nuovo profilo non richieda pin di input aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="3d34e-113">You can reset the profile while the filter's input pins are connected, as long as the new profile does not require any additional input pins.</span></span> <span data-ttu-id="3d34e-114">Se ad esempio si modifica il profilo da un profilo audio di input singolo a un profilo audio e video di due input, solo il pin audio verrà riconnesso e non verrà creato alcun nuovo PIN per il flusso video.</span><span class="sxs-lookup"><span data-stu-id="3d34e-114">For example, if you change the profile from a one-input audio-only profile to a two-input audio and video profile, just the audio pin will be reconnected and no new pin will be created for the video stream.</span></span>

<span data-ttu-id="3d34e-115">Aggiunta di metadati</span><span class="sxs-lookup"><span data-stu-id="3d34e-115">Adding Metadata</span></span>

<span data-ttu-id="3d34e-116">Per aggiungere metadati a un file, eseguire una query sul filtro [WM ASF Writer](wm-asf-writer-filter.md) per l'interfaccia **IWMHeaderInfo** .</span><span class="sxs-lookup"><span data-stu-id="3d34e-116">To add metadata to a file, query the [WM ASF Writer](wm-asf-writer-filter.md) filter for the **IWMHeaderInfo** interface.</span></span> <span data-ttu-id="3d34e-117">Quando al filtro viene assegnato un profilo, utilizzare i metodi dell'interfaccia **IWMHeaderInfo** per scrivere i metadati.</span><span class="sxs-lookup"><span data-stu-id="3d34e-117">After the filter has been given a profile, use the **IWMHeaderInfo** interface methods to write the metadata.</span></span>

<span data-ttu-id="3d34e-118">Indicizzazione di un file</span><span class="sxs-lookup"><span data-stu-id="3d34e-118">Indexing a File</span></span>

<span data-ttu-id="3d34e-119">Per impostazione predefinita, il writer ASF WM crea file indicizzati temporaneamente.</span><span class="sxs-lookup"><span data-stu-id="3d34e-119">The WM ASF Writer creates temporally indexed files by default.</span></span> <span data-ttu-id="3d34e-120">Per creare un file indicizzato con frame, usare il metodo [**IConfigAsfWriter:: SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) per disabilitare tutte le indicizzazione, quindi creare il file.</span><span class="sxs-lookup"><span data-stu-id="3d34e-120">To create a frame-indexed file, use the [**IConfigAsfWriter::SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) method to disable all indexing, then create the file.</span></span> <span data-ttu-id="3d34e-121">Al termine, usare direttamente Windows Media Format SDK per creare un indice basato su frame per il file.</span><span class="sxs-lookup"><span data-stu-id="3d34e-121">When it is complete, use the Windows Media Format SDK directly to create a frame-based index for the file.</span></span>

<span data-ttu-id="3d34e-122">Codifica Two-Pass</span><span class="sxs-lookup"><span data-stu-id="3d34e-122">Two-Pass Encoding</span></span>

<span data-ttu-id="3d34e-123">La codifica a due passaggi è supportata solo nei codec Windows Media versione 8 e successive.</span><span class="sxs-lookup"><span data-stu-id="3d34e-123">Two-pass encoding is supported only on Windows Media codecs of version 8 and later.</span></span> <span data-ttu-id="3d34e-124">Inserire il writer ASF WM in modalità di pre-elaborazione chiamando [**IConfigAsfWriter2:: separat**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) e specificando am \_ CONFIGASFWRITER \_ param \_ MultiPASS nel parametro *dwParam* e **true** nel parametro *dwParam1* .</span><span class="sxs-lookup"><span data-stu-id="3d34e-124">Put the WM ASF Writer into preprocess mode by calling [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) and specifying AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS in the *dwParam* parameter and **TRUE** in the *dwParam1* parameter.</span></span>

<span data-ttu-id="3d34e-125">Eseguire quindi il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="3d34e-125">Then run the filter graph.</span></span> <span data-ttu-id="3d34e-126">Al termine di tutti i passaggi di pre-elaborazione (in genere verrà eseguito solo un passaggio di pre-elaborazione), l'applicazione riceverà un evento di [**\_ \_ completamento della pre-elaborazione EC**](ec-preprocess-complete.md) dal filtro.</span><span class="sxs-lookup"><span data-stu-id="3d34e-126">When all the preprocessing passes are done (typically only one preprocessing pass will be performed), the application will receive an [**EC\_PREPROCESS\_COMPLETE**](ec-preprocess-complete.md) event from the filter.</span></span> <span data-ttu-id="3d34e-127">Quando viene ricevuto questo evento, usare [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) per reimpostare il puntatore del flusso all'inizio ed eseguire di nuovo il grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="3d34e-127">When this event is received, use [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) to reset the stream pointer back to the beginning, and run the filter graph again.</span></span> <span data-ttu-id="3d34e-128">Dopo l'ultimo passaggio, in genere il secondo passaggio, l'applicazione riceverà un evento [**EC \_ complete**](ec-complete.md) per indicare che il processo di codifica è completo.</span><span class="sxs-lookup"><span data-stu-id="3d34e-128">After the last pass (typically the second pass), the application will receive an [**EC\_COMPLETE**](ec-complete.md) event to signify that the encoding process is complete.</span></span> <span data-ttu-id="3d34e-129">Se un passaggio di pre-elaborazione viene annullato prima della ricezione dell'evento di **\_ \_ completamento della pre-elaborazione EC** , chiamare [**IConfigAsfWriter2:: ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) per reimpostare il filtro prima di tentare un'altra esecuzione di pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="3d34e-129">If a preprocessing pass is canceled before the **EC\_PREPROCESS\_COMPLETE** event is received, call [**IConfigAsfWriter2::ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) to reset the filter before attempting another preprocessing run.</span></span>

<span data-ttu-id="3d34e-130">È necessario impostare il \_ \_ parametro CONFIGASFWRITER param \_ MultiPASS su **false** se si desidera che il filtro venga escluso completamente dalla modalità di pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="3d34e-130">It is only necessary to set the AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS parameter to **FALSE** if you want to put the filter out of preprocessing mode completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d34e-131">È responsabilità dell'applicazione abilitare la modalità di pre-elaborazione in base al profilo che verrà usato per la codifica.</span><span class="sxs-lookup"><span data-stu-id="3d34e-131">It is the application's responsibility to enable the preprocessing mode based on the profile that will be used for encoding.</span></span> <span data-ttu-id="3d34e-132">Alcuni profili richiedono la codifica a due passaggi. Se si tenta di codificare un file con un profilo di questo tipo e non si imposta AM \_ CONFIGASFWRITER \_ param \_ MultiPASS su **true**, verrà generato un errore [**EC \_ USERABORT**](ec-userabort.md) .</span><span class="sxs-lookup"><span data-stu-id="3d34e-132">Some profiles require two-pass encoding; if you attempt to encode a file with such a profile, and do not set AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS to **TRUE**, an [**EC\_USERABORT**](ec-userabort.md) error will result.</span></span> <span data-ttu-id="3d34e-133">Per ulteriori informazioni, vedere la documentazione di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="3d34e-133">For more information, see the Windows Media Format SDK documentation.</span></span>

 

<span data-ttu-id="3d34e-134">Recupero e impostazione delle proprietà del buffer in fase di esecuzione</span><span class="sxs-lookup"><span data-stu-id="3d34e-134">Getting and Setting Buffer Properties at Run Time</span></span>

<span data-ttu-id="3d34e-135">In alcuni scenari, ad esempio se si vuole forzare l'inserimento di fotogrammi chiave durante la scrittura di un file, è possibile che un'applicazione debba ottenere o impostare informazioni su un buffer di Windows Media in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3d34e-135">In some scenarios, for example if you want to force key-frame insertion when writing a file, an application may need to get or set information about a Windows Media buffer at run time.</span></span> <span data-ttu-id="3d34e-136">I filtri [WM ASF Reader](wm-asf-reader-filter.md) e [WM ASF Writer](wm-asf-writer-filter.md) supportano entrambi un meccanismo di callback che consente a un'applicazione di accedere all'interfaccia **INSSBuffer3** su ogni singolo buffer multimediale durante la lettura o la scrittura di file.</span><span class="sxs-lookup"><span data-stu-id="3d34e-136">The [WM ASF Reader](wm-asf-reader-filter.md) and [WM ASF Writer](wm-asf-writer-filter.md) filters both support a callback mechanism that enables an application to access the **INSSBuffer3** interface on each individual media buffer during file reading or file writing.</span></span> <span data-ttu-id="3d34e-137">Le applicazioni possono usare questa interfaccia per designare esempi specifici come fotogrammi chiave, impostare codici temporali SMPTE, specificare le impostazioni interlacciate o aggiungere qualsiasi tipo di dati privati a un flusso.</span><span class="sxs-lookup"><span data-stu-id="3d34e-137">Applications can use this interface to designate specific samples as key frames, set SMPTE time codes, specify interlace settings, or add any type of private data to a stream.</span></span>

<span data-ttu-id="3d34e-138">Usare l'interfaccia [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) per registrare i callback dal pin che sta gestendo il flusso video.</span><span class="sxs-lookup"><span data-stu-id="3d34e-138">Use the [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) interface to register for callbacks from the pin that is handling the video stream.</span></span> <span data-ttu-id="3d34e-139">Il pin chiamerà il metodo [**IAMWMBufferPassCallback:: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) per ogni buffer.</span><span class="sxs-lookup"><span data-stu-id="3d34e-139">The pin will call your [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) method for each buffer.</span></span>

<span data-ttu-id="3d34e-140">Pixel non quadrati</span><span class="sxs-lookup"><span data-stu-id="3d34e-140">Non-Square Pixels</span></span>

<span data-ttu-id="3d34e-141">Il writer ASF WM si connette a un filtro upstream, ad esempio il decodificatore DV, che restituisce informazioni sulle proporzioni in pixel.</span><span class="sxs-lookup"><span data-stu-id="3d34e-141">The WM ASF Writer connects to an upstream filter, such as the DV Decoder, that outputs pixel aspect ratio information.</span></span> <span data-ttu-id="3d34e-142">Il writer ASF WM scriverà queste informazioni come estensioni dell'unità dati per ogni esempio nel file.</span><span class="sxs-lookup"><span data-stu-id="3d34e-142">The WM ASF Writer will write this information as data unit extensions for every sample in the file.</span></span>

<span data-ttu-id="3d34e-143">Quando il lettore ASF WM rileva le informazioni sulle proporzioni in pixel nell'intestazione del file o nelle estensioni dell'unità dati per gli esempi, offre un formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) come prima scelta nel pin di output.</span><span class="sxs-lookup"><span data-stu-id="3d34e-143">When the WM ASF Reader encounters pixel aspect ratio information in the file header or in data unit extensions for the samples, it will offer a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format as a first choice on its output pin.</span></span> <span data-ttu-id="3d34e-144">I membri **dwPictAspectRatioX** e **dwPictAspectRatioY** della struttura, che descrivono le proporzioni del rettangolo video, verranno adattati correttamente per tenere conto delle proporzioni in pixel.</span><span class="sxs-lookup"><span data-stu-id="3d34e-144">The **dwPictAspectRatioX** and **dwPictAspectRatioY** members of the structure, which describe the video rectangle's aspect ratio, will be correctly adjusted to account for the pixel aspect ratio.</span></span>

<span data-ttu-id="3d34e-145">Gestione del formato interlacciato</span><span class="sxs-lookup"><span data-stu-id="3d34e-145">Maintaining Interlaced Format</span></span>

<span data-ttu-id="3d34e-146">Se si acquisisce video interlacciato da un televisore o una fotocamera DV, potrebbe essere necessario mantenere il video originale come campi indipendenti se si prevede che il file codificato venga riprodotto in un televisore o in un altro dispositivo di visualizzazione interlacciato.</span><span class="sxs-lookup"><span data-stu-id="3d34e-146">If you capture interlaced video from a television or a DV camera, you might wish to preserve the original video as independent fields if you expect the encoded file to be played back on a television or other interlaced display device.</span></span> <span data-ttu-id="3d34e-147">(I monitoraggi computer sono dispositivi di analisi progressiva). Se si esegue la disinterlacciamento di un video e quindi lo si riinterlaccia per la riproduzione in un televisore, si verifica una perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="3d34e-147">(Computer monitors are progressive scanning devices.) If you deinterlace a video, and then reinterlace it for playback on a television, some loss of data will be incurred.</span></span> <span data-ttu-id="3d34e-148">In un file ASF, le informazioni di interlacciamento vengono archiviate come estensioni di unità dati che l'applicazione applica a ogni esempio utilizzando il metodo [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="3d34e-148">In an ASF file, interlacing information is stored as data unit extensions that the application applies to each sample using the [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) method described previously.</span></span> <span data-ttu-id="3d34e-149">Per codificare un file che conserva le impostazioni di interlacciamento originali, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="3d34e-149">To encode a file that preserves the original interlace settings, follow these steps:</span></span>

1.  <span data-ttu-id="3d34e-150">Implementare una classe che supporta **IAMWMBufferPassCallback** e scrivere una funzione Notify che imposta i flag di interlacciamento per ogni campione.</span><span class="sxs-lookup"><span data-stu-id="3d34e-150">Implement a class that supports **IAMWMBufferPassCallback** and write a Notify function that sets the interlace flags for each sample.</span></span> <span data-ttu-id="3d34e-151">Questa funzione verrà chiamata dal writer ASF WM prima di elaborare ogni campione.</span><span class="sxs-lookup"><span data-stu-id="3d34e-151">This function will be called by the WM ASF Writer before it processes each sample.</span></span>
    ```C++
    // Set to WM_CT_TOP_FIELD_FIRST if that is your format.
    BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
    HRESULT hr = S_OK;

    hr = pNSSBuffer3->SetProperty(
        WM_SampleExtensionGUID_ContentType, 
        (void*) &flag, 
        WM_SampleExtension_ContentType_Size
        );         
    ```

    

2.  <span data-ttu-id="3d34e-152">Impostare le estensioni dell'unità dati nel profilo prima di passare il profilo al filtro.</span><span class="sxs-lookup"><span data-stu-id="3d34e-152">Set the data unit extensions on the profile before you pass the profile to the filter.</span></span>
    ```C++
    hr = pWMStreamConfig2->AddDataUnitExtension(
        WM_SampleExtensionGUID_ContentType, 
        WM_SampleExtension_ContentType_Size, 
        NULL, 
        0 
        );
    ```

    

3.  <span data-ttu-id="3d34e-153">Dopo aver configurato il filtro con il profilo, ottenere l'interfaccia **IWMWriterAdvanced2** dal writer ASF WM e chiamare il metodo **SetInputSettings** .</span><span class="sxs-lookup"><span data-stu-id="3d34e-153">After you configure the filter with the profile, obtain the **IWMWriterAdvanced2** interface from the WM ASF Writer and call the **SetInputSettings** method.</span></span>

    ``

    ``

    ```C++
    // Must do this first.
    hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);
      
    CComPtr<IServiceProvider> pProvider;
    CComPtr<IWMWriterAdvanced2> pWMWA2;

    hr = pConfigAsfWriter2->QueryInterface( __uuidof(IServiceProvider),
                                             (void**)&pProvider);
    if (SUCCEEDED(hr))
    {
        hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
            IID_IWMWriterAdvanced2,
            (void**)&pWMWA2);
    }

    BOOL pValue = TRUE;

    // Set the first parameter to your actual input number.
    hr = pWMWA2->SetInputSetting(0, g_wszInterlacedCoding,
        WMT_TYPE_BOOL, (BYTE*) &pValue, sizeof(WMT_TYPE_BOOL));
                
    ```

    

## <a name="related-topics"></a><span data-ttu-id="3d34e-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3d34e-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d34e-155">Creazione di file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="3d34e-155">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



