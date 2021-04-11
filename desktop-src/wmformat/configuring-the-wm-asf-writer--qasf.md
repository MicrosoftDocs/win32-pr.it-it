---
title: Configurazione del writer ASF WM (QASF)
description: Configurazione del writer ASF WM (QASF)
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- Windows Media Format SDK, configurazione di WM ASF Writer (QASF)
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, WM ASF Writer
- Windows Media Format SDK, QASF
- Advanced Systems Format (ASF), configurazione di WM ASF Writer (QASF)
- ASF (Advanced Systems Format), configurazione di WM ASF Writer (QASF)
- ASF (Advanced Systems Format), writer ASF WM
- ASF (formato avanzato dei sistemi), writer ASF WM
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Formato Advanced Systems (ASF), QASF
- ASF (formato avanzato dei sistemi), QASF
- DirectShow, configurazione di WM ASF Writer (QASF)
- DirectShow, WM-writer ASF
- DirectShow, QASF
- Writer ASF WM, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f954522c4acae89e6f6dd001561811088c2a9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118258"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a><span data-ttu-id="73e0f-119">Configurazione del writer ASF WM (QASF)</span><span class="sxs-lookup"><span data-stu-id="73e0f-119">Configuring the WM ASF Writer (QASF)</span></span>

<span data-ttu-id="73e0f-120">Quando il filtro del [writer ASF WM](wm-asf-writer-filter.md) viene creato, viene configurato automaticamente con il \_ profilo WMProfile \_ V80 256Video come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="73e0f-120">When the [WM ASF Writer](wm-asf-writer-filter.md) filter is created, it is configured automatically with the WMProfile\_V80\_256Video profile as a default.</span></span> <span data-ttu-id="73e0f-121">Poiché questo profilo usa i codec Windows Media Audio e Windows Media Video versione 8, è consigliabile creare un profilo personalizzato che usa i codec della serie Windows Media 9, quindi passare il puntatore [**IWMProfile**](iwmprofile.md) al filtro usando il metodo [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="73e0f-121">Because this profile uses the Windows Media Audio and Windows Media Video version 8 codecs, it is recommended that you create a custom profile that uses the Windows Media 9 Series codecs, and then pass its [**IWMProfile**](iwmprofile.md) pointer to the filter using the [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) method.</span></span> <span data-ttu-id="73e0f-122">Il filtro deve essere aggiunto al grafico prima che il filtro possa essere configurato e deve essere configurato prima di poter essere connesso ai filtri upstream.</span><span class="sxs-lookup"><span data-stu-id="73e0f-122">The filter must be added to the graph before the filter can be configured, and it must be configured before it can be connected to upstream filters.</span></span> <span data-ttu-id="73e0f-123">Il filtro usa il profilo per determinare il tipo di file di formato Windows Media da scrivere, il numero di pin di input da configurare e i tipi di supporti che i pin possono accettare.</span><span class="sxs-lookup"><span data-stu-id="73e0f-123">The filter uses the profile to determine what kind of Windows Media Format file to write, how many input pins to set up, and what media types the pins can accept.</span></span>

<span data-ttu-id="73e0f-124">Il filtro consente di reimpostare i profili mentre i pin di input sono connessi, purché il nuovo profilo non richieda pin di input aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="73e0f-124">The filter allows profiles to be reset while its input pins are connected, as long as the new profile does not require any additional input pins.</span></span> <span data-ttu-id="73e0f-125">Ad esempio, se si modifica il profilo da un profilo audio di input singolo a un profilo audio e video di due input, solo il pin audio sarà reconnectedAll i dati di input devono essere timestamp e tutti i pin di input devono essere connessi prima che il filtro possa essere eseguito o sospeso.</span><span class="sxs-lookup"><span data-stu-id="73e0f-125">For example, if you change the profile from a one-input audio-only profile to a two-input audio and video profile, just the audio pin will be reconnectedAll input data must be time-stamped, and all input pins must be connected before the filter can be run or paused.</span></span> <span data-ttu-id="73e0f-126">Ciò significa che se si configura il filtro con un profilo con un flusso audio e un flusso video, il filtro creerà un pin di input audio e video ed è necessario che entrambi i pin siano connessi prima di poter eseguire il filtro.</span><span class="sxs-lookup"><span data-stu-id="73e0f-126">This means that if you configure the filter with a profile that has an audio stream and a video stream, the filter will create an audio and a video input pin, and both pins must be connected before the filter can be run.</span></span>

<span data-ttu-id="73e0f-127">Aggiunta di estensioni di unità dati</span><span class="sxs-lookup"><span data-stu-id="73e0f-127">Adding Data Unit Extensions</span></span>

<span data-ttu-id="73e0f-128">È possibile configurare un flusso del profilo per le estensioni dell'unità dati, ad esempio i codici temporali SMPTE, prima o dopo la connessione del filtro, purché si segua questo ordine di operazioni:</span><span class="sxs-lookup"><span data-stu-id="73e0f-128">You can configure a profile stream for data unit extensions, such as SMPTE time codes, either before or after the filter is connected, as long as you follow this order of operations:</span></span>

1.  <span data-ttu-id="73e0f-129">Aggiungere una o più estensioni di unità dati al flusso usando [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span><span class="sxs-lookup"><span data-stu-id="73e0f-129">Add one or more data unit extensions to the stream using [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span></span>
2.  <span data-ttu-id="73e0f-130">Chiamare [**WMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) per aggiornare il profilo.</span><span class="sxs-lookup"><span data-stu-id="73e0f-130">Call [**WMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) to update the profile.</span></span>
3.  <span data-ttu-id="73e0f-131">Chiamare [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) con l'oggetto profilo aggiornato.</span><span class="sxs-lookup"><span data-stu-id="73e0f-131">Call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) with the updated profile object.</span></span>
4.  <span data-ttu-id="73e0f-132">Trovare il pin di input del video e chiamare il metodo [**IAMWMBufferPass:: senotify**](iamwmbufferpass-setnotify.md) per registrare l'interfaccia [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73e0f-132">Find the video input pin, and call its [**IAMWMBufferPass::SetNotify**](iamwmbufferpass-setnotify.md) method to register your application-defined [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

<span data-ttu-id="73e0f-133">Quando si esegue il grafo, viene chiamato il metodo [**IAMWMBufferPassCallback:: Notify**](iamwmbufferpasscallback-notify.md) per ogni frame e sarà possibile ottenere e impostare le proprietà nell'esempio usando i relativi metodi di interfaccia [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .</span><span class="sxs-lookup"><span data-stu-id="73e0f-133">When the graph runs, your [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) method will be called for each frame, and you will be able to get and set properties on the sample using its [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface methods.</span></span>

> [!Note]  
> <span data-ttu-id="73e0f-134">In alcuni scenari con utilizzo intensivo del processore, ad esempio la telecine inversa, il writer ASF WM potrebbe richiedere un maggior numero di buffer di output rispetto ad alcuni filtri downstream che possono supportare.</span><span class="sxs-lookup"><span data-stu-id="73e0f-134">In some processor-intensive scenarios such as inverse telecine, the WM ASF Writer may require more output buffers than some downstream filters can support.</span></span> <span data-ttu-id="73e0f-135">Il decodificatore DV, ad esempio, non accetterà più di un buffer per il pin di output e lo stesso vale per il decompressore AVI in determinate condizioni.</span><span class="sxs-lookup"><span data-stu-id="73e0f-135">The DV Decoder, for example, will not accept more than one buffer for its output pin and the same is true for the AVI Decompressor in certain conditions.</span></span> <span data-ttu-id="73e0f-136">Se si verificano problemi durante il tentativo di connessione a questi filtri o quando si esegue il grafo, potrebbe essere necessario scrivere un filtro intermediario che accetti un numero qualsiasi di buffer nel pin di output.</span><span class="sxs-lookup"><span data-stu-id="73e0f-136">If you encounter problems when attempting to connect to these filters, or possibly when running the graph, it may be necessary to write an intermediary filter that accepts any number of buffers on its output pin.</span></span>

 

 

 