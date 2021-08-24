---
description: QueryAccept (Upstream)
ms.assetid: 3153e3a4-2227-4fdd-b2b0-218763013d2d
title: QueryAccept (Upstream)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65133e132a0e1c2e6880009eda8b56fde9bf77a8bc7d68a850a6f8963604aecd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747577"
---
# <a name="queryaccept-upstream"></a>QueryAccept (Upstream)

Questo meccanismo consente a un pin di input di proporre una modifica del formato al peer upstream. Il filtro downstream deve collegare un tipo di supporto all'esempio che il filtro upstream otterrà nella chiamata successiva a [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). A tale scopo, tuttavia, il filtro downstream deve fornire un allocatore personalizzato per la connessione. Questo allocatore deve implementare un metodo privato che il filtro downstream può usare per impostare il tipo di supporto nell'esempio successivo.

Si verificano i passaggi seguenti:

1.  Il filtro downstream controlla se la connessione pin usa l'allocatore personalizzato del filtro. Se il filtro upstream è proprietario dell'allocatore, il filtro downstream non può modificare il formato.
2.  Il filtro downstream chiama [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di output upstream (vedere la figura, passaggio A).
3.  Se `QueryAccept` restituisce S \_ OK, il filtro downstream chiama il metodo privato sull'allocatore per impostare il tipo di supporto. All'interno di questo metodo privato, l'allocatore chiama [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) nell'esempio disponibile successivo (B).
4.  Il filtro upstream chiama **GetBuffer** per ottenere un nuovo esempio (C) e [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) per ottenere il tipo di supporto (D).
5.  Quando il filtro upstream recapita l'esempio, deve lasciare il tipo di supporto collegato a tale esempio. In questo modo, il filtro downstream può confermare che il tipo di supporto è stato modificato (E).

Se il filtro upstream accetta la modifica del formato, deve anche essere in grado di tornare al tipo di supporto originale, come illustrato nel diagramma seguente.

![queryaccept (upstream)](images/dynformat4.png)

Gli esempi principali di questo tipo di modifica del formato coinvolgono DirectShow renderer video.

-   Il filtro [renderer video originale](video-renderer-filter.md) può passare da RGB a YUV durante lo streaming. Quando il filtro si connette, richiede un formato RGB che corrisponda alle impostazioni di visualizzazione correnti. In questo modo è possibile eseguire il fall back su GDI, se necessario. Dopo l'inizio dello streaming, se DirectDraw è disponibile, il renderer video richiede una modifica del formato a un tipo YUV. In un secondo momento, potrebbe tornare a RGB se perde la superficie directdraw per qualsiasi motivo.
-   Il filtro vmr (Video Mixing Renderer) più recente si connetterà a qualsiasi formato supportato dall'hardware grafico, inclusi i tipi YUV. Tuttavia, l'hardware grafico potrebbe modificare lo stride della superficie DirectDraw sottostante per ottimizzare le prestazioni. Il filtro VMR usa per segnalare il nuovo stride, specificato nel membro `QueryAccept` **biWidth** della **struttura BITMAPINFOHEADER.** I rettangoli di origine e di destinazione nella struttura **VIDEOINFOHEADER** o **VIDEOINFOHEADER2** identificano l'area in cui deve essere decodificato il video.

**Nota sull'implementazione**

È improbabile che si scriverà un filtro che deve richiedere modifiche al formato upstream, poiché si tratta principalmente di una funzionalità dei renderer video. Tuttavia, se si scrive un filtro di trasformazione video o un decodificatore video, il filtro deve rispondere correttamente alle richieste del renderer video.

Un filtro trans-in-place che si trova tra il renderer video e il decodificatore deve passare tutte le `QueryAccept` chiamate a monte. Archiviare le nuove informazioni sul formato all'arrivo.

Un filtro di copia-trasformazione, ovvero un filtro non trans-in-place, deve implementare uno dei comportamenti seguenti:

-   Passare le modifiche del formato a monte e archiviare le nuove informazioni sul formato all'arrivo. Il filtro deve usare un allocatore personalizzato in modo che possa collegare il formato all'esempio upstream.
-   Eseguire la conversione del formato all'interno del filtro. Questo è probabilmente più semplice rispetto al passaggio della modifica del formato a monte. Tuttavia, potrebbe essere meno efficiente rispetto all'uso della decodifica del filtro decodificatore nel formato corretto.
-   Come ultima risorsa, è sufficiente rifiutare la modifica del formato. Per altre informazioni, vedere il codice sorgente per il metodo [**CTransInPlaceOutputPin::CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) nella libreria DirectShow di classi di base. Il rifiuto di una modifica del formato può tuttavia ridurre le prestazioni, perché impedisce al renderer video di usare il formato più efficiente.

Lo pseudocodice seguente illustra come implementare un filtro di copia-trasformazione (derivato da **CTransformFilter**) in grado di passare tra i tipi di output YUV e RGB. In questo esempio si presuppone che il filtro esempli la conversione stessa, anziché passare la modifica del formato a monte.


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



 

 



