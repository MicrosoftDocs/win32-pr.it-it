---
title: Uso dei modelli di conformità dei dispositivi
description: Uso dei modelli di conformità dei dispositivi
ms.assetid: 230744d2-7c0f-4a14-8018-da88b5285add
keywords:
- profili, modelli di conformità del dispositivo
- profili, modelli di conformità
- codec, modelli di conformità del dispositivo
- codec, modelli di conformità
- modelli di conformità del dispositivo, informazioni
- modelli di conformità
- modelli, modelli di conformità dei dispositivi
- ASF (Advanced Systems Format), modelli di conformità dei dispositivi
- ASF (Advanced Systems Format), modelli di conformità dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036d304aa43c0dce5fe4d5302dccc32484657155
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117359"
---
# <a name="working-with-device-conformance-templates"></a><span data-ttu-id="9c0a5-112">Uso dei modelli di conformità dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="9c0a5-112">Working with Device Conformance Templates</span></span>

<span data-ttu-id="9c0a5-113">A causa dell'elevata flessibilità dei file ASF, è spesso difficile determinare se un file è adatto per la riproduzione in un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="9c0a5-113">Because of the great flexibility of ASF files, it is often difficult to determine whether a file is appropriate for playback on a specific device.</span></span> <span data-ttu-id="9c0a5-114">Ad esempio, i file scritti per la riproduzione locale nei computer desktop non sono ottimali per l'utilizzo nei dispositivi palmari.</span><span class="sxs-lookup"><span data-stu-id="9c0a5-114">For example, files written for local playback on desktop computers are not optimal for use on handheld devices.</span></span> <span data-ttu-id="9c0a5-115">I modelli di conformità del dispositivo consentono alle applicazioni di identificare rapidamente il tipo di dispositivo di riproduzione per cui è previsto un file.</span><span class="sxs-lookup"><span data-stu-id="9c0a5-115">Device conformance templates enable applications to quickly identify the type of playback device for which a file was intended.</span></span> <span data-ttu-id="9c0a5-116">Se il modello di conformità del dispositivo non corrisponde al dispositivo, l'applicazione può informare l'utente che il file non è appropriato per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c0a5-116">If the device conformance template does not match the device, the application can inform the user that the file is inappropriate for the device.</span></span> <span data-ttu-id="9c0a5-117">In questo modo, l'utente può garantire una migliore esperienza di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="9c0a5-117">In this way, the user can be assured of a better playback experience.</span></span>

<span data-ttu-id="9c0a5-118">Se i file vengono scritti esclusivamente per l'uso in Personal computer, i modelli di conformità dei dispositivi non saranno più fattori per la creazione di profili.</span><span class="sxs-lookup"><span data-stu-id="9c0a5-118">If you are writing files exclusively for use on personal computers, device conformance templates will not be as much of a factor in creating profiles.</span></span> <span data-ttu-id="9c0a5-119">Lo scopo principale di questi modelli è garantire che i file creati per l'uso con hardware speciale siano compatibili con un intero intervallo di dispositivi e non solo con un singolo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c0a5-119">The main purpose of these templates is to ensure that files created for use with special hardware are compatible with a whole range of devices and not just a single device.</span></span>

