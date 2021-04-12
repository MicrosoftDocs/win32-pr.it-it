---
description: Passaggio 3C.
ms.assetid: e780df46-bf47-4334-b788-05ad8179f051
title: Passaggio 3C. Implementare il metodo CheckTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78148701fc54e73a6970d45fde95d70f4cf0df3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233523"
---
# <a name="step-3c-implement-the-checktransform-method"></a>Passaggio 3C. Implementare il metodo CheckTransform

Questo è il passaggio 3C dell'esercitazione sulla [scrittura dei filtri di trasformazione](writing-transform-filters.md).

> [!Note]  
> Questo passaggio non è necessario per i filtri che derivano da **CTransInPlaceFilter**.

 

Il metodo [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) controlla se un tipo di output proposto è compatibile con il tipo di input corrente. Il metodo viene chiamato anche se il pin di input si riconnette dopo la connessione del PIN di output.

Nell'esempio seguente viene verificato se il formato è RLE8 video; le dimensioni dell'immagine corrispondono al formato di input; e le voci della tavolozza sono le stesse. Rifiuta inoltre i rettangoli di origine e di destinazione che non corrispondono alla dimensione dell'immagine.


```C++
HRESULT CRleFilter::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    // Check the major type.
    if (mtOut->majortype != MEDIATYPE_Video)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the subtype and format type.
    FOURCCMap fccMap = FCC('MRLE'); 
    if (mtOut->subtype != static_cast<GUID>(fccMap))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if ((mtOut->formattype != FORMAT_VideoInfo) || 
        (mtOut->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare the bitmap information against the input type.
    ASSERT(mtIn->formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pBmiOut = HEADER(mtOut->pbFormat);
    BITMAPINFOHEADER *pBmiIn = HEADER(mtIn->pbFormat);
    if ((pBmiOut->biPlanes != 1) ||
        (pBmiOut->biBitCount != 8) ||
        (pBmiOut->biCompression != BI_RLE8) ||
        (pBmiOut->biWidth != pBmiIn->biWidth) ||
        (pBmiOut->biHeight != pBmiIn->biHeight))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare source and target rectangles.
    RECT rcImg;
    SetRect(&rcImg, 0, 0, pBmiIn->biWidth, pBmiIn->biHeight);
    RECT *prcSrc = &((VIDEOINFOHEADER*)(mtIn->pbFormat))->rcSource;
    RECT *prcTarget = &((VIDEOINFOHEADER*)(mtOut->pbFormat))->rcTarget;
    if (!IsRectEmpty(prcSrc) && !EqualRect(prcSrc, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
    if (!IsRectEmpty(prcTarget) && !EqualRect(prcTarget, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the palette table.
    if (pBmiOut->biClrUsed != pBmiIn->biClrUsed)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pBmiOut->biClrUsed * sizeof(RGBQUAD);
    if (mtOut->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if (0 != memcmp(pBmiOut + 1, pBmiIn + 1, cbPalette))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



**Riconnessioni pin**

Le applicazioni possono disconnettere e riconnettere i pin. Si supponga che un'applicazione connetta entrambi i pin, disconnette il pin di input e quindi riconnette il pin di input usando una nuova dimensione dell'immagine. In tal caso, **CheckTransform** ha esito negativo perché le dimensioni dell'immagine non corrispondono più. Questo comportamento è ragionevole, sebbene anche il filtro possa provare a riconnettere il pin di output con un nuovo tipo di supporto.

Successivo: [passaggio 4. Impostare le proprietà dell'allocatore](step-4--set-allocator-properties.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riconnessione di pin](reconnecting-pins.md)
</dt> <dt>

[Rettangoli di origine e di destinazione nei renderer video](source-and-target-rectangles-in-video-renderers.md)
</dt> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



