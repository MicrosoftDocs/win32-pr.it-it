---
description: Visualizzazione di didascalie chiuse
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Visualizzazione di didascalie chiuse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ff2d6d213259ccce6e9b02272d0c9db3ad7b71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558056"
---
# <a name="viewing-closed-captions"></a><span data-ttu-id="f5b67-103">Visualizzazione di didascalie chiuse</span><span class="sxs-lookup"><span data-stu-id="f5b67-103">Viewing Closed Captions</span></span>

<span data-ttu-id="f5b67-104">Per supportare le didascalie chiuse nella televisione analoga, il filtro di acquisizione espone un pin che recapita i dati di VBI o della didascalia chiusa.</span><span class="sxs-lookup"><span data-stu-id="f5b67-104">To support closed captions in analog television, the capture filter exposes a pin that delivers either VBI or closed caption data.</span></span> <span data-ttu-id="f5b67-105">Il pin avrà una delle categorie di pin seguenti:</span><span class="sxs-lookup"><span data-stu-id="f5b67-105">The pin will have one of the following pin categories:</span></span>

-   <span data-ttu-id="f5b67-106">Pin VBI (PIN \_ Category \_ VBI).</span><span class="sxs-lookup"><span data-stu-id="f5b67-106">VBI pin (PIN\_CATEGORY\_VBI).</span></span> <span data-ttu-id="f5b67-107">Fornisce un flusso di esempi di forma d'onda VBI.</span><span class="sxs-lookup"><span data-stu-id="f5b67-107">Delivers a stream of VBI waveform samples.</span></span> <span data-ttu-id="f5b67-108">Questi vengono passati a un filtro decodificatore che estrae i dati di didascalia chiusi.</span><span class="sxs-lookup"><span data-stu-id="f5b67-108">These are passed to a decoder filter that extracts the closed captioning data.</span></span>
-   <span data-ttu-id="f5b67-109">Pin CC ( \_ categoria pin \_ CC).</span><span class="sxs-lookup"><span data-stu-id="f5b67-109">CC pin (PIN\_CATEGORY\_CC).</span></span> <span data-ttu-id="f5b67-110">Recapita le coppie di byte con didascalia chiusa, estratti dai dati riga 21.</span><span class="sxs-lookup"><span data-stu-id="f5b67-110">Delivers closed-caption byte pairs, extracted from the line-21 data.</span></span>
-   <span data-ttu-id="f5b67-111">Hardware slicing CC pin (PINNAME \_ video \_ CC \_ Capture).</span><span class="sxs-lookup"><span data-stu-id="f5b67-111">Hardware slicing CC pin (PINNAME\_VIDEO\_CC\_CAPTURE).</span></span>