<span data-ttu-id="9c0a5-120">Un modello di conformità del dispositivo è un'asserzione che un file ASF contiene dati codificati all'interno di determinati parametri.</span><span class="sxs-lookup"><span data-stu-id="9c0a5-120">A device conformance template is an assertion that an ASF file contains data encoded within certain parameters.</span></span> <span data-ttu-id="9c0a5-121">Per altre informazioni sulle impostazioni appropriate per i singoli modelli, vedere [parametri di modello di conformità del dispositivo](device-conformance-template-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9c0a5-121">For more information about the settings appropriate to the individual templates, see [Device Conformance Template Parameters](device-conformance-template-parameters.md).</span></span>

<span data-ttu-id="9c0a5-122">I codec seguenti supportano i modelli di conformità dei dispositivi:</span><span class="sxs-lookup"><span data-stu-id="9c0a5-122">The following codecs support device conformance templates:</span></span>

-   <span data-ttu-id="9c0a5-123">Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="9c0a5-123">Windows Media Video 9</span></span>
-   <span data-ttu-id="9c0a5-124">Windows Media Audio 9 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="9c0a5-124">Windows Media Audio 9 and later</span></span>
-   <span data-ttu-id="9c0a5-125">Windows Media Audio 9 Professional e versioni successive</span><span class="sxs-lookup"><span data-stu-id="9c0a5-125">Windows Media Audio 9 Professional and later</span></span>
-   <span data-ttu-id="9c0a5-126">Windows Media Audio 9 Voice</span><span class="sxs-lookup"><span data-stu-id="9c0a5-126">Windows Media Audio 9 Voice</span></span>

<span data-ttu-id="9c0a5-127">Non è necessario eseguire alcun passaggio speciale per usare i modelli di conformità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c0a5-127">You do not need to take any special steps to use device conformance templates.</span></span> <span data-ttu-id="9c0a5-128">Il codec scrive automaticamente una stringa di modello per ogni flusso appropriato nel file.</span><span class="sxs-lookup"><span data-stu-id="9c0a5-128">The codec automatically writes a template string for each appropriate stream in the file.</span></span> <span data-ttu-id="9c0a5-129">Il codec deciderà il modello da usare, in base alle impostazioni di configurazione del flusso nel profilo.</span><span class="sxs-lookup"><span data-stu-id="9c0a5-129">The codec will decide which template to use, based on the stream configuration settings in the profile.</span></span> <span data-ttu-id="9c0a5-130">Ci sono alcune sovrapposizioni nei parametri del modello di conformità del dispositivo, quindi è possibile richiedere un modello specifico anziché consentire al codec di assegnarne uno.</span><span class="sxs-lookup"><span data-stu-id="9c0a5-130">There is some overlap in device conformance template parameters, so you may want to request a specific template instead of letting the codec assign one for you.</span></span> <span data-ttu-id="9c0a5-131">È possibile specificare il modello desiderato impostando la proprietà g \_ wszDecoderComplexityRequested con i metodi dell'interfaccia [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) dell'oggetto di configurazione del flusso appropriato.</span><span class="sxs-lookup"><span data-stu-id="9c0a5-131">You can specify which template you want by setting the g\_wszDecoderComplexityRequested property with the methods of the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the appropriate stream configuration object.</span></span>

<span data-ttu-id="9c0a5-132">Quando viene scritto un file ASF, il modello di conformità effettivo del dispositivo per ogni flusso viene impostato sul valore passato al writer dal codec.</span><span class="sxs-lookup"><span data-stu-id="9c0a5-132">When an ASF file is written, the actual device conformance template for each stream is set to the value passed to the writer by the codec.</span></span> <span data-ttu-id="9c0a5-133">Quando si apre un file per la lettura, è possibile individuare il modello a cui i flussi del file sono conformi usando i metodi dell'interfaccia [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) per recuperare l' \_ attributo wszDeviceConformanceTemplate a livello di flusso g.</span><span class="sxs-lookup"><span data-stu-id="9c0a5-133">When opening a file for reading, you can find out which template the streams of the file conform to by using the methods of the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface to retrieve the g\_wszDeviceConformanceTemplate stream-level attribute.</span></span> <span data-ttu-id="9c0a5-134">Per ulteriori informazioni sugli attributi, vedere [utilizzo dei metadati](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="9c0a5-134">For more information about attributes, see [Working with Metadata](working-with-metadata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c0a5-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c0a5-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c0a5-136">**Progettazione di profili**</span><span class="sxs-lookup"><span data-stu-id="9c0a5-136">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> <dt>

[<span data-ttu-id="9c0a5-137">**Parametri del modello di conformità del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="9c0a5-137">**Device Conformance Template Parameters**</span></span>](device-conformance-template-parameters.md)
</dt> </dl>

 

 




