---
description: Un codificatore converte audio o video non compressi in pacchetti compressi nel formato specificato dall'applicazione. Per convertire i file multimediali in formato ASF, è possibile usare i codec audio e video di Windows Media.
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Codificatori Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a642702562cbb6a70b0380deb196c70c4f8207b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320557"
---
# <a name="windows-media-encoders"></a><span data-ttu-id="d553a-104">Codificatori Windows Media</span><span class="sxs-lookup"><span data-stu-id="d553a-104">Windows Media Encoders</span></span>

<span data-ttu-id="d553a-105">Un codificatore converte audio o video non compressi in pacchetti compressi nel formato specificato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d553a-105">An encoder converts uncompressed audio or video into compressed packets in the format specified by the application.</span></span> <span data-ttu-id="d553a-106">Per convertire i file multimediali in formato ASF, è possibile usare i codec audio e video di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d553a-106">For converting media files into ASF format, you can use the Windows Media audio and video codecs.</span></span>

<span data-ttu-id="d553a-107">Un codificatore viene identificato dal GUID che rappresenta la categoria: audio o video.</span><span class="sxs-lookup"><span data-stu-id="d553a-107">An encoder is identified by the GUID that represents the category: audio or video.</span></span> <span data-ttu-id="d553a-108">Il tipo di output del codificatore è rappresentato da un elemento principale del tipo di supporto e dal GUID del sottotipo.</span><span class="sxs-lookup"><span data-stu-id="d553a-108">The encoder's output type is represented by a media type's major and the sub type GUID.</span></span>

-   <span data-ttu-id="d553a-109">Codec audio Windows Media</span><span class="sxs-lookup"><span data-stu-id="d553a-109">Windows Media audio codecs</span></span>

    <span data-ttu-id="d553a-110">Categoria: **\_ \_ \_ codificatore audio della categoria MFT**</span><span class="sxs-lookup"><span data-stu-id="d553a-110">Category: **MFT\_CATEGORY\_AUDIO\_ENCODER**</span></span>

    <span data-ttu-id="d553a-111">Tipo principale: MFMediaType \_ audio</span><span class="sxs-lookup"><span data-stu-id="d553a-111">Major type: MFMediaType\_Audio</span></span>

    <span data-ttu-id="d553a-112">Sottotipo: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF</span><span class="sxs-lookup"><span data-stu-id="d553a-112">SubType: MFAudioFormat\_WMAudioV9, MFAudioFormat\_WMAudioV8, MFAudioFormat\_WMAudio\_Lossless, MFAudioFormat\_WMASPDIF</span></span>

-   <span data-ttu-id="d553a-113">Codec video di Windows Media</span><span class="sxs-lookup"><span data-stu-id="d553a-113">Windows Media video codecs</span></span>

    <span data-ttu-id="d553a-114">Categoria: **\_ \_ \_ codificatore video della categoria MFT**</span><span class="sxs-lookup"><span data-stu-id="d553a-114">Category: **MFT\_CATEGORY\_VIDEO\_ENCODER**</span></span>

    <span data-ttu-id="d553a-115">Tipo principale: video di MFMediaType \_</span><span class="sxs-lookup"><span data-stu-id="d553a-115">Major type: MFMediaType\_Video</span></span>

    <span data-ttu-id="d553a-116">Sottotipo: MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat WMV2 \_ , MFVideoFormat \_ WMV1</span><span class="sxs-lookup"><span data-stu-id="d553a-116">SubType: MFVideoFormat\_WVC1, MFVideoFormat\_WMV3, MFVideoFormat\_WMV2, MFVideoFormat\_WMV1</span></span>

