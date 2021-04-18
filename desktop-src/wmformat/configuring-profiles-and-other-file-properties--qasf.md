---
title: Configurazione di profili e altre proprietà di file (QASF)
description: Configurazione di profili e altre proprietà di file (QASF)
ms.assetid: a462fc8b-5a2e-4c93-828d-177d1965b734
keywords:
- Windows Media Format SDK, configurazione di profili (QASF)
- Windows Media Format SDK, configurazione delle proprietà dei file (QASF)
- Windows Media Format SDK, metadati (QASF)
- ASF (Advanced Systems Format), configurazione dei profili (QASF)
- ASF (formato avanzato dei sistemi), configurazione di profili (QASF)
- ASF (Advanced Systems Format), configurazione delle proprietà dei file (QASF)
- ASF (formato avanzato dei sistemi), configurazione delle proprietà dei file (QASF)
- ASF (Advanced Systems Format), metadati (QASF)
- ASF (formato avanzato dei sistemi), metadati (QASF)
- Windows Media Format SDK, QASF
- Formato Advanced Systems (ASF), QASF
- ASF (formato avanzato dei sistemi), QASF
- metadati, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb6afedfa00813e7447e5bcaefe1f251c02575
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473739"
---
# <a name="configuring-profiles-and-other-file-properties-qasf"></a><span data-ttu-id="39839-116">Configurazione di profili e altre proprietà di file (QASF)</span><span class="sxs-lookup"><span data-stu-id="39839-116">Configuring Profiles and Other File Properties (QASF)</span></span>

<span data-ttu-id="39839-117">Gli elementi seguenti descrivono come eseguire diverse attività correlate alla creazione di file ASF.</span><span class="sxs-lookup"><span data-stu-id="39839-117">The following items describe how to perform various tasks related to the creation of ASF files.</span></span>

## <a name="creating-a-profile-qasf"></a><span data-ttu-id="39839-118">Creazione di un profilo (QASF)</span><span class="sxs-lookup"><span data-stu-id="39839-118">Creating a Profile (QASF)</span></span>

<span data-ttu-id="39839-119">Per creare un profilo personalizzato, usare direttamente Windows Media Format SDK per creare un oggetto di gestione profili tramite la funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="39839-119">To create a custom profile, use the Windows Media Format SDK directly to create a profile manager object by using the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span> <span data-ttu-id="39839-120">Successivamente, creare il profilo e passarlo al [writer ASF WM](wm-asf-writer-filter.md) usando il metodo [**IConfigASFWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="39839-120">Next, create the profile, and pass it to the [WM ASF Writer](wm-asf-writer-filter.md) by using the [**IConfigASFWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) method.</span></span> <span data-ttu-id="39839-121">Questo è l'unico modo per configurare il filtro con un profilo che usa i codec della serie Windows Media Audio e video 9.</span><span class="sxs-lookup"><span data-stu-id="39839-121">This is the only way to configure the filter with a profile that uses the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="39839-122">È possibile aggiungere i profili di sistema per le versioni precedenti di questi codec usando il metodo [**IConfigASFWriter:: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) .</span><span class="sxs-lookup"><span data-stu-id="39839-122">System profiles for earlier versions of these codecs can be added by using the [**IConfigASFWriter::ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) method.</span></span>

## <a name="adding-metadata-qasf"></a><span data-ttu-id="39839-123">Aggiunta di metadati (QASF)</span><span class="sxs-lookup"><span data-stu-id="39839-123">Adding Metadata (QASF)</span></span>

<span data-ttu-id="39839-124">Per aggiungere metadati a un file, chiamare **QueryInterface** dall'interfaccia **IBASEFILTER** sul [writer ASF WM](wm-asf-writer-filter.md) per recuperare l'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) .</span><span class="sxs-lookup"><span data-stu-id="39839-124">To add metadata to a file, call **QueryInterface** from the **IBaseFilter** interface on the [WM ASF Writer](wm-asf-writer-filter.md) to retrieve the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface.</span></span> <span data-ttu-id="39839-125">Quando al filtro viene assegnato un profilo, utilizzare i metodi dell'interfaccia **IWMHeaderInfo** per scrivere i metadati.</span><span class="sxs-lookup"><span data-stu-id="39839-125">After the filter has been given a profile, use the **IWMHeaderInfo** interface methods to write the metadata.</span></span>

## <a name="indexing-a-file-qasf"></a><span data-ttu-id="39839-126">Indicizzazione di un file (QASF)</span><span class="sxs-lookup"><span data-stu-id="39839-126">Indexing a File (QASF)</span></span>