<span data-ttu-id="f5b67-112">Per visualizzare in anteprima le didascalie chiuse, chiamare [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con la categoria pin VBI e, in caso di errore, richiamarla con la categoria CC.</span><span class="sxs-lookup"><span data-stu-id="f5b67-112">To preview closed captions, call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the VBI pin category, and if that fails, call it again with the CC category.</span></span>


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



<span data-ttu-id="f5b67-113">Il diagramma seguente illustra un tipico grafico di filtro per la visualizzazione di didascalie chiuse.</span><span class="sxs-lookup"><span data-stu-id="f5b67-113">The following diagram shows a typical filter graph for displaying closed captions.</span></span>

![grafico di anteprima sottotitoli codificati](images/vidcap08.png)

<span data-ttu-id="f5b67-115">Questo grafico usa i filtri seguenti per la visualizzazione dei sottotitoli chiusi:</span><span class="sxs-lookup"><span data-stu-id="f5b67-115">This graph uses the following filters for closed caption display:</span></span>

-   <span data-ttu-id="f5b67-116">[Convertitore da tee a sink a sink](tee-sink-to-sink-converter.md).</span><span class="sxs-lookup"><span data-stu-id="f5b67-116">[Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md).</span></span> <span data-ttu-id="f5b67-117">Accetta le informazioni VBI dal filtro di acquisizione e le suddivide in flussi distinti per ognuno dei servizi dati presenti sul segnale.</span><span class="sxs-lookup"><span data-stu-id="f5b67-117">Accepts the VBI information from the capture filter and splits it into separate streams for each of the data services present on the signal.</span></span> <span data-ttu-id="f5b67-118">Microsoft fornisce codec VBI per la didascalia chiusa, NABTS e il televideo internazionale (WST).</span><span class="sxs-lookup"><span data-stu-id="f5b67-118">Microsoft provides VBI codecs for Closed Caption, NABTS, and World Standard Teletext (WST).</span></span>
-   <span data-ttu-id="f5b67-119">[Decodificatore CC](cc-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f5b67-119">[CC Decoder](cc-decoder-filter.md).</span></span> <span data-ttu-id="f5b67-120">Decodifica i dati CC dalle forme d'onda VBI campionate fornite dal filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="f5b67-120">Decodes CC data from the sampled VBI waveforms provided by the capture filter.</span></span>
-   <span data-ttu-id="f5b67-121">[Decodificatore riga 21](line-21-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f5b67-121">[Line 21 Decoder](line-21-decoder-filter.md).</span></span> <span data-ttu-id="f5b67-122">Converte le coppie di byte CC e disegna il testo della didascalia sulle bitmap.</span><span class="sxs-lookup"><span data-stu-id="f5b67-122">Translates the CC byte pairs and draws the caption text onto bitmaps.</span></span> <span data-ttu-id="f5b67-123">Il filtro downstream (in questo caso il mixer overlay) sovrappone le bitmap nel video.</span><span class="sxs-lookup"><span data-stu-id="f5b67-123">The downstream filter (in this case the Overlay Mixer) overlays the bitmaps onto the video.</span></span>

<span data-ttu-id="f5b67-124">Il metodo [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) del generatore di grafici di acquisizione aggiunge questi filtri automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f5b67-124">The Capture Graph Builder's [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds these filters automatically.</span></span> <span data-ttu-id="f5b67-125">Se il filtro di acquisizione ha un pin CC anziché un pin VBI, il pin CC viene connesso direttamente al filtro decodificatore riga 21.</span><span class="sxs-lookup"><span data-stu-id="f5b67-125">If the capture filter has a CC pin instead of a VBI pin, the CC pin is connected directly to the Line 21 Decoder filter.</span></span>

> [!Note]  
> <span data-ttu-id="f5b67-126">Se si usa il filtro VMR (video Mixing Renderer) per il rendering, usare il filtro decodificatore riga 21 2.</span><span class="sxs-lookup"><span data-stu-id="f5b67-126">If you are using the Video Mixing Renderer (VMR) filter for rendering, use the Line 21 Decoder Filter 2.</span></span> <span data-ttu-id="f5b67-127">Questo filtro ha la stessa funzionalità del decodificatore della riga 21, ma il CLSID è CLSID \_ Line21Decoder2.</span><span class="sxs-lookup"><span data-stu-id="f5b67-127">This filter has the same functionality as the Line 21 Decoder, but the CLSID is CLSID\_Line21Decoder2.</span></span>

 

> [!Note]  
> <span data-ttu-id="f5b67-128">Il filtro del decodificatore CC è stato rimosso in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f5b67-128">The CC Decoder filter was removed in Windows Vista.</span></span> <span data-ttu-id="f5b67-129">Le nuove applicazioni devono usare il filtro VBICodec, documentato nella documentazione relativa alle tecnologie Microsoft TV.</span><span class="sxs-lookup"><span data-stu-id="f5b67-129">New applications should use the VBICodec filter, which is documented in the Microsoft TV Technologies documentation.</span></span>

 

<span data-ttu-id="f5b67-130">Se il dispositivo di acquisizione usa una porta video, il filtro di acquisizione potrebbe avere una porta video VBI pin (PIN \_ Category \_ VIDEOPORT \_ VBI).</span><span class="sxs-lookup"><span data-stu-id="f5b67-130">If the capture device uses a video port, the capture filter might have a video port VBI pin (PIN\_CATEGORY\_VIDEOPORT\_VBI).</span></span> <span data-ttu-id="f5b67-131">Questo pin deve essere connesso al filtro [VBI Surface allocator](vbi-surface-allocator.md) , che alloca le superfici in modo da contenere i dati VBI acquisiti.</span><span class="sxs-lookup"><span data-stu-id="f5b67-131">This pin must be connected to the [VBI Surface Allocator](vbi-surface-allocator.md) filter, which allocates surfaces to hold the captured VBI data.</span></span> <span data-ttu-id="f5b67-132">Il metodo [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) aggiunge questo filtro se necessario.</span><span class="sxs-lookup"><span data-stu-id="f5b67-132">The [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds this filter if it is required.</span></span> <span data-ttu-id="f5b67-133">Il diagramma seguente mostra un grafico di filtro con l'allocatore della superficie di VBI.</span><span class="sxs-lookup"><span data-stu-id="f5b67-133">The following diagram shows a filter graph with the VBI Surface Allocator.</span></span>

![grafico di anteprima dei sottotitoli codificati con VBI Surface allocator](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a><span data-ttu-id="f5b67-135">Abilitazione e disabilitazione delle didascalie</span><span class="sxs-lookup"><span data-stu-id="f5b67-135">Enabling and Disabling the Captions</span></span>

<span data-ttu-id="f5b67-136">Per controllare la visualizzazione dei sottotitoli, usare l'interfaccia [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) sul filtro del decodificatore della riga 21.</span><span class="sxs-lookup"><span data-stu-id="f5b67-136">To control the captioning display, use the [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) interface on the Line 21 Decoder filter.</span></span> <span data-ttu-id="f5b67-137">Ad esempio, è possibile disattivare la visualizzazione didascalia usando il metodo [**IAMLine21Decoder:: SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) , come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f5b67-137">For example, you can turn off the captioning display using the [**IAMLine21Decoder::SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) method, as follows:</span></span>


```C++
// Use the FindInterface method to find the interface.
IAMLine21Decoder *pLine21 = NULL;
hr = pBuild->FindInterface(
    &LOOK_DOWNSTREAM_ONLY, // Look downstream from pCap 
    NULL,                  // No particular media type
    pCap,                  // Pointer to the capture filter.
    IID_IAMLine21Decoder, (void**)&pLine21);
if (SUCCEEDED(hr))
{
    pLine21->SetServiceState(AM_L21_CCSTATE_Off);
    // (Use AM_L21_CCSTATE_On to enable.)
    pLine21->Release();
}
```



<span data-ttu-id="f5b67-138">Questo esempio usa il metodo [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) per individuare l'interfaccia [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) .</span><span class="sxs-lookup"><span data-stu-id="f5b67-138">This example uses the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to locate the [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) interface.</span></span> <span data-ttu-id="f5b67-139">Il primo parametro di **FindInterface** è **&cercare \_ \_ solo downstream**, che specifica la ricerca a valle dal filtro di acquisizione (*pCap*).</span><span class="sxs-lookup"><span data-stu-id="f5b67-139">The first parameter to **FindInterface** is **&LOOK\_DOWNSTREAM\_ONLY**, which specifies to search downstream from the capture filter (*pCap*).</span></span>

### <a name="capturing-closed-caption-bitmaps"></a><span data-ttu-id="f5b67-140">Acquisizione di bitmap didascalia chiuse</span><span class="sxs-lookup"><span data-stu-id="f5b67-140">Capturing Closed Caption Bitmaps</span></span>

<span data-ttu-id="f5b67-141">È possibile acquisire le bitmap della didascalia in un file.</span><span class="sxs-lookup"><span data-stu-id="f5b67-141">You can capture the caption bitmaps into a file.</span></span> <span data-ttu-id="f5b67-142">A tale scopo, aggiungere la sezione relativa alla scrittura di file del grafico di filtro, come descritto in [acquisizione di video in un file](capturing-video-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="f5b67-142">To do so, add the file-writing section of the filter graph, as described in [Capturing Video to a File](capturing-video-to-a-file.md).</span></span> <span data-ttu-id="f5b67-143">Eseguire quindi il rendering del pin CC o VBI nel filtro Mux:</span><span class="sxs-lookup"><span data-stu-id="f5b67-143">Then render the CC or VBI pin to the mux filter:</span></span>


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



<span data-ttu-id="f5b67-144">Se si sta acquisendo anche il video, verrà creato un file con due flussi video distinti.</span><span class="sxs-lookup"><span data-stu-id="f5b67-144">If you are also capturing the video, this will create a file with two separate video streams.</span></span> <span data-ttu-id="f5b67-145">Il video non verrà acquisito con le didascalie sovrapposte sopra l'immagine.</span><span class="sxs-lookup"><span data-stu-id="f5b67-145">It will not capture video with captions overlaid on top of the picture.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5b67-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5b67-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5b67-147">Didascalie e televideo chiusi</span><span class="sxs-lookup"><span data-stu-id="f5b67-147">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> </dl>

 

 



