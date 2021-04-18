---
description: Il sistema trasmette l'evento DBT \_ DEVICEREMOVECOMPLETE Device quando un dispositivo o un elemento multimediale è stato rimosso fisicamente.
ms.assetid: e25d35b9-f8f1-4850-996c-e1cb393cca66
title: Evento DBT_DEVICEREMOVECOMPLETE (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c899d8cee4a0be34829ba0a8edbaf27be71f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304852"
---
# <a name="dbt_deviceremovecomplete-event"></a><span data-ttu-id="405d5-103">\_Evento DEVICEREMOVECOMPLETE DBT</span><span class="sxs-lookup"><span data-stu-id="405d5-103">DBT\_DEVICEREMOVECOMPLETE event</span></span>

<span data-ttu-id="405d5-104">Il sistema trasmette l'evento DBT \_ DEVICEREMOVECOMPLETE Device quando un dispositivo o un elemento multimediale è stato rimosso fisicamente.</span><span class="sxs-lookup"><span data-stu-id="405d5-104">The system broadcasts the DBT\_DEVICEREMOVECOMPLETE device event when a device or piece of media has been physically removed.</span></span>

<span data-ttu-id="405d5-105">Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ DEVICEREMOVECOMPLETE e *lParam* impostati come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="405d5-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEREMOVECOMPLETE and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="405d5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="405d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="405d5-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="405d5-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="405d5-108">Handle di una finestra.</span><span class="sxs-lookup"><span data-stu-id="405d5-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="405d5-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="405d5-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="405d5-110">Identificatore del messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="405d5-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="405d5-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="405d5-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="405d5-112">Imposta su DBT \_ DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="405d5-112">Set to DBT\_DEVICEREMOVECOMPLETE</span></span>

</dd> <dt>

<span data-ttu-id="405d5-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="405d5-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="405d5-114">Puntatore a una struttura che identifica la periferica rimossa.</span><span class="sxs-lookup"><span data-stu-id="405d5-114">A pointer to a structure identifying the device removed.</span></span> <span data-ttu-id="405d5-115">La struttura è costituita da un'intestazione indipendente dall'evento, seguita da membri dipendenti dall'evento che descrivono il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="405d5-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="405d5-116">Per usare questa struttura, considerare la struttura come una [**struttura \_ \_ HDR di sviluppo broadcast**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , quindi controllare il membro **dbch \_ DeviceType** per determinare il tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="405d5-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="405d5-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="405d5-117">Return value</span></span>

<span data-ttu-id="405d5-118">Restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="405d5-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="405d5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="405d5-119">Remarks</span></span>

<span data-ttu-id="405d5-120">Il sistema può trasmettere un \_ messaggio DBT DEVICEREMOVECOMPLETE senza inviare i messaggi [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) e [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="405d5-120">The system may broadcast a DBT\_DEVICEREMOVECOMPLETE message without sending corresponding [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) and [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) messages.</span></span> <span data-ttu-id="405d5-121">In questi casi, le applicazioni e i driver devono essere ripristinati dalla perdita del dispositivo nel modo migliore possibile.</span><span class="sxs-lookup"><span data-stu-id="405d5-121">In such cases, the applications and drivers must recover from the loss of the device as best they can.</span></span>

<span data-ttu-id="405d5-122">Se è in corso la rimozione del supporto, il tipo di dispositivo in arrivo è un volume (il membro **dbch \_ DeviceType** è DBT \_ DEVTYP \_ volume) e la modifica ha effetto sui supporti (il membro dei **\_ flag dbcv** è DBTF \_ ).</span><span class="sxs-lookup"><span data-stu-id="405d5-122">If media is being removed, the type of device arriving is a volume (the **dbch\_devicetype** member is DBT\_DEVTYP\_VOLUME) and the change effects the media (the **dbcv\_flags** member is DBTF\_MEDIA).</span></span>

## <a name="examples"></a><span data-ttu-id="405d5-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="405d5-123">Examples</span></span>

<span data-ttu-id="405d5-124">Per un esempio, vedere [rilevamento dell'inserimento o della rimozione di supporti](detecting-media-insertion-or-removal.md) o [elaborazione di una richiesta di rimozione di un dispositivo](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="405d5-124">For an example, see [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md) or [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="405d5-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="405d5-125">Requirements</span></span>



| <span data-ttu-id="405d5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="405d5-126">Requirement</span></span> | <span data-ttu-id="405d5-127">Valore</span><span class="sxs-lookup"><span data-stu-id="405d5-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="405d5-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="405d5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="405d5-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="405d5-129">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="405d5-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="405d5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="405d5-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="405d5-131">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="405d5-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="405d5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="405d5-133"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="405d5-133"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="405d5-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="405d5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="405d5-135">Eventi dispositivo</span><span class="sxs-lookup"><span data-stu-id="405d5-135">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="405d5-136">Eventi di gestione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="405d5-136">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="405d5-137">**SVILUPPO \_ broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="405d5-137">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="405d5-138">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="405d5-138">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




