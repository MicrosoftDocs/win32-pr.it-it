---
description: Contiene l'intestazione della sequenza MPEG-1 o MPEG-2 per un tipo di supporto video.
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: Attributo MF_MT_MPEG_SEQUENCE_HEADER (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4003137ec4d2942bc95f56b2ce54644eb7b678d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315032"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a><span data-ttu-id="9dad1-103">\_ \_ \_ Attributo header della sequenza MF mt MPEG \_</span><span class="sxs-lookup"><span data-stu-id="9dad1-103">MF\_MT\_MPEG\_SEQUENCE\_HEADER attribute</span></span>

<span data-ttu-id="9dad1-104">Contiene l'intestazione della sequenza MPEG-1 o MPEG-2 per un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="9dad1-104">Contains the MPEG-1 or MPEG-2 sequence header for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="9dad1-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9dad1-105">Data type</span></span>

<span data-ttu-id="9dad1-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="9dad1-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="9dad1-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="9dad1-107">Remarks</span></span>

<span data-ttu-id="9dad1-108">Questo attributo corrisponde al membro **dwSequenceHeader** della struttura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) o al membro **bSequenceHeader** della struttura [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="9dad1-108">This attribute corresponds to the **dwSequenceHeader** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure, or the **bSequenceHeader** member of the [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) structure.</span></span>

<span data-ttu-id="9dad1-109">Per i video H264 e H265, il BLOB contiene [unità NAL](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) concatenate nel formato allegato B, insieme ai relativi codici iniziali.</span><span class="sxs-lookup"><span data-stu-id="9dad1-109">For h264 and h265 video, the blob contains concatenated [NAL units](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) in Annex B format, along with their start codes.</span></span> <span data-ttu-id="9dad1-110">In particolare, per i video H264 si tratta di SPS & unità NAL di PPS.</span><span class="sxs-lookup"><span data-stu-id="9dad1-110">Specifically, for h264 video they are SPS & PPS NAL units.</span></span> <span data-ttu-id="9dad1-111">Per H265 sono VPS, SPS & PPS.</span><span class="sxs-lookup"><span data-stu-id="9dad1-111">For h265 they are VPS, SPS & PPS.</span></span>

<span data-ttu-id="9dad1-112">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="9dad1-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dad1-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9dad1-113">Requirements</span></span>



| <span data-ttu-id="9dad1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dad1-114">Requirement</span></span> | <span data-ttu-id="9dad1-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9dad1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9dad1-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dad1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9dad1-117">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="9dad1-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="9dad1-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dad1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9dad1-119">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="9dad1-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="9dad1-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9dad1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dad1-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dad1-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dad1-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9dad1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dad1-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9dad1-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9dad1-124">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="9dad1-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="9dad1-125">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="9dad1-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="9dad1-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="9dad1-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="9dad1-127">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="9dad1-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
