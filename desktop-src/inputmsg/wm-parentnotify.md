---
title: Messaggio WM_PARENTNOTIFY
description: Inviato a una finestra quando si verifica un'azione significativa in una finestra discendente.
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- Messaggi e notifiche di input del messaggio WM_PARENTNOTIFY
topic_type:
- apiref
api_name:
- WM_PARENTNOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 2e19edf25933a035514f9c42b0da6014eccfdb0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518321"
---
# <a name="wm_parentnotify-message"></a><span data-ttu-id="f3f91-104">Messaggio WM_PARENTNOTIFY</span><span class="sxs-lookup"><span data-stu-id="f3f91-104">WM_PARENTNOTIFY message</span></span>

<span data-ttu-id="f3f91-105">Inviato a una finestra quando si verifica un'azione significativa in una finestra discendente.</span><span class="sxs-lookup"><span data-stu-id="f3f91-105">Sent to a window when a significant action occurs on a descendant window.</span></span> <span data-ttu-id="f3f91-106">Questo messaggio è ora esteso per includere l'evento [**WM_POINTERDOWN**](wm-pointerdown.md) .</span><span class="sxs-lookup"><span data-stu-id="f3f91-106">This message is now extended to include the [**WM_POINTERDOWN**](wm-pointerdown.md) event.</span></span> <span data-ttu-id="f3f91-107">Quando viene creata la finestra figlio, il sistema invia [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) appena prima della funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) che crea la finestra restituisce.</span><span class="sxs-lookup"><span data-stu-id="f3f91-107">When the child window is being created, the system sends [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) just before the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function that creates the window returns.</span></span> <span data-ttu-id="f3f91-108">Quando la finestra figlio viene distrutta, il sistema invia il messaggio prima che venga eseguita un'elaborazione per eliminare la finestra.</span><span class="sxs-lookup"><span data-stu-id="f3f91-108">When the child window is being destroyed, the system sends the message before any processing to destroy the window takes place.</span></span>

