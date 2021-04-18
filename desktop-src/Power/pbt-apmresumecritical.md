---
description: Notifica alle applicazioni che il sistema ha ripreso l'operazione.
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: Evento PBT_APMRESUMECRITICAL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4a76e163f2e61e723f4df6572254e8ef89b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312034"
---
# <a name="pbt_apmresumecritical-event"></a><span data-ttu-id="b754b-103">\_Evento APMRESUMECRITICAL PBT</span><span class="sxs-lookup"><span data-stu-id="b754b-103">PBT\_APMRESUMECRITICAL event</span></span>

<span data-ttu-id="b754b-104">\[PBT \_ APMRESUMECRITICAL è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="b754b-104">\[PBT\_APMRESUMECRITICAL is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b754b-105">Il supporto per questo evento è stato rimosso in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b754b-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="b754b-106">In alternativa, usare [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) .\]</span><span class="sxs-lookup"><span data-stu-id="b754b-106">Use [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) instead.\]</span></span>

<span data-ttu-id="b754b-107">Notifica alle applicazioni che il sistema ha ripreso l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b754b-107">Notifies applications that the system has resumed operation.</span></span> <span data-ttu-id="b754b-108">Questo evento può indicare che alcune o tutte le applicazioni non hanno ricevuto un evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) .</span><span class="sxs-lookup"><span data-stu-id="b754b-108">This event can indicate that some or all applications did not receive a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event.</span></span> <span data-ttu-id="b754b-109">Questo evento, ad esempio, può essere trasmesso dopo una sospensione critica causata da una batteria in errore.</span><span class="sxs-lookup"><span data-stu-id="b754b-109">For example, this event can be broadcast after a critical suspension caused by a failing battery.</span></span>

<span data-ttu-id="b754b-110">Una finestra riceve questo evento tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="b754b-110">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="b754b-111">I parametri *wParam* e *lParam* sono impostati come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="b754b-111">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMECRITICAL
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="b754b-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="b754b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b754b-113">*HWND*</span><span class="sxs-lookup"><span data-stu-id="b754b-113">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b754b-114">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="b754b-114">A handle to window.</span></span>

<span data-ttu-id="b754b-115"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="b754b-115"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="b754b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b754b-116">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="b754b-117">Significato</span><span class="sxs-lookup"><span data-stu-id="b754b-117">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="b754b-118"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="b754b-118"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="b754b-119">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="b754b-119">Message identifier.</span></span><br/> |



 

<span data-ttu-id="b754b-120"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="b754b-120"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="b754b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b754b-121">Value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="b754b-122">Significato</span><span class="sxs-lookup"><span data-stu-id="b754b-122">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMECRITICAL"></span><span id="pbt_apmresumecritical"></span><dl> <span data-ttu-id="b754b-123"><dt>**PBT \_ APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="b754b-123"><dt>**PBT\_APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt></span></span> </dl> | <span data-ttu-id="b754b-124">Identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="b754b-124">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b754b-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b754b-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b754b-126">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b754b-126">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b754b-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b754b-127">Return value</span></span>

<span data-ttu-id="b754b-128">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="b754b-128">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b754b-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="b754b-129">Remarks</span></span>

<span data-ttu-id="b754b-130">Poiché si verifica una sospensione critica senza notifica precedente, le risorse e i dati precedentemente disponibili potrebbero non essere presenti quando l'applicazione riceve questo evento.</span><span class="sxs-lookup"><span data-stu-id="b754b-130">Because a critical suspension occurs without prior notification, resources and data previously available may not be present when the application receives this event.</span></span> <span data-ttu-id="b754b-131">L'applicazione deve tentare di ripristinare il proprio stato al meglio della propria capacità.</span><span class="sxs-lookup"><span data-stu-id="b754b-131">The application should attempt to restore its state to the best of its ability.</span></span> <span data-ttu-id="b754b-132">In una sospensione critica, il sistema gestisce lo stato della DRAM e dei dischi rigidi locali, ma non può mantenere le connessioni nette.</span><span class="sxs-lookup"><span data-stu-id="b754b-132">While in a critical suspension, the system maintains the state of the DRAM and local hard disks, but may not maintain net connections.</span></span> <span data-ttu-id="b754b-133">È possibile che un'applicazione debba intervenire in relazione ai file aperti in rete prima della sospensione critica.</span><span class="sxs-lookup"><span data-stu-id="b754b-133">An application may need to take action with respect to files that were open on the network before critical suspension.</span></span>

## <a name="requirements"></a><span data-ttu-id="b754b-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b754b-134">Requirements</span></span>



| <span data-ttu-id="b754b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b754b-135">Requirement</span></span> | <span data-ttu-id="b754b-136">Valore</span><span class="sxs-lookup"><span data-stu-id="b754b-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b754b-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b754b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b754b-138">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b754b-138">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b754b-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b754b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b754b-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b754b-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b754b-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b754b-141">End of client support</span></span><br/>    | <span data-ttu-id="b754b-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b754b-142">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="b754b-143">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b754b-143">End of server support</span></span><br/>    | <span data-ttu-id="b754b-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b754b-144">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="b754b-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b754b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="b754b-146"><dt>WinUser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b754b-146"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b754b-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b754b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b754b-148">Eventi di riattivazione del sistema</span><span class="sxs-lookup"><span data-stu-id="b754b-148">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="b754b-149">Eventi di risparmio energia</span><span class="sxs-lookup"><span data-stu-id="b754b-149">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="b754b-150">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="b754b-150">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




