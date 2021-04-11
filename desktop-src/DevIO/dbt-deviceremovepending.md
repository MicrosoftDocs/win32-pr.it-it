---
description: Il sistema trasmette l'evento DBT \_ DEVICEREMOVEPENDING Device quando è in corso la rimozione di un dispositivo o di un elemento multimediale e non è più disponibile per l'uso.
ms.assetid: 28cb4481-8961-4896-9608-afccba9a2bfe
title: Evento DBT_DEVICEREMOVEPENDING (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421851dc46d905ae85941b92df6649ccb504ee50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126792"
---
# <a name="dbt_deviceremovepending-event"></a><span data-ttu-id="1cfda-103">\_Evento DEVICEREMOVEPENDING DBT</span><span class="sxs-lookup"><span data-stu-id="1cfda-103">DBT\_DEVICEREMOVEPENDING event</span></span>

<span data-ttu-id="1cfda-104">Il sistema trasmette l'evento DBT \_ DEVICEREMOVEPENDING Device quando è in corso la rimozione di un dispositivo o di un elemento multimediale e non è più disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="1cfda-104">The system broadcasts the DBT\_DEVICEREMOVEPENDING device event when a device or piece of media is being removed and is no longer available for use.</span></span>

<span data-ttu-id="1cfda-105">Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ DEVICEREMOVEPENDING e *lParam* impostati come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="1cfda-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEREMOVEPENDING and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="1cfda-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cfda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cfda-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="1cfda-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="1cfda-108">Handle di una finestra.</span><span class="sxs-lookup"><span data-stu-id="1cfda-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="1cfda-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="1cfda-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="1cfda-110">Identificatore del messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="1cfda-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1cfda-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1cfda-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1cfda-112">Impostare su DBT \_ DEVICEREMOVEPENDING.</span><span class="sxs-lookup"><span data-stu-id="1cfda-112">Set to DBT\_DEVICEREMOVEPENDING.</span></span>

</dd> <dt>

<span data-ttu-id="1cfda-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1cfda-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1cfda-114">Puntatore a una struttura che identifica il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1cfda-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="1cfda-115">La struttura è costituita da un'intestazione indipendente dall'evento, seguita da membri dipendenti dall'evento che descrivono il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1cfda-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="1cfda-116">Per usare questa struttura, considerare la struttura come una [**struttura \_ \_ HDR di sviluppo broadcast**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , quindi controllare il membro **dbch \_ DeviceType** per determinare il tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1cfda-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cfda-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cfda-117">Return value</span></span>

<span data-ttu-id="1cfda-118">Restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="1cfda-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cfda-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cfda-119">Remarks</span></span>

<span data-ttu-id="1cfda-120">Il sistema può trasmettere un \_ messaggio DBT DEVICEREMOVEPENDING senza inviare un messaggio [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="1cfda-120">The system may broadcast a DBT\_DEVICEREMOVEPENDING message without sending a corresponding [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message.</span></span> <span data-ttu-id="1cfda-121">In questi casi, le applicazioni e i driver devono essere ripristinati dalla perdita del dispositivo nel modo migliore possibile.</span><span class="sxs-lookup"><span data-stu-id="1cfda-121">In such cases, the applications and drivers must recover from the loss of the device as best they can.</span></span>

## <a name="examples"></a><span data-ttu-id="1cfda-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="1cfda-122">Examples</span></span>

<span data-ttu-id="1cfda-123">Per un esempio, vedere [elaborazione di una richiesta di rimozione di un dispositivo](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="1cfda-123">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cfda-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cfda-124">Requirements</span></span>



| <span data-ttu-id="1cfda-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cfda-125">Requirement</span></span> | <span data-ttu-id="1cfda-126">Valore</span><span class="sxs-lookup"><span data-stu-id="1cfda-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1cfda-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cfda-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1cfda-128">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1cfda-128">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="1cfda-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cfda-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1cfda-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1cfda-130">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="1cfda-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cfda-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cfda-132"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cfda-132"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cfda-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cfda-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cfda-134">Eventi dispositivo</span><span class="sxs-lookup"><span data-stu-id="1cfda-134">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="1cfda-135">Eventi di gestione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="1cfda-135">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="1cfda-136">**SVILUPPO \_ broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="1cfda-136">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="1cfda-137">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="1cfda-137">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




