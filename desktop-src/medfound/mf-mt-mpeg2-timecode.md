---
description: Per un tipo di supporto che descrive un flusso di trasporto MPEG-2 (TS), specifica che i pacchetti di trasporto contengono un codice a 4 byte.
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: Attributo MF_MT_MPEG2_TIMECODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc9db5d7b3c6e94f7845bec2bd98c569d1b1f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232387"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a><span data-ttu-id="800fe-103">\_ \_ Attributo timecode MF mt MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="800fe-103">MF\_MT\_MPEG2\_TIMECODE attribute</span></span>

<span data-ttu-id="800fe-104">Per un tipo di supporto che descrive un flusso di trasporto MPEG-2 (TS), specifica che i pacchetti di trasporto contengono un codice a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="800fe-104">For a media type that describes an MPEG-2 transport stream (TS), specifies the transport packets contain a 4-byte time code.</span></span>

## <a name="data-type"></a><span data-ttu-id="800fe-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="800fe-105">Data type</span></span>

<span data-ttu-id="800fe-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="800fe-106">**UINT32**</span></span>



| <span data-ttu-id="800fe-107">Valore</span><span class="sxs-lookup"><span data-stu-id="800fe-107">Value</span></span>                                                                                                | <span data-ttu-id="800fe-108">Significato</span><span class="sxs-lookup"><span data-stu-id="800fe-108">Meaning</span></span>                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="800fe-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="800fe-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="800fe-110">Nessun codice ora aggiunto.</span><span class="sxs-lookup"><span data-stu-id="800fe-110">No time code is added.</span></span><br/>                                                                                                              |
| <span id="1"></span><dl> <span data-ttu-id="800fe-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="800fe-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="800fe-112">All'inizio di ogni pacchetto di trasporto viene aggiunto un codice a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="800fe-112">A 4-byte time code is added at the start of each transport packet.</span></span> <span data-ttu-id="800fe-113">Questo codice temporale è necessario per alcuni standard della televisione digitale.</span><span class="sxs-lookup"><span data-stu-id="800fe-113">This time code is required by some digital television standards.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="800fe-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="800fe-114">Requirements</span></span>



| <span data-ttu-id="800fe-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="800fe-115">Requirement</span></span> | <span data-ttu-id="800fe-116">Valore</span><span class="sxs-lookup"><span data-stu-id="800fe-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="800fe-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="800fe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="800fe-118">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="800fe-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="800fe-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="800fe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="800fe-120">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="800fe-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="800fe-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="800fe-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="800fe-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="800fe-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="800fe-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="800fe-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="800fe-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="800fe-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




