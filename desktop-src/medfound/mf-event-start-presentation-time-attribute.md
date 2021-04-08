---
description: Ora di inizio per la presentazione, in unità di 100 nanosecondi, misurata dal clock di presentazione.
ms.assetid: d19d851c-ab4a-4a9d-bcc4-8dd4e993fa2c
title: Attributo MF_EVENT_START_PRESENTATION_TIME (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65bf6142ce12a7bf921fd26373ea5d10ab384560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058363"
---
# <a name="mf_event_start_presentation_time-attribute"></a><span data-ttu-id="536d3-103">\_ \_ \_ Attributo tempo di presentazione di inizio evento MF \_</span><span class="sxs-lookup"><span data-stu-id="536d3-103">MF\_EVENT\_START\_PRESENTATION\_TIME attribute</span></span>

<span data-ttu-id="536d3-104">Ora di inizio per la presentazione, in unità di 100 nanosecondi, misurata dal clock di presentazione.</span><span class="sxs-lookup"><span data-stu-id="536d3-104">The starting time for the presentation, in 100-nanosecond units, as measured by the presentation clock.</span></span>

## <a name="data-type"></a><span data-ttu-id="536d3-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="536d3-105">Data type</span></span>

<span data-ttu-id="536d3-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="536d3-106">**UINT64**</span></span>

<span data-ttu-id="536d3-107">Considera come valore **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="536d3-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="536d3-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="536d3-108">Remarks</span></span>

<span data-ttu-id="536d3-109">Questo attributo viene utilizzato con l'evento [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) .</span><span class="sxs-lookup"><span data-stu-id="536d3-109">This attribute is used with the [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) event.</span></span>

<span data-ttu-id="536d3-110">Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**.</span><span class="sxs-lookup"><span data-stu-id="536d3-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="536d3-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="536d3-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="536d3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="536d3-112">Requirements</span></span>



| <span data-ttu-id="536d3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="536d3-113">Requirement</span></span> | <span data-ttu-id="536d3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="536d3-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="536d3-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="536d3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="536d3-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="536d3-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="536d3-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="536d3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="536d3-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="536d3-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="536d3-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="536d3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="536d3-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="536d3-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="536d3-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="536d3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="536d3-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="536d3-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="536d3-123">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="536d3-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="536d3-124">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="536d3-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="536d3-125">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="536d3-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




