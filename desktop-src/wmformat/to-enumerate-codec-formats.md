---
title: Per enumerare i formati di codec
description: Per enumerare i formati di codec
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- flussi, enumerazione dei formati di codec
- codec, enumerazioni
- flussi, formati di codec
- codec, formati
- codec, interfaccia IWMCodecInfo
- IWMCodecInfo, formati di codec
- codec, interfaccia IWMCodecInfo3
- IWMCodecInfo3, formati di codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ea062723ec1480a82b45fd025fb7a8c37020d5
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046430"
---
# <a name="to-enumerate-codec-formats"></a><span data-ttu-id="f5a43-111">Per enumerare i formati di codec</span><span class="sxs-lookup"><span data-stu-id="f5a43-111">To Enumerate Codec Formats</span></span>

<span data-ttu-id="f5a43-112">Un formato di codec è un oggetto di configurazione del flusso popolato con i dati di un codec.</span><span class="sxs-lookup"><span data-stu-id="f5a43-112">A codec format is a stream configuration object populated with data from a codec.</span></span> <span data-ttu-id="f5a43-113">Ogni formato di codec contiene una configurazione multimediale supportata dal codec.</span><span class="sxs-lookup"><span data-stu-id="f5a43-113">Each codec format contains a media configuration supported by the codec.</span></span> <span data-ttu-id="f5a43-114">La maggior parte dei codec audio supporta un numero finito di formati, ciascuno dei quali è enumerato dal codec ed è possibile accedervi usando i metodi di [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo).</span><span class="sxs-lookup"><span data-stu-id="f5a43-114">Most audio codecs support a finite number of formats, each of which is enumerated by the codec and can be accessed using the methods of [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo).</span></span> <span data-ttu-id="f5a43-115">I codec video, d'altra parte, forniscono un unico formato.</span><span class="sxs-lookup"><span data-stu-id="f5a43-115">Video codecs, on the other hand, provide only a single format.</span></span> <span data-ttu-id="f5a43-116">Ciò è dovuto al fatto che i flussi video presentano variabili, ad esempio le dimensioni del frame, più flessibili rispetto alle impostazioni di un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="f5a43-116">This is because video streams have variables, like frame size, that are more flexible than the settings of an audio stream.</span></span> <span data-ttu-id="f5a43-117">Con un flusso video, è necessario compilare alcuni valori di configurazione del flusso. è necessario modificare le configurazioni del flusso audio solo per assegnare un nome, un nome di connessione e un numero di flusso.</span><span class="sxs-lookup"><span data-stu-id="f5a43-117">With a video stream, you must fill in some of the stream configuration values; audio stream configurations should only be edited to assign a name, connection name, and stream number.</span></span> <span data-ttu-id="f5a43-118">Per altre informazioni, vedere [configurazione comune a tutti i flussi](configuration-common-to-all-streams.md).</span><span class="sxs-lookup"><span data-stu-id="f5a43-118">For more information, see [Configuration Common to All Streams](configuration-common-to-all-streams.md).</span></span>

<span data-ttu-id="f5a43-119">I formati di codec enumerati dipendono dalle impostazioni correnti di enumerazione dei codec, che vengono impostate usando [**IWMCodecInfo3:: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting).</span><span class="sxs-lookup"><span data-stu-id="f5a43-119">The codec formats enumerated depend upon the current codec enumeration settings, which are set using [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting).</span></span> <span data-ttu-id="f5a43-120">Attualmente sono supportate solo due proprietà del codec: g \_ wszNumPasses, che specifica il numero di sessioni di codifica che verranno eseguite dal codec e g \_ wszVBREnabled, che specifica se il codec userà la codifica della velocità in bit variabile.</span><span class="sxs-lookup"><span data-stu-id="f5a43-120">Currently, only two codec properties are supported: g\_wszNumPasses, which specifies the number of encoding passes that the codec will perform, and g\_wszVBREnabled, which specifies whether the codec will use variable bit rate encoding.</span></span> <span data-ttu-id="f5a43-121">Il numero massimo di passaggi di codifica supportati da uno qualsiasi dei codec è due, quindi sono disponibili quattro configurazioni distinte per le quali è possibile recuperare i codec, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f5a43-121">The maximum number of encoding passes supported by any of the codecs is two, so there are four distinct configurations for which you can retrieve codecs, as shown in the following table.</span></span>