<span data-ttu-id="39839-127">Per impostazione predefinita, il writer ASF WM crea file indicizzati temporaneamente.</span><span class="sxs-lookup"><span data-stu-id="39839-127">The WM ASF Writer creates temporally indexed files by default.</span></span> <span data-ttu-id="39839-128">Per creare un file indicizzato con frame, usare il metodo [**IConfigAsfWriter:: SetIndexMode**](iconfigasfwriter-setindexmode.md) per disabilitare tutte le indicizzazione, quindi creare il file.</span><span class="sxs-lookup"><span data-stu-id="39839-128">To create a frame-indexed file, use the [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md) method to disable all indexing, then create the file.</span></span> <span data-ttu-id="39839-129">Al termine, usare direttamente Windows Media Format SDK per creare un indice basato su frame per il file.</span><span class="sxs-lookup"><span data-stu-id="39839-129">When it is complete, use the Windows Media Format SDK directly to create a frame-based index for the file.</span></span>

## <a name="performing-two-pass-encoding-qasf"></a><span data-ttu-id="39839-130">Esecuzione della codifica Two-Pass (QASF)</span><span class="sxs-lookup"><span data-stu-id="39839-130">Performing Two-Pass Encoding (QASF)</span></span>

<span data-ttu-id="39839-131">La codifica a due passaggi è supportata solo nei codec Windows Media versione 8 e successive.</span><span class="sxs-lookup"><span data-stu-id="39839-131">Two-pass encoding is supported only on Windows Media codecs of version 8 and later.</span></span> <span data-ttu-id="39839-132">Inserire il writer ASF WM in modalità di pre-elaborazione chiamando [**IConfigAsfWriter2:: separat**](iconfigasfwriter2-setparam.md) e specificando am \_ CONFIGASFWRITER \_ param \_ MultiPASS nel parametro *dwParam* e **true** nel parametro *dwParam1* .</span><span class="sxs-lookup"><span data-stu-id="39839-132">Put the WM ASF Writer into preprocess mode by calling [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) and specifying AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS in the *dwParam* parameter and **TRUE** in the *dwParam1* parameter.</span></span>

<span data-ttu-id="39839-133">Eseguire quindi il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="39839-133">Then run the filter graph.</span></span> <span data-ttu-id="39839-134">Al termine di tutti i passaggi di pre-elaborazione (in genere verrà eseguito solo un passaggio di pre-elaborazione), l'applicazione riceverà un evento di **\_ \_ completamento della pre-elaborazione EC** dal filtro.</span><span class="sxs-lookup"><span data-stu-id="39839-134">When all the preprocessing passes are done (typically only one preprocessing pass will be performed), the application will receive an **EC\_PREPROCESS\_COMPLETE** event from the filter.</span></span> <span data-ttu-id="39839-135">Quando viene ricevuto questo evento, usare **IMediaSeeking:: Sepositions** per reimpostare il puntatore del flusso all'inizio ed eseguire di nuovo il grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="39839-135">When this event is received, use **IMediaSeeking::SetPositions** to reset the stream pointer back to the beginning, and run the filter graph again.</span></span> <span data-ttu-id="39839-136">Dopo l'ultimo passaggio, in genere il secondo passaggio, l'applicazione riceverà un evento **EC \_ complete** per indicare che il processo di codifica è completo.</span><span class="sxs-lookup"><span data-stu-id="39839-136">After the last pass (typically the second pass), the application will receive an **EC\_COMPLETE** event to signify that the encoding process is complete.</span></span> <span data-ttu-id="39839-137">Se un passaggio di pre-elaborazione viene annullato prima della ricezione dell'evento di **\_ \_ completamento della pre-elaborazione EC** , chiamare [**IConfigAsfWriter2:: ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) per reimpostare il filtro prima di tentare un'altra esecuzione di pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="39839-137">If a preprocessing pass is canceled before the **EC\_PREPROCESS\_COMPLETE** event is received, call [**IConfigAsfWriter2::ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) to reset the filter before attempting another preprocessing run.</span></span>

<span data-ttu-id="39839-138">È necessario chiamare **IConfigAsfWriter:: separat**(AM \_ CONFIGASFWRITER \_ param \_ MultiPASS, **false**) se si desidera che il filtro venga escluso completamente dalla modalità di pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="39839-138">It is only necessary to call **IConfigAsfWriter::SetParam**(AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS, **FALSE**) if you want to put the filter out of preprocessing mode completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39839-139">È responsabilità dell'applicazione abilitare la modalità di pre-elaborazione in base al profilo che verrà usato per la codifica.</span><span class="sxs-lookup"><span data-stu-id="39839-139">It is the application's responsibility to enable preprocessing mode based on the profile that will be used for encoding.</span></span> <span data-ttu-id="39839-140">Alcuni profili richiedono la codifica a due passaggi. Se si tenta di codificare un file con un profilo di questo tipo e non si imposta AM \_ CONFIGASFWRITER \_ param \_ MultiPASS su **true**, \_ verrà generato un errore EC USERABORT.</span><span class="sxs-lookup"><span data-stu-id="39839-140">Some profiles require two-pass encoding; if you attempt to encode a file with such a profile, and do not set AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS to **TRUE**, an EC\_USERABORT error will result.</span></span> <span data-ttu-id="39839-141">Per ulteriori informazioni su come determinare se un determinato profilo richiede una codifica a due passaggi, vedere [utilizzo Two-Pass codifica](using-two-pass-encoding.md) o [scrittura di flussi di velocità in bit variabili](writing-variable-bit-rate-streams.md).</span><span class="sxs-lookup"><span data-stu-id="39839-141">For more information on how to determine whether a given profile requires two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md) or [Writing Variable Bit Rate Streams](writing-variable-bit-rate-streams.md).</span></span>

 

