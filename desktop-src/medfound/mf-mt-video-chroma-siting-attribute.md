---
description: Viene descritto come Chroma è stato campionato per un tipo di supporto video YCbCr.
ms.assetid: 0c930348-8669-42cc-9d74-df9ef475bdc8
title: Attributo MF_MT_VIDEO_CHROMA_SITING (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa634cf9a9ca7f5c292eb0cf06c6a1a14c788d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314030"
---
# <a name="mf_mt_video_chroma_siting-attribute"></a><span data-ttu-id="5e420-103">\_Attributo di \_ localizzazione del video MF mt \_ \_</span><span class="sxs-lookup"><span data-stu-id="5e420-103">MF\_MT\_VIDEO\_CHROMA\_SITING attribute</span></span>

<span data-ttu-id="5e420-104">Descrive il modo in cui Chroma è stato campionato per un tipo di supporto video Cb'Cr.</span><span class="sxs-lookup"><span data-stu-id="5e420-104">Describes how chroma was sampled for a Y'Cb'Cr' video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="5e420-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5e420-105">Data type</span></span>

<span data-ttu-id="5e420-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5e420-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5e420-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e420-107">Remarks</span></span>

<span data-ttu-id="5e420-108">Il valore di questo attributo è **un operatore OR** bit per bit di flag dell'enumerazione [**MFVideoChromaSubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) .</span><span class="sxs-lookup"><span data-stu-id="5e420-108">The value of this attribute is a bitwise **OR** of flags from the [**MFVideoChromaSubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) enumeration.</span></span>

<span data-ttu-id="5e420-109">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5e420-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e420-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e420-110">Requirements</span></span>



| <span data-ttu-id="5e420-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e420-111">Requirement</span></span> | <span data-ttu-id="5e420-112">Valore</span><span class="sxs-lookup"><span data-stu-id="5e420-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e420-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e420-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5e420-114">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5e420-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5e420-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e420-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5e420-116">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="5e420-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5e420-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e420-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e420-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e420-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e420-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e420-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e420-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5e420-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5e420-121">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="5e420-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5e420-122">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="5e420-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5e420-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5e420-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="5e420-124">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="5e420-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="5e420-125">Informazioni sui colori estesi</span><span class="sxs-lookup"><span data-stu-id="5e420-125">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




