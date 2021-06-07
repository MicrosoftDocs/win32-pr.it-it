---
title: Per enumerare i formati di codec
description: Per enumerare i formati di codec
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- flussi, enumerazione dei formati di codec
- codec, enumerazioni
- flussi, formati di codec
- codec, formati
- codecs,interfaccia IWMCodecInfo
- IWMCodecInfo,formati codec
- codecs,interfaccia IWMCodecInfo3
- IWMCodecInfo3,formati codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a00c9afdbeba5a187be4b992a19d4c9bdb138e1
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444782"
---
# <a name="to-enumerate-codec-formats"></a><span data-ttu-id="bfcde-111">Per enumerare i formati di codec</span><span class="sxs-lookup"><span data-stu-id="bfcde-111">To Enumerate Codec Formats</span></span>

<span data-ttu-id="bfcde-112">Un formato codec è un oggetto di configurazione del flusso popolato con i dati di un codec.</span><span class="sxs-lookup"><span data-stu-id="bfcde-112">A codec format is a stream configuration object populated with data from a codec.</span></span> <span data-ttu-id="bfcde-113">Ogni formato di codec contiene una configurazione multimediale supportata dal codec.</span><span class="sxs-lookup"><span data-stu-id="bfcde-113">Each codec format contains a media configuration supported by the codec.</span></span> <span data-ttu-id="bfcde-114">La maggior parte dei codec audio supporta un numero finito di formati, ognuno dei quali viene enumerato dal codec ed è accessibile tramite i metodi [**di IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo).</span><span class="sxs-lookup"><span data-stu-id="bfcde-114">Most audio codecs support a finite number of formats, each of which is enumerated by the codec and can be accessed using the methods of [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo).</span></span> <span data-ttu-id="bfcde-115">I codec video, d'altra parte, forniscono un solo formato.</span><span class="sxs-lookup"><span data-stu-id="bfcde-115">Video codecs, on the other hand, provide only a single format.</span></span> <span data-ttu-id="bfcde-116">Questo perché i flussi video hanno variabili, come le dimensioni dei fotogrammi, più flessibili rispetto alle impostazioni di un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="bfcde-116">This is because video streams have variables, like frame size, that are more flexible than the settings of an audio stream.</span></span> <span data-ttu-id="bfcde-117">Con un flusso video, è necessario compilare alcuni dei valori di configurazione del flusso. Le configurazioni del flusso audio devono essere modificate solo per assegnare un nome, un nome di connessione e un numero di flusso.</span><span class="sxs-lookup"><span data-stu-id="bfcde-117">With a video stream, you must fill in some of the stream configuration values; audio stream configurations should only be edited to assign a name, connection name, and stream number.</span></span> <span data-ttu-id="bfcde-118">Per altre informazioni, vedere [Configurazione comune a tutti i flussi.](configuration-common-to-all-streams.md)</span><span class="sxs-lookup"><span data-stu-id="bfcde-118">For more information, see [Configuration Common to All Streams](configuration-common-to-all-streams.md).</span></span>

<span data-ttu-id="bfcde-119">I formati di codec enumerati dipendono dalle impostazioni correnti dell'enumerazione dei codec, impostate tramite [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting).</span><span class="sxs-lookup"><span data-stu-id="bfcde-119">The codec formats enumerated depend upon the current codec enumeration settings, which are set using [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting).</span></span> <span data-ttu-id="bfcde-120">Attualmente sono supportate solo due proprietà del codec: g wszNumPasses, che specifica il numero di passaggi di codifica che il codec eseguirà, e \_ g wszVBREnabled, che specifica se il codec userà la codifica a velocità in \_ bit variabile.</span><span class="sxs-lookup"><span data-stu-id="bfcde-120">Currently, only two codec properties are supported: g\_wszNumPasses, which specifies the number of encoding passes that the codec will perform, and g\_wszVBREnabled, which specifies whether the codec will use variable bit rate encoding.</span></span> <span data-ttu-id="bfcde-121">Il numero massimo di passaggi di codifica supportati da uno dei codec è due, quindi sono disponibili quattro configurazioni distinte per cui è possibile recuperare i codec, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="bfcde-121">The maximum number of encoding passes supported by any of the codecs is two, so there are four distinct configurations for which you can retrieve codecs, as shown in the following table.</span></span>



