---
description: Specifica il livello MPEG-2 o H. 264 in un tipo di supporto video.
ms.assetid: 8dd8e8c4-5a6f-4a87-a643-73af35c362a9
title: Attributo MF_MT_MPEG2_LEVEL (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111c4b30befb1d4b25a688d25f46f02bcef21541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232388"
---
# <a name="mf_mt_mpeg2_level-attribute"></a><span data-ttu-id="c2213-103">\_ \_ Attributo livello MPEG2 MF mt \_</span><span class="sxs-lookup"><span data-stu-id="c2213-103">MF\_MT\_MPEG2\_LEVEL attribute</span></span>

<span data-ttu-id="c2213-104">Specifica il livello MPEG-2 o H. 264 in un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="c2213-104">Specifies the MPEG-2 or H.264 level in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="c2213-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c2213-105">Data type</span></span>

<span data-ttu-id="c2213-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c2213-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c2213-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2213-107">Remarks</span></span>

<span data-ttu-id="c2213-108">Per il video MPEG-2, il valore di questo attributo è un membro dell'enumerazione [**am \_ MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) .</span><span class="sxs-lookup"><span data-stu-id="c2213-108">For MPEG-2 video, the value of this attribute is a member of the [**AM\_MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) enumeration.</span></span>

<span data-ttu-id="c2213-109">Per il video H. 264, il valore è un membro dell'enumerazione [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) .</span><span class="sxs-lookup"><span data-stu-id="c2213-109">For H.264 video, the value is a member of the [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) enumeration.</span></span>

<span data-ttu-id="c2213-110">Questo attributo corrisponde al membro **dwLevel** della struttura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="c2213-110">This attribute corresponds to the **dwLevel** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span>

<span data-ttu-id="c2213-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c2213-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2213-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2213-112">Requirements</span></span>



| <span data-ttu-id="c2213-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2213-113">Requirement</span></span> | <span data-ttu-id="c2213-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c2213-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2213-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2213-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c2213-116">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c2213-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c2213-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2213-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c2213-118">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c2213-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c2213-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2213-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2213-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2213-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2213-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2213-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2213-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c2213-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c2213-123">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="c2213-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c2213-124">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="c2213-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c2213-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="c2213-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="c2213-126">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="c2213-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
