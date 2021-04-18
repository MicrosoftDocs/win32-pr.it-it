---
description: Specifica le primarie colore personalizzate per un tipo di supporto video.
ms.assetid: dc5df755-53cf-4910-af42-309f1f46b1ed
title: Attributo MF_MT_CUSTOM_VIDEO_PRIMARIES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d63e39638f74cacafa1b4376b28c7703f7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318424"
---
# <a name="mf_mt_custom_video_primaries-attribute"></a><span data-ttu-id="3ef18-103">\_ \_ \_ Attributo primari video personalizzati MF mt \_</span><span class="sxs-lookup"><span data-stu-id="3ef18-103">MF\_MT\_CUSTOM\_VIDEO\_PRIMARIES attribute</span></span>

<span data-ttu-id="3ef18-104">Specifica le primarie colore personalizzate per un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="3ef18-104">Specifies custom color primaries for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="3ef18-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3ef18-105">Data type</span></span>

<span data-ttu-id="3ef18-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3ef18-106">**UINT32**</span></span>

<span data-ttu-id="3ef18-107">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="3ef18-107">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="3ef18-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ef18-108">Remarks</span></span>

<span data-ttu-id="3ef18-109">I dati dell'attributo sono una struttura di [**\_ \_ \_ primari video personalizzati di mt**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) .</span><span class="sxs-lookup"><span data-stu-id="3ef18-109">The attribute data is an [**MT\_CUSTOM\_VIDEO\_PRIMARIES**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) structure.</span></span>

<span data-ttu-id="3ef18-110">Questo attributo specifica il volume di colori effettivo del contenuto o una visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3ef18-110">This attribute specifies the actual color volume of content or a display.</span></span> <span data-ttu-id="3ef18-111">Le informazioni di master del volume dei colori CEA-861,3/SMPTE ST. 2086 vengono archiviate in questo attributo dai decodificatori.</span><span class="sxs-lookup"><span data-stu-id="3ef18-111">CEA-861.3 / SMPTE ST.2086 color volume mastering information is stored in this attribute by decoders.</span></span> <span data-ttu-id="3ef18-112">Si noti che questo attributo non sostituisce l'attributo delle [**\_ \_ \_ primarie del video MF mt**](mf-mt-video-primaries-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="3ef18-112">Note that this attribute does not replace the [**MF\_MT\_VIDEO\_PRIMARIES**](mf-mt-video-primaries-attribute.md)attribute.</span></span> <span data-ttu-id="3ef18-113">Questo attributo descrive un suggerimento sul volume di colori del contenuto, mentre le **\_ \_ \_ primarie del video MF mt** descrivono le primarie di colore in cui il contenuto è effettivamente codificato (ad esempio, il significato di 1,0 nei canali R/g/B di una rappresentazione a virgola mobile).</span><span class="sxs-lookup"><span data-stu-id="3ef18-113">This attribute describes a hint about the color volume of the content, whereas **MF\_MT\_VIDEO\_PRIMARIES** describes the color primaries in which the content is actually coded (e.g: the meaning of 1.0 in the R/G/B channels of a floating point representation).</span></span>

<span data-ttu-id="3ef18-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3ef18-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ef18-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ef18-115">Requirements</span></span>



| <span data-ttu-id="3ef18-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ef18-116">Requirement</span></span> | <span data-ttu-id="3ef18-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3ef18-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef18-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ef18-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3ef18-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ef18-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3ef18-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ef18-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3ef18-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ef18-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3ef18-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ef18-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ef18-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ef18-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ef18-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ef18-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef18-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3ef18-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3ef18-126">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="3ef18-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="3ef18-127">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="3ef18-127">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="3ef18-128">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="3ef18-128">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="3ef18-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="3ef18-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

 