|    &nbsp;    | <span data-ttu-id="bfcde-122">Flusso CBR (Constant Bit Rate)</span><span class="sxs-lookup"><span data-stu-id="bfcde-122">Constant bit rate (CBR) stream</span></span> | <span data-ttu-id="bfcde-123">Flusso CBR a 2 passi</span><span class="sxs-lookup"><span data-stu-id="bfcde-123">2-pass CBR stream</span></span> | <span data-ttu-id="bfcde-124">Flusso VBR (Quality-Based Variable Bit Rate)</span><span class="sxs-lookup"><span data-stu-id="bfcde-124">Quality-based variable bit rate (VBR) stream</span></span> | <span data-ttu-id="bfcde-125">Flusso VBR basato su velocità in bit (vincolato o senza vincoli)</span><span class="sxs-lookup"><span data-stu-id="bfcde-125">Bit-rate-based VBR stream (constrained or unconstrained)</span></span> |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="bfcde-126">g \_ wszVBREnabled</span><span class="sxs-lookup"><span data-stu-id="bfcde-126">g\_wszVBREnabled</span></span> | <span data-ttu-id="bfcde-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="bfcde-127">FALSE</span></span>                          | <span data-ttu-id="bfcde-128">FALSE</span><span class="sxs-lookup"><span data-stu-id="bfcde-128">FALSE</span></span>             | <span data-ttu-id="bfcde-129">TRUE</span><span class="sxs-lookup"><span data-stu-id="bfcde-129">TRUE</span></span>                                         | <span data-ttu-id="bfcde-130">true</span><span class="sxs-lookup"><span data-stu-id="bfcde-130">TRUE</span></span>                                                     |
| <span data-ttu-id="bfcde-131">g \_ wszNumPasses</span><span class="sxs-lookup"><span data-stu-id="bfcde-131">g\_wszNumPasses</span></span>  | <span data-ttu-id="bfcde-132">1</span><span class="sxs-lookup"><span data-stu-id="bfcde-132">1</span></span>                              | <span data-ttu-id="bfcde-133">2</span><span class="sxs-lookup"><span data-stu-id="bfcde-133">2</span></span>                 | <span data-ttu-id="bfcde-134">1</span><span class="sxs-lookup"><span data-stu-id="bfcde-134">1</span></span>                                            | <span data-ttu-id="bfcde-135">2</span><span class="sxs-lookup"><span data-stu-id="bfcde-135">2</span></span>                                                        |



 

<span data-ttu-id="bfcde-136">Per enumerare i formati supportati per un codec, usare [**IWMCodecInfo::GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) per trovare il numero di codec supportati.</span><span class="sxs-lookup"><span data-stu-id="bfcde-136">To enumerate the formats supported for a codec, use [**IWMCodecInfo::GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) to find the number of supported codecs.</span></span> <span data-ttu-id="bfcde-137">Chiamare quindi [**IWMCodecInfo::GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) per ogni formato.</span><span class="sxs-lookup"><span data-stu-id="bfcde-137">Then call [**IWMCodecInfo::GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) for each format.</span></span> <span data-ttu-id="bfcde-138">Gli indici di formato vanno da zero a uno minore del numero totale di formati supportati.</span><span class="sxs-lookup"><span data-stu-id="bfcde-138">The format indexes range from zero, to one less than the total number of supported formats.</span></span> <span data-ttu-id="bfcde-139">È possibile recuperare una descrizione del formato chiamando [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc).</span><span class="sxs-lookup"><span data-stu-id="bfcde-139">You can retrieve a description of the format by calling [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc).</span></span> <span data-ttu-id="bfcde-140">Quando si **usa GetCodecFormatDesc**, non è necessario usare **GetCodecFormat**, perché l'oggetto di configurazione del flusso viene recuperato da entrambi i metodi.</span><span class="sxs-lookup"><span data-stu-id="bfcde-140">When using **GetCodecFormatDesc**, you do not need to use **GetCodecFormat**, because the stream configuration object is retrieved by both methods.</span></span> <span data-ttu-id="bfcde-141">I formati di codec video non includono una descrizione.</span><span class="sxs-lookup"><span data-stu-id="bfcde-141">Video codec formats do not include a description.</span></span> <span data-ttu-id="bfcde-142">Ogni codec video ha un solo formato usato per tutti i flussi di quel tipo.</span><span class="sxs-lookup"><span data-stu-id="bfcde-142">Each video codec has only one format that is used for all streams of that type.</span></span>

<span data-ttu-id="bfcde-143">Quando si recupera un formato codec, si ottiene [**l'interfaccia IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) di un oggetto di configurazione del flusso contenente le impostazioni del formato.</span><span class="sxs-lookup"><span data-stu-id="bfcde-143">When you retrieve a codec format, you get the [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) interface of a stream configuration object containing the format settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfcde-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bfcde-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfcde-145">**Recupero delle informazioni di configurazione del flusso dai codec**</span><span class="sxs-lookup"><span data-stu-id="bfcde-145">**Getting Stream Configuration Information from Codecs**</span></span>](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




