---
description: Il sistema trasmette l'evento DBT \_ CONFIGCHANGED Device per indicare che la configurazione corrente è cambiata a causa di un ancoraggio o di Undock. Un'applicazione o un driver che archivia i dati nel registro di sistema sotto la \_ chiave di configurazione HKEY corrente \_ dovrebbe aggiornare i dati.
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: Evento DBT_CONFIGCHANGED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242832378ba9ca3d3006965719942aa41ecff93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225646"
---
# <a name="dbt_configchanged-event"></a><span data-ttu-id="bead0-104">\_Evento CONFIGCHANGED DBT</span><span class="sxs-lookup"><span data-stu-id="bead0-104">DBT\_CONFIGCHANGED event</span></span>

<span data-ttu-id="bead0-105">Il sistema trasmette l'evento DBT \_ CONFIGCHANGED Device per indicare che la configurazione corrente è cambiata a causa di un ancoraggio o di Undock.</span><span class="sxs-lookup"><span data-stu-id="bead0-105">The system broadcasts the DBT\_CONFIGCHANGED device event to indicate that the current configuration has changed, due to a dock or undock.</span></span> <span data-ttu-id="bead0-106">Un'applicazione o un driver che archivia i dati nel registro di sistema sotto la \_ chiave di configurazione HKEY corrente \_ dovrebbe aggiornare i dati.</span><span class="sxs-lookup"><span data-stu-id="bead0-106">An application or driver that stores data in the registry under the HKEY\_CURRENT\_CONFIG key should update the data.</span></span>

<span data-ttu-id="bead0-107">Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ CONFIGCHANGED e *lParam* impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="bead0-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CONFIGCHANGED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="bead0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bead0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bead0-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="bead0-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bead0-110">Handle di una finestra.</span><span class="sxs-lookup"><span data-stu-id="bead0-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="bead0-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="bead0-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="bead0-112">Identificatore del messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="bead0-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bead0-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bead0-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bead0-114">Impostare su DBT \_ CONFIGCHANGED.</span><span class="sxs-lookup"><span data-stu-id="bead0-114">Set to DBT\_CONFIGCHANGED.</span></span>

</dd> <dt>

<span data-ttu-id="bead0-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bead0-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bead0-116">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="bead0-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bead0-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bead0-117">Return value</span></span>

<span data-ttu-id="bead0-118">Restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="bead0-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bead0-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bead0-119">Requirements</span></span>



| <span data-ttu-id="bead0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bead0-120">Requirement</span></span> | <span data-ttu-id="bead0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="bead0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bead0-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bead0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bead0-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bead0-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="bead0-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bead0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bead0-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bead0-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="bead0-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bead0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bead0-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="bead0-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bead0-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bead0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bead0-129">Eventi dispositivo</span><span class="sxs-lookup"><span data-stu-id="bead0-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="bead0-130">Eventi di gestione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="bead0-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="bead0-131">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="bead0-131">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