<span data-ttu-id="f3f91-109">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f3f91-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="f3f91-110">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="f3f91-110">\[!Important\]</span></span>  
> <span data-ttu-id="f3f91-111">Le applicazioni desktop devono essere compatibili con DPI.</span><span class="sxs-lookup"><span data-stu-id="f3f91-111">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="f3f91-112">Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI.</span><span class="sxs-lookup"><span data-stu-id="f3f91-112">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="f3f91-113">La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo).</span><span class="sxs-lookup"><span data-stu-id="f3f91-113">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="f3f91-114">Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3f91-114">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a><span data-ttu-id="f3f91-115">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3f91-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3f91-116">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3f91-116">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3f91-117">La parola più bassa di *wParam* specifica l'evento per il quale l'elemento padre riceve la notifica.</span><span class="sxs-lookup"><span data-stu-id="f3f91-117">The low-order word of *wParam* specifies the event for which the parent is being notified.</span></span> <span data-ttu-id="f3f91-118">Il valore della parola più ordinata dipende dal valore della parola di basso livello.</span><span class="sxs-lookup"><span data-stu-id="f3f91-118">The value of the high-order word depends on the value of the low-order word.</span></span> <span data-ttu-id="f3f91-119">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f3f91-119">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="f3f91-120">LOWORD (*wParam*)</span><span class="sxs-lookup"><span data-stu-id="f3f91-120">LOWORD(*wParam*)</span></span>                                                                                                                                                                                                             | <span data-ttu-id="f3f91-121">Significato</span><span class="sxs-lookup"><span data-stu-id="f3f91-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <span data-ttu-id="f3f91-122"><dt>**WM_CREATE**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="f3f91-122"><dt>**WM_CREATE**</dt> <dt>0x0001</dt></span></span> </dl>                | <span data-ttu-id="f3f91-123">È in corso la creazione della finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="f3f91-123">The child window is being created.</span></span><br/> <span data-ttu-id="f3f91-124">HIWORD (*wParam*) è l'identificatore della finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="f3f91-124">HIWORD(*wParam*) is the identifier of the child window.</span></span><br/> <span data-ttu-id="f3f91-125">*lParam* è un handle per la finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="f3f91-125">*lParam* is a handle to the child window.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <span data-ttu-id="f3f91-126"><dt>**WM_DESTROY**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="f3f91-126"><dt>**WM_DESTROY**</dt> <dt>0x0002</dt></span></span> </dl>             | <span data-ttu-id="f3f91-127">La finestra figlio verrà eliminata definitivamente.</span><span class="sxs-lookup"><span data-stu-id="f3f91-127">The child window is being destroyed.</span></span><br/> <span data-ttu-id="f3f91-128">HIWORD (*wParam*) è l'identificatore della finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="f3f91-128">HIWORD(*wParam*) is the identifier of the child window.</span></span><br/> <span data-ttu-id="f3f91-129">*lParam* è un handle per la finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="f3f91-129">*lParam* is a handle to the child window.</span></span><br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <span data-ttu-id="f3f91-130"><dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt></span><span class="sxs-lookup"><span data-stu-id="f3f91-130"><dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt></span></span> </dl> | <span data-ttu-id="f3f91-131">L'utente ha posizionato il cursore sulla finestra figlio e ha fatto clic con il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="f3f91-131">The user has placed the cursor over the child window and has clicked the left mouse button.</span></span><br/> <span data-ttu-id="f3f91-132">HIWORD (*wParam*) non è definito.</span><span class="sxs-lookup"><span data-stu-id="f3f91-132">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="f3f91-133">*lParam* è la coordinata x del cursore è la parola di basso livello e la coordinata y del cursore è la parola più ordinata.</span><span class="sxs-lookup"><span data-stu-id="f3f91-133">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <span data-ttu-id="f3f91-134"><dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt></span><span class="sxs-lookup"><span data-stu-id="f3f91-134"><dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt></span></span> </dl> | <span data-ttu-id="f3f91-135">L'utente ha posizionato il cursore sulla finestra figlio e ha fatto clic sul pulsante centrale del mouse.</span><span class="sxs-lookup"><span data-stu-id="f3f91-135">The user has placed the cursor over the child window and has clicked the middle mouse button.</span></span><br/> <span data-ttu-id="f3f91-136">HIWORD (*wParam*) non è definito.</span><span class="sxs-lookup"><span data-stu-id="f3f91-136">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="f3f91-137">*lParam* è la coordinata x del cursore è la parola di basso livello e la coordinata y del cursore è la parola più ordinata.</span><span class="sxs-lookup"><span data-stu-id="f3f91-137">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <span data-ttu-id="f3f91-138"><dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt></span><span class="sxs-lookup"><span data-stu-id="f3f91-138"><dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt></span></span> </dl> | <span data-ttu-id="f3f91-139">L'utente ha posizionato il cursore sulla finestra figlio e ha fatto clic con il pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="f3f91-139">The user has placed the cursor over the child window and has clicked the right mouse button.</span></span><br/> <span data-ttu-id="f3f91-140">HIWORD (*wParam*) non è definito.</span><span class="sxs-lookup"><span data-stu-id="f3f91-140">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="f3f91-141">*lParam* è la coordinata x del cursore è la parola di basso livello e la coordinata y del cursore è la parola più ordinata.</span><span class="sxs-lookup"><span data-stu-id="f3f91-141">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <span data-ttu-id="f3f91-142"><dt>**WM_xBUTTONDOWN**</dt> <dt>0x020B</dt></span><span class="sxs-lookup"><span data-stu-id="f3f91-142"><dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt></span></span> </dl> | <span data-ttu-id="f3f91-143">L'utente ha posizionato il cursore sulla finestra figlio e ha fatto clic sul primo o sul secondo pulsante X.</span><span class="sxs-lookup"><span data-stu-id="f3f91-143">The user has placed the cursor over the child window and has clicked the first or second X button.</span></span><br/> <span data-ttu-id="f3f91-144">HIWORD (*wParam*) indica quale pulsante è stato premuto.</span><span class="sxs-lookup"><span data-stu-id="f3f91-144">HIWORD(*wParam*) indicates which button was pressed.</span></span> <span data-ttu-id="f3f91-145">Questo parametro può essere uno dei valori seguenti: XBUTTON1 o XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="f3f91-145">This parameter can be one of the following values: XBUTTON1 or XBUTTON2.</span></span><br/> <span data-ttu-id="f3f91-146">*lParam* è la coordinata x del cursore è la parola di basso livello e la coordinata y del cursore è la parola più ordinata.</span><span class="sxs-lookup"><span data-stu-id="f3f91-146">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <span data-ttu-id="f3f91-147"><dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt></span><span class="sxs-lookup"><span data-stu-id="f3f91-147"><dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt></span></span> </dl> | <span data-ttu-id="f3f91-148">Un puntatore ha effettuato il contatto con la finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="f3f91-148">A pointer has made contact with the child window.</span></span><br/> <span data-ttu-id="f3f91-149">HIWORD (*wParam*) contiene l'identificatore del puntatore che ha generato l'evento [**WM_POINTERDOWN**](wm-pointerdown.md) .</span><span class="sxs-lookup"><span data-stu-id="f3f91-149">HIWORD(*wParam*) contains the identifier of the pointer that generated the [**WM_POINTERDOWN**](wm-pointerdown.md) event.</span></span><br/>                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="f3f91-150">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3f91-150">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3f91-151">Contiene la posizione del punto del puntatore.</span><span class="sxs-lookup"><span data-stu-id="f3f91-151">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="f3f91-152">Poiché il puntatore può rendere il contatto con il dispositivo su un'area non banale, questa posizione del punto può essere una semplificazione di un'area del puntatore più complessa.</span><span class="sxs-lookup"><span data-stu-id="f3f91-152">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="f3f91-153">Laddove possibile, un'applicazione deve usare le informazioni complete sull'area del puntatore anziché la posizione del punto.</span><span class="sxs-lookup"><span data-stu-id="f3f91-153">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="f3f91-154">Utilizzare le macro seguenti per recuperare le coordinate dello schermo fisico del punto.</span><span class="sxs-lookup"><span data-stu-id="f3f91-154">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="f3f91-155">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): coordinata X (punto orizzontale).</span><span class="sxs-lookup"><span data-stu-id="f3f91-155">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="f3f91-156">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordinata Y (punto verticale).</span><span class="sxs-lookup"><span data-stu-id="f3f91-156">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3f91-157">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3f91-157">Return value</span></span>

