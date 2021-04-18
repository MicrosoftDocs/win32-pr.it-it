---
description: Inviato a un'applicazione quando un utente annulla le attività di inserimento nel journal dell'applicazione. Il messaggio viene pubblicato con un handle di finestra NULL.
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: Messaggio WM_CANCELJOURNAL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5676472d12c8cef2a03e508eca6bb742596a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314878"
---
# <a name="wm_canceljournal-message"></a><span data-ttu-id="3d506-104">\_Messaggio CANCELJOURNAL WM</span><span class="sxs-lookup"><span data-stu-id="3d506-104">WM\_CANCELJOURNAL message</span></span>

<span data-ttu-id="3d506-105">Inviato a un'applicazione quando un utente annulla le attività di inserimento nel journal dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3d506-105">Posted to an application when a user cancels the application's journaling activities.</span></span> <span data-ttu-id="3d506-106">Il messaggio viene pubblicato con un handle di finestra **null** .</span><span class="sxs-lookup"><span data-stu-id="3d506-106">The message is posted with a **NULL** window handle.</span></span>


```C++
#define WM_CANCELJOURNAL                0x004B
```



## <a name="parameters"></a><span data-ttu-id="3d506-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d506-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d506-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d506-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d506-109">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="3d506-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3d506-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d506-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d506-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="3d506-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d506-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d506-112">Return value</span></span>

<span data-ttu-id="3d506-113">Tipo: **void**</span><span class="sxs-lookup"><span data-stu-id="3d506-113">Type: **void**</span></span>

<span data-ttu-id="3d506-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="3d506-114">This message does not return a value.</span></span> <span data-ttu-id="3d506-115">È concepita per essere elaborata dall'interno del ciclo principale di un'applicazione o da una routine hook [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) , non da una routine di finestra.</span><span class="sxs-lookup"><span data-stu-id="3d506-115">It is meant to be processed from within an application's main loop or a [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) hook procedure, not from a window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d506-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d506-116">Remarks</span></span>