<span data-ttu-id="d553a-117">Questi codificatori vengono implementati come [Media Foundation Transform](media-foundation-transforms.md) (MFT) e Media Foundation forniscono l'accesso all'applicazione tramite l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) del codificatore.</span><span class="sxs-lookup"><span data-stu-id="d553a-117">These encoders are implemented as [Media Foundation transform](media-foundation-transforms.md) (MFT) and Media Foundation provides access to the application through the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface of the encoder.</span></span> <span data-ttu-id="d553a-118">Se si usano componenti del livello pipeline per la codifica ASF, il codificatore MFT viene inserito nella pipeline come nodo di trasformazione perché è responsabile della trasformazione dei dati multimediali che passano attraverso l'origine al sink.</span><span class="sxs-lookup"><span data-stu-id="d553a-118">If you are using pipeline layer components for ASF encoding, the encoder MFT is inserted into the pipeline as a transform node because it is responsible for transforming media data that flows through the source to the sink.</span></span> <span data-ttu-id="d553a-119">Se l'origine è un tipo compresso, la pipeline aggiunge i decodificatori necessari per convertire l'origine in un tipo non compresso.</span><span class="sxs-lookup"><span data-stu-id="d553a-119">If the source is a compressed type, then the pipeline adds the required decoders to convert the source into an uncompressed type.</span></span> <span data-ttu-id="d553a-120">Un codificatore ha un flusso di input e un flusso di output.</span><span class="sxs-lookup"><span data-stu-id="d553a-120">An encoder has one input stream and one output stream.</span></span> <span data-ttu-id="d553a-121">Il codificatore riceve i dati di input e produce dati codificati in base alla configurazione e al formato impostati dall'applicazione prima della sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="d553a-121">The encoder receives input data and produces encoded data according to the configuration and format set by the application prior to the encoding session.</span></span> <span data-ttu-id="d553a-122">Il formato del flusso di output è descritto da un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="d553a-122">The format of the output stream is described by a media type.</span></span>

<span data-ttu-id="d553a-123">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="d553a-123">This section contains the following topics.</span></span>



| <span data-ttu-id="d553a-124">Argomento</span><span class="sxs-lookup"><span data-stu-id="d553a-124">Topic</span></span>                                                                              | <span data-ttu-id="d553a-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d553a-125">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d553a-126">Creazione di un'istanza di un codificatore MFT</span><span class="sxs-lookup"><span data-stu-id="d553a-126">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)                  | <span data-ttu-id="d553a-127">Viene illustrato come creare il codificatore.</span><span class="sxs-lookup"><span data-stu-id="d553a-127">Explains how to create the encoder.</span></span>                                                         |
| [<span data-ttu-id="d553a-128">Proprietà di codifica</span><span class="sxs-lookup"><span data-stu-id="d553a-128">Encoding Properties</span></span>](configuring-the-encoder.md)                                 | <span data-ttu-id="d553a-129">Viene illustrato come configurare il codificatore impostando le proprietà appropriate nel codificatore MFT.</span><span class="sxs-lookup"><span data-stu-id="d553a-129">Explains how to configure the encoder by setting appropriate properties on the encoder MFT.</span></span> |
| [<span data-ttu-id="d553a-130">Negoziazione del tipo di supporto sul codificatore</span><span class="sxs-lookup"><span data-stu-id="d553a-130">Media Type Negotiation on the Encoder</span></span>](media-type-negotiation-on-the-encoder.md) | <span data-ttu-id="d553a-131">Viene illustrato come impostare i tipi di supporto di input e di output nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="d553a-131">Explains how to set input and output media types on the encoder.</span></span>                            |
| [<span data-ttu-id="d553a-132">Configurazione di un codificatore WMV</span><span class="sxs-lookup"><span data-stu-id="d553a-132">Configuring a WMV Encoder</span></span>](configuring-a-wmv-encoder.md)                         | <span data-ttu-id="d553a-133">Viene illustrato come configurare un codificatore Windows Media Video (WMV).</span><span class="sxs-lookup"><span data-stu-id="d553a-133">Explains how to configure a Windows Media Video (WMV) encoder.</span></span>                              |
| [<span data-ttu-id="d553a-134">Impostazione di un tipo di output per un codificatore WMA</span><span class="sxs-lookup"><span data-stu-id="d553a-134">Setting an Output Type for a WMA Encoder</span></span>](configuring-a-wma-encoder.md)          | <span data-ttu-id="d553a-135">Viene illustrato come impostare un tipo di output in un codificatore Windows Media Audio (WMA).</span><span class="sxs-lookup"><span data-stu-id="d553a-135">Explains how to set an output type on a Windows Media Audio (WMA) encoder.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="d553a-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d553a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d553a-137">Componenti ASF a livello pipeline</span><span class="sxs-lookup"><span data-stu-id="d553a-137">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