<span data-ttu-id="f3f91-158">Se l'applicazione elabora il messaggio, viene restituito zero.</span><span class="sxs-lookup"><span data-stu-id="f3f91-158">If the application processes this message, it returns zero.</span></span>

<span data-ttu-id="f3f91-159">Se l'applicazione non elabora questo messaggio, chiama [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="f3f91-159">If the application does not process this message, it calls [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="f3f91-160">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3f91-160">Remarks</span></span>

<span data-ttu-id="f3f91-161">Questo messaggio viene inviato anche a tutte le finestre predecessori della finestra figlio, inclusa la finestra di primo livello.</span><span class="sxs-lookup"><span data-stu-id="f3f91-161">This message is also sent to all ancestor windows of the child window, including the top-level window.</span></span>

<span data-ttu-id="f3f91-162">Tutte le finestre figlio, ad eccezione di quelle con lo stile **WS_EX_NOPARENTNOTIFY** finestra estesa, inviano questo messaggio alle finestre padre.</span><span class="sxs-lookup"><span data-stu-id="f3f91-162">All child windows, except those that have the **WS_EX_NOPARENTNOTIFY** extended window style, send this message to their parent windows.</span></span> <span data-ttu-id="f3f91-163">Per impostazione predefinita, le finestre figlio in una finestra di dialogo hanno lo stile **WS_EX_NOPARENTNOTIFY** , a meno che non venga chiamata la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) per creare la finestra figlio senza questo stile.</span><span class="sxs-lookup"><span data-stu-id="f3f91-163">By default, child windows in a dialog box have the **WS_EX_NOPARENTNOTIFY** style, unless the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function is called to create the child window without this style.</span></span>

<span data-ttu-id="f3f91-164">Questa notifica fornisce alle finestre predecessore della finestra figlio un'opportunità per esaminare le informazioni del puntatore e, se necessario, acquisire il puntatore usando le funzioni di acquisizione del puntatore.</span><span class="sxs-lookup"><span data-stu-id="f3f91-164">This notification provides the child window's ancestor windows an opportunity to examine the pointer information and, if required, capture the pointer using the pointer capture functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3f91-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3f91-165">Requirements</span></span>



| <span data-ttu-id="f3f91-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3f91-166">Requirement</span></span> | <span data-ttu-id="f3f91-167">Valore</span><span class="sxs-lookup"><span data-stu-id="f3f91-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f91-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3f91-168">Minimum supported client</span></span><br/> | <span data-ttu-id="f3f91-169">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f3f91-169">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="f3f91-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3f91-170">Minimum supported server</span></span><br/> | <span data-ttu-id="f3f91-171">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f3f91-171">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f3f91-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3f91-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3f91-173"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3f91-173"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3f91-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3f91-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3f91-175">Messaggi</span><span class="sxs-lookup"><span data-stu-id="f3f91-175">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="f3f91-176">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="f3f91-176">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="f3f91-177">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="f3f91-177">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

<span data-ttu-id="f3f91-178">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f3f91-178">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f3f91-179">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f3f91-179">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f3f91-180">**WM_CREATE**</span><span class="sxs-lookup"><span data-stu-id="f3f91-180">**WM_CREATE**</span></span>](../winmsg/wm-create.md)
</dt> <dt>

[<span data-ttu-id="f3f91-181">**WM_DESTROY**</span><span class="sxs-lookup"><span data-stu-id="f3f91-181">**WM_DESTROY**</span></span>](../winmsg/wm-destroy.md)
</dt> <dt>

[<span data-ttu-id="f3f91-182">**WM_LBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="f3f91-182">**WM_LBUTTONDOWN**</span></span>](../inputdev/wm-lbuttondown.md)
</dt> <dt>

[<span data-ttu-id="f3f91-183">**WM_MBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="f3f91-183">**WM_MBUTTONDOWN**</span></span>](../inputdev/wm-mbuttondown.md)
</dt> <dt>

[<span data-ttu-id="f3f91-184">**WM_RBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="f3f91-184">**WM_RBUTTONDOWN**</span></span>](../inputdev/wm-rbuttondown.md)
</dt> <dt>

[<span data-ttu-id="f3f91-185">**WM_XBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="f3f91-185">**WM_XBUTTONDOWN**</span></span>](../inputdev/wm-xbuttondown.md)
</dt> </dl>

 

