---
description: Frequenza dei fotogrammi di un tipo di supporto video, in frame al secondo.
ms.assetid: 8336559c-06f1-478e-b921-e9eae7425230
title: Attributo MF_MT_FRAME_RATE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8df2ef4268bd643d9f65eb16c3f7257bcaceb1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401760"
---
# <a name="mf_mt_frame_rate-attribute"></a><span data-ttu-id="33928-103">\_ \_ Attributo frequenza di fotogrammi MF mt \_</span><span class="sxs-lookup"><span data-stu-id="33928-103">MF\_MT\_FRAME\_RATE attribute</span></span>

<span data-ttu-id="33928-104">Frequenza dei fotogrammi di un tipo di supporto video, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="33928-104">Frame rate of a video media type, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="33928-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="33928-105">Data type</span></span>

<span data-ttu-id="33928-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="33928-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="33928-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="33928-107">Remarks</span></span>

<span data-ttu-id="33928-108">La frequenza dei fotogrammi è espressa come rapporto.</span><span class="sxs-lookup"><span data-stu-id="33928-108">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="33928-109">I 32 bit superiori del valore dell'attributo contengono il numeratore e i 32 bit inferiori contengono il denominatore.</span><span class="sxs-lookup"><span data-stu-id="33928-109">The upper 32 bits of the attribute value contain the numerator and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="33928-110">Se, ad esempio, la frequenza dei fotogrammi è di 30 fotogrammi al secondo (fps), il rapporto è 30/1.</span><span class="sxs-lookup"><span data-stu-id="33928-110">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span> <span data-ttu-id="33928-111">Se la frequenza dei fotogrammi è 29,97 fps, il rapporto è 30000/1001.</span><span class="sxs-lookup"><span data-stu-id="33928-111">If the frame rate is 29.97 fps, the ratio is 30,000/1001.</span></span>

<span data-ttu-id="33928-112">Per impostare il valore, utilizzare la funzione [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="33928-112">To set the value, use the [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) function.</span></span> <span data-ttu-id="33928-113">Per ottenere il valore, usare la funzione [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="33928-113">To get the value, use the [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) function.</span></span>

<span data-ttu-id="33928-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="33928-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="33928-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="33928-115">Examples</span></span>

<span data-ttu-id="33928-116">Nell'esempio seguente viene impostata la frequenza dei fotogrammi su un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="33928-116">The following example sets the frame rate on a video media type.</span></span>


```
// Helper function to set the frame rate on a video media type.
inline HRESULT SetFrameRate(
    IMFMediaType *pType, 
    UINT32 numerator, 
    UINT32 denominator
    )
{
    return MFSetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        numerator, 
        denominator
        );
}
```



<span data-ttu-id="33928-117">Nell'esempio seguente viene ottenuta la frequenza dei fotogrammi da un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="33928-117">The following example gets the frame rate from a video media type.</span></span>


```
// Helper function to get the frame rate from a video media type.
inline HRESULT GetFrameRate(
    IMFMediaType *pType, 
    UINT32 *pNumerator, 
    UINT32 *pDenominator
    )
{
    return MFGetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        pNumerator, 
        pDenominator
        );
}
```



## <a name="requirements"></a><span data-ttu-id="33928-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33928-118">Requirements</span></span>



| <span data-ttu-id="33928-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="33928-119">Requirement</span></span> | <span data-ttu-id="33928-120">Valore</span><span class="sxs-lookup"><span data-stu-id="33928-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="33928-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33928-121">Minimum supported client</span></span><br/> | <span data-ttu-id="33928-122">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="33928-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="33928-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33928-123">Minimum supported server</span></span><br/> | <span data-ttu-id="33928-124">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="33928-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="33928-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33928-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="33928-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="33928-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33928-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33928-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33928-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33928-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="33928-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="33928-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="33928-130">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="33928-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="33928-131">**MFAverageTimePerFrameToFrameRate**</span><span class="sxs-lookup"><span data-stu-id="33928-131">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate)
</dt> <dt>

[<span data-ttu-id="33928-132">**MFFrameRateToAverageTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="33928-132">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe)
</dt> </dl>

 

 




