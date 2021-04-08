---
description: Specifica il profilo MPEG-2 o H. 264 in un tipo di supporto video.
ms.assetid: 8c6a68cb-d976-4099-8934-064f0e8f6374
title: Attributo MF_MT_MPEG2_PROFILE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee5c64ea9f5bdf73a78d6ae29124c7cd5b37df43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883214"
---
# <a name="mf_mt_mpeg2_profile-attribute"></a><span data-ttu-id="dbc33-103">\_ \_ Attributo profilo MF mt MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="dbc33-103">MF\_MT\_MPEG2\_PROFILE attribute</span></span>

<span data-ttu-id="dbc33-104">Specifica il profilo MPEG-2 o H. 264 in un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="dbc33-104">Specifies the MPEG-2 or H.264 profile in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="dbc33-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="dbc33-105">Data type</span></span>

<span data-ttu-id="dbc33-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dbc33-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="dbc33-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="dbc33-107">Remarks</span></span>

<span data-ttu-id="dbc33-108">Per il video MPEG-2, il valore di questo attributo è un membro dell'enumerazione [**am \_ MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) .</span><span class="sxs-lookup"><span data-stu-id="dbc33-108">For MPEG-2 video, the value of this attribute is a member of the [**AM\_MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) enumeration.</span></span>

<span data-ttu-id="dbc33-109">Per il video H. 264, il valore è un membro dell'enumerazione [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .</span><span class="sxs-lookup"><span data-stu-id="dbc33-109">For H.264 video, the value is a member of the [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) enumeration.</span></span>

<span data-ttu-id="dbc33-110">Questo attributo corrisponde al membro **dwProfile** della struttura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="dbc33-110">This attribute corresponds to the **dwProfile** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span>

<span data-ttu-id="dbc33-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="dbc33-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc33-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbc33-112">Requirements</span></span>



| <span data-ttu-id="dbc33-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbc33-113">Requirement</span></span> | <span data-ttu-id="dbc33-114">Valore</span><span class="sxs-lookup"><span data-stu-id="dbc33-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc33-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbc33-115">Minimum supported client</span></span><br/> | <span data-ttu-id="dbc33-116">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dbc33-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="dbc33-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbc33-117">Minimum supported server</span></span><br/> | <span data-ttu-id="dbc33-118">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="dbc33-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="dbc33-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dbc33-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbc33-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbc33-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbc33-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbc33-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc33-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dbc33-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dbc33-123">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="dbc33-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="dbc33-124">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="dbc33-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="dbc33-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="dbc33-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="dbc33-126">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="dbc33-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
