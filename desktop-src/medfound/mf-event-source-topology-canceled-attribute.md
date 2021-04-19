---
description: Specifica se l'origine del sequencer ha annullato una topologia.
ms.assetid: b7252336-1612-43fc-8f08-1fdfdbb293eb
title: Attributo MF_EVENT_SOURCE_TOPOLOGY_CANCELED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a161aec292d834b0418f59f1c26ea2f11a538e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319610"
---
# <a name="mf_event_source_topology_canceled-attribute"></a><span data-ttu-id="f4e82-103">\_Attributo per \_ la \_ topologia di origine eventi MF \_</span><span class="sxs-lookup"><span data-stu-id="f4e82-103">MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED attribute</span></span>

<span data-ttu-id="f4e82-104">Specifica se l' [origine del sequencer](sequencer-source.md) ha annullato una topologia.</span><span class="sxs-lookup"><span data-stu-id="f4e82-104">Specifies whether the [Sequencer Source](sequencer-source.md) canceled a topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="f4e82-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f4e82-105">Data type</span></span>

<span data-ttu-id="f4e82-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f4e82-106">**UINT32**</span></span>

<span data-ttu-id="f4e82-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="f4e82-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4e82-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4e82-108">Remarks</span></span>

<span data-ttu-id="f4e82-109">Questo attributo viene usato con gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4e82-109">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="f4e82-110">MEEndOfPresentationSegment</span><span class="sxs-lookup"><span data-stu-id="f4e82-110">MEEndOfPresentationSegment</span></span>](meendofpresentationsegment.md)
-   [<span data-ttu-id="f4e82-111">MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="f4e82-111">MEEndOfPresentation</span></span>](meendofpresentation.md)

<span data-ttu-id="f4e82-112">Se questo attributo è presente e diverso da zero, significa che il segmento di presentazione è stato terminato perché l'origine del sequencer ha annullato la topologia.</span><span class="sxs-lookup"><span data-stu-id="f4e82-112">If this attribute is present and nonzero, it means that the presentation segment ended because the sequencer source canceled the topology.</span></span> <span data-ttu-id="f4e82-113">In caso contrario, il segmento di presentazione termina normalmente.</span><span class="sxs-lookup"><span data-stu-id="f4e82-113">Otherwise, the presentation segment ended normally.</span></span>

<span data-ttu-id="f4e82-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f4e82-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4e82-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4e82-115">Requirements</span></span>



| <span data-ttu-id="f4e82-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4e82-116">Requirement</span></span> | <span data-ttu-id="f4e82-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f4e82-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4e82-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4e82-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f4e82-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4e82-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f4e82-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4e82-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f4e82-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f4e82-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f4e82-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4e82-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4e82-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4e82-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4e82-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4e82-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4e82-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4e82-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4e82-126">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="f4e82-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4e82-127">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="f4e82-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f4e82-128">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="f4e82-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f4e82-129">Eventi di origine di Sequencer</span><span class="sxs-lookup"><span data-stu-id="f4e82-129">Sequencer Source Events</span></span>](sequencer-source-events.md)
</dt> </dl>

 

 




