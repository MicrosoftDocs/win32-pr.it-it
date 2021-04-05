---
description: Ora di presentazione in cui i sink dei supporti eseguiranno il rendering del primo campione della nuova topologia.
ms.assetid: 02a8c542-b519-495e-9fb2-8db2f5384db7
title: Attributo MF_EVENT_START_PRESENTATION_TIME_AT_OUTPUT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a588bc6604deed6c6865cd8283390d28e3ffd49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882833"
---
# <a name="mf_event_start_presentation_time_at_output-attribute"></a><span data-ttu-id="f3d64-103">\_ \_ \_ \_ Ora di presentazione dell'avvio \_ dell'evento MF all' \_ attributo di output</span><span class="sxs-lookup"><span data-stu-id="f3d64-103">MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT attribute</span></span>

<span data-ttu-id="f3d64-104">Ora di presentazione in cui i sink dei supporti eseguiranno il rendering del primo campione della nuova topologia.</span><span class="sxs-lookup"><span data-stu-id="f3d64-104">The presentation time at which the media sinks will render the first sample of the new topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="f3d64-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f3d64-105">Data type</span></span>

<span data-ttu-id="f3d64-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="f3d64-106">**UINT64**</span></span>

<span data-ttu-id="f3d64-107">Considera come valore **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="f3d64-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3d64-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3d64-108">Remarks</span></span>

<span data-ttu-id="f3d64-109">Se tutti gli oggetti pipeline nella topologia precedente hanno memorizzato nel buffer i dati, questo valore sarà leggermente inferiore al valore nell'attributo dell' [**offset dell'ora di \_ presentazione dell'evento \_ \_ \_ MF**](mf-event-presentation-time-offset-attribute.md) , perché i sink devono eseguire il rendering dei dati memorizzati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="f3d64-109">If any pipeline objects in the previous topology buffered data, this value will be slightly less than the value in the [**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**](mf-event-presentation-time-offset-attribute.md) attribute, because the sinks must render the buffered data.</span></span>

<span data-ttu-id="f3d64-110">Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**.</span><span class="sxs-lookup"><span data-stu-id="f3d64-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="f3d64-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f3d64-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3d64-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3d64-112">Requirements</span></span>



| <span data-ttu-id="f3d64-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3d64-113">Requirement</span></span> | <span data-ttu-id="f3d64-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f3d64-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d64-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3d64-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f3d64-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3d64-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f3d64-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3d64-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f3d64-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f3d64-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f3d64-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3d64-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3d64-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3d64-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3d64-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3d64-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3d64-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f3d64-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f3d64-123">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="f3d64-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="f3d64-124">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="f3d64-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="f3d64-125">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="f3d64-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




