---
description: Il sistema trasmette l'evento DBT \_ devnode \_ Changed Device quando un dispositivo è stato aggiunto o rimosso dal sistema. Le applicazioni che gestiscono elenchi di dispositivi nel sistema devono aggiornare gli elenchi.
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: Evento DBT_DEVNODES_CHANGED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1450e9a87d541e5df3d9a9286e48601697e6aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126789"
---
# <a name="dbt_devnodes_changed-event"></a><span data-ttu-id="bbe2a-104">\_Evento di modifica devnode di DBT \_</span><span class="sxs-lookup"><span data-stu-id="bbe2a-104">DBT\_DEVNODES\_CHANGED event</span></span>

<span data-ttu-id="bbe2a-105">Il sistema trasmette l'evento DBT \_ devnode \_ Changed Device quando un dispositivo è stato aggiunto o rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="bbe2a-105">The system broadcasts the DBT\_DEVNODES\_CHANGED device event when a device has been added to or removed from the system.</span></span> <span data-ttu-id="bbe2a-106">Le applicazioni che gestiscono elenchi di dispositivi nel sistema devono aggiornare gli elenchi.</span><span class="sxs-lookup"><span data-stu-id="bbe2a-106">Applications that maintain lists of devices in the system should refresh their lists.</span></span>

<span data-ttu-id="bbe2a-107">Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ devnode \_ modificato e *lParam* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="bbe2a-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVNODES\_CHANGED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="bbe2a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bbe2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbe2a-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="bbe2a-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bbe2a-110">Handle di una finestra.</span><span class="sxs-lookup"><span data-stu-id="bbe2a-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="bbe2a-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="bbe2a-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="bbe2a-112">Identificatore del messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="bbe2a-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bbe2a-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bbe2a-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbe2a-114">Impostare su DBT \_ devnode \_ modificato.</span><span class="sxs-lookup"><span data-stu-id="bbe2a-114">Set to DBT\_DEVNODES\_CHANGED.</span></span>

</dd> <dt>

<span data-ttu-id="bbe2a-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bbe2a-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbe2a-116">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="bbe2a-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbe2a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bbe2a-117">Return value</span></span>

<span data-ttu-id="bbe2a-118">Restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="bbe2a-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbe2a-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbe2a-119">Remarks</span></span>

<span data-ttu-id="bbe2a-120">Non sono disponibili informazioni aggiuntive sul dispositivo che è stato aggiunto o rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="bbe2a-120">There is no additional information about which device has been added to or removed from the system.</span></span> <span data-ttu-id="bbe2a-121">Le applicazioni che richiedono altre informazioni devono registrarsi per la notifica del dispositivo tramite la funzione [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) .</span><span class="sxs-lookup"><span data-stu-id="bbe2a-121">Applications that require more information should register for device notification using the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbe2a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbe2a-122">Requirements</span></span>



| <span data-ttu-id="bbe2a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbe2a-123">Requirement</span></span> | <span data-ttu-id="bbe2a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="bbe2a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bbe2a-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbe2a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bbe2a-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bbe2a-126">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="bbe2a-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbe2a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bbe2a-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bbe2a-128">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="bbe2a-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbe2a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbe2a-130"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbe2a-130"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbe2a-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbe2a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbe2a-132">Eventi dispositivo</span><span class="sxs-lookup"><span data-stu-id="bbe2a-132">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="bbe2a-133">Eventi di gestione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="bbe2a-133">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="bbe2a-134">**SVILUPPO \_ broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="bbe2a-134">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="bbe2a-135">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="bbe2a-135">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




