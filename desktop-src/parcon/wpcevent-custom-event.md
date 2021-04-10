---
description: Evento per utente che supporta fino a tre campi.
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: Evento WPCEVENT_CUSTOM (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d20cb2450cd18bb0c77993622d226cfc06dff6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227363"
---
# <a name="wpcevent_custom-event"></a><span data-ttu-id="5a7b4-103">\_Evento personalizzato WPCEVENT</span><span class="sxs-lookup"><span data-stu-id="5a7b4-103">WPCEVENT\_CUSTOM event</span></span>

<span data-ttu-id="5a7b4-104">Evento per utente che supporta fino a tre campi.</span><span class="sxs-lookup"><span data-stu-id="5a7b4-104">Per-user event that supports up to three fields.</span></span>

<span data-ttu-id="5a7b4-105">Gli eventi vengono visualizzati nel **Visualizzatore attività** nell' **altra** sezione con la gerarchia seguente:</span><span class="sxs-lookup"><span data-stu-id="5a7b4-105">Events are displayed in the **Activity Viewer** in the **Other** section with the following hierarchy:</span></span>

1.  <span data-ttu-id="5a7b4-106">Publisher</span><span class="sxs-lookup"><span data-stu-id="5a7b4-106">Publisher</span></span>

2.  <span data-ttu-id="5a7b4-107">Applicazione</span><span class="sxs-lookup"><span data-stu-id="5a7b4-107">Application</span></span>

3.  <span data-ttu-id="5a7b4-108">Evento</span><span class="sxs-lookup"><span data-stu-id="5a7b4-108">Event</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a><span data-ttu-id="5a7b4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a7b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a7b4-110">*Autore*</span><span class="sxs-lookup"><span data-stu-id="5a7b4-110">*Publisher*</span></span> 
</dt> <dd>

<span data-ttu-id="5a7b4-111">Server di pubblicazione dell'evento (ad esempio, un nome della società).</span><span class="sxs-lookup"><span data-stu-id="5a7b4-111">The publisher of the event (for example, a company name).</span></span>

</dd> <dt>

<span data-ttu-id="5a7b4-112">*AppName*</span><span class="sxs-lookup"><span data-stu-id="5a7b4-112">*AppName*</span></span> 
</dt> <dd>

<span data-ttu-id="5a7b4-113">Nome dell'applicazione che genera l'evento.</span><span class="sxs-lookup"><span data-stu-id="5a7b4-113">The name of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="5a7b4-114">*AppVersion*</span><span class="sxs-lookup"><span data-stu-id="5a7b4-114">*AppVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="5a7b4-115">Versione dell'applicazione che genera l'evento.</span><span class="sxs-lookup"><span data-stu-id="5a7b4-115">The version of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="5a7b4-116">*Event*</span><span class="sxs-lookup"><span data-stu-id="5a7b4-116">*Event*</span></span> 
</dt> <dd>

<span data-ttu-id="5a7b4-117">Nome dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5a7b4-117">The name for the event.</span></span>

</dd> <dt>

<span data-ttu-id="5a7b4-118">*Value1*</span><span class="sxs-lookup"><span data-stu-id="5a7b4-118">*Value1*</span></span> 
</dt> <dd>

<span data-ttu-id="5a7b4-119">Campo personalizzato 1.</span><span class="sxs-lookup"><span data-stu-id="5a7b4-119">Custom field 1.</span></span>

</dd> <dt>

<span data-ttu-id="5a7b4-120">*Value2*</span><span class="sxs-lookup"><span data-stu-id="5a7b4-120">*Value2*</span></span> 
</dt> <dd>

<span data-ttu-id="5a7b4-121">Campo personalizzato 2.</span><span class="sxs-lookup"><span data-stu-id="5a7b4-121">Custom field 2.</span></span>

</dd> <dt>

<span data-ttu-id="5a7b4-122">*Valore3*</span><span class="sxs-lookup"><span data-stu-id="5a7b4-122">*Value3*</span></span> 
</dt> <dd>

<span data-ttu-id="5a7b4-123">Campo personalizzato 3.</span><span class="sxs-lookup"><span data-stu-id="5a7b4-123">Custom field 3.</span></span>

</dd> <dt>

<span data-ttu-id="5a7b4-124">*Bloccato*</span><span class="sxs-lookup"><span data-stu-id="5a7b4-124">*Blocked*</span></span> 
</dt> <dd>

<span data-ttu-id="5a7b4-125">Valore dell'enumerazione [**WPCFLAG che \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) indica le informazioni sugli eventi che vengono bloccati dall'utilizzo e sui controlli.</span><span class="sxs-lookup"><span data-stu-id="5a7b4-125">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="5a7b4-126">*Motivo*</span><span class="sxs-lookup"><span data-stu-id="5a7b4-126">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="5a7b4-127">Stringa personalizzata che fornisce informazioni aggiuntive sul motivo del blocco o non blocco.</span><span class="sxs-lookup"><span data-stu-id="5a7b4-127">A custom string that provides extra information about the reason for blocking or not blocking.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a7b4-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a7b4-128">Requirements</span></span>



| <span data-ttu-id="5a7b4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a7b4-129">Requirement</span></span> | <span data-ttu-id="5a7b4-130">Valore</span><span class="sxs-lookup"><span data-stu-id="5a7b4-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a7b4-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a7b4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5a7b4-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a7b4-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a7b4-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a7b4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5a7b4-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5a7b4-134">None supported</span></span><br/>                                                             |
| <span data-ttu-id="5a7b4-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a7b4-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a7b4-136"><dt>Wpcevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a7b4-136"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a7b4-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a7b4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a7b4-138">Uso delle API di registrazione per i controlli padre</span><span class="sxs-lookup"><span data-stu-id="5a7b4-138">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="5a7b4-139">**\_argomenti \_ CONVERSATIONINITEVENT di WPC**</span><span class="sxs-lookup"><span data-stu-id="5a7b4-139">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




