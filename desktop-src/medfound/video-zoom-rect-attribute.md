---
description: Specifica il rettangolo di origine per il mixer video del renderer video avanzato (EVR). Il rettangolo di origine è la parte del fotogramma video che il mixer Blits alla superficie di destinazione.
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: Attributo VIDEO_ZOOM_RECT (EVR. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda4efca5beab844baf3b3f53074d6b3012e8621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308968"
---
# <a name="video_zoom_rect-attribute"></a><span data-ttu-id="01924-104">\_ \_ Attributo Rect zoom video</span><span class="sxs-lookup"><span data-stu-id="01924-104">VIDEO\_ZOOM\_RECT attribute</span></span>

<span data-ttu-id="01924-105">Specifica il rettangolo di origine per il mixer video del [renderer video avanzato](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="01924-105">Specifies the source rectangle for video mixer of the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="01924-106">Il rettangolo di origine è la parte del fotogramma video che il mixer Blits alla superficie di destinazione.</span><span class="sxs-lookup"><span data-stu-id="01924-106">The source rectangle is the portion of the video frame that the mixer blits to the destination surface.</span></span>

## <a name="data-type"></a><span data-ttu-id="01924-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="01924-107">Data type</span></span>

<span data-ttu-id="01924-108">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="01924-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="01924-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="01924-109">Remarks</span></span>

<span data-ttu-id="01924-110">Il valore di questo attributo è una struttura [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .</span><span class="sxs-lookup"><span data-stu-id="01924-110">The value of this attribute is an [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) structure.</span></span>

<span data-ttu-id="01924-111">Il rettangolo di origine è definito in relazione a un sistema di coordinate normalizzato, in cui l'intero frame video occupa un rettangolo con le coordinate {0, 0, 1, 1}.</span><span class="sxs-lookup"><span data-stu-id="01924-111">The source rectangle is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="01924-112">Il rettangolo di origine deve rientrare nel fotogramma video; le coordinate del rettangolo di origine hanno un intervallo di (0... 1).</span><span class="sxs-lookup"><span data-stu-id="01924-112">The source rectangle must fit within the video frame; the coordinates of the source rectangle have a range of (0...1).</span></span>

<span data-ttu-id="01924-113">Il relatore EVR standard imposta questo attributo sul mixer.</span><span class="sxs-lookup"><span data-stu-id="01924-113">The standard EVR presenter sets this attribute on the mixer.</span></span> <span data-ttu-id="01924-114">Per impostare l'attributo, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="01924-114">To set the attribute, do the following:</span></span>

1.  <span data-ttu-id="01924-115">Chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sul mixer per ottenere l'archivio di attributi del mixer.</span><span class="sxs-lookup"><span data-stu-id="01924-115">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the mixer, to get the mixer's attribute store.</span></span>
2.  <span data-ttu-id="01924-116">Chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) SetAttribute per impostare l'attributo **video \_ Zoom \_ Rect** nel mixer.</span><span class="sxs-lookup"><span data-stu-id="01924-116">Call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) to set the **VIDEO\_ZOOM\_RECT** attribute on the mixer.</span></span> <span data-ttu-id="01924-117">Il valore è una struttura [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .</span><span class="sxs-lookup"><span data-stu-id="01924-117">The value is an [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) structure.</span></span>

<span data-ttu-id="01924-118">In un EVR Presenter personalizzato è possibile usare questo attributo per implementare il metodo [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) .</span><span class="sxs-lookup"><span data-stu-id="01924-118">In a custom EVR presenter, you can use this attribute to implement the [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) method.</span></span> <span data-ttu-id="01924-119">Per altre informazioni, vedere [rettangoli di origine e di destinazione](how-to-write-an-evr-presenter.md).</span><span class="sxs-lookup"><span data-stu-id="01924-119">For more information, see [Source and Destination Rectangles](how-to-write-an-evr-presenter.md).</span></span>

<span data-ttu-id="01924-120">La costante GUID per questo attributo viene esportata da strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="01924-120">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="01924-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="01924-121">Examples</span></span>

<span data-ttu-id="01924-122">Nell'esempio seguente viene impostato il rettangolo di origine nel mixer.</span><span class="sxs-lookup"><span data-stu-id="01924-122">The following example sets the source rectangle on the mixer.</span></span>


```C++
HRESULT SetMixerSourceRect(IMFTransform *pMixer, const MFVideoNormalizedRect& nrcSource)
{
    if (pMixer == NULL)
    {
        return E_POINTER;
    }

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMixer->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetBlob(VIDEO_ZOOM_RECT, (const UINT8*)&nrcSource, sizeof(nrcSource));
        pAttributes->Release();
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="01924-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01924-123">Requirements</span></span>



| <span data-ttu-id="01924-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="01924-124">Requirement</span></span> | <span data-ttu-id="01924-125">Valore</span><span class="sxs-lookup"><span data-stu-id="01924-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="01924-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01924-126">Minimum supported client</span></span><br/> | <span data-ttu-id="01924-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01924-127">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="01924-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01924-128">Minimum supported server</span></span><br/> | <span data-ttu-id="01924-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="01924-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="01924-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01924-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="01924-131"><dt>EVR. h</dt></span><span class="sxs-lookup"><span data-stu-id="01924-131"><dt>Evr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01924-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01924-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01924-133">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01924-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="01924-134">Attributi renderer video avanzati</span><span class="sxs-lookup"><span data-stu-id="01924-134">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="01924-135">Come scrivere un presentatore EVR</span><span class="sxs-lookup"><span data-stu-id="01924-135">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> <dt>

[<span data-ttu-id="01924-136">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="01924-136">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="01924-137">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="01924-137">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




