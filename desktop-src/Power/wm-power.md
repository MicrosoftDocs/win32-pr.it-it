---
description: Notifica alle applicazioni che il sistema, in genere un personal computer alimentato dalla batteria, sta per entrare in modalità sospesa.
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: Messaggio WM_POWER (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53fd165ee1cefe8970f85daea04b931a673b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312005"
---
# <a name="wm_power-message"></a><span data-ttu-id="30ddc-103">\_Power Message di WM</span><span class="sxs-lookup"><span data-stu-id="30ddc-103">WM\_POWER message</span></span>

<span data-ttu-id="30ddc-104">Notifica alle applicazioni che il sistema, in genere un personal computer alimentato dalla batteria, sta per entrare in modalità sospesa.</span><span class="sxs-lookup"><span data-stu-id="30ddc-104">Notifies applications that the system, typically a battery-powered personal computer, is about to enter a suspended mode.</span></span>

> [!Note]  
> <span data-ttu-id="30ddc-105">Il messaggio di **\_ risparmio energia WM** è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="30ddc-105">The **WM\_POWER** message is obsolete.</span></span> <span data-ttu-id="30ddc-106">Viene fornita solo per la compatibilità con le applicazioni basate su Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="30ddc-106">It is provided only for compatibility with 16-bit Windows-based applications.</span></span> <span data-ttu-id="30ddc-107">Le applicazioni devono usare il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="30ddc-107">Applications should use the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span>

 

<span data-ttu-id="30ddc-108">Una finestra riceve questo messaggio tramite la funzione **WindowProc** .</span><span class="sxs-lookup"><span data-stu-id="30ddc-108">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWER
  WPARAM wParam,  // power-event notification
  LPARAM lParam   // not used
); 
```



## <a name="parameters"></a><span data-ttu-id="30ddc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="30ddc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30ddc-110">*HWND*</span><span class="sxs-lookup"><span data-stu-id="30ddc-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="30ddc-111">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="30ddc-111">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="30ddc-112">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="30ddc-112">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="30ddc-113">Identificatore del messaggio di **\_ alimentazione WM** .</span><span class="sxs-lookup"><span data-stu-id="30ddc-113">The **WM\_POWER** message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="30ddc-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30ddc-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30ddc-115">Notifica degli eventi di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="30ddc-115">The power-event notification.</span></span> <span data-ttu-id="30ddc-116">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="30ddc-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="30ddc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="30ddc-117">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="30ddc-118">Significato</span><span class="sxs-lookup"><span data-stu-id="30ddc-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <span data-ttu-id="30ddc-119"><dt>**\_CRITICALRESUME PWR**</dt></span><span class="sxs-lookup"><span data-stu-id="30ddc-119"><dt>**PWR\_CRITICALRESUME**</dt></span></span> </dl> | <span data-ttu-id="30ddc-120">Indica che il sistema sta riprendendo l'operazione dopo l'attivazione della modalità sospesa senza prima trasmettere un messaggio di notifica **PWR \_ SUSPENDREQUEST** all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="30ddc-120">Indicates that the system is resuming operation after entering suspended mode without first broadcasting a **PWR\_SUSPENDREQUEST** notification message to the application.</span></span> <span data-ttu-id="30ddc-121">Un'applicazione deve eseguire tutte le azioni di ripristino necessarie.</span><span class="sxs-lookup"><span data-stu-id="30ddc-121">An application should perform any necessary recovery actions.</span></span><br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <span data-ttu-id="30ddc-122"><dt>**\_SUSPENDREQUEST PWR**</dt></span><span class="sxs-lookup"><span data-stu-id="30ddc-122"><dt>**PWR\_SUSPENDREQUEST**</dt></span></span> </dl> | <span data-ttu-id="30ddc-123">Indica che il sistema sta per attivare la modalità sospesa.</span><span class="sxs-lookup"><span data-stu-id="30ddc-123">Indicates that the system is about to enter suspended mode.</span></span><br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <span data-ttu-id="30ddc-124"><dt>**\_SUSPENDRESUME PWR**</dt></span><span class="sxs-lookup"><span data-stu-id="30ddc-124"><dt>**PWR\_SUSPENDRESUME**</dt></span></span> </dl>    | <span data-ttu-id="30ddc-125">Indica che il sistema sta riprendendo l'operazione dopo che è stata attivata la modalità sospesa normalmente, il sistema trasmette un messaggio di notifica **PWR \_ SUSPENDREQUEST** all'applicazione prima che il sistema sia stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="30ddc-125">Indicates that the system is resuming operation after having entered suspended mode normally that is, the system broadcast a **PWR\_SUSPENDREQUEST** notification message to the application before the system was suspended.</span></span> <span data-ttu-id="30ddc-126">Un'applicazione deve eseguire tutte le azioni di ripristino necessarie.</span><span class="sxs-lookup"><span data-stu-id="30ddc-126">An application should perform any necessary recovery actions.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="30ddc-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30ddc-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30ddc-128">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="30ddc-128">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30ddc-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30ddc-129">Return value</span></span>

<span data-ttu-id="30ddc-130">Il valore restituito da un'applicazione dipende dal valore del parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="30ddc-130">The value an application returns depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="30ddc-131">Se *wParam* è **PWR \_ SUSPENDREQUEST**, il valore restituito è **PWR \_ non riesce** a impedire che il sistema entri nello stato Suspended. in caso contrario, è **PWR \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="30ddc-131">If *wParam* is **PWR\_SUSPENDREQUEST**, the return value is **PWR\_FAIL** to prevent the system from entering the suspended state; otherwise, it is **PWR\_OK**.</span></span> <span data-ttu-id="30ddc-132">Se *wParam* è **PWR \_ SUSPENDRESUME** o **PWR \_ CRITICALRESUME**, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="30ddc-132">If *wParam* is **PWR\_SUSPENDRESUME** or **PWR\_CRITICALRESUME**, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="30ddc-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="30ddc-133">Remarks</span></span>

<span data-ttu-id="30ddc-134">Questo messaggio viene trasmesso solo a un'applicazione in esecuzione in un sistema conforme alla specifica del BIOS (Basic Input/Output System) di Advanced Power Management (APM).</span><span class="sxs-lookup"><span data-stu-id="30ddc-134">This message is broadcast only to an application that is running on a system that conforms to the Advanced Power Management (APM) basic input/output system (BIOS) specification.</span></span> <span data-ttu-id="30ddc-135">Il messaggio viene trasmesso dal driver di gestione del risparmio energia a ogni finestra restituita dalla funzione **EnumWindows** .</span><span class="sxs-lookup"><span data-stu-id="30ddc-135">The message is broadcast by the power-management driver to each window returned by the **EnumWindows** function.</span></span>

<span data-ttu-id="30ddc-136">La modalità sospesa è lo stato in cui si verifica la maggiore quantità di risparmio energia, ma vengono conservati tutti i dati e i parametri operativi.</span><span class="sxs-lookup"><span data-stu-id="30ddc-136">The suspended mode is the state in which the greatest amount of power savings occurs, but all operational data and parameters are preserved.</span></span> <span data-ttu-id="30ddc-137">Il contenuto della memoria ad accesso casuale (RAM) viene mantenuto, ma è probabile che molti dispositivi siano spenti.</span><span class="sxs-lookup"><span data-stu-id="30ddc-137">Random-access memory (RAM) contents are preserved, but many devices are likely to be turned off.</span></span>

## <a name="requirements"></a><span data-ttu-id="30ddc-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30ddc-138">Requirements</span></span>



| <span data-ttu-id="30ddc-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="30ddc-139">Requirement</span></span> | <span data-ttu-id="30ddc-140">Valore</span><span class="sxs-lookup"><span data-stu-id="30ddc-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30ddc-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30ddc-141">Minimum supported client</span></span><br/> | <span data-ttu-id="30ddc-142">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="30ddc-142">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="30ddc-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30ddc-143">Minimum supported server</span></span><br/> | <span data-ttu-id="30ddc-144">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="30ddc-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="30ddc-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30ddc-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="30ddc-146"><dt>WinUser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30ddc-146"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30ddc-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30ddc-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ddc-148">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="30ddc-148">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




