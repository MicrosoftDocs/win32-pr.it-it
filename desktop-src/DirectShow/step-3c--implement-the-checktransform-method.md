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
# <a name="step-3c-implement-the-checktransform-method"></a><span data-ttu-id="75fe9-104">Passaggio 3C.</span><span class="sxs-lookup"><span data-stu-id="75fe9-104">Step 3C.</span></span> <span data-ttu-id="75fe9-105">Implementare il metodo CheckTransform</span><span class="sxs-lookup"><span data-stu-id="75fe9-105">Implement the CheckTransform Method</span></span>

<span data-ttu-id="75fe9-106">Questo è il passaggio 3C dell'esercitazione sulla [scrittura dei filtri di trasformazione](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="75fe9-106">This is step 3C of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="75fe9-107">Questo passaggio non è necessario per i filtri che derivano da **CTransInPlaceFilter**.</span><span class="sxs-lookup"><span data-stu-id="75fe9-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="75fe9-108">Il metodo [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) controlla se un tipo di output proposto è compatibile con il tipo di input corrente.</span><span class="sxs-lookup"><span data-stu-id="75fe9-108">The [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method checks if a proposed output type is compatible with the current input type.</span></span> <span data-ttu-id="75fe9-109">Il metodo viene chiamato anche se il pin di input si riconnette dopo la connessione del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="75fe9-109">The method is also called if the input pin reconnects after the output pin connects.</span></span>

<span data-ttu-id="75fe9-110">Nell'esempio seguente viene verificato se il formato è RLE8 video; le dimensioni dell'immagine corrispondono al formato di input; e le voci della tavolozza sono le stesse.</span><span class="sxs-lookup"><span data-stu-id="75fe9-110">The following example verifies whether the format is RLE8 video; the image dimensions match the input format; and the palette entries are the same.</span></span> <span data-ttu-id="75fe9-111">Rifiuta inoltre i rettangoli di origine e di destinazione che non corrispondono alla dimensione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="75fe9-111">It also rejects source and target rectangles that do not match the image size.</span></span>


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



<span data-ttu-id="75fe9-112">**Riconnessioni pin**</span><span class="sxs-lookup"><span data-stu-id="75fe9-112">**Pin Reconnections**</span></span>

<span data-ttu-id="75fe9-113">Le applicazioni possono disconnettere e riconnettere i pin.</span><span class="sxs-lookup"><span data-stu-id="75fe9-113">Applications can disconnect and reconnect pins.</span></span> <span data-ttu-id="75fe9-114">Si supponga che un'applicazione connetta entrambi i pin, disconnette il pin di input e quindi riconnette il pin di input usando una nuova dimensione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="75fe9-114">Suppose an application connects both pins, disconnects the input pin, and then reconnects the input pin using a new image size.</span></span> <span data-ttu-id="75fe9-115">In tal caso, **CheckTransform** ha esito negativo perché le dimensioni dell'immagine non corrispondono più.</span><span class="sxs-lookup"><span data-stu-id="75fe9-115">In that case, **CheckTransform** fails because the dimensions of the image no longer match.</span></span> <span data-ttu-id="75fe9-116">Questo comportamento è ragionevole, sebbene anche il filtro possa provare a riconnettere il pin di output con un nuovo tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="75fe9-116">This behavior is reasonable, although the filter could also try reconnecting the output pin with a new media type.</span></span>

<span data-ttu-id="75fe9-117">Successivo: [passaggio 4. Impostare le proprietà dell'allocatore](step-4--set-allocator-properties.md).</span><span class="sxs-lookup"><span data-stu-id="75fe9-117">Next: [Step 4. Set Allocator Properties](step-4--set-allocator-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="75fe9-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="75fe9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75fe9-119">Riconnessione di pin</span><span class="sxs-lookup"><span data-stu-id="75fe9-119">Reconnecting Pins</span></span>](reconnecting-pins.md)
</dt> <dt>

[<span data-ttu-id="75fe9-120">Rettangoli di origine e di destinazione nei renderer video</span><span class="sxs-lookup"><span data-stu-id="75fe9-120">Source and Target Rectangles in Video Renderers</span></span>](source-and-target-rectangles-in-video-renderers.md)
</dt> <dt>

[<span data-ttu-id="75fe9-121">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="75fe9-121">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



