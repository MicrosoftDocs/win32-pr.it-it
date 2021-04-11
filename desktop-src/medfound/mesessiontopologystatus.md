---
description: Generato dalla sessione multimediale quando lo stato di una topologia cambia.
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: Evento MESessionTopologyStatus (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11948e27997037c1e875e192fd712a2f8a132b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967053"
---
# <a name="mesessiontopologystatus-event"></a><span data-ttu-id="756fe-103">Evento MESessionTopologyStatus</span><span class="sxs-lookup"><span data-stu-id="756fe-103">MESessionTopologyStatus event</span></span>

<span data-ttu-id="756fe-104">Generato dalla sessione multimediale quando lo stato di una topologia cambia.</span><span class="sxs-lookup"><span data-stu-id="756fe-104">Raised by the Media Session when the status of a topology changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="756fe-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="756fe-105">Event values</span></span>

<span data-ttu-id="756fe-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="756fe-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="756fe-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="756fe-107">VARTYPE</span></span>                | <span data-ttu-id="756fe-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="756fe-108">Description</span></span>                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="756fe-109">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="756fe-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="756fe-110">Puntatore all'interfaccia [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) della topologia.</span><span class="sxs-lookup"><span data-stu-id="756fe-110">Pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the topology.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="756fe-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="756fe-111">Attributes</span></span>

<span data-ttu-id="756fe-112">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="756fe-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="756fe-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="756fe-113">Attribute</span></span>                                                                            | <span data-ttu-id="756fe-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="756fe-114">Description</span></span>                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="756fe-115">**\_ \_ stato topologia evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="756fe-115">**MF\_EVENT\_TOPOLOGY\_STATUS**</span></span>](mf-event-topology-status-attribute.md)<br/> | <span data-ttu-id="756fe-116">Specifica il nuovo stato della topologia.</span><span class="sxs-lookup"><span data-stu-id="756fe-116">Specifies the new status of the topology.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="756fe-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="756fe-117">Remarks</span></span>

<span data-ttu-id="756fe-118">Per un esempio di codice che recupera il puntatore [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) dall'evento, vedere evento [MESessionTopologySet](mesessiontopologyset.md) .</span><span class="sxs-lookup"><span data-stu-id="756fe-118">For a code example that retrieves the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) pointer from the event, see [MESessionTopologySet](mesessiontopologyset.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="756fe-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="756fe-119">Requirements</span></span>



| <span data-ttu-id="756fe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="756fe-120">Requirement</span></span> | <span data-ttu-id="756fe-121">Valore</span><span class="sxs-lookup"><span data-stu-id="756fe-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="756fe-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="756fe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="756fe-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="756fe-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="756fe-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="756fe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="756fe-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="756fe-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="756fe-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="756fe-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="756fe-127"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="756fe-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="756fe-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="756fe-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="756fe-129">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="756fe-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