## <a name="getting-and-setting-buffer-properties-at-run-time-qasf"></a><span data-ttu-id="39839-142">Recupero e impostazione delle proprietà del buffer in fase di esecuzione (QASF)</span><span class="sxs-lookup"><span data-stu-id="39839-142">Getting and Setting Buffer Properties at Run Time (QASF)</span></span>

<span data-ttu-id="39839-143">In alcuni scenari, ad esempio se si vuole forzare l'inserimento di fotogrammi chiave durante la scrittura di un file, è possibile che un'applicazione debba ottenere o impostare informazioni su un buffer di Windows Media in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="39839-143">In some scenarios, for example if you want to force key-frame insertion when writing a file, an application may need to get or set information about a Windows Media buffer at run time.</span></span> <span data-ttu-id="39839-144">I filtri [WM ASF Reader](wm-asf-reader-filter.md) e [WM ASF Writer](wm-asf-writer-filter.md) supportano entrambi un meccanismo di callback che consente a un'applicazione di accedere all'interfaccia [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) su ogni singolo buffer multimediale durante la lettura o la scrittura di file.</span><span class="sxs-lookup"><span data-stu-id="39839-144">The [WM ASF Reader](wm-asf-reader-filter.md) and [WM ASF Writer](wm-asf-writer-filter.md) filters both support a callback mechanism that enables an application to access the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface on each individual media buffer during file reading or file writing.</span></span> <span data-ttu-id="39839-145">Le applicazioni possono usare questa interfaccia per designare esempi specifici come fotogrammi chiave, o [*cleanpoints*](wmformat-glossary.md), per impostare codici temporali SMPTE, per specificare le impostazioni interlacciate o per aggiungere qualsiasi tipo di dati privati a un flusso.</span><span class="sxs-lookup"><span data-stu-id="39839-145">Applications can use this interface to designate specific samples as key frames, or [*cleanpoints*](wmformat-glossary.md), to set SMPTE time codes, to specify interlace settings, or add any type of private data to a stream.</span></span>

<span data-ttu-id="39839-146">Usare l'interfaccia [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) per registrare i callback dal pin che sta gestendo il flusso video.</span><span class="sxs-lookup"><span data-stu-id="39839-146">Use the [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) interface to register for callbacks from the pin that is handling the video stream.</span></span> <span data-ttu-id="39839-147">Quando il pin chiama il metodo [**IAMWMBufferPassCallback:: Notify**](iamwmbufferpasscallback-notify.md) , esaminare gli indicatori temporali sul buffer e, se necessario, chiamare [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) per impostare la proprietà **\_ SampleExtensionGUID \_ OutputCleanPoint di WM** sul buffer su **true**.</span><span class="sxs-lookup"><span data-stu-id="39839-147">When the pin calls your [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) method, examine the time stamps on the buffer and, if appropriate, call [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) to set the **WM\_SampleExtensionGUID\_OutputCleanPoint** property on the buffer to **TRUE**.</span></span>

## <a name="non-square-pixel-support-qasf"></a><span data-ttu-id="39839-148">Supporto di pixel non quadrati (QASF)</span><span class="sxs-lookup"><span data-stu-id="39839-148">Non-Square Pixel Support (QASF)</span></span>

<span data-ttu-id="39839-149">Il writer ASF WM si connette a un filtro upstream, ad esempio il decodificatore DV, che restituisce informazioni sulle proporzioni in pixel.</span><span class="sxs-lookup"><span data-stu-id="39839-149">The WM ASF Writer connects to an upstream filter, such as the DV Decoder, that outputs pixel aspect ratio information.</span></span> <span data-ttu-id="39839-150">Il writer ASF WM scriverà queste informazioni come estensioni dell'unità dati per ogni esempio nel file.</span><span class="sxs-lookup"><span data-stu-id="39839-150">The WM ASF Writer will write this information as data unit extensions for every sample in the file.</span></span>

