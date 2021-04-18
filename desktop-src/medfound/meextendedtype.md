---
description: Tipo di evento personalizzato.
ms.assetid: a54a446c-0e96-467b-90f6-0f64a7c1727d
title: Evento MEExtendedType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5551110fc3637a40834a7bf9251826f151ec62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309638"
---
# <a name="meextendedtype-event"></a><span data-ttu-id="09720-103">Evento MEExtendedType</span><span class="sxs-lookup"><span data-stu-id="09720-103">MEExtendedType event</span></span>

<span data-ttu-id="09720-104">Tipo di evento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="09720-104">Custom event type.</span></span> <span data-ttu-id="09720-105">È possibile utilizzare questo tipo di evento per definire eventi personalizzati per il componente.</span><span class="sxs-lookup"><span data-stu-id="09720-105">You can use this event type to define custom events for your component.</span></span> <span data-ttu-id="09720-106">Utilizzare il tipo di evento esteso per identificare l'evento.</span><span class="sxs-lookup"><span data-stu-id="09720-106">Use the extended event type to identify the event.</span></span> <span data-ttu-id="09720-107">Il tipo di evento esteso è un valore GUID associato all'evento.</span><span class="sxs-lookup"><span data-stu-id="09720-107">The extended event type is a GUID value associated with the event.</span></span> <span data-ttu-id="09720-108">Per ulteriori informazioni, vedere [**IMFMediaEvent:: GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span><span class="sxs-lookup"><span data-stu-id="09720-108">For more information, see [**IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span></span>

## <a name="event-values"></a><span data-ttu-id="09720-109">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="09720-109">Event values</span></span>

<span data-ttu-id="09720-110">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="09720-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="09720-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="09720-111">VARTYPE</span></span>              | <span data-ttu-id="09720-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09720-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="09720-113">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="09720-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="09720-114">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="09720-114">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="09720-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09720-115">Requirements</span></span>



| <span data-ttu-id="09720-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="09720-116">Requirement</span></span> | <span data-ttu-id="09720-117">Valore</span><span class="sxs-lookup"><span data-stu-id="09720-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09720-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09720-118">Minimum supported client</span></span><br/> | <span data-ttu-id="09720-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09720-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="09720-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09720-120">Minimum supported server</span></span><br/> | <span data-ttu-id="09720-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09720-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="09720-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09720-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="09720-123"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09720-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09720-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09720-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09720-125">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="09720-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




