---
description: Frequenza approssimativa dei dati del flusso video, in bit al secondo, per un tipo di supporto video.
ms.assetid: cf9374a7-3688-4a6c-8339-d68c267c9bed
title: Attributo MF_MT_AVG_BITRATE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e4497c58abf8587e72dea47d4f8ac222a1b0692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401773"
---
# <a name="mf_mt_avg_bitrate-attribute"></a><span data-ttu-id="7f809-103">\_ \_ \_ Attributo media bitrate MF mt</span><span class="sxs-lookup"><span data-stu-id="7f809-103">MF\_MT\_AVG\_BITRATE attribute</span></span>

<span data-ttu-id="7f809-104">Frequenza approssimativa dei dati del flusso video, in bit al secondo, per un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="7f809-104">Approximate data rate of the video stream, in bits per second, for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="7f809-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7f809-105">Data type</span></span>

<span data-ttu-id="7f809-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7f809-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7f809-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f809-107">Remarks</span></span>

<span data-ttu-id="7f809-108">Questo attributo corrisponde al membro **dwBitRate** delle strutture [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) e [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="7f809-108">This attribute corresponds to the **dwBitRate** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structures.</span></span>

<span data-ttu-id="7f809-109">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7f809-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f809-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f809-110">Requirements</span></span>



| <span data-ttu-id="7f809-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f809-111">Requirement</span></span> | <span data-ttu-id="7f809-112">Valore</span><span class="sxs-lookup"><span data-stu-id="7f809-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f809-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f809-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7f809-114">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7f809-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7f809-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f809-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7f809-116">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="7f809-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7f809-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f809-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f809-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f809-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f809-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f809-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f809-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7f809-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f809-121">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="7f809-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7f809-122">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="7f809-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="7f809-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="7f809-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="7f809-124">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="7f809-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