|                  | <span data-ttu-id="f5a43-122">Flusso di velocità in bit costante (CBR)</span><span class="sxs-lookup"><span data-stu-id="f5a43-122">Constant bit rate (CBR) stream</span></span> | <span data-ttu-id="f5a43-123">flusso CBR 2-pass</span><span class="sxs-lookup"><span data-stu-id="f5a43-123">2-pass CBR stream</span></span> | <span data-ttu-id="f5a43-124">Flusso della velocità in bit della variabile basata sulla qualità (VBR)</span><span class="sxs-lookup"><span data-stu-id="f5a43-124">Quality-based variable bit rate (VBR) stream</span></span> | <span data-ttu-id="f5a43-125">Flusso VBR basato sulla velocità in bit (vincolato o non vincolato)</span><span class="sxs-lookup"><span data-stu-id="f5a43-125">Bit-rate-based VBR stream (constrained or unconstrained)</span></span> |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="f5a43-126">g \_ wszVBREnabled</span><span class="sxs-lookup"><span data-stu-id="f5a43-126">g\_wszVBREnabled</span></span> | <span data-ttu-id="f5a43-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="f5a43-127">FALSE</span></span>                          | <span data-ttu-id="f5a43-128">FALSE</span><span class="sxs-lookup"><span data-stu-id="f5a43-128">FALSE</span></span>             | <span data-ttu-id="f5a43-129">TRUE</span><span class="sxs-lookup"><span data-stu-id="f5a43-129">TRUE</span></span>                                         | <span data-ttu-id="f5a43-130">true</span><span class="sxs-lookup"><span data-stu-id="f5a43-130">TRUE</span></span>                                                     |
| <span data-ttu-id="f5a43-131">g \_ wszNumPasses</span><span class="sxs-lookup"><span data-stu-id="f5a43-131">g\_wszNumPasses</span></span>  | <span data-ttu-id="f5a43-132">1</span><span class="sxs-lookup"><span data-stu-id="f5a43-132">1</span></span>                              | <span data-ttu-id="f5a43-133">2</span><span class="sxs-lookup"><span data-stu-id="f5a43-133">2</span></span>                 | <span data-ttu-id="f5a43-134">1</span><span class="sxs-lookup"><span data-stu-id="f5a43-134">1</span></span>                                            | <span data-ttu-id="f5a43-135">2</span><span class="sxs-lookup"><span data-stu-id="f5a43-135">2</span></span>                                                        |



 

<span data-ttu-id="f5a43-136">Per enumerare i formati supportati per un codec, usare [**IWMCodecInfo:: GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) per trovare il numero di codec supportati.</span><span class="sxs-lookup"><span data-stu-id="f5a43-136">To enumerate the formats supported for a codec, use [**IWMCodecInfo::GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) to find the number of supported codecs.</span></span> <span data-ttu-id="f5a43-137">Chiamare quindi [**IWMCodecInfo:: GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) per ogni formato.</span><span class="sxs-lookup"><span data-stu-id="f5a43-137">Then call [**IWMCodecInfo::GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) for each format.</span></span> <span data-ttu-id="f5a43-138">Gli indici di formato variano da zero a uno inferiore al numero totale di formati supportati.</span><span class="sxs-lookup"><span data-stu-id="f5a43-138">The format indexes range from zero, to one less than the total number of supported formats.</span></span> <span data-ttu-id="f5a43-139">È possibile recuperare una descrizione del formato chiamando [**IWMCodecInfo2:: GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc).</span><span class="sxs-lookup"><span data-stu-id="f5a43-139">You can retrieve a description of the format by calling [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc).</span></span> <span data-ttu-id="f5a43-140">Quando si usa **GetCodecFormatDesc**, non è necessario usare **GetCodecFormat**, perché l'oggetto di configurazione del flusso viene recuperato da entrambi i metodi.</span><span class="sxs-lookup"><span data-stu-id="f5a43-140">When using **GetCodecFormatDesc**, you do not need to use **GetCodecFormat**, because the stream configuration object is retrieved by both methods.</span></span> <span data-ttu-id="f5a43-141">I formati di codec video non includono una descrizione.</span><span class="sxs-lookup"><span data-stu-id="f5a43-141">Video codec formats do not include a description.</span></span> <span data-ttu-id="f5a43-142">Ogni codec video ha un solo formato utilizzato per tutti i flussi di quel tipo.</span><span class="sxs-lookup"><span data-stu-id="f5a43-142">Each video codec has only one format that is used for all streams of that type.</span></span>

<span data-ttu-id="f5a43-143">Quando si recupera un formato di codec, si ottiene l'interfaccia [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) di un oggetto di configurazione del flusso contenente le impostazioni di formato.</span><span class="sxs-lookup"><span data-stu-id="f5a43-143">When you retrieve a codec format, you get the [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) interface of a stream configuration object containing the format settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5a43-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5a43-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5a43-145">**Recupero delle informazioni di configurazione dei flussi dai codec**</span><span class="sxs-lookup"><span data-stu-id="f5a43-145">**Getting Stream Configuration Information from Codecs**</span></span>](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