<span data-ttu-id="3d506-117">Le modalità di riproduzione e registrazione del journal sono modalità imposte nel sistema che consentono a un'applicazione di registrare o riprodurre l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3d506-117">Journal record and playback modes are modes imposed on the system that let an application sequentially record or play back user input.</span></span> <span data-ttu-id="3d506-118">Il sistema immette queste modalità quando un'applicazione installa una procedura di hook [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) o [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3d506-118">The system enters these modes when an application installs a [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) or [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) hook procedure.</span></span> <span data-ttu-id="3d506-119">Quando il sistema si trova in una di queste modalità di inserimento nel journal, le applicazioni devono eseguire la lettura degli input dalla coda di input.</span><span class="sxs-lookup"><span data-stu-id="3d506-119">When the system is in either of these journaling modes, applications must take turns reading input from the input queue.</span></span> <span data-ttu-id="3d506-120">Se un'applicazione interrompe la lettura dell'input mentre il sistema è in modalità di inserimento nel journal, è necessario attendere le altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3d506-120">If any one application stops reading input while the system is in a journaling mode, other applications are forced to wait.</span></span>

<span data-ttu-id="3d506-121">Per garantire un sistema affidabile, che non può essere reso non risposta da alcuna applicazione, il sistema annulla automaticamente le attività di inserimento nel journal quando un utente preme CTRL + ESC o CTRL + ALT + CANC.</span><span class="sxs-lookup"><span data-stu-id="3d506-121">To ensure a robust system, one that cannot be made unresponsive by any one application, the system automatically cancels any journaling activities when a user presses CTRL+ESC or CTRL+ALT+DEL.</span></span> <span data-ttu-id="3d506-122">Il sistema quindi sgancia le procedure di hook di inserimento nel journal e inserisce un messaggio **WM \_ CANCELJOURNAL** , con un handle di finestra **null** , per l'applicazione che ha impostato l'hook di inserimento nel journal.</span><span class="sxs-lookup"><span data-stu-id="3d506-122">The system then unhooks any journaling hook procedures, and posts a **WM\_CANCELJOURNAL** message, with a **NULL** window handle, to the application that set the journaling hook.</span></span>

<span data-ttu-id="3d506-123">Il messaggio **WM \_ CANCELJOURNAL** ha un handle di finestra **null** , pertanto non può essere inviato a una routine di finestra.</span><span class="sxs-lookup"><span data-stu-id="3d506-123">The **WM\_CANCELJOURNAL** message has a **NULL** window handle, therefore it cannot be dispatched to a window procedure.</span></span> <span data-ttu-id="3d506-124">Per un'applicazione è possibile visualizzare un messaggio **WM \_ CANCELJOURNAL** in due modi: se l'applicazione è in esecuzione nel proprio ciclo principale, deve intercettare il messaggio tra la chiamata a [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) e la relativa chiamata a [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage).</span><span class="sxs-lookup"><span data-stu-id="3d506-124">There are two ways for an application to see a **WM\_CANCELJOURNAL** message: If the application is running in its own main loop, it must catch the message between its call to [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) and its call to [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage).</span></span> <span data-ttu-id="3d506-125">Se l'applicazione non è in esecuzione nel proprio ciclo principale, deve impostare una procedura [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) Hook (tramite una chiamata a [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) che specifica il tipo di hook **WH \_ GetMessage** ) che controlla il messaggio.</span><span class="sxs-lookup"><span data-stu-id="3d506-125">If the application is not running in its own main loop, it must set a [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) hook procedure (through a call to [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) specifying the **WH\_GETMESSAGE** hook type) that watches for the message.</span></span>

<span data-ttu-id="3d506-126">Quando un'applicazione visualizza un messaggio **WM \_ CANCELJOURNAL** , può ipotizzare due elementi: l'utente ha intenzionalmente annullato il record Journal o la modalità di riproduzione e il sistema ha già annullato le procedure di hook di riproduzione o di record Journal.</span><span class="sxs-lookup"><span data-stu-id="3d506-126">When an application sees a **WM\_CANCELJOURNAL** message, it can assume two things: the user has intentionally canceled the journal record or playback mode, and the system has already unhooked any journal record or playback hook procedures.</span></span>

<span data-ttu-id="3d506-127">Si noti che le combinazioni di tasti indicate in precedenza (CTRL + ESC o CTRL + ALT + CANC) determinano l'annullamento del journaling da parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="3d506-127">Note that the key combinations mentioned above (CTRL+ESC or CTRL+ALT+DEL) cause the system to cancel journaling.</span></span> <span data-ttu-id="3d506-128">Se un'applicazione non risponde, concede all'utente un mezzo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3d506-128">If any one application is made unresponsive, they give the user a means of recovery.</span></span> <span data-ttu-id="3d506-129">Il codice della chiave virtuale di [**\_ annullamento VK**](../inputdev/virtual-key-codes.md) (in genere implementato come combinazione di tasti Ctrl + Break) indica il modo in cui un'applicazione che si trova in una modalità di registrazione journal deve controllare come un segnale che l'utente desidera annullare l'attività di inserimento nel journal.</span><span class="sxs-lookup"><span data-stu-id="3d506-129">The [**VK\_CANCEL**](../inputdev/virtual-key-codes.md) virtual key code (usually implemented as the CTRL+BREAK key combination) is what an application that is in journal record mode should watch for as a signal that the user wishes to cancel the journaling activity.</span></span> <span data-ttu-id="3d506-130">La differenza consiste nel fatto che la verifica dell' **\_ annullamento del VK** è un comportamento suggerito per le applicazioni di inserimento nel journal, mentre CTRL + ESC o CTRL + ALT + CANC provocano l'annullamento del journaling da parte del sistema, indipendentemente dal comportamento di un'applicazione di journaling.</span><span class="sxs-lookup"><span data-stu-id="3d506-130">The difference is that watching for **VK\_CANCEL** is a suggested behavior for journaling applications, whereas CTRL+ESC or CTRL+ALT+DEL cause the system to cancel journaling regardless of a journaling application's behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d506-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d506-131">Requirements</span></span>



| <span data-ttu-id="3d506-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d506-132">Requirement</span></span> | <span data-ttu-id="3d506-133">Valore</span><span class="sxs-lookup"><span data-stu-id="3d506-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d506-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d506-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3d506-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3d506-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3d506-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d506-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3d506-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3d506-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3d506-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d506-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d506-139"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d506-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d506-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d506-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="3d506-141">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3d506-141">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="3d506-142">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3d506-142">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="3d506-143">[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3d506-143">[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="3d506-144">[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3d506-144">[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3d506-145">**SetWindowsHookEx**</span><span class="sxs-lookup"><span data-stu-id="3d506-145">**SetWindowsHookEx**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

<span data-ttu-id="3d506-146">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="3d506-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3d506-147">Hook</span><span class="sxs-lookup"><span data-stu-id="3d506-147">Hooks</span></span>](hooks.md)
</dt> </dl>

 

 
