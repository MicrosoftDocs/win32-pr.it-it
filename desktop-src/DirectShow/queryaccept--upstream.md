---
description: QueryAccept (upstream)
ms.assetid: 3153e3a4-2227-4fdd-b2b0-218763013d2d
title: QueryAccept (upstream)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7707c52d36c3d065c4a7277939f724aabdb73e46
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747095"
---
# <a name="queryaccept-upstream"></a><span data-ttu-id="a209e-103">QueryAccept (upstream)</span><span class="sxs-lookup"><span data-stu-id="a209e-103">QueryAccept (Upstream)</span></span>

<span data-ttu-id="a209e-104">Questo meccanismo consente a un pin di input di proporre una modifica di formato al peer upstream.</span><span class="sxs-lookup"><span data-stu-id="a209e-104">This mechanism enables an input pin to propose a format change to its upstream peer.</span></span> <span data-ttu-id="a209e-105">Il filtro downstream deve alleghi un tipo di supporto all'esempio che il filtro upstream otterrà nella chiamata successiva a [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).</span><span class="sxs-lookup"><span data-stu-id="a209e-105">The downstream filter must attach a media type to the sample that the upstream filter will obtain in its next call to [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).</span></span> <span data-ttu-id="a209e-106">A tale scopo, tuttavia, il filtro downstream deve fornire un allocatore personalizzato per la connessione.</span><span class="sxs-lookup"><span data-stu-id="a209e-106">In order to do this, however, the downstream filter must provide a custom allocator for the connection.</span></span> <span data-ttu-id="a209e-107">Questo allocatore deve implementare un metodo privato che il filtro downstream può utilizzare per impostare il tipo di supporto nell'esempio successivo.</span><span class="sxs-lookup"><span data-stu-id="a209e-107">This allocator must implement a private method that the downstream filter can use to set the media type on the next sample.</span></span>

<span data-ttu-id="a209e-108">Si verificano i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a209e-108">The following steps occur:</span></span>

