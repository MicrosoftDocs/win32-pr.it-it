---
description: Notifica alle applicazioni che l'autorizzazione per sospendere il computer è stata negata.
ms.assetid: 0f68628f-9d38-45ca-9487-95bf62075e00
title: Evento PBT_APMQUERYSUSPENDFAILED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1544cd5ed94ae0228c739e2ddb576b0bd77146eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312036"
---
# <a name="pbt_apmquerysuspendfailed-event"></a><span data-ttu-id="d77b4-103">\_Evento APMQUERYSUSPENDFAILED PBT</span><span class="sxs-lookup"><span data-stu-id="d77b4-103">PBT\_APMQUERYSUSPENDFAILED event</span></span>

<span data-ttu-id="d77b4-104">\[PBT \_ APMQUERYSUSPENDFAILED è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d77b4-104">\[PBT\_APMQUERYSUSPENDFAILED is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d77b4-105">Il supporto per questo evento è stato rimosso in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d77b4-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="d77b4-106">In alternativa, usare [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) .\]</span><span class="sxs-lookup"><span data-stu-id="d77b4-106">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) instead.\]</span></span>

<span data-ttu-id="d77b4-107">Notifica alle applicazioni che l'autorizzazione per sospendere il computer è stata negata.</span><span class="sxs-lookup"><span data-stu-id="d77b4-107">Notifies applications that permission to suspend the computer was denied.</span></span> <span data-ttu-id="d77b4-108">Questo evento viene trasmesso se un'applicazione o un driver ha restituito la **\_ richiesta broadcast \_ Deny** a un evento [PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md) precedente.</span><span class="sxs-lookup"><span data-stu-id="d77b4-108">This event is broadcast if any application or driver returned **BROADCAST\_QUERY\_DENY** to a previous [PBT\_APMQUERYSUSPEND](pbt-apmquerysuspend.md) event.</span></span>

<span data-ttu-id="d77b4-109">Una finestra riceve questo evento tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="d77b4-109">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="d77b4-110">I parametri *wParam* e *lParam* sono impostati come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="d77b4-110">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPENDFAILED
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="d77b4-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="d77b4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d77b4-112">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d77b4-112">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d77b4-113">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="d77b4-113">A handle to window.</span></span>

<span data-ttu-id="d77b4-114"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="d77b4-114"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="d77b4-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d77b4-115">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="d77b4-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d77b4-116">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="d77b4-117"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="d77b4-117"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="d77b4-118">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="d77b4-118">Message identifier.</span></span><br/> |



 

<span data-ttu-id="d77b4-119"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="d77b4-119"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="d77b4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d77b4-120">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="d77b4-121">Significato</span><span class="sxs-lookup"><span data-stu-id="d77b4-121">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPENDFAILED"></span><span id="pbt_apmquerysuspendfailed"></span><dl> <span data-ttu-id="d77b4-122"><dt>**PBT \_ APMQUERYSUSPENDFAILED**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="d77b4-122"><dt>**PBT\_APMQUERYSUSPENDFAILED**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="d77b4-123">Identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d77b4-123">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d77b4-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d77b4-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d77b4-125">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d77b4-125">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d77b4-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d77b4-126">Return value</span></span>

<span data-ttu-id="d77b4-127">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="d77b4-127">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d77b4-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="d77b4-128">Remarks</span></span>

<span data-ttu-id="d77b4-129">Le applicazioni in genere rispondono a questo evento riprendendo il normale funzionamento.</span><span class="sxs-lookup"><span data-stu-id="d77b4-129">Applications typically respond to this event by resuming normal operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="d77b4-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d77b4-130">Requirements</span></span>



| <span data-ttu-id="d77b4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d77b4-131">Requirement</span></span> | <span data-ttu-id="d77b4-132">Valore</span><span class="sxs-lookup"><span data-stu-id="d77b4-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d77b4-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d77b4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d77b4-134">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d77b4-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d77b4-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d77b4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d77b4-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d77b4-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d77b4-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d77b4-137">End of client support</span></span><br/>    | <span data-ttu-id="d77b4-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d77b4-138">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="d77b4-139">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="d77b4-139">End of server support</span></span><br/>    | <span data-ttu-id="d77b4-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d77b4-140">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="d77b4-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d77b4-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="d77b4-142"><dt>WinUser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d77b4-142"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d77b4-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d77b4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d77b4-144">Risparmio energia</span><span class="sxs-lookup"><span data-stu-id="d77b4-144">Power Management</span></span>](power-management-portal.md)
</dt> <dt>

[<span data-ttu-id="d77b4-145">Eventi di risparmio energia</span><span class="sxs-lookup"><span data-stu-id="d77b4-145">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="d77b4-146">\_APMQUERYSUSPEND PBT</span><span class="sxs-lookup"><span data-stu-id="d77b4-146">PBT\_APMQUERYSUSPEND</span></span>](pbt-apmquerysuspend.md)
</dt> <dt>

[<span data-ttu-id="d77b4-147">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="d77b4-147">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