<span data-ttu-id="39839-151">Quando il lettore ASF WM rileva le informazioni sulle proporzioni in pixel nell'intestazione del file o nelle estensioni dell'unità dati per gli esempi, offre un tipo di supporto **VIDEOINFOHEADER2** come prima scelta nel pin di output.</span><span class="sxs-lookup"><span data-stu-id="39839-151">When the WM ASF Reader encounters pixel aspect ratio information in the file header or in data unit extensions for the samples, it will offer a **VIDEOINFOHEADER2** media type as a first choice on its output pin.</span></span> <span data-ttu-id="39839-152">I membri **dwPictAspectRatioX** e **dwPictAspectRatioY** della struttura, che descrivono le proporzioni del rettangolo video, verranno adattati correttamente per tenere conto delle proporzioni in pixel.</span><span class="sxs-lookup"><span data-stu-id="39839-152">The **dwPictAspectRatioX** and **dwPictAspectRatioY** members of the structure, which describe the video rectangle's aspect ratio, will be correctly adjusted to account for the pixel aspect ratio.</span></span>

## <a name="maintaining-interlaced-format"></a><span data-ttu-id="39839-153">Gestione del formato interlacciato</span><span class="sxs-lookup"><span data-stu-id="39839-153">Maintaining Interlaced Format</span></span>

<span data-ttu-id="39839-154">Se si acquisisce video interlacciato da un televisore o una fotocamera DV, potrebbe essere necessario mantenere il video originale come campi indipendenti se si prevede che il file codificato venga riprodotto in un televisore o in un altro dispositivo di visualizzazione interlacciato.</span><span class="sxs-lookup"><span data-stu-id="39839-154">If you capture interlaced video from a television or a DV camera, you might wish to preserve the original video as independent fields if you expect the encoded file to be played back on a television or other interlaced display device.</span></span> <span data-ttu-id="39839-155">(I monitoraggi computer sono dispositivi di analisi progressiva). Se si esegue la disinterlacciamento di un video e quindi lo si riinterlaccia per la riproduzione in un televisore, si verifica una perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="39839-155">(Computer monitors are progressive scanning devices.) If you deinterlace a video, and then reinterlace it for playback on a television, some loss of data will be incurred.</span></span> <span data-ttu-id="39839-156">In un file ASF, le informazioni di interlacciamento vengono archiviate come estensioni di unità dati che l'applicazione applica a ogni esempio utilizzando il metodo **IAMWMBufferPassCallback** descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="39839-156">In an ASF file, interlacing information is stored as data unit extensions that the application applies to each sample using the **IAMWMBufferPassCallback** method described previously.</span></span> <span data-ttu-id="39839-157">Per codificare un file che conserva le impostazioni di interlacciamento originali, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="39839-157">To encode a file that preserves the original interlace settings, follow these steps:</span></span>

-   <span data-ttu-id="39839-158">Implementare una classe che supporta **IAMWMBufferPassCallback** e scrivere una funzione Notify che imposta i flag di interlacciamento per ogni campione.</span><span class="sxs-lookup"><span data-stu-id="39839-158">Implement a class that supports **IAMWMBufferPassCallback** and write a Notify function that sets the interlace flags for each sample.</span></span> <span data-ttu-id="39839-159">Questa funzione verrà chiamata dal writer ASF WM prima di elaborare ogni campione.</span><span class="sxs-lookup"><span data-stu-id="39839-159">This function will be called by the WM ASF Writer before it processes each sample.</span></span>


```C++
// Set to WM_CT_TOP_FIELD_FIRST if that is your format.
BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
            HRESULT hr = pNSSBuffer3->SetProperty(WM_SampleExtensionGUID_ContentType, (void*) &flag, WM_SampleExtension_ContentType_Size);
           
```



-   <span data-ttu-id="39839-160">Impostare le estensioni dell'unità dati nel profilo prima di passare il profilo al filtro.</span><span class="sxs-lookup"><span data-stu-id="39839-160">Set the data unit extensions on the profile before you pass the profile to the filter.</span></span>


```C++
hr = pWMStreamConfig2->AddDataUnitExtension( WM_SampleExtensionGUID_ContentType, WM_SampleExtension_ContentType_Size, NULL, 0 );
```



-   <span data-ttu-id="39839-161">Dopo aver configurato il filtro con il profilo, ottenere l'interfaccia **IWMWriterAdvanced2** dal writer ASF WM e chiamare il metodo **SetInputSettings** .</span><span class="sxs-lookup"><span data-stu-id="39839-161">After you configure the filter with the profile, obtain the **IWMWriterAdvanced2** interface from the WM ASF Writer and call the **SetInputSettings** method.</span></span>

`// Must do this first.`

`hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);`


```C++
  
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



 

 