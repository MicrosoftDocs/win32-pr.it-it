---
description: GUID di tipo principale per un tipo di supporto.
ms.assetid: b88b5fcf-8025-4638-930d-9fc5cf0ec8a3
title: Attributo MF_MT_MAJOR_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c4cc02df4f89e261605c91b71ac1c80ba38b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307508"
---
# <a name="mf_mt_major_type-attribute"></a><span data-ttu-id="6d11b-103">\_Attributo di \_ tipo principale MF mt \_</span><span class="sxs-lookup"><span data-stu-id="6d11b-103">MF\_MT\_MAJOR\_TYPE attribute</span></span>

<span data-ttu-id="6d11b-104">GUID di tipo principale per un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6d11b-104">Major type GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="6d11b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6d11b-105">Data type</span></span>

<span data-ttu-id="6d11b-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="6d11b-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="6d11b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d11b-107">Remarks</span></span>

<span data-ttu-id="6d11b-108">Il tipo principale definisce la categoria complessiva dei dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="6d11b-108">The major type defines the overall category of the media data.</span></span> <span data-ttu-id="6d11b-109">I tipi principali includono video, audio, script e così via.</span><span class="sxs-lookup"><span data-stu-id="6d11b-109">Major types include video, audio, script, and so forth.</span></span> <span data-ttu-id="6d11b-110">Per un elenco di valori possibili, vedere [principali tipi di supporti](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="6d11b-110">For a list of possible values, see [Major Media Types](media-type-guids.md).</span></span>

<span data-ttu-id="6d11b-111">Un metodo alternativo per recuperare questo attributo consiste nel chiamare [**IMFMediaType:: GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="6d11b-111">An alternate way to retrieve this attribute is to call [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).</span></span>

<span data-ttu-id="6d11b-112">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6d11b-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d11b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d11b-113">Requirements</span></span>



| <span data-ttu-id="6d11b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d11b-114">Requirement</span></span> | <span data-ttu-id="6d11b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6d11b-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d11b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d11b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6d11b-117">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6d11b-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6d11b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d11b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6d11b-119">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="6d11b-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6d11b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d11b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d11b-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d11b-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d11b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d11b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d11b-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6d11b-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6d11b-124">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="6d11b-124">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="6d11b-125">**IMFAttributes:: Seguid**</span><span class="sxs-lookup"><span data-stu-id="6d11b-125">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="6d11b-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6d11b-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="6d11b-127">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="6d11b-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




