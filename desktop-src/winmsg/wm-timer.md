---
description: Inserito nella coda di messaggi del thread di installazione quando scade un timer. Il messaggio viene inserito dalla funzione GetMessage o PeekMessage.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: Messaggio WM_TIMER (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c99db67c9c9b3419e477ccd0a78133df453a7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233016"
---
# <a name="wm_timer-message"></a><span data-ttu-id="9c797-104">\_Messaggio timer WM</span><span class="sxs-lookup"><span data-stu-id="9c797-104">WM\_TIMER message</span></span>

<span data-ttu-id="9c797-105">Inserito nella coda di messaggi del thread di installazione quando scade un timer.</span><span class="sxs-lookup"><span data-stu-id="9c797-105">Posted to the installing thread's message queue when a timer expires.</span></span> <span data-ttu-id="9c797-106">Il messaggio viene inserito dalla funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="9c797-106">The message is posted by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span>


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a><span data-ttu-id="9c797-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c797-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c797-108">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c797-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c797-109">Identificatore del timer.</span><span class="sxs-lookup"><span data-stu-id="9c797-109">The timer identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9c797-110">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c797-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c797-111">Puntatore a una funzione di callback definita dall'applicazione passata alla funzione [**setimer**](/windows/win32/api/winuser/nf-winuser-settimer) durante l'installazione del timer.</span><span class="sxs-lookup"><span data-stu-id="9c797-111">A pointer to an application-defined callback function that was passed to the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function when the timer was installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c797-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c797-112">Return value</span></span>

<span data-ttu-id="9c797-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="9c797-113">Type: **LRESULT**</span></span>

<span data-ttu-id="9c797-114">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="9c797-114">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c797-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c797-115">Remarks</span></span>

<span data-ttu-id="9c797-116">È possibile elaborare il messaggio fornendo un caso **del \_ timer WM** nella procedura della finestra.</span><span class="sxs-lookup"><span data-stu-id="9c797-116">You can process the message by providing a **WM\_TIMER** case in the window procedure.</span></span> <span data-ttu-id="9c797-117">In caso contrario, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) chiamerà la funzione di callback [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) specificata nella chiamata alla funzione [**setimer**](/windows/win32/api/winuser/nf-winuser-settimer) utilizzata per installare il timer.</span><span class="sxs-lookup"><span data-stu-id="9c797-117">Otherwise, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) will call the [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) callback function specified in the call to the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function used to install the timer.</span></span>

<span data-ttu-id="9c797-118">Il messaggio del **\_ timer WM** è un messaggio con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="9c797-118">The **WM\_TIMER** message is a low-priority message.</span></span> <span data-ttu-id="9c797-119">Le funzioni [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) e [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) pubblicano questo messaggio solo quando non sono presenti altri messaggi con priorità più elevata nella coda di messaggi del thread.</span><span class="sxs-lookup"><span data-stu-id="9c797-119">The [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) and [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) functions post this message only when no other higher-priority messages are in the thread's message queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c797-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c797-120">Requirements</span></span>



| <span data-ttu-id="9c797-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c797-121">Requirement</span></span> | <span data-ttu-id="9c797-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9c797-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c797-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c797-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9c797-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9c797-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9c797-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c797-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9c797-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9c797-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9c797-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c797-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c797-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c797-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c797-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c797-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c797-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="9c797-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9c797-131">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="9c797-131">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="9c797-132">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="9c797-132">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="9c797-133">**SetTimer**</span><span class="sxs-lookup"><span data-stu-id="9c797-133">**SetTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[<span data-ttu-id="9c797-134">**TimerProc**</span><span class="sxs-lookup"><span data-stu-id="9c797-134">**TimerProc**</span></span>](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

<span data-ttu-id="9c797-135">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="9c797-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9c797-136">Timer</span><span class="sxs-lookup"><span data-stu-id="9c797-136">Timers</span></span>](timers.md)
</dt> </dl>

 

 
