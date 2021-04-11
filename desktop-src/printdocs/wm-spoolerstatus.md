---
description: Il \_ messaggio WM SPOOLERSTATUS viene inviato da Gestione stampa ogni volta che un processo viene aggiunto o rimosso dalla coda di Print Manager.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: Messaggio WM_SPOOLERSTATUS (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 460e36e44f219bcbe6f514d7d368accddae46b83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131802"
---
# <a name="wm_spoolerstatus-message"></a><span data-ttu-id="a2e6b-103">\_Messaggio SPOOLERSTATUS WM</span><span class="sxs-lookup"><span data-stu-id="a2e6b-103">WM\_SPOOLERSTATUS message</span></span>

<span data-ttu-id="a2e6b-104">Il messaggio **WM \_ SPOOLERSTATUS** viene inviato da Gestione stampa ogni volta che un processo viene aggiunto o rimosso dalla coda di Print Manager.</span><span class="sxs-lookup"><span data-stu-id="a2e6b-104">The **WM\_SPOOLERSTATUS** message is sent from Print Manager whenever a job is added to or removed from the Print Manager queue.</span></span>

<span data-ttu-id="a2e6b-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a2e6b-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="a2e6b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2e6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2e6b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2e6b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2e6b-108">Flag JOBSTATUS della richiesta pull \_ .</span><span class="sxs-lookup"><span data-stu-id="a2e6b-108">The PR\_JOBSTATUS flag.</span></span>

</dd> <dt>

<span data-ttu-id="a2e6b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2e6b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2e6b-110">La parola più bassa indica il numero di processi rimanenti nella coda del gestore di stampa.</span><span class="sxs-lookup"><span data-stu-id="a2e6b-110">The low-order word specifies the number of jobs remaining in the Print Manager queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2e6b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2e6b-111">Return value</span></span>

<span data-ttu-id="a2e6b-112">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a2e6b-112">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2e6b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2e6b-113">Remarks</span></span>

<span data-ttu-id="a2e6b-114">Questo messaggio è esclusivamente a scopo informativo.</span><span class="sxs-lookup"><span data-stu-id="a2e6b-114">This message is for informational purposes only.</span></span> <span data-ttu-id="a2e6b-115">Questo messaggio è consultivo e non ha una semantica di recapito garantita.</span><span class="sxs-lookup"><span data-stu-id="a2e6b-115">This message is advisory and does not have guaranteed delivery semantics.</span></span> <span data-ttu-id="a2e6b-116">Le applicazioni non devono presupporre che ricevano un \_ messaggio WM SPOOLERSTATUS per ogni modifica dello stato dello spooler.</span><span class="sxs-lookup"><span data-stu-id="a2e6b-116">Applications should not assume that they will receive a WM\_SPOOLERSTATUS message for every change in spooler status.</span></span>

<span data-ttu-id="a2e6b-117">Il \_ messaggio WM SPOOLERSTATUS non è supportato dopo Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a2e6b-117">The WM\_SPOOLERSTATUS message is not supported after Windows XP.</span></span> <span data-ttu-id="a2e6b-118">Per ricevere una notifica delle modifiche apportate allo stato della coda di stampa, è possibile usare [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) e [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span><span class="sxs-lookup"><span data-stu-id="a2e6b-118">To be notified of changes to the print queue status, you can use [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) and [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2e6b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2e6b-119">Requirements</span></span>



| <span data-ttu-id="a2e6b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2e6b-120">Requirement</span></span> | <span data-ttu-id="a2e6b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a2e6b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2e6b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2e6b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a2e6b-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a2e6b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a2e6b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2e6b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a2e6b-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a2e6b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a2e6b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2e6b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2e6b-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2e6b-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2e6b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2e6b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2e6b-129">Stampa</span><span class="sxs-lookup"><span data-stu-id="a2e6b-129">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a2e6b-130">Messaggi dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="a2e6b-130">Print Spooler API Messages</span></span>](printing-and-print-spooler-messages.md)
</dt> <dt>

[<span data-ttu-id="a2e6b-131">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="a2e6b-131">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="a2e6b-132">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="a2e6b-132">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> </dl>

 

