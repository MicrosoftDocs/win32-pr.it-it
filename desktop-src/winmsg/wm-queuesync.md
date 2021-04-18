---
description: Inviato da un'applicazione di training basata su computer (CBT) per separare i messaggi di input dell'utente da altri messaggi inviati tramite la \_ procedura WH JOURNALPLAYBACK.
ms.assetid: 9ac265be-1fcc-476f-9dee-3e961340b5a1
title: Messaggio WM_QUEUESYNC (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d859f858ab7cf8182282cc20dbf514cfc2d9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312366"
---
# <a name="wm_queuesync-message"></a><span data-ttu-id="4b07d-103">\_Messaggio QUEUESYNC WM</span><span class="sxs-lookup"><span data-stu-id="4b07d-103">WM\_QUEUESYNC message</span></span>

<span data-ttu-id="4b07d-104">Inviato da un'applicazione di training basata su computer (CBT) per separare i messaggi di input dell'utente da altri messaggi inviati tramite la procedura [**WH \_ JOURNALPLAYBACK**](about-hooks.md) .</span><span class="sxs-lookup"><span data-stu-id="4b07d-104">Sent by a computer-based training (CBT) application to separate user-input messages from other messages sent through the [**WH\_JOURNALPLAYBACK**](about-hooks.md) procedure.</span></span>


```C++
#define WM_QUEUESYNC                    0x0023
```



## <a name="parameters"></a><span data-ttu-id="4b07d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b07d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b07d-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b07d-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b07d-107">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="4b07d-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4b07d-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b07d-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b07d-109">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="4b07d-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b07d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b07d-110">Return value</span></span>

<span data-ttu-id="4b07d-111">Tipo: **void**</span><span class="sxs-lookup"><span data-stu-id="4b07d-111">Type: **void**</span></span>

<span data-ttu-id="4b07d-112">Un'applicazione CBT deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="4b07d-112">A CBT application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b07d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b07d-113">Remarks</span></span>

<span data-ttu-id="4b07d-114">Ogni volta che un'applicazione CBT usa la procedura [**WH \_ JOURNALPLAYBACK**](about-hooks.md) , il primo e l'ultimo messaggio sono **WM \_ QUEUESYNC**.</span><span class="sxs-lookup"><span data-stu-id="4b07d-114">Whenever a CBT application uses the [**WH\_JOURNALPLAYBACK**](about-hooks.md) procedure, the first and last messages are **WM\_QUEUESYNC**.</span></span> <span data-ttu-id="4b07d-115">Ciò consente all'applicazione CBT di intercettare ed esaminare i messaggi avviati dall'utente senza eseguire questa operazione per gli eventi inviati.</span><span class="sxs-lookup"><span data-stu-id="4b07d-115">This allows the CBT application to intercept and examine user-initiated messages without doing so for events that it sends.</span></span>

<span data-ttu-id="4b07d-116">Se un'applicazione specifica un handle di finestra **null** , il messaggio viene inserito nella coda di messaggi della finestra attiva.</span><span class="sxs-lookup"><span data-stu-id="4b07d-116">If an application specifies a **NULL** window handle, the message is posted to the message queue of the active window.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b07d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b07d-117">Requirements</span></span>



| <span data-ttu-id="4b07d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b07d-118">Requirement</span></span> | <span data-ttu-id="4b07d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4b07d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b07d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b07d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4b07d-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4b07d-121">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4b07d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b07d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4b07d-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b07d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4b07d-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b07d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b07d-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b07d-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b07d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b07d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="4b07d-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4b07d-127">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="4b07d-128">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4b07d-128">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4b07d-129">**SetWindowsHookEx**</span><span class="sxs-lookup"><span data-stu-id="4b07d-129">**SetWindowsHookEx**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

<span data-ttu-id="4b07d-130">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="4b07d-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4b07d-131">Hook</span><span class="sxs-lookup"><span data-stu-id="4b07d-131">Hooks</span></span>](hooks.md)
</dt> </dl>

 

 
