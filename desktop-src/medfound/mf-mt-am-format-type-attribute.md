---
description: Contiene un GUID del formato DirectShow per un tipo di supporto.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: Attributo MF_MT_AM_FORMAT_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a8faf88128075e5c5b51c1b5ace39329d4e1fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344571"
---
# <a name="mf_mt_am_format_type-attribute"></a><span data-ttu-id="a912a-103">\_ \_ \_ Attributo tipo di formato MF mt \_</span><span class="sxs-lookup"><span data-stu-id="a912a-103">MF\_MT\_AM\_FORMAT\_TYPE attribute</span></span>

<span data-ttu-id="a912a-104">Contiene un GUID del formato DirectShow per un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="a912a-104">Contains a DirectShow format GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a912a-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a912a-105">Data type</span></span>

<span data-ttu-id="a912a-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="a912a-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="a912a-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="a912a-107">Remarks</span></span>

<span data-ttu-id="a912a-108">Questo attributo può essere impostato quando un tipo di supporto DirectShow viene convertito in un tipo di supporto Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a912a-108">This attribute might be set when a DirectShow media type is converted into a Media Foundation media type.</span></span> <span data-ttu-id="a912a-109">L'attributo indica il tipo di formato DirectShow originale.</span><span class="sxs-lookup"><span data-stu-id="a912a-109">The attribute indicates the original DirectShow format type.</span></span> <span data-ttu-id="a912a-110">Il valore corrisponde al membro formatType della struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="a912a-110">The value corresponds to the formattype member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="a912a-111">Per un formato audio, l' [**attributo \_ \_ \_ dati utente MF mt**](mf-mt-user-data-attribute.md) può contenere il blocco di formato originale, se il tipo di formato DirectShow non è stato riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="a912a-111">For an audio format, the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute might contain the original format block, if the DirectShow format type was not recognized.</span></span>

<span data-ttu-id="a912a-112">Non impostare questo attributo su un tipo di supporto a meno che non si converta una struttura del formato DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a912a-112">Do not set this attribute on a media type unless you are converting a DirectShow format structure.</span></span>

<span data-ttu-id="a912a-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a912a-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a912a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a912a-114">Requirements</span></span>



| <span data-ttu-id="a912a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a912a-115">Requirement</span></span> | <span data-ttu-id="a912a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a912a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a912a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a912a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a912a-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a912a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a912a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a912a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a912a-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a912a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a912a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a912a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a912a-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a912a-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a912a-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a912a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a912a-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a912a-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a912a-125">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="a912a-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="a912a-126">Conversioni di tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="a912a-126">Media Type Conversions</span></span>](media-type-conversions.md)
</dt> <dt>

[<span data-ttu-id="a912a-127">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="a912a-127">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="a912a-128">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="a912a-128">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="a912a-129">**IMFAttributes:: Seguid**</span><span class="sxs-lookup"><span data-stu-id="a912a-129">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="a912a-130">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a912a-130">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a912a-131">**MFCreateMediaTypeFromRepresentation**</span><span class="sxs-lookup"><span data-stu-id="a912a-131">**MFCreateMediaTypeFromRepresentation**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
