---
description: Evento di modifica dell'impostazione di risparmio energia inviato con un \_ messaggio della finestra WM POWERBROADCAST o in un callback di notifica HandlerEx per i servizi.
ms.assetid: 0bcadb85-47c5-48a9-b3f9-f0a1ca60b503
title: Evento PBT_POWERSETTINGCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f38486d2e5cce1cfe541468e548e92353c9837
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881713"
---
# <a name="pbt_powersettingchange-event"></a><span data-ttu-id="d480c-103">\_Evento POWERSETTINGCHANGE PBT</span><span class="sxs-lookup"><span data-stu-id="d480c-103">PBT\_POWERSETTINGCHANGE event</span></span>

<span data-ttu-id="d480c-104">Evento di modifica dell'impostazione di risparmio energia inviato con un messaggio della finestra [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) o in un callback di notifica [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) per i servizi.</span><span class="sxs-lookup"><span data-stu-id="d480c-104">Power setting change event sent with a [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) window message or in a [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) notification callback for services.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_POWERSETTINGCHANGE
            LPARAM lParam); // Pointer to POWERBROADCAST_SETTING
```



## <a name="parameters"></a><span data-ttu-id="d480c-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="d480c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d480c-106">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d480c-106">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d480c-107">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="d480c-107">A handle to window.</span></span>

<span data-ttu-id="d480c-108"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="d480c-108"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="d480c-109">Valore</span><span class="sxs-lookup"><span data-stu-id="d480c-109">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="d480c-110">Significato</span><span class="sxs-lookup"><span data-stu-id="d480c-110">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="d480c-111"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="d480c-111"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="d480c-112">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="d480c-112">Message identifier.</span></span><br/> |



 

<span data-ttu-id="d480c-113"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="d480c-113"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="d480c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d480c-114">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="d480c-115">Significato</span><span class="sxs-lookup"><span data-stu-id="d480c-115">Meaning</span></span>                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="d480c-116"><dt>**PBT \_ POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="d480c-116"><dt>**PBT\_POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt></span></span> </dl> | <span data-ttu-id="d480c-117">Identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d480c-117">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d480c-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d480c-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d480c-119">Puntatore a una struttura di [**\_ Impostazioni POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="d480c-119">Pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d480c-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d480c-120">Return value</span></span>

<span data-ttu-id="d480c-121">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="d480c-121">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d480c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d480c-122">Requirements</span></span>



| <span data-ttu-id="d480c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d480c-123">Requirement</span></span> | <span data-ttu-id="d480c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d480c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d480c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d480c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d480c-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d480c-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d480c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d480c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d480c-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d480c-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d480c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d480c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d480c-130"><dt>WinUser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d480c-130"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d480c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d480c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d480c-132">Eventi di risparmio energia</span><span class="sxs-lookup"><span data-stu-id="d480c-132">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="d480c-133">**HandlerEx**</span><span class="sxs-lookup"><span data-stu-id="d480c-133">**HandlerEx**</span></span>](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)
</dt> <dt>

[<span data-ttu-id="d480c-134">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="d480c-134">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> <dt>

[<span data-ttu-id="d480c-135">**\_impostazione POWERBROADCAST**</span><span class="sxs-lookup"><span data-stu-id="d480c-135">**POWERBROADCAST\_SETTING**</span></span>](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)
</dt> </dl>

 

