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
# <a name="queryaccept-upstream"></a>QueryAccept (upstream)

Questo meccanismo consente a un pin di input di proporre una modifica di formato al peer upstream. Il filtro downstream deve alleghi un tipo di supporto all'esempio che il filtro upstream otterrà nella chiamata successiva a [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). A tale scopo, tuttavia, il filtro downstream deve fornire un allocatore personalizzato per la connessione. Questo allocatore deve implementare un metodo privato che il filtro downstream può utilizzare per impostare il tipo di supporto nell'esempio successivo.

Si verificano i passaggi seguenti:

1.  Il filtro downstream controlla se la connessione pin usa l'allocatore personalizzato del filtro. Se il filtro upstream è proprietario dell'allocatore, il filtro downstream non può modificare il formato.
2.  Il filtro downstream chiama [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di output upstream (vedere la figura, passaggio A).
3.  Se `QueryAccept` restituisce S \_ OK, il filtro downstream chiama il metodo privato sul relativo allocatore per impostare il tipo di supporto. All'interno di questo metodo privato, l'allocatore chiama [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) sul successivo esempio disponibile (B).
4.  Il filtro upstream chiama **GetBuffer** per ottenere un nuovo esempio (C) e [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) per ottenere il tipo di supporto (D).
5.  Quando il filtro upstream recapita l'esempio, deve lasciare il tipo di supporto allegato a tale esempio. In questo modo, il filtro downstream può confermare che il tipo di supporto è stato modificato (E).

Se il filtro upstream accetta la modifica del formato, deve anche essere in grado di tornare al tipo di supporto originale, come illustrato nella figura seguente.

![queryaccept (upstream)](images/dynformat4.png)

Gli esempi principali di questo tipo di modifica del formato coinvolgono i renderer video DirectShow.

-   Il filtro [renderer video](video-renderer-filter.md) originale può spostarsi tra i tipi RGB e YUV durante il flusso. Quando il filtro si connette, è necessario un formato RGB che corrisponda alle impostazioni di visualizzazione correnti. In questo modo si garantisce che sia possibile eseguire il fallback su GDI se necessario. Dopo l'inizio del flusso, se è disponibile DirectDraw, il renderer video richiede una modifica del formato a un tipo YUV. In un secondo momento potrebbe tornare a RGB se la superficie DirectDraw viene persa per qualsiasi motivo.
-   Il nuovo filtro VMR (video Mixing Renderer) si connetterà con qualsiasi formato supportato dall'hardware grafico, inclusi i tipi YUV. Tuttavia, l'hardware grafico potrebbe modificare lo stride della superficie DirectDraw sottostante per ottimizzare le prestazioni. Il filtro VMR USA `QueryAccept` per segnalare la nuova stride, specificata nel membro **biWidth** della struttura **BITMAPINFOHEADER** . I rettangoli di origine e di destinazione nella struttura **VIDEOINFOHEADER** o **VIDEOINFOHEADER2** identificano l'area in cui il video deve essere decodificato.

**Nota sull'implementazione**

È improbabile che si scriva un filtro che deve richiedere modifiche al formato upstream, poiché si tratta principalmente di una funzionalità dei renderer di video. Tuttavia, se si scrive un filtro di trasformazione video o un decodificatore video, è necessario che il filtro risponda correttamente alle richieste dal renderer video.

Un filtro Trans-on-Place che si trova tra il renderer video e il decodificatore deve passare tutte le `QueryAccept` chiamate upstream. Archiviare le nuove informazioni sul formato al suo arrivo.

Un filtro per la trasformazione copia, ovvero un filtro non trans-on-Place, deve implementare uno dei comportamenti seguenti:

-   Il formato del passaggio passa a Monte e archivia le nuove informazioni sul formato al suo arrivo. Il filtro deve usare un allocatore personalizzato per poter alleghiare il formato all'esempio upstream.
-   Eseguire la conversione del formato all'interno del filtro. Questa operazione è probabilmente più semplice rispetto alla modifica del formato a Monte. Tuttavia, potrebbe essere meno efficiente rispetto a consentire al filtro del decodificatore di decodificare il formato corretto.
-   Come ultima risorsa, è sufficiente rifiutare la modifica del formato. Per ulteriori informazioni, fare riferimento al codice sorgente per il metodo [**CTransInPlaceOutputPin:: CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) nella libreria di classi base DirectShow. Il rifiuto di una modifica di formato può tuttavia ridurre le prestazioni, perché impedisce al renderer video di usare il formato più efficiente.

Lo pseudo codice seguente mostra come implementare un filtro di copia/trasformazione (derivato da **CTransformFilter**) che può passare tra i tipi di output YUV e RGB. In questo esempio si presuppone che il filtro esegue la conversione stessa, anziché passare la modifica del formato upstream.


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



 

 



