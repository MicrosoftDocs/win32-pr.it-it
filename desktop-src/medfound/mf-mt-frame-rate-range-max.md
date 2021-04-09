---
description: Frequenza massima dei fotogrammi supportata da un dispositivo di acquisizione video, in frame al secondo.
ms.assetid: 8e0c4996-9f78-424e-b012-502228b6a27a
title: Attributo MF_MT_FRAME_RATE_RANGE_MAX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62399445cd31c7820ea9de7082fce71febbf3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967039"
---
# <a name="mf_mt_frame_rate_range_max-attribute"></a><span data-ttu-id="36767-103">\_ \_ \_ \_ Attributo max frequenza frame frequenza MF mt \_</span><span class="sxs-lookup"><span data-stu-id="36767-103">MF\_MT\_FRAME\_RATE\_RANGE\_MAX attribute</span></span>

<span data-ttu-id="36767-104">Frequenza massima dei fotogrammi supportata da un dispositivo di acquisizione video, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="36767-104">The maximum frame rate that is supported by a video capture device, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="36767-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="36767-105">Data type</span></span>

<span data-ttu-id="36767-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="36767-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="36767-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="36767-107">Get/set</span></span>

<span data-ttu-id="36767-108">Per ottenere questo attributo, chiamare [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="36767-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="36767-109">Per impostare questo attributo, chiamare [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="36767-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="remarks"></a><span data-ttu-id="36767-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="36767-110">Remarks</span></span>

<span data-ttu-id="36767-111">La frequenza dei fotogrammi è espressa come rapporto.</span><span class="sxs-lookup"><span data-stu-id="36767-111">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="36767-112">I 32 bit superiori del valore dell'attributo contengono il numeratore e i 32 bit inferiori contengono il denominatore.</span><span class="sxs-lookup"><span data-stu-id="36767-112">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="36767-113">Se, ad esempio, la frequenza dei fotogrammi è di 30 fotogrammi al secondo (fps), il rapporto è 30/1.</span><span class="sxs-lookup"><span data-stu-id="36767-113">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span>

<span data-ttu-id="36767-114">Se il dispositivo di acquisizione indica una frequenza massima dei fotogrammi, l'origine del supporto imposta questo attributo sul tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="36767-114">If the capture device reports a maximum frame rate, the media source sets this attribute on the media type.</span></span> <span data-ttu-id="36767-115">La frequenza minima dei fotogrammi viene specificata nell'attributo dell' [ \_ intervallo di \_ \_ frequenza \_ \_ dei fotogrammi MF mt](mf-mt-frame-rate-range-min.md) .</span><span class="sxs-lookup"><span data-stu-id="36767-115">The minimum frame rate is given in the [MF\_MT\_FRAME\_RATE\_RANGE\_MIN](mf-mt-frame-rate-range-min.md) attribute.</span></span> <span data-ttu-id="36767-116">Non è garantito che il dispositivo supporti ogni incremento entro questo intervallo.</span><span class="sxs-lookup"><span data-stu-id="36767-116">The device is not guaranteed to support every increment within this range.</span></span>

<span data-ttu-id="36767-117">Per impostare la frequenza dei fotogrammi del dispositivo, modificare prima di tutto il valore dell'attributo [**MF \_ mt \_ frame \_ rate**](mf-mt-frame-rate-attribute.md) nel tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="36767-117">To set the device's frame rate, first modify the value of the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="36767-118">Impostare quindi il tipo di supporto nell'origine supporto.</span><span class="sxs-lookup"><span data-stu-id="36767-118">Then set the media type on the media source.</span></span>

<span data-ttu-id="36767-119">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="36767-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="36767-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36767-120">Requirements</span></span>



| <span data-ttu-id="36767-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="36767-121">Requirement</span></span> | <span data-ttu-id="36767-122">Valore</span><span class="sxs-lookup"><span data-stu-id="36767-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36767-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36767-123">Minimum supported client</span></span><br/> | <span data-ttu-id="36767-124">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="36767-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="36767-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36767-125">Minimum supported server</span></span><br/> | <span data-ttu-id="36767-126">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="36767-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="36767-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36767-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="36767-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="36767-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36767-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36767-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36767-130">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="36767-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="36767-131">Come impostare la frequenza dei fotogrammi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="36767-131">How to Set the Video Capture Frame Rate</span></span>](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[<span data-ttu-id="36767-132">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="36767-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="36767-133">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="36767-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="36767-134">\_intervallo di \_ \_ frequenza frame \_ MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="36767-134">MF\_MT\_FRAME\_RATE\_RANGE\_MIN</span></span>](mf-mt-frame-rate-range-min.md)
</dt> </dl>

 

 




