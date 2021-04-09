---
description: Il sistema trasmette l'evento DBT \_ DEVICEQUERYREMOVEFAILED Device quando una richiesta di rimozione di un dispositivo o di un elemento multimediale è stata annullata.
ms.assetid: a24916a9-b67a-4622-b9f3-4b4f26bf4d6b
title: Evento DBT_DEVICEQUERYREMOVEFAILED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848c7378cdbac95729eee70c70a1e323373b8e85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877754"
---
# <a name="dbt_devicequeryremovefailed-event"></a><span data-ttu-id="d2a2f-103">\_Evento DEVICEQUERYREMOVEFAILED DBT</span><span class="sxs-lookup"><span data-stu-id="d2a2f-103">DBT\_DEVICEQUERYREMOVEFAILED event</span></span>

<span data-ttu-id="d2a2f-104">Il sistema trasmette l'evento DBT \_ DEVICEQUERYREMOVEFAILED Device quando una richiesta di rimozione di un dispositivo o di un elemento multimediale è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="d2a2f-104">The system broadcasts the DBT\_DEVICEQUERYREMOVEFAILED device event when a request to remove a device or piece of media has been canceled.</span></span>

<span data-ttu-id="d2a2f-105">Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ DEVICEQUERYREMOVEFAILED e *lParam* impostati come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="d2a2f-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEQUERYREMOVEFAILED and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="d2a2f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2a2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a2f-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d2a2f-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d2a2f-108">Handle di una finestra.</span><span class="sxs-lookup"><span data-stu-id="d2a2f-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="d2a2f-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="d2a2f-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="d2a2f-110">Identificatore del messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="d2a2f-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d2a2f-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2a2f-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2a2f-112">Impostare su DBT \_ DEVICEQUERYREMOVEFAILED.</span><span class="sxs-lookup"><span data-stu-id="d2a2f-112">Set to DBT\_DEVICEQUERYREMOVEFAILED.</span></span>

</dd> <dt>

<span data-ttu-id="d2a2f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2a2f-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2a2f-114">Puntatore a una struttura che identifica il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2a2f-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="d2a2f-115">La struttura è costituita da un'intestazione indipendente dall'evento, seguita da membri dipendenti dall'evento che descrivono il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2a2f-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="d2a2f-116">Per usare questa struttura, considerare la struttura come una [**struttura \_ \_ HDR di sviluppo broadcast**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , quindi controllare il membro **dbch \_ DeviceType** per determinare il tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2a2f-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a2f-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2a2f-117">Return value</span></span>

<span data-ttu-id="d2a2f-118">Restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="d2a2f-118">Return **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="d2a2f-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="d2a2f-119">Examples</span></span>

<span data-ttu-id="d2a2f-120">Per un esempio, vedere [elaborazione di una richiesta di rimozione di un dispositivo](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="d2a2f-120">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2a2f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2a2f-121">Requirements</span></span>



| <span data-ttu-id="d2a2f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2a2f-122">Requirement</span></span> | <span data-ttu-id="d2a2f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d2a2f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d2a2f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2a2f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d2a2f-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2a2f-125">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="d2a2f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2a2f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d2a2f-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2a2f-127">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="d2a2f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2a2f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2a2f-129"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2a2f-129"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2a2f-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2a2f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a2f-131">Eventi dispositivo</span><span class="sxs-lookup"><span data-stu-id="d2a2f-131">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="d2a2f-132">Eventi di gestione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="d2a2f-132">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="d2a2f-133">**SVILUPPO \_ broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="d2a2f-133">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="d2a2f-134">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="d2a2f-134">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




