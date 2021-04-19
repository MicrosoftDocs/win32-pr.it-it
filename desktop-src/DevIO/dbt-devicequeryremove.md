---
description: Il sistema trasmette l'evento del \_ dispositivo DEVICEQUERYREMOVE di DBT per richiedere l'autorizzazione per rimuovere un dispositivo o un elemento multimediale.
ms.assetid: a0e9aa57-da0e-4e9c-99d0-5502040d2664
title: Evento DBT_DEVICEQUERYREMOVE (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c9dbdee13318f9a664582fdba8f9e3f9bfc5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304853"
---
# <a name="dbt_devicequeryremove-event"></a><span data-ttu-id="36ffc-103">\_Evento DEVICEQUERYREMOVE DBT</span><span class="sxs-lookup"><span data-stu-id="36ffc-103">DBT\_DEVICEQUERYREMOVE event</span></span>

<span data-ttu-id="36ffc-104">Il sistema trasmette l'evento del \_ dispositivo DEVICEQUERYREMOVE di DBT per richiedere l'autorizzazione per rimuovere un dispositivo o un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="36ffc-104">The system broadcasts the DBT\_DEVICEQUERYREMOVE device event to request permission to remove a device or piece of media.</span></span> <span data-ttu-id="36ffc-105">Questo messaggio è l'ultima possibilità per le applicazioni e i driver di prepararsi per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="36ffc-105">This message is the last chance for applications and drivers to prepare for this removal.</span></span> <span data-ttu-id="36ffc-106">Tuttavia, qualsiasi applicazione può negare questa richiesta e annullare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="36ffc-106">However, any application can deny this request and cancel the operation.</span></span>

<span data-ttu-id="36ffc-107">Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ DEVICEQUERYREMOVE e *lParam* impostati come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="36ffc-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEQUERYREMOVE and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="36ffc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="36ffc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36ffc-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="36ffc-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="36ffc-110">Handle di una finestra.</span><span class="sxs-lookup"><span data-stu-id="36ffc-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="36ffc-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="36ffc-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="36ffc-112">Identificatore del messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="36ffc-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="36ffc-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36ffc-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36ffc-114">Impostare su DBT \_ DEVICEQUERYREMOVE.</span><span class="sxs-lookup"><span data-stu-id="36ffc-114">Set to DBT\_DEVICEQUERYREMOVE.</span></span>

</dd> <dt>

<span data-ttu-id="36ffc-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36ffc-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36ffc-116">Puntatore a una struttura che identifica il dispositivo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="36ffc-116">A pointer to a structure identifying the device to remove.</span></span> <span data-ttu-id="36ffc-117">La struttura è costituita da un'intestazione indipendente dall'evento, seguita da membri dipendenti dall'evento che descrivono il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36ffc-117">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="36ffc-118">Per usare questa struttura, considerare la struttura come una [**struttura \_ \_ HDR di sviluppo broadcast**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , quindi controllare il membro **dbch \_ DeviceType** per determinare il tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36ffc-118">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36ffc-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="36ffc-119">Return value</span></span>

<span data-ttu-id="36ffc-120">Restituisce **true** per concedere l'autorizzazione per la rimozione di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36ffc-120">Return **TRUE** to grant permission to remove a device.</span></span>

<span data-ttu-id="36ffc-121">Return BROADCAST \_ query \_ Nega per negare l'autorizzazione per rimuovere un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36ffc-121">Return BROADCAST\_QUERY\_DENY to deny permission to remove a device.</span></span>

## <a name="remarks"></a><span data-ttu-id="36ffc-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="36ffc-122">Remarks</span></span>

<span data-ttu-id="36ffc-123">È necessario chiudere tutti gli handle del dispositivo o la rimozione del dispositivo non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="36ffc-123">You must close all handles to the device or the device removal will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="36ffc-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="36ffc-124">Examples</span></span>

<span data-ttu-id="36ffc-125">Per un esempio, vedere [elaborazione di una richiesta di rimozione di un dispositivo](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="36ffc-125">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36ffc-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36ffc-126">Requirements</span></span>



| <span data-ttu-id="36ffc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="36ffc-127">Requirement</span></span> | <span data-ttu-id="36ffc-128">Valore</span><span class="sxs-lookup"><span data-stu-id="36ffc-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="36ffc-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36ffc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="36ffc-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="36ffc-130">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="36ffc-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36ffc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="36ffc-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="36ffc-132">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="36ffc-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36ffc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="36ffc-134"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="36ffc-134"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36ffc-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36ffc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36ffc-136">Eventi dispositivo</span><span class="sxs-lookup"><span data-stu-id="36ffc-136">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="36ffc-137">Eventi di gestione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="36ffc-137">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="36ffc-138">**SVILUPPO \_ broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="36ffc-138">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="36ffc-139">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="36ffc-139">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




