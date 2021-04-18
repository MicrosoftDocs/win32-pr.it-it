---
description: Notifica alle applicazioni che il BIOS APM ha segnalato un evento APM OEM.
ms.assetid: 3251ac00-41f1-44e9-a579-fa31e7c7d2ff
title: Evento PBT_APMOEMEVENT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a99b99bdaf69b1a53a24ad33cd898fd1c806694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312037"
---
# <a name="pbt_apmoemevent-event"></a><span data-ttu-id="2017a-103">\_Evento APMOEMEVENT PBT</span><span class="sxs-lookup"><span data-stu-id="2017a-103">PBT\_APMOEMEVENT event</span></span>

<span data-ttu-id="2017a-104">\[PBT \_ APMOEMEVENT è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="2017a-104">\[PBT\_APMOEMEVENT is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2017a-105">Il supporto per questo evento è stato rimosso in Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="2017a-105">Support for this event was removed in Windows Vista.\]</span></span>

<span data-ttu-id="2017a-106">Notifica alle applicazioni che il BIOS APM ha segnalato un evento APM OEM.</span><span class="sxs-lookup"><span data-stu-id="2017a-106">Notifies applications that the APM BIOS has signaled an APM OEM event.</span></span>

<span data-ttu-id="2017a-107">Una finestra riceve questo evento tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="2017a-107">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="2017a-108">I parametri *wParam* e *lParam* sono impostati come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="2017a-108">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMOEMEVENT
            LPARAM lParam); // OEM event code
```



## <a name="parameters"></a><span data-ttu-id="2017a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2017a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2017a-110">*HWND*</span><span class="sxs-lookup"><span data-stu-id="2017a-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="2017a-111">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="2017a-111">A handle to window.</span></span>

<span data-ttu-id="2017a-112"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="2017a-112"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="2017a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="2017a-113">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="2017a-114">Significato</span><span class="sxs-lookup"><span data-stu-id="2017a-114">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="2017a-115"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="2017a-115"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="2017a-116">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="2017a-116">Message identifier.</span></span><br/> |



 

<span data-ttu-id="2017a-117"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="2017a-117"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="2017a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2017a-118">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="2017a-119">Significato</span><span class="sxs-lookup"><span data-stu-id="2017a-119">Meaning</span></span>                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMOEMEVENT"></span><span id="pbt_apmoemevent"></span><dl> <span data-ttu-id="2017a-120"><dt>**PBT \_ APMOEMEVENT**</dt> <dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="2017a-120"><dt>**PBT\_APMOEMEVENT**</dt> <dt>11 (0xB)</dt></span></span> </dl> | <span data-ttu-id="2017a-121">Identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="2017a-121">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2017a-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2017a-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2017a-123">Codice evento definito dall'OEM segnalato dal BIOS APM del sistema.</span><span class="sxs-lookup"><span data-stu-id="2017a-123">The OEM-defined event code that was signaled by the system's APM BIOS.</span></span> <span data-ttu-id="2017a-124">I codici evento OEM sono compresi nell'intervallo 0200H-02FFh.</span><span class="sxs-lookup"><span data-stu-id="2017a-124">OEM event codes are in the range 0200h - 02FFh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2017a-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2017a-125">Return value</span></span>

<span data-ttu-id="2017a-126">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="2017a-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2017a-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="2017a-127">Remarks</span></span>

<span data-ttu-id="2017a-128">Poiché non tutte le implementazioni del BIOS APM forniscono notifiche degli eventi OEM, questo evento potrebbe non essere mai trasmesso in alcuni computer.</span><span class="sxs-lookup"><span data-stu-id="2017a-128">Because not all APM BIOS implementations provide OEM event notifications, this event may never be broadcast on some computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="2017a-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2017a-129">Requirements</span></span>



| <span data-ttu-id="2017a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2017a-130">Requirement</span></span> | <span data-ttu-id="2017a-131">Valore</span><span class="sxs-lookup"><span data-stu-id="2017a-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2017a-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2017a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2017a-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2017a-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2017a-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2017a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2017a-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2017a-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2017a-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2017a-136">End of client support</span></span><br/>    | <span data-ttu-id="2017a-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2017a-137">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="2017a-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="2017a-138">End of server support</span></span><br/>    | <span data-ttu-id="2017a-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2017a-139">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="2017a-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2017a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2017a-141"><dt>WinUser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2017a-141"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2017a-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2017a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2017a-143">Eventi di risparmio energia</span><span class="sxs-lookup"><span data-stu-id="2017a-143">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="2017a-144">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="2017a-144">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




