---
description: Frequenza di errore dei dati, in bit di errori al secondo, per un tipo di supporto video.
ms.assetid: 90433ff4-a563-4751-86d9-caac0cc58194
title: Attributo MF_MT_AVG_BIT_ERROR_RATE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21eb33d1bc1636dd047dbd56ce6b7ad3a683f356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226637"
---
# <a name="mf_mt_avg_bit_error_rate-attribute"></a><span data-ttu-id="78752-103">\_ \_ \_ \_ Attributo frequenza media errori bit \_ MF mt</span><span class="sxs-lookup"><span data-stu-id="78752-103">MF\_MT\_AVG\_BIT\_ERROR\_RATE attribute</span></span>

<span data-ttu-id="78752-104">Frequenza di errore dei dati, in bit di errori al secondo, per un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="78752-104">Data error rate, in bit errors per second, for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="78752-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="78752-105">Data type</span></span>

<span data-ttu-id="78752-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="78752-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="78752-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="78752-107">Remarks</span></span>

<span data-ttu-id="78752-108">Questo attributo corrisponde al membro **dwBitErrorRate** delle strutture [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) e [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="78752-108">This attribute corresponds to the **dwBitErrorRate** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structures.</span></span>

<span data-ttu-id="78752-109">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="78752-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="78752-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78752-110">Requirements</span></span>



| <span data-ttu-id="78752-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="78752-111">Requirement</span></span> | <span data-ttu-id="78752-112">Valore</span><span class="sxs-lookup"><span data-stu-id="78752-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="78752-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78752-113">Minimum supported client</span></span><br/> | <span data-ttu-id="78752-114">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="78752-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="78752-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78752-115">Minimum supported server</span></span><br/> | <span data-ttu-id="78752-116">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="78752-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="78752-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78752-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="78752-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="78752-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78752-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78752-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78752-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="78752-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="78752-121">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="78752-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="78752-122">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="78752-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="78752-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="78752-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="78752-124">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="78752-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
