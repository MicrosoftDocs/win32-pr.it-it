---
description: Notifica alle applicazioni che il sistema riprende la sospensione o l'ibernazione. Questo evento viene recapitato ogni volta che il sistema riprende e non indica se un utente è presente.
ms.assetid: cd331f79-b64d-479e-aea8-5118ccc87224
title: Evento PBT_APMRESUMEAUTOMATIC (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a481dee356c85b3831fcace0c1ff127b0b276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881714"
---
# <a name="pbt_apmresumeautomatic-event"></a><span data-ttu-id="4e9fd-104">\_Evento APMRESUMEAUTOMATIC PBT</span><span class="sxs-lookup"><span data-stu-id="4e9fd-104">PBT\_APMRESUMEAUTOMATIC event</span></span>

<span data-ttu-id="4e9fd-105">Notifica alle applicazioni che il sistema riprende la sospensione o l'ibernazione.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-105">Notifies applications that the system is resuming from sleep or hibernation.</span></span> <span data-ttu-id="4e9fd-106">Questo evento viene recapitato ogni volta che il sistema riprende e non indica se un utente è presente.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-106">This event is delivered every time the system resumes and does not indicate whether a user is present.</span></span>

<span data-ttu-id="4e9fd-107">Una finestra riceve questo evento tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="4e9fd-107">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="4e9fd-108">I parametri *wParam* e *lParam* sono impostati come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-108">The *wParam* and *lParam* parameters are set as described following.</span></span>

> [!Note]  
> <span data-ttu-id="4e9fd-109">Nei sistemi Windows 10, versione 1507 o versioni successive, se il sistema riprende dalla modalità di sospensione solo per entrare immediatamente in ibernazione, questo evento non viene recapitato.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-109">In Windows 10, version 1507 systems or later, if the system is resuming from sleep only to immediately enter hibernation, this event is not delivered.</span></span> <span data-ttu-id="4e9fd-110">In questo caso non viene inviato un messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="4e9fd-110">A [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message is not sent in this case.</span></span>

 


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMEAUTOMATIC
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="4e9fd-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e9fd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e9fd-112">*HWND*</span><span class="sxs-lookup"><span data-stu-id="4e9fd-112">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="4e9fd-113">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-113">A handle to window.</span></span>

<span data-ttu-id="4e9fd-114"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="4e9fd-114"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="4e9fd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4e9fd-115">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="4e9fd-116">Significato</span><span class="sxs-lookup"><span data-stu-id="4e9fd-116">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="4e9fd-117"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="4e9fd-117"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="4e9fd-118">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-118">Message identifier.</span></span><br/> |



 

<span data-ttu-id="4e9fd-119"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="4e9fd-119"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="4e9fd-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4e9fd-120">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="4e9fd-121">Significato</span><span class="sxs-lookup"><span data-stu-id="4e9fd-121">Meaning</span></span>                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="4e9fd-122"><dt>**PBT \_ APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="4e9fd-122"><dt>**PBT\_APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="4e9fd-123">Identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-123">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4e9fd-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e9fd-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e9fd-125">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-125">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e9fd-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e9fd-126">Return value</span></span>

<span data-ttu-id="4e9fd-127">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-127">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e9fd-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e9fd-128">Remarks</span></span>

<span data-ttu-id="4e9fd-129">Se il sistema rileva qualsiasi attività utente dopo la trasmissione \_ di PBT APMRESUMEAUTOMATIC, trasmette un evento [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) per consentire alle applicazioni di essere in grado di riprendere l'interazione completa con l'utente.</span><span class="sxs-lookup"><span data-stu-id="4e9fd-129">If the system detects any user activity after broadcasting PBT\_APMRESUMEAUTOMATIC, it will broadcast a [PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md) event to let applications know they can resume full interaction with the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e9fd-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e9fd-130">Requirements</span></span>



| <span data-ttu-id="4e9fd-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e9fd-131">Requirement</span></span> | <span data-ttu-id="4e9fd-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4e9fd-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e9fd-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e9fd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4e9fd-134">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4e9fd-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4e9fd-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e9fd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4e9fd-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4e9fd-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4e9fd-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e9fd-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e9fd-138"><dt>WinUser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e9fd-138"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e9fd-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e9fd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e9fd-140">Eventi di riattivazione del sistema</span><span class="sxs-lookup"><span data-stu-id="4e9fd-140">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="4e9fd-141">Eventi di risparmio energia</span><span class="sxs-lookup"><span data-stu-id="4e9fd-141">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="4e9fd-142">\_APMRESUMESUSPEND PBT</span><span class="sxs-lookup"><span data-stu-id="4e9fd-142">PBT\_APMRESUMESUSPEND</span></span>](pbt-apmresumesuspend.md)
</dt> <dt>

[<span data-ttu-id="4e9fd-143">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="4e9fd-143">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




