---
description: Specifica le primarie colore per un tipo di supporto video.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: Attributo MF_MT_VIDEO_PRIMARIES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cdf26a3f49c7e2bb3aa0f48c52c9b283edd8cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318064"
---
# <a name="mf_mt_video_primaries-attribute"></a><span data-ttu-id="69cfd-103">\_ \_ Attributo principali video MF mt \_</span><span class="sxs-lookup"><span data-stu-id="69cfd-103">MF\_MT\_VIDEO\_PRIMARIES attribute</span></span>

<span data-ttu-id="69cfd-104">Specifica le primarie colore per un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="69cfd-104">Specifies the color primaries for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="69cfd-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="69cfd-105">Data type</span></span>

<span data-ttu-id="69cfd-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="69cfd-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="69cfd-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="69cfd-107">Remarks</span></span>

<span data-ttu-id="69cfd-108">Il valore di questo attributo è un membro dell'enumerazione [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) .</span><span class="sxs-lookup"><span data-stu-id="69cfd-108">The value of this attribute is a member of the [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) enumeration.</span></span>

<span data-ttu-id="69cfd-109">L'enumerazione [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) identifica le primarie cromatiche associate a determinati standard video comuni.</span><span class="sxs-lookup"><span data-stu-id="69cfd-109">The [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) enumeration identifies color primaries associated with certain common video standards.</span></span> <span data-ttu-id="69cfd-110">Se il tipo di supporto usa le primarie di colore non identificate nell'enumerazione **MFVideoPrimaries** , impostare l'attributo di [**\_ \_ \_ \_ primari video personalizzati MF mt**](mf-mt-custom-video-primaries-attribute.md) anziché questo attributo.</span><span class="sxs-lookup"><span data-stu-id="69cfd-110">If the media type uses color primaries that are not identified in the **MFVideoPrimaries** enumeration, set the [**MF\_MT\_CUSTOM\_VIDEO\_PRIMARIES**](mf-mt-custom-video-primaries-attribute.md) attribute instead of this attribute.</span></span>

<span data-ttu-id="69cfd-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="69cfd-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="69cfd-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69cfd-112">Requirements</span></span>



| <span data-ttu-id="69cfd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="69cfd-113">Requirement</span></span> | <span data-ttu-id="69cfd-114">Valore</span><span class="sxs-lookup"><span data-stu-id="69cfd-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69cfd-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69cfd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="69cfd-116">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="69cfd-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="69cfd-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69cfd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="69cfd-118">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="69cfd-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="69cfd-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69cfd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="69cfd-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="69cfd-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69cfd-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69cfd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69cfd-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="69cfd-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="69cfd-123">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="69cfd-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="69cfd-124">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="69cfd-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="69cfd-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="69cfd-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="69cfd-126">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="69cfd-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="69cfd-127">Informazioni sui colori estesi</span><span class="sxs-lookup"><span data-stu-id="69cfd-127">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