1.  <span data-ttu-id="a209e-109">Il filtro downstream controlla se la connessione pin usa l'allocatore personalizzato del filtro.</span><span class="sxs-lookup"><span data-stu-id="a209e-109">The downstream filter checks whether the pin connection uses the filter's custom allocator.</span></span> <span data-ttu-id="a209e-110">Se il filtro upstream è proprietario dell'allocatore, il filtro downstream non può modificare il formato.</span><span class="sxs-lookup"><span data-stu-id="a209e-110">If the upstream filter owns the allocator, the downstream filter cannot change the format.</span></span>
2.  <span data-ttu-id="a209e-111">Il filtro downstream chiama [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di output upstream (vedere la figura, passaggio A).</span><span class="sxs-lookup"><span data-stu-id="a209e-111">The downstream filter calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on the upstream output pin (see illustration, step A).</span></span>
3.  <span data-ttu-id="a209e-112">Se `QueryAccept` restituisce S \_ OK, il filtro downstream chiama il metodo privato sul relativo allocatore per impostare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="a209e-112">If `QueryAccept` returns S\_OK, the downstream filter calls the private method on its allocator in order to set the media type.</span></span> <span data-ttu-id="a209e-113">All'interno di questo metodo privato, l'allocatore chiama [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) sul successivo esempio disponibile (B).</span><span class="sxs-lookup"><span data-stu-id="a209e-113">Within this private method, the allocator calls [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) on the next available sample (B).</span></span>
4.  <span data-ttu-id="a209e-114">Il filtro upstream chiama **GetBuffer** per ottenere un nuovo esempio (C) e [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) per ottenere il tipo di supporto (D).</span><span class="sxs-lookup"><span data-stu-id="a209e-114">The upstream filter calls **GetBuffer** to get a new sample (C) and [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) to get the media type (D).</span></span>
5.  <span data-ttu-id="a209e-115">Quando il filtro upstream recapita l'esempio, deve lasciare il tipo di supporto allegato a tale esempio.</span><span class="sxs-lookup"><span data-stu-id="a209e-115">When the upstream filter delivers the sample, it should leave the media type attached to that sample.</span></span> <span data-ttu-id="a209e-116">In questo modo, il filtro downstream può confermare che il tipo di supporto è stato modificato (E).</span><span class="sxs-lookup"><span data-stu-id="a209e-116">That way, the downstream filter can confirm that the media type has changed (E).</span></span>

<span data-ttu-id="a209e-117">Se il filtro upstream accetta la modifica del formato, deve anche essere in grado di tornare al tipo di supporto originale, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="a209e-117">If the upstream filter accepts the format change, it must also be able to switch back to the original media type, as shown in the following diagram.</span></span>

![queryaccept (upstream)](images/dynformat4.png)

<span data-ttu-id="a209e-119">Gli esempi principali di questo tipo di modifica del formato coinvolgono i renderer video DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a209e-119">The main examples of this kind of format change involve the DirectShow video renderers.</span></span>

-   <span data-ttu-id="a209e-120">Il filtro [renderer video](video-renderer-filter.md) originale può spostarsi tra i tipi RGB e YUV durante il flusso.</span><span class="sxs-lookup"><span data-stu-id="a209e-120">The original [Video Renderer](video-renderer-filter.md) filter can switch between RGB and YUV types during streaming.</span></span> <span data-ttu-id="a209e-121">Quando il filtro si connette, è necessario un formato RGB che corrisponda alle impostazioni di visualizzazione correnti.</span><span class="sxs-lookup"><span data-stu-id="a209e-121">When the filter connects, it requires an RGB format that matches the current display settings.</span></span> <span data-ttu-id="a209e-122">In questo modo si garantisce che sia possibile eseguire il fallback su GDI se necessario.</span><span class="sxs-lookup"><span data-stu-id="a209e-122">This guarantees that it can fall back on GDI if it needs to.</span></span> <span data-ttu-id="a209e-123">Dopo l'inizio del flusso, se è disponibile DirectDraw, il renderer video richiede una modifica del formato a un tipo YUV.</span><span class="sxs-lookup"><span data-stu-id="a209e-123">After streaming begins, if DirectDraw is available, the Video Renderer requests a format change to a YUV type.</span></span> <span data-ttu-id="a209e-124">In un secondo momento potrebbe tornare a RGB se la superficie DirectDraw viene persa per qualsiasi motivo.</span><span class="sxs-lookup"><span data-stu-id="a209e-124">Later, it might switch back to RGB if it loses the DirectDraw surface for any reason.</span></span>
-   <span data-ttu-id="a209e-125">Il nuovo filtro VMR (video Mixing Renderer) si connetterà con qualsiasi formato supportato dall'hardware grafico, inclusi i tipi YUV.</span><span class="sxs-lookup"><span data-stu-id="a209e-125">The newer Video Mixing Renderer (VMR) filter will connect with any format that is supported by the graphics hardware, including YUV types.</span></span> <span data-ttu-id="a209e-126">Tuttavia, l'hardware grafico potrebbe modificare lo stride della superficie DirectDraw sottostante per ottimizzare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a209e-126">However, the graphics hardware might change the stride of the underlying DirectDraw surface in order to optimize performance.</span></span> <span data-ttu-id="a209e-127">Il filtro VMR USA `QueryAccept` per segnalare la nuova stride, specificata nel membro **biWidth** della struttura **BITMAPINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="a209e-127">The VMR filter uses `QueryAccept` to report the new stride, which is specified in the **biWidth** member of the **BITMAPINFOHEADER** structure.</span></span> <span data-ttu-id="a209e-128">I rettangoli di origine e di destinazione nella struttura **VIDEOINFOHEADER** o **VIDEOINFOHEADER2** identificano l'area in cui il video deve essere decodificato.</span><span class="sxs-lookup"><span data-stu-id="a209e-128">The source and target rectangles in the **VIDEOINFOHEADER** or **VIDEOINFOHEADER2** structure identify the region where the video should be decoded.</span></span>

<span data-ttu-id="a209e-129">**Nota sull'implementazione**</span><span class="sxs-lookup"><span data-stu-id="a209e-129">**Implementation Note**</span></span>

<span data-ttu-id="a209e-130">È improbabile che si scriva un filtro che deve richiedere modifiche al formato upstream, poiché si tratta principalmente di una funzionalità dei renderer di video.</span><span class="sxs-lookup"><span data-stu-id="a209e-130">It is unlikely that you will write a filter that needs to request upstream format changes, since this is mainly a feature of video renderers.</span></span> <span data-ttu-id="a209e-131">Tuttavia, se si scrive un filtro di trasformazione video o un decodificatore video, è necessario che il filtro risponda correttamente alle richieste dal renderer video.</span><span class="sxs-lookup"><span data-stu-id="a209e-131">However, if you write a video transform filter or a video decoder, your filter must respond correctly to requests from the video renderer.</span></span>

<span data-ttu-id="a209e-132">Un filtro Trans-on-Place che si trova tra il renderer video e il decodificatore deve passare tutte le `QueryAccept` chiamate upstream.</span><span class="sxs-lookup"><span data-stu-id="a209e-132">A trans-in-place filter that sits between the video renderer and the decoder should pass all `QueryAccept` calls upstream.</span></span> <span data-ttu-id="a209e-133">Archiviare le nuove informazioni sul formato al suo arrivo.</span><span class="sxs-lookup"><span data-stu-id="a209e-133">Store the new format information when it arrives.</span></span>

<span data-ttu-id="a209e-134">Un filtro per la trasformazione copia, ovvero un filtro non trans-on-Place, deve implementare uno dei comportamenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a209e-134">A copy-transform filter (that is, a non-trans-in-place filter) should implement one of the following behaviors:</span></span>

-   <span data-ttu-id="a209e-135">Il formato del passaggio passa a Monte e archivia le nuove informazioni sul formato al suo arrivo.</span><span class="sxs-lookup"><span data-stu-id="a209e-135">Pass format changes upstream and store the new format information when it arrives.</span></span> <span data-ttu-id="a209e-136">Il filtro deve usare un allocatore personalizzato per poter alleghiare il formato all'esempio upstream.</span><span class="sxs-lookup"><span data-stu-id="a209e-136">Your filter must use a custom allocator so that it can attach the format to the upstream sample.</span></span>
-   <span data-ttu-id="a209e-137">Eseguire la conversione del formato all'interno del filtro.</span><span class="sxs-lookup"><span data-stu-id="a209e-137">Perform the format conversion inside the filter.</span></span> <span data-ttu-id="a209e-138">Questa operazione è probabilmente più semplice rispetto alla modifica del formato a Monte.</span><span class="sxs-lookup"><span data-stu-id="a209e-138">This is probably easier than passing the format change upstream.</span></span> <span data-ttu-id="a209e-139">Tuttavia, potrebbe essere meno efficiente rispetto a consentire al filtro del decodificatore di decodificare il formato corretto.</span><span class="sxs-lookup"><span data-stu-id="a209e-139">However, it might be less efficient than letting the decoder filter decode into the correct format.</span></span>
-   <span data-ttu-id="a209e-140">Come ultima risorsa, è sufficiente rifiutare la modifica del formato.</span><span class="sxs-lookup"><span data-stu-id="a209e-140">As a last resort, simply reject the format change.</span></span> <span data-ttu-id="a209e-141">Per ulteriori informazioni, fare riferimento al codice sorgente per il metodo [**CTransInPlaceOutputPin:: CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) nella libreria di classi base DirectShow. Il rifiuto di una modifica di formato può tuttavia ridurre le prestazioni, perché impedisce al renderer video di usare il formato più efficiente.</span><span class="sxs-lookup"><span data-stu-id="a209e-141">(For more information, refer to the source code for the [**CTransInPlaceOutputPin::CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) method in the DirectShow base class library.) Rejecting a format change can reduce performance, however, because it prevents the video renderer from using the most efficient format.</span></span>

<span data-ttu-id="a209e-142">Lo pseudo codice seguente mostra come implementare un filtro di copia/trasformazione (derivato da **CTransformFilter**) che può passare tra i tipi di output YUV e RGB.</span><span class="sxs-lookup"><span data-stu-id="a209e-142">The following pseudo-code shows how you might implement a copy-transform filter (derived from **CTransformFilter**) that can switch between YUV and RGB output types.</span></span> <span data-ttu-id="a209e-143">In questo esempio si presuppone che il filtro esegue la conversione stessa, anziché passare la modifica del formato upstream.</span><span class="sxs-lookup"><span data-stu-id="a209e-143">This example assumes that the filter does the conversion itself, rather than passing the format change upstream.</span></span>


```C++
HRESULT CMyTransform::CheckInputType(const CMediaType *pmt)
{
    if (pmt is a YUV type that you support) {
        return S_OK;
    }
    else {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
}

HRESULT CMyTransform::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    if (mtOut is a YUV or RGB type that you support)
    {
        if ((mtIn has the same video dimensions as mtOut) &&
            (you support the mtIn-to-mtOut transform))
        {
            return S_OK;
        }
    }
    // otherwise
    return VFW_E_TYPE_NOT_ACCEPTED;
}

// GetMediaType: Return a preferred output type.
HRESULT CMyTransform::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    if (iPosition < 0) {
        return E_INVALIDARG;
    }
    switch (iPosition)
    {
    case 0:
        Copy the input type (YUV) to pMediaType
        return S_OK;
    case 1:
        Construct an RGB type that matches the input type.
        return S_OK;
    default:
        return VFW_S_NO_MORE_ITEMS;
    }
}

// SetMediaType: Override from CTransformFilter. 
HRESULT CMyTransform::SetMediaType(
    PIN_DIRECTION direction, const CMediaType *pmt)
{
    // Capture this information...
    if (direction == PINDIR_OUTPUT)
    {
       m_bYuv = (pmt->subtype == MEDIASUBTYPE_UYVY);
    }
    return S_OK;
}

HRESULT CMyTransform::Transform(
    IMediaSample *pSource, IMediaSample *pDest)
{
    // Look for format changes from downstream.
    CMediaType *pMT = NULL;
    HRESULT hr = pDest->GetMediaType((AM_MEDIA_TYPE**)&pMT);
    if (hr == S_OK)
    {
        hr = m_pOutput->CheckMediaType(pMT);
        if(FAILED(hr))
        {
            DeleteMediaType(pMT);
            return E_FAIL;
        }
        // Notify our own output pin about the new type.
        m_pOutput->SetMediaType(pMT);
        DeleteMediaType(pMT);
    }
    // Process the buffers
    if (m_bYuv) {
        return ProcessFrameYUV(pSource, pDest);
    }
    else {
        return ProcessFrameRGB(pSource, pDest);
    }
}
```



 

 



