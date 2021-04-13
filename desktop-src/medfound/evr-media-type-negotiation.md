---
description: Negoziazione del tipo di supporto EVR
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: Negoziazione del tipo di supporto EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb1f87a24db866c9e80b211b0385c12dcd6b594
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351456"
---
# <a name="evr-media-type-negotiation"></a><span data-ttu-id="83871-103">Negoziazione del tipo di supporto EVR</span><span class="sxs-lookup"><span data-stu-id="83871-103">EVR Media Type Negotiation</span></span>

<span data-ttu-id="83871-104">In questo argomento viene descritto il modo in cui il renderer video avanzato (EVR) convalida i tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="83871-104">This topic describes how the enhanced video renderer (EVR) validates media types.</span></span>

-   <span data-ttu-id="83871-105">Per il filtro EVR DirectShow, la negoziazione dei tipi si verifica quando i pin del filtro sono connessi.</span><span class="sxs-lookup"><span data-stu-id="83871-105">For the DirectShow EVR filter, type negotiation occurs when the filter's pins are connected.</span></span>

-   <span data-ttu-id="83871-106">Per il sink di supporto EVR, i tipi di supporto vengono impostati tramite l'interfaccia [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) nei sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="83871-106">For the EVR media sink, the media types are set through the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the stream sinks.</span></span> <span data-ttu-id="83871-107">In genere, il caricatore della topologia negozia i tipi di supporto, anche se l'applicazione può anche impostare direttamente i tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="83871-107">Typically the topology loader negotiates the media types, although the application can also set the media types directly.</span></span>

<span data-ttu-id="83871-108">EVR non segnala i tipi di supporto preferiti.</span><span class="sxs-lookup"><span data-stu-id="83871-108">The EVR does not report any preferred media types.</span></span> <span data-ttu-id="83871-109">Il client deve testare i tipi di supporti fino a quando non trova un tipo accettabile.</span><span class="sxs-lookup"><span data-stu-id="83871-109">The client must test media types until it finds an acceptable type.</span></span> <span data-ttu-id="83871-110">Il tipo di supporto per il flusso di riferimento deve essere impostato prima di poter impostare i tipi in uno qualsiasi dei sottoflussi.</span><span class="sxs-lookup"><span data-stu-id="83871-110">The media type for the reference stream must be set before the types can be set on any of the substreams.</span></span>

<span data-ttu-id="83871-111">Per il flusso di riferimento, il mixer EVR ottiene un elenco di formati di destinazione di rendering DXVA (DirectX Video Acceleration) compatibili.</span><span class="sxs-lookup"><span data-stu-id="83871-111">For the reference stream, the EVR mixer gets a list of compatible DirectX Video Acceleration (DXVA) render target formats.</span></span> <span data-ttu-id="83871-112">EVR Presenter utilizza questo elenco per selezionare il formato per la catena di scambio Direct3D.</span><span class="sxs-lookup"><span data-stu-id="83871-112">The EVR presenter uses this list to select the format for the Direct3D swap chain.</span></span> <span data-ttu-id="83871-113">Se non è possibile trovare un formato di destinazione di rendering compatibile, EVR rifiuterà il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="83871-113">If no compatible render target format can be found, the EVR rejects the media type.</span></span>

<span data-ttu-id="83871-114">Per i sottoflussi, il mixer EVR esegue una query per determinare se il dispositivo DXVA supporta tale formato in combinazione con il formato di destinazione di rendering selezionato per il flusso di riferimento.</span><span class="sxs-lookup"><span data-stu-id="83871-114">For the substreams, the EVR mixer queries whether the DXVA device supports that substream format in combination with the render target format that was selected for the reference stream.</span></span> <span data-ttu-id="83871-115">Di conseguenza, i formati dei sottoflussi disponibili possono variare a seconda del flusso di riferimento.</span><span class="sxs-lookup"><span data-stu-id="83871-115">As a result, the available substream formats might change depending on the reference stream.</span></span>

