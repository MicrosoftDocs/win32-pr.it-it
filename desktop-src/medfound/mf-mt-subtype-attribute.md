---
description: GUID del sottotipo per un tipo di supporto.
ms.assetid: 8e600943-92f1-4936-8c00-842fc7f4cb57
title: Attributo MF_MT_SUBTYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f156e356a0e80d6b2c4bff1ae6f266e4d64b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050093"
---
# <a name="mf_mt_subtype-attribute"></a><span data-ttu-id="7c6c2-103">\_Attributo del \_ sottotipo MF mt</span><span class="sxs-lookup"><span data-stu-id="7c6c2-103">MF\_MT\_SUBTYPE attribute</span></span>

<span data-ttu-id="7c6c2-104">GUID del sottotipo per un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="7c6c2-104">Subtype GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="7c6c2-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7c6c2-105">Data type</span></span>

<span data-ttu-id="7c6c2-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="7c6c2-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="7c6c2-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c6c2-107">Remarks</span></span>

<span data-ttu-id="7c6c2-108">Il GUID del sottotipo definisce un tipo di formato multimediale specifico all'interno di un tipo principale.</span><span class="sxs-lookup"><span data-stu-id="7c6c2-108">The subtype GUID defines a specific media format type within a major type.</span></span> <span data-ttu-id="7c6c2-109">Ad esempio, all'interno di video, i sottotipi includono RGB-24, RGB-32, UYVY, AYUV e così via.</span><span class="sxs-lookup"><span data-stu-id="7c6c2-109">For example, within video, the subtypes include RGB-24, RGB-32, UYVY, AYUV, and so forth.</span></span> <span data-ttu-id="7c6c2-110">All'interno di audio, i sottotipi includono audio PCM, Windows Media Audio 9 e così via.</span><span class="sxs-lookup"><span data-stu-id="7c6c2-110">Within audio, the subtypes include PCM audio, Windows Media Audio 9, and so forth.</span></span>

<span data-ttu-id="7c6c2-111">Per i valori possibili, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="7c6c2-111">For possible values, see the following topics:</span></span>

-   [<span data-ttu-id="7c6c2-112">GUID del sottotipo audio</span><span class="sxs-lookup"><span data-stu-id="7c6c2-112">Audio Subtype GUIDs</span></span>](audio-subtype-guids.md)
-   [<span data-ttu-id="7c6c2-113">GUID del sottotipo video</span><span class="sxs-lookup"><span data-stu-id="7c6c2-113">Video Subtype GUIDs</span></span>](video-subtype-guids.md)

<span data-ttu-id="7c6c2-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7c6c2-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c6c2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c6c2-115">Requirements</span></span>



| <span data-ttu-id="7c6c2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c6c2-116">Requirement</span></span> | <span data-ttu-id="7c6c2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7c6c2-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7c6c2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c6c2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7c6c2-119">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7c6c2-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7c6c2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c6c2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7c6c2-121">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="7c6c2-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7c6c2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c6c2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c6c2-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c6c2-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c6c2-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c6c2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c6c2-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7c6c2-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7c6c2-126">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="7c6c2-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="7c6c2-127">**IMFAttributes:: Seguid**</span><span class="sxs-lookup"><span data-stu-id="7c6c2-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="7c6c2-128">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="7c6c2-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="7c6c2-129">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="7c6c2-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




