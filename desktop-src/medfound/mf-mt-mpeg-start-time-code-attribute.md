---
description: Codice dell'ora di inizio del GOP (Group-of-Pictures), per un tipo di supporto video MPEG-1 o MPEG-2.
ms.assetid: 8313b83c-5a0a-4aaa-bdc8-58a987c329c7
title: Attributo MF_MT_MPEG_START_TIME_CODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b19a041dbcd791359d704b407445779927d0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315033"
---
# <a name="mf_mt_mpeg_start_time_code-attribute"></a><span data-ttu-id="a8641-103">\_ \_ \_ \_ Attributo codice ora di inizio MF mt MPEG \_</span><span class="sxs-lookup"><span data-stu-id="a8641-103">MF\_MT\_MPEG\_START\_TIME\_CODE attribute</span></span>

<span data-ttu-id="a8641-104">Codice dell'ora di inizio del GOP (Group-of-Pictures), per un tipo di supporto video MPEG-1 o MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="a8641-104">Group-of-pictures (GOP) start time code, for an MPEG-1 or MPEG-2 video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a8641-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a8641-105">Data type</span></span>

<span data-ttu-id="a8641-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a8641-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a8641-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8641-107">Remarks</span></span>

<span data-ttu-id="a8641-108">Questo attributo corrisponde al membro **dwStartTimeCode** delle strutture [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) e [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="a8641-108">This attribute corresponds to the **dwStartTimeCode** member of the [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) and [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structures.</span></span>

<span data-ttu-id="a8641-109">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a8641-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8641-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8641-110">Requirements</span></span>



| <span data-ttu-id="a8641-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8641-111">Requirement</span></span> | <span data-ttu-id="a8641-112">Valore</span><span class="sxs-lookup"><span data-stu-id="a8641-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a8641-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8641-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a8641-114">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a8641-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a8641-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8641-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a8641-116">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="a8641-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a8641-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8641-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8641-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8641-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8641-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8641-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8641-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a8641-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a8641-121">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="a8641-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a8641-122">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="a8641-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a8641-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a8641-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a8641-124">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="a8641-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="a8641-125">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a8641-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 
