---
description: Contiene i flag varie per un tipo di supporto video MPEG-2.
ms.assetid: 2e1bf3e3-c005-418b-b9fd-1d43c42dad6f
title: Attributo MF_MT_MPEG2_FLAGS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ef0a0def9c3e5413ec9b9bf7568fcbe9add851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318065"
---
# <a name="mf_mt_mpeg2_flags-attribute"></a><span data-ttu-id="cfb3b-103">\_ \_ Attributo flag MPEG2 MF mt \_</span><span class="sxs-lookup"><span data-stu-id="cfb3b-103">MF\_MT\_MPEG2\_FLAGS attribute</span></span>

<span data-ttu-id="cfb3b-104">Contiene i flag varie per un tipo di supporto video MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-104">Contains miscellaneous flags for an MPEG-2 video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="cfb3b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cfb3b-105">Data type</span></span>

<span data-ttu-id="cfb3b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cfb3b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cfb3b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="cfb3b-107">Remarks</span></span>

<span data-ttu-id="cfb3b-108">Questo attributo corrisponde al membro **dwFlags** della struttura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="cfb3b-108">This attribute corresponds to the **dwFlags** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="cfb3b-109">Per un elenco dei flag validi, vedere la documentazione relativa a **MPEG2VIDEOINFO**.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-109">For a list of valid flags, see the documentation for **MPEG2VIDEOINFO**.</span></span>

<span data-ttu-id="cfb3b-110">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="cfb3b-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfb3b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfb3b-111">Requirements</span></span>



| <span data-ttu-id="cfb3b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfb3b-112">Requirement</span></span> | <span data-ttu-id="cfb3b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="cfb3b-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb3b-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfb3b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="cfb3b-115">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cfb3b-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="cfb3b-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfb3b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="cfb3b-117">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="cfb3b-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="cfb3b-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cfb3b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfb3b-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfb3b-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfb3b-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfb3b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfb3b-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cfb3b-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cfb3b-122">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="cfb3b-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="cfb3b-123">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="cfb3b-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="cfb3b-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="cfb3b-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="cfb3b-125">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="cfb3b-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
