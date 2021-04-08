---
description: Il sistema invia l' \_ evento DBT CUSTOMEVENT Device quando si è verificato un evento personalizzato definito dal driver.
ms.assetid: 6e66fa93-0cd7-4202-83eb-cddc668525ae
title: Evento DBT_CUSTOMEVENT (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777049a0a94b16450ed9ee8567f3fc6506e47174
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748362"
---
# <a name="dbt_customevent-event"></a><span data-ttu-id="f026c-103">\_Evento CUSTOMEVENT DBT</span><span class="sxs-lookup"><span data-stu-id="f026c-103">DBT\_CUSTOMEVENT event</span></span>

<span data-ttu-id="f026c-104">Il sistema invia l' \_ evento DBT CUSTOMEVENT Device quando si è verificato un evento personalizzato definito dal driver.</span><span class="sxs-lookup"><span data-stu-id="f026c-104">The system sends the DBT\_CUSTOMEVENT device event when a driver-defined custom event has occurred.</span></span>

<span data-ttu-id="f026c-105">Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ CUSTOMEVENT e *lParam* impostati come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="f026c-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CUSTOMEVENT and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="f026c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f026c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f026c-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="f026c-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f026c-108">Handle di una finestra.</span><span class="sxs-lookup"><span data-stu-id="f026c-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="f026c-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="f026c-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="f026c-110">Identificatore del messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="f026c-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f026c-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f026c-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f026c-112">Impostare su DBT \_ CUSTOMEVENT.</span><span class="sxs-lookup"><span data-stu-id="f026c-112">Set to DBT\_CUSTOMEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="f026c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f026c-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f026c-114">Puntatore a una struttura che identifica il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f026c-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="f026c-115">La struttura è costituita da un'intestazione indipendente dall'evento, seguita da membri dipendenti dall'evento che descrivono il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f026c-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="f026c-116">Per usare questa struttura, considerare la struttura come una [**struttura \_ \_ HDR di sviluppo broadcast**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , quindi controllare il membro **dbch \_ DeviceType** per determinare il tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f026c-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f026c-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f026c-117">Return value</span></span>

<span data-ttu-id="f026c-118">Restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="f026c-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f026c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f026c-119">Requirements</span></span>



| <span data-ttu-id="f026c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f026c-120">Requirement</span></span> | <span data-ttu-id="f026c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f026c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f026c-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f026c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f026c-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f026c-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="f026c-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f026c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f026c-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f026c-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="f026c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f026c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f026c-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f026c-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f026c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f026c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f026c-129">Eventi dispositivo</span><span class="sxs-lookup"><span data-stu-id="f026c-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="f026c-130">Eventi di gestione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="f026c-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="f026c-131">**SVILUPPO \_ broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="f026c-131">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="f026c-132">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="f026c-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




