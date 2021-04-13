---
description: Il sistema trasmette l'evento DBT \_ DEVICEARRIVAL Device quando un dispositivo o un elemento multimediale è stato inserito e diventa disponibile.
ms.assetid: 8e44cb02-cf79-4b19-807e-20cea07362af
title: Evento DBT_DEVICEARRIVAL (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69c2feec996b4306c271454767ca4e75d1ff855
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483277"
---
# <a name="dbt_devicearrival-event"></a><span data-ttu-id="1a244-103">\_Evento DEVICEARRIVAL DBT</span><span class="sxs-lookup"><span data-stu-id="1a244-103">DBT\_DEVICEARRIVAL event</span></span>

<span data-ttu-id="1a244-104">Il sistema trasmette l'evento DBT \_ DEVICEARRIVAL Device quando un dispositivo o un elemento multimediale è stato inserito e diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="1a244-104">The system broadcasts the DBT\_DEVICEARRIVAL device event when a device or piece of media has been inserted and becomes available.</span></span>

<span data-ttu-id="1a244-105">Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ DEVICEARRIVAL e *lParam* impostati come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="1a244-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEARRIVAL and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="1a244-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a244-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a244-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="1a244-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="1a244-108">Handle di una finestra.</span><span class="sxs-lookup"><span data-stu-id="1a244-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="1a244-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="1a244-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="1a244-110">Identificatore del messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="1a244-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1a244-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a244-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a244-112">Impostare su DBT \_ DEVICEARRIVAL.</span><span class="sxs-lookup"><span data-stu-id="1a244-112">Set to DBT\_DEVICEARRIVAL.</span></span>

</dd> <dt>

<span data-ttu-id="1a244-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a244-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a244-114">Puntatore a una struttura che identifica il dispositivo inserito.</span><span class="sxs-lookup"><span data-stu-id="1a244-114">A pointer to a structure identifying the device inserted.</span></span> <span data-ttu-id="1a244-115">La struttura è costituita da un'intestazione indipendente dall'evento, seguita da membri dipendenti dall'evento che descrivono il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a244-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="1a244-116">Per usare questa struttura, considerare la struttura come una [**struttura \_ \_ HDR di sviluppo broadcast**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , quindi controllare il membro **dbch \_ DeviceType** per determinare il tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a244-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a244-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a244-117">Return value</span></span>

<span data-ttu-id="1a244-118">Restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="1a244-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a244-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a244-119">Remarks</span></span>

<span data-ttu-id="1a244-120">Se è in corso l'inserimento del supporto, il tipo di dispositivo in arrivo è un volume (il membro **dbch \_ DeviceType** è DBT \_ DEVTYP \_ volume) e la modifica ha effetto sui supporti (il membro dei **\_ flag dbcv** è DBTF \_ ).</span><span class="sxs-lookup"><span data-stu-id="1a244-120">If media is being inserted, the type of device arriving is a volume (the **dbch\_devicetype** member is DBT\_DEVTYP\_VOLUME) and the change effects the media (the **dbcv\_flags** member is DBTF\_MEDIA).</span></span>

## <a name="examples"></a><span data-ttu-id="1a244-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="1a244-121">Examples</span></span>

<span data-ttu-id="1a244-122">Per un esempio, vedere [rilevamento dell'inserimento o della rimozione dei supporti](detecting-media-insertion-or-removal.md).</span><span class="sxs-lookup"><span data-stu-id="1a244-122">For an example, see [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a244-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a244-123">Requirements</span></span>



| <span data-ttu-id="1a244-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a244-124">Requirement</span></span> | <span data-ttu-id="1a244-125">Valore</span><span class="sxs-lookup"><span data-stu-id="1a244-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1a244-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a244-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1a244-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1a244-127">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="1a244-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a244-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1a244-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1a244-129">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="1a244-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a244-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a244-131"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a244-131"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a244-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a244-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a244-133">Eventi dispositivo</span><span class="sxs-lookup"><span data-stu-id="1a244-133">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="1a244-134">Eventi di gestione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="1a244-134">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="1a244-135">**SVILUPPO \_ broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="1a244-135">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="1a244-136">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="1a244-136">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




