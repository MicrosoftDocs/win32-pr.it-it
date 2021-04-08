---
description: Il sistema trasmette l'evento DBT \_ CONFIGCHANGECANCELED Device quando una richiesta di modifica della configurazione corrente (dock o Undock) è stata annullata.
ms.assetid: b4b1455c-9a04-4fa0-a3fa-ed991f278c0c
title: Evento DBT_CONFIGCHANGECANCELED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97944daa698808c55f88bc377c9bf1c59c1217fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877758"
---
# <a name="dbt_configchangecanceled-event"></a><span data-ttu-id="546b4-103">\_Evento CONFIGCHANGECANCELED DBT</span><span class="sxs-lookup"><span data-stu-id="546b4-103">DBT\_CONFIGCHANGECANCELED event</span></span>

<span data-ttu-id="546b4-104">Il sistema trasmette l'evento DBT \_ CONFIGCHANGECANCELED Device quando una richiesta di modifica della configurazione corrente (dock o Undock) è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="546b4-104">The system broadcasts the DBT\_CONFIGCHANGECANCELED device event when a request to change the current configuration (dock or undock) has been canceled.</span></span>

<span data-ttu-id="546b4-105">Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ CONFIGCHANGECANCELED e *lParam* impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="546b4-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CONFIGCHANGECANCELED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="546b4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="546b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="546b4-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="546b4-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="546b4-108">Handle di una finestra.</span><span class="sxs-lookup"><span data-stu-id="546b4-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="546b4-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="546b4-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="546b4-110">Identificatore del messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="546b4-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="546b4-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="546b4-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="546b4-112">Impostare su DBT \_ CONFIGCHANGECANCELED.</span><span class="sxs-lookup"><span data-stu-id="546b4-112">Set to DBT\_CONFIGCHANGECANCELED.</span></span>

</dd> <dt>

<span data-ttu-id="546b4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="546b4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="546b4-114">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="546b4-114">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="546b4-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="546b4-115">Return value</span></span>

<span data-ttu-id="546b4-116">Restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="546b4-116">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="546b4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="546b4-117">Requirements</span></span>



| <span data-ttu-id="546b4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="546b4-118">Requirement</span></span> | <span data-ttu-id="546b4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="546b4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="546b4-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="546b4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="546b4-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="546b4-121">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="546b4-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="546b4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="546b4-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="546b4-123">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="546b4-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="546b4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="546b4-125"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="546b4-125"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="546b4-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="546b4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="546b4-127">Eventi dispositivo</span><span class="sxs-lookup"><span data-stu-id="546b4-127">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="546b4-128">Eventi di gestione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="546b4-128">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="546b4-129">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="546b4-129">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




