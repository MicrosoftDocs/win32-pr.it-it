---
description: In questo argomento vengono fornite alcune linee guida per l'implementazione di un decodificatore o un codificatore come Media Foundation Transform (MFT).
ms.assetid: b15bda0a-0fdd-4601-975d-a71c47c974bf
title: Implementazione di un codec MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4412db23747e9a6b3468e9e428120d099b2445ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233748"
---
# <a name="implementing-a-codec-mft"></a><span data-ttu-id="bebac-103">Implementazione di un codec MFT</span><span class="sxs-lookup"><span data-stu-id="bebac-103">Implementing a Codec MFT</span></span>

<span data-ttu-id="bebac-104">In questo argomento vengono fornite alcune linee guida per l'implementazione di un decodificatore o un codificatore come Media Foundation Transform (MFT).</span><span class="sxs-lookup"><span data-stu-id="bebac-104">This topic provides some guidelines for implementing a decoder or encoder as a Media Foundation Transform (MFT) .</span></span>

-   [<span data-ttu-id="bebac-105">Codificatori</span><span class="sxs-lookup"><span data-stu-id="bebac-105">Encoders</span></span>](#encoders)
    -   [<span data-ttu-id="bebac-106">Negoziazione del formato del codificatore</span><span class="sxs-lookup"><span data-stu-id="bebac-106">Encoder Format Negotiation</span></span>](#encoder-format-negotiation)
-   [<span data-ttu-id="bebac-107">Decodificatori</span><span class="sxs-lookup"><span data-stu-id="bebac-107">Decoders</span></span>](#decoders)
    -   [<span data-ttu-id="bebac-108">Decodificatori solo transcodificati</span><span class="sxs-lookup"><span data-stu-id="bebac-108">Transcode-Only Decoders</span></span>](#transcode-only-decoders)
    -   [<span data-ttu-id="bebac-109">Attributi di telecine</span><span class="sxs-lookup"><span data-stu-id="bebac-109">Telecine Attributes</span></span>](#telecine-attributes)
-   [<span data-ttu-id="bebac-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bebac-110">Related topics</span></span>](#related-topics)

## <a name="encoders"></a><span data-ttu-id="bebac-111">Codificatori</span><span class="sxs-lookup"><span data-stu-id="bebac-111">Encoders</span></span>

### <a name="encoder-format-negotiation"></a><span data-ttu-id="bebac-112">Negoziazione del formato del codificatore</span><span class="sxs-lookup"><span data-stu-id="bebac-112">Encoder Format Negotiation</span></span>

<span data-ttu-id="bebac-113">La procedura seguente viene usata per inizializzare un codificatore:</span><span class="sxs-lookup"><span data-stu-id="bebac-113">The following procedure is used to initialize an encoder:</span></span>

1.  <span data-ttu-id="bebac-114">Eseguire una query su MFT per l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="bebac-114">Query the MFT for the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>
2.  <span data-ttu-id="bebac-115">Chiamare [**ICodecAPI:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) per impostare le proprietà di codifica.</span><span class="sxs-lookup"><span data-stu-id="bebac-115">Call [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) to set encoding properties.</span></span>
3.  <span data-ttu-id="bebac-116">Chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare il formato di codifica.</span><span class="sxs-lookup"><span data-stu-id="bebac-116">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the encoding format.</span></span>
4.  <span data-ttu-id="bebac-117">Chiamare [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) per ottenere un elenco di tipi di input compatibili.</span><span class="sxs-lookup"><span data-stu-id="bebac-117">Call [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) to get a list of compatible input types.</span></span> <span data-ttu-id="bebac-118">Questo passaggio potrebbe essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="bebac-118">(This step might be skipped.)</span></span>
5.  <span data-ttu-id="bebac-119">Chiamare [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) per impostare il formato di input non compresso.</span><span class="sxs-lookup"><span data-stu-id="bebac-119">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the uncompressed input format.</span></span>

<span data-ttu-id="bebac-120">Dopo aver impostato il tipo di output nel passaggio 3, il metodo [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) deve restituire un elenco di tipi di input compatibili con il tipo di output corrente.</span><span class="sxs-lookup"><span data-stu-id="bebac-120">After the output type is set in step 3, the [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) method must return a list of input types that are compatible with the current output type.</span></span> <span data-ttu-id="bebac-121">In altre parole, qualsiasi tipo restituito da **GetInputAvailableType** a questo punto deve essere valido per [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span><span class="sxs-lookup"><span data-stu-id="bebac-121">In other words, any types returned by **GetInputAvailableType** at this point must be valid for [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span>

<span data-ttu-id="bebac-122">Per i decodificatori, l'ordine in cui vengono impostati i tipi è invertito: il tipo di input è impostato per primo, seguito dal tipo di output.</span><span class="sxs-lookup"><span data-stu-id="bebac-122">For decoders, the order in which types are set is reversed: The input type is set first, followed by the output type.</span></span> <span data-ttu-id="bebac-123">Dopo aver impostato il tipo di input, il metodo [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) deve restituire un elenco di tipi che possono essere passati al metodo [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) .</span><span class="sxs-lookup"><span data-stu-id="bebac-123">After the input type is set, the [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method must return a list of types that can be passed to the [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) method.</span></span>

<span data-ttu-id="bebac-124">I codificatori e i decodificatori devono supportare NV12 come formato non compresso comune.</span><span class="sxs-lookup"><span data-stu-id="bebac-124">Encoders and decoders should support NV12 as a common uncompressed format.</span></span> <span data-ttu-id="bebac-125">Ciò garantisce che i componenti della pipeline possano interagire con le conversioni minime dello spazio dei tipi.</span><span class="sxs-lookup"><span data-stu-id="bebac-125">This ensures that pipeline components can interoperate with minimal colorspace conversions.</span></span> <span data-ttu-id="bebac-126">Naturalmente, anche altri formati possono essere supportati.</span><span class="sxs-lookup"><span data-stu-id="bebac-126">Of course, other formats can be supported as well.</span></span>

## <a name="decoders"></a><span data-ttu-id="bebac-127">Decodificatori</span><span class="sxs-lookup"><span data-stu-id="bebac-127">Decoders</span></span>

### <a name="transcode-only-decoders"></a><span data-ttu-id="bebac-128">Decodificatori di Transcode-Only</span><span class="sxs-lookup"><span data-stu-id="bebac-128">Transcode-Only Decoders</span></span>

<span data-ttu-id="bebac-129">Alcuni decodificatori sono ottimizzati per la transcodifica (decodifica e Ricodifica di un flusso) e non sono adatti per l'uso durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="bebac-129">Some decoders are optimized for transcoding (decoding and then re-encoding a stream) and are not suitable for use during playback.</span></span>

<span data-ttu-id="bebac-130">Se un decodificatore MFT è destinato solo alla transcodifica, impostare il flag dell' **\_ enumerazione MFT \_ flag \_ transcode \_ only** quando si registra il MFT.</span><span class="sxs-lookup"><span data-stu-id="bebac-130">If a decoder MFT is intended only for transcoding, set the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag when you register the MFT.</span></span> <span data-ttu-id="bebac-131">Vedere [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).</span><span class="sxs-lookup"><span data-stu-id="bebac-131">(See [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).)</span></span>

<span data-ttu-id="bebac-132">Per impostazione predefinita, i decodificatori di transcodifica non vengono restituiti dalla funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="bebac-132">By default, transcode decoders are not returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span> <span data-ttu-id="bebac-133">Per enumerare i decodificatori di transcodifica, chiamare **MFTEnumEx** e impostare il flag di **enumerazione del \_ flag di enumerazione \_ \_ \_ MFT** nel parametro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="bebac-133">To enumerate transcode decoders, call **MFTEnumEx** and set the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag in *Flags* parameter.</span></span> <span data-ttu-id="bebac-134">Se utilizzata nella funzione **MFTEnumEx** , questo flag enumera sia i decodificatori transcodificati che altri decodificatori.</span><span class="sxs-lookup"><span data-stu-id="bebac-134">When used in the **MFTEnumEx** function, this flag enumerated both transcode decoders and other decoders.</span></span>



| <span data-ttu-id="bebac-135">**\_ \_ \_ \_ Solo transcodifica flag di enumerazione MFT** MFTRegister</span><span class="sxs-lookup"><span data-stu-id="bebac-135">MFTRegister **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY**</span></span> | <span data-ttu-id="bebac-136">**\_ \_ \_ \_ Solo transcodifica flag di enumerazione MFT** MFTEnumEx</span><span class="sxs-lookup"><span data-stu-id="bebac-136">MFTEnumEx **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY**</span></span> | <span data-ttu-id="bebac-137">Il MFT è enumerato?</span><span class="sxs-lookup"><span data-stu-id="bebac-137">Is MFT Enumerated?</span></span> |
|--------------------------------------------------|------------------------------------------------|--------------------|
| <span data-ttu-id="bebac-138">1</span><span class="sxs-lookup"><span data-stu-id="bebac-138">1</span></span>                                                | <span data-ttu-id="bebac-139">1</span><span class="sxs-lookup"><span data-stu-id="bebac-139">1</span></span>                                              | <span data-ttu-id="bebac-140">Sì</span><span class="sxs-lookup"><span data-stu-id="bebac-140">Yes</span></span>                |
| <span data-ttu-id="bebac-141">1</span><span class="sxs-lookup"><span data-stu-id="bebac-141">1</span></span>                                                | <span data-ttu-id="bebac-142">0</span><span class="sxs-lookup"><span data-stu-id="bebac-142">0</span></span>                                              | <span data-ttu-id="bebac-143">No</span><span class="sxs-lookup"><span data-stu-id="bebac-143">No</span></span>                 |
| <span data-ttu-id="bebac-144">0</span><span class="sxs-lookup"><span data-stu-id="bebac-144">0</span></span>                                                | <span data-ttu-id="bebac-145">1</span><span class="sxs-lookup"><span data-stu-id="bebac-145">1</span></span>                                              | <span data-ttu-id="bebac-146">Sì</span><span class="sxs-lookup"><span data-stu-id="bebac-146">Yes</span></span>                |
| <span data-ttu-id="bebac-147">0</span><span class="sxs-lookup"><span data-stu-id="bebac-147">0</span></span>                                                | <span data-ttu-id="bebac-148">0</span><span class="sxs-lookup"><span data-stu-id="bebac-148">0</span></span>                                              | <span data-ttu-id="bebac-149">Sì</span><span class="sxs-lookup"><span data-stu-id="bebac-149">Yes</span></span>                |



 

### <a name="telecine-attributes"></a><span data-ttu-id="bebac-150">Attributi di telecine</span><span class="sxs-lookup"><span data-stu-id="bebac-150">Telecine Attributes</span></span>

<span data-ttu-id="bebac-151">L'origine multimediale potrebbe alleghi gli attributi di telecine seguenti agli esempi di supporti che fornisce.</span><span class="sxs-lookup"><span data-stu-id="bebac-151">The media source might attach the following telecine attributes to the media samples that it delivers.</span></span>



| <span data-ttu-id="bebac-152">Attributo</span><span class="sxs-lookup"><span data-stu-id="bebac-152">Attribute</span></span>                                                                                   | <span data-ttu-id="bebac-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bebac-153">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="bebac-154">**\_RepeatFirstField MFSampleExtension**</span><span class="sxs-lookup"><span data-stu-id="bebac-154">**MFSampleExtension\_RepeatFirstField**</span></span>](mfsampleextension-repeatfirstfield-attribute.md) | <span data-ttu-id="bebac-155">Equivalente al flag "Repeat First Field" (RFF).</span><span class="sxs-lookup"><span data-stu-id="bebac-155">Equivalent to "repeat first field" (RFF) flag.</span></span> |
| [<span data-ttu-id="bebac-156">**\_BottomFieldFirst MFSampleExtension**</span><span class="sxs-lookup"><span data-stu-id="bebac-156">**MFSampleExtension\_BottomFieldFirst**</span></span>](mfsampleextension-bottomfieldfirst-attribute.md) | <span data-ttu-id="bebac-157">Inverso del flag "Top Field First" (TFF).</span><span class="sxs-lookup"><span data-stu-id="bebac-157">Inverse of "top field first" (TFF) flag.</span></span>       |



 

<span data-ttu-id="bebac-158">Questi flag forniscono un suggerimento al renderer video migliorato (EVR) quando esegue il deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="bebac-158">These flags provide a hint to the enhanced video renderer (EVR) when it performs deinterlacing.</span></span> <span data-ttu-id="bebac-159">Un decodificatore deve propagare questi flag downstream copiando gli esempi di output, in modo che raggiungano la EVR.</span><span class="sxs-lookup"><span data-stu-id="bebac-159">A decoder should propagate these flags downstream by copying them to the output samples, so that they reach the EVR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bebac-160">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bebac-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bebac-161">Scrittura di un MFT personalizzato</span><span class="sxs-lookup"><span data-stu-id="bebac-161">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