<span data-ttu-id="83871-116">Ecco il processo in modo più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="83871-116">Here is the process in more detail.</span></span> <span data-ttu-id="83871-117">Questi dettagli non sono importanti per la maggior parte delle applicazioni, ma possono essere utili se si sta scrivendo un mixer o un Presenter personalizzato.</span><span class="sxs-lookup"><span data-stu-id="83871-117">These details are not important for most applications, but might be helpful if you are writing a custom mixer or presenter.</span></span>

<span data-ttu-id="83871-118">Per il flusso di riferimento, la negoziazione si verifica nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="83871-118">For the reference stream, negotiation happens as follows:</span></span>

1.  <span data-ttu-id="83871-119">EVR chiama [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) sul mixer.</span><span class="sxs-lookup"><span data-stu-id="83871-119">The EVR calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) on the mixer.</span></span>

2.  <span data-ttu-id="83871-120">Il mixer converte il tipo di supporto in una descrizione di DXVA 2,0, usando la struttura [**\_ VideoDesc di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) .</span><span class="sxs-lookup"><span data-stu-id="83871-120">The mixer converts the media type to a DXVA 2.0 description, using the [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure.</span></span>

3.  <span data-ttu-id="83871-121">Il mixer chiama [**IDirectXVideoProcessorService:: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) per ottenere un elenco di GUID del processore video.</span><span class="sxs-lookup"><span data-stu-id="83871-121">The mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) to get a list of video processor GUIDs.</span></span>

4.  <span data-ttu-id="83871-122">Per ogni GUID del processore video, il mixer chiama [**IDirectXVideoProcessorService:: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) per ottenere i formati di destinazione di rendering supportati.</span><span class="sxs-lookup"><span data-stu-id="83871-122">For each video processor GUID, the mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) to get the supported render target formats.</span></span>

5.  <span data-ttu-id="83871-123">EVR chiama [**IMFVideoPresenter::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) sul Presenter con il messaggio MFVP \_ INVALIDATEMEDIATYPE message \_ .</span><span class="sxs-lookup"><span data-stu-id="83871-123">The EVR calls [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) on the presenter with the MFVP\_MESSAGE\_INVALIDATEMEDIATYPE message.</span></span> <span data-ttu-id="83871-124">Questo messaggio fa in modo che il relatore selezioni un nuovo formato.</span><span class="sxs-lookup"><span data-stu-id="83871-124">This message causes the presenter to select a new format.</span></span>

6.  <span data-ttu-id="83871-125">Il Presenter chiama [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere un elenco dei formati di output disponibili dal mixer.</span><span class="sxs-lookup"><span data-stu-id="83871-125">The presenter calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get a list of available output formats from the mixer.</span></span> <span data-ttu-id="83871-126">Il mixer genera questo elenco dai formati ottenuti nel passaggio 4.</span><span class="sxs-lookup"><span data-stu-id="83871-126">The mixer generates this list from the formats obtained in step 4.</span></span>

7.  <span data-ttu-id="83871-127">Il Presenter seleziona un formato e chiama [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) sul mixer.</span><span class="sxs-lookup"><span data-stu-id="83871-127">The presenter selects a format and calls [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) on the mixer.</span></span>

<span data-ttu-id="83871-128">Per i sottoflussi, il processo è più semplice:</span><span class="sxs-lookup"><span data-stu-id="83871-128">For substreams, the process is simpler:</span></span>

1.  <span data-ttu-id="83871-129">EVR chiama [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) sul mixer.</span><span class="sxs-lookup"><span data-stu-id="83871-129">The EVR calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) on the mixer.</span></span>

2.  <span data-ttu-id="83871-130">Il mixer chiama [**IDirectXVideoProcessorService:: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) per ottenere un elenco dei formati sottoflussi disponibili.</span><span class="sxs-lookup"><span data-stu-id="83871-130">The mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) to get a list of available substream formats.</span></span>

3.  <span data-ttu-id="83871-131">Se il formato proposto è contenuto nell'elenco, EVR accetta il tipo di input.</span><span class="sxs-lookup"><span data-stu-id="83871-131">If the proposed format is contained in this list, the EVR accepts the input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83871-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="83871-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83871-133">Renderer video migliorato</span><span class="sxs-lookup"><span data-stu-id="83871-133">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 



