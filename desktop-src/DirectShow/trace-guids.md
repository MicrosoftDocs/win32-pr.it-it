---
description: I GUID seguenti vengono usati per la traccia eventi in DirectShow.
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: GUID di traccia (PerfStruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AUDIOBREAK
- GUID_DSHOW_CTL
- GUID_STREAMTRACE
- GUID_VIDEOREND
api_type:
- HeaderDef
api_location:
- PerfStruct.h
ms.openlocfilehash: 4b2f2a6a678c029d01d9bf55481837d81d48557e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331430"
---
# <a name="trace-guids"></a><span data-ttu-id="2997b-103">GUID di traccia</span><span class="sxs-lookup"><span data-stu-id="2997b-103">Trace GUIDs</span></span>

<span data-ttu-id="2997b-104">I GUID seguenti vengono usati per la traccia eventi in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2997b-104">The following GUIDs are used for event tracing in DirectShow.</span></span>



| <span data-ttu-id="2997b-105">GUID</span><span class="sxs-lookup"><span data-stu-id="2997b-105">GUID</span></span>                                                                                                                                                                   | <span data-ttu-id="2997b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2997b-106">Description</span></span>                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <span data-ttu-id="2997b-107"><dt>**GUID \_ AUDIOBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="2997b-107"><dt>**GUID\_AUDIOBREAK**</dt></span></span> </dl>    | <span data-ttu-id="2997b-108">Evento di break audio.</span><span class="sxs-lookup"><span data-stu-id="2997b-108">Audio break event.</span></span> <span data-ttu-id="2997b-109">Per gli eventi di questo tipo viene utilizzata la struttura [**\_ \_ AUDIOBREAK dshow PERFINFO**](perfinfo-dshow-audiobreak.md) per i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="2997b-109">Events of this type use the [**PERFINFO\_DSHOW\_AUDIOBREAK**](perfinfo-dshow-audiobreak.md) structure for event data.</span></span><br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <span data-ttu-id="2997b-110"><dt>**\_dshow GUID \_ CTL**</dt></span><span class="sxs-lookup"><span data-stu-id="2997b-110"><dt>**GUID\_DSHOW\_CTL**</dt></span></span> </dl>      | <span data-ttu-id="2997b-111">Provider di eventi DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2997b-111">DirectShow event provider.</span></span><br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <span data-ttu-id="2997b-112"><dt>**GUID \_ STREAMTRACE**</dt></span><span class="sxs-lookup"><span data-stu-id="2997b-112"><dt>**GUID\_STREAMTRACE**</dt></span></span> </dl> | <span data-ttu-id="2997b-113">Evento di streaming generale.</span><span class="sxs-lookup"><span data-stu-id="2997b-113">General streaming event.</span></span> <span data-ttu-id="2997b-114">Per gli eventi di questo tipo viene utilizzata la struttura [**\_ \_ STREAMTRACE dshow PERFINFO**](perfinfo-dshow-streamtrace.md) per i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="2997b-114">Events of this type use the [**PERFINFO\_DSHOW\_STREAMTRACE**](perfinfo-dshow-streamtrace.md) structure for event data.</span></span><br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <span data-ttu-id="2997b-115"><dt>**GUID \_ VIDEOREND**</dt></span><span class="sxs-lookup"><span data-stu-id="2997b-115"><dt>**GUID\_VIDEOREND**</dt></span></span> </dl>       | <span data-ttu-id="2997b-116">Evento di rendering video.</span><span class="sxs-lookup"><span data-stu-id="2997b-116">Video rendering event.</span></span> <span data-ttu-id="2997b-117">Per gli eventi di questo tipo viene utilizzata la struttura [**\_ \_ AVREND dshow PERFINFO**](perfinfo-dshow-avrend.md) per i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="2997b-117">Events of this type use the [**PERFINFO\_DSHOW\_AVREND**](perfinfo-dshow-avrend.md) structure for event data.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="2997b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2997b-118">Requirements</span></span>



| <span data-ttu-id="2997b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2997b-119">Requirement</span></span> | <span data-ttu-id="2997b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2997b-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2997b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2997b-121">Header</span></span><br/> | <dl> <span data-ttu-id="2997b-122"><dt>PerfStruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="2997b-122"><dt>PerfStruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2997b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2997b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2997b-124">Traccia eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="2997b-124">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> </dl>

 

 




