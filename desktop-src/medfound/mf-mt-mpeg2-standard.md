---
description: Per un tipo di supporto che descrive un flusso di programma MPEG-2 (PS) o un flusso di trasporto (TS), specifica lo standard usato per eseguire il multiplexing del flusso.
ms.assetid: 3D4C1A81-A9BA-427F-93DB-F522A0616EAB
title: Attributo MF_MT_MPEG2_STANDARD (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0650a68975f449ea938b41872005e11d79922393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310827"
---
# <a name="mf_mt_mpeg2_standard-attribute"></a><span data-ttu-id="5b6e0-103">\_ \_ Attributo standard MF mt MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="5b6e0-103">MF\_MT\_MPEG2\_STANDARD attribute</span></span>

<span data-ttu-id="5b6e0-104">Per un tipo di supporto che descrive un flusso di programma MPEG-2 (PS) o un flusso di trasporto (TS), specifica lo standard usato per eseguire il multiplexing del flusso.</span><span class="sxs-lookup"><span data-stu-id="5b6e0-104">For a media type that describes an MPEG-2 program stream (PS) or transport stream (TS), specifies the standard that is used to multiplex the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="5b6e0-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5b6e0-105">Data type</span></span>

<span data-ttu-id="5b6e0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5b6e0-106">**UINT32**</span></span>



| <span data-ttu-id="5b6e0-107">Valore</span><span class="sxs-lookup"><span data-stu-id="5b6e0-107">Value</span></span>                                                                                                | <span data-ttu-id="5b6e0-108">Significato</span><span class="sxs-lookup"><span data-stu-id="5b6e0-108">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="5b6e0-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="5b6e0-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="5b6e0-110">MPEG-2 PS o TS standard.</span><span class="sxs-lookup"><span data-stu-id="5b6e0-110">Standard MPEG-2 PS or TS.</span></span><br/>                                       |
| <span id="1"></span><dl> <span data-ttu-id="5b6e0-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="5b6e0-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="5b6e0-112">Standard ATSC (Advanced Television Systems Committee).</span><span class="sxs-lookup"><span data-stu-id="5b6e0-112">Advanced Television Systems Committee (ATSC) standard.</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="5b6e0-113"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="5b6e0-113"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="5b6e0-114">Standard DVB (Digital video broadcast).</span><span class="sxs-lookup"><span data-stu-id="5b6e0-114">Digital Video Broadcasting (DVB) standard.</span></span><br/>                      |
| <span id="3"></span><dl> <span data-ttu-id="5b6e0-115"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="5b6e0-115"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="5b6e0-116">Association of Radio Industries and Businesss (ARIB) standard.</span><span class="sxs-lookup"><span data-stu-id="5b6e0-116">Association of Radio Industries and Businesses (ARIB) standard.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5b6e0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b6e0-117">Requirements</span></span>



| <span data-ttu-id="5b6e0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b6e0-118">Requirement</span></span> | <span data-ttu-id="5b6e0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5b6e0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6e0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b6e0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5b6e0-121">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5b6e0-121">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="5b6e0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b6e0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5b6e0-123">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="5b6e0-123">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5b6e0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b6e0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b6e0-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b6e0-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b6e0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b6e0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b6e0-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5b6e0-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




