---
title: Messaggio WM_NCPOINTERUP
description: Inviato quando un puntatore che ha effettuato il contatto sull'area non client di una finestra interrompe il contatto.
ms.assetid: 4bdc11da-227c-4be1-bf0b-99704caa1322
keywords:
- Messaggi e notifiche di input del messaggio WM_NCPOINTERUP
topic_type:
- apiref
api_name:
- WM_NCPOINTERUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: a875814b51558c20de47eeee525f6dd35f716fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742575"
---
# <a name="wm_ncpointerup-message"></a><span data-ttu-id="e4c3b-104">Messaggio WM_NCPOINTERUP</span><span class="sxs-lookup"><span data-stu-id="e4c3b-104">WM_NCPOINTERUP message</span></span>

<span data-ttu-id="e4c3b-105">Inviato quando un puntatore che ha effettuato il contatto sull'area non client di una finestra interrompe il contatto.</span><span class="sxs-lookup"><span data-stu-id="e4c3b-105">Posted when a pointer that made contact over the non-client area of a window breaks contact.</span></span> <span data-ttu-id="e4c3b-106">Il messaggio è destinato alla finestra su cui il puntatore fa riferimento e il puntatore è, a quel punto, acquisito in modo implicito nella finestra, in modo che la finestra continui a ricevere l'input per il puntatore finché non interrompe il contatto, inclusa la notifica **WM_NCPOINTERUP** .</span><span class="sxs-lookup"><span data-stu-id="e4c3b-106">The message targets the window over which the pointer makes contact and the pointer is, at that point, implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact, including the **WM_NCPOINTERUP** notification.</span></span>

<span data-ttu-id="e4c3b-107">Se una finestra ha acquisito questo puntatore, questo messaggio non viene inviato.</span><span class="sxs-lookup"><span data-stu-id="e4c3b-107">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="e4c3b-108">Al contrario, viene pubblicato un [**WM_POINTERUP**](wm-pointerup.md) nella finestra che ha acquisito il puntatore.</span><span class="sxs-lookup"><span data-stu-id="e4c3b-108">Instead, a [**WM_POINTERUP**](wm-pointerup.md) is posted to the window that has captured this pointer.</span></span>

> <span data-ttu-id="e4c3b-109">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="e4c3b-109">\[!Important\]</span></span>  
> <span data-ttu-id="e4c3b-110">Le applicazioni desktop devono essere compatibili con DPI.</span><span class="sxs-lookup"><span data-stu-id="e4c3b-110">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="e4c3b-111">Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI.</span><span class="sxs-lookup"><span data-stu-id="e4c3b-111">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="e4c3b-112">La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo).</span><span class="sxs-lookup"><span data-stu-id="e4c3b-112">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="e4c3b-113">Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4c3b-113">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_NCPOINTERUP               0x0243
```



## <a name="parameters"></a><span data-ttu-id="e4c3b-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4c3b-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4c3b-115">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4c3b-115">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4c3b-116">Contiene l'identificatore del puntatore e informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="e4c3b-116">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="e4c3b-117">Usare le macro seguenti per recuperare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="e4c3b-117">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="e4c3b-118">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore</span><span class="sxs-lookup"><span data-stu-id="e4c3b-118">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="e4c3b-119">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): valore hit-test restituito dall'elaborazione del messaggio di [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="e4c3b-119">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="e4c3b-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4c3b-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4c3b-121">Contiene la posizione del punto del puntatore.</span><span class="sxs-lookup"><span data-stu-id="e4c3b-121">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="e4c3b-122">Poiché il puntatore può rendere il contatto con il dispositivo su un'area non banale, questa posizione del punto può essere una semplificazione di un'area del puntatore più complessa.</span><span class="sxs-lookup"><span data-stu-id="e4c3b-122">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="e4c3b-123">Laddove possibile, un'applicazione deve usare le informazioni complete sull'area del puntatore anziché la posizione del punto.</span><span class="sxs-lookup"><span data-stu-id="e4c3b-123">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="e4c3b-124">Utilizzare le macro seguenti per recuperare le coordinate dello schermo fisico del punto.</span><span class="sxs-lookup"><span data-stu-id="e4c3b-124">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="e4c3b-125">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): coordinata X (punto orizzontale).</span><span class="sxs-lookup"><span data-stu-id="e4c3b-125">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="e4c3b-126">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordinata Y (punto verticale).</span><span class="sxs-lookup"><span data-stu-id="e4c3b-126">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4c3b-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4c3b-127">Return value</span></span>

<span data-ttu-id="e4c3b-128">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="e4c3b-128">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="e4c3b-129">Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="e4c3b-129">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="e4c3b-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4c3b-130">Remarks</span></span>

<span data-ttu-id="e4c3b-131">Se l'applicazione non elabora questo messaggio, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) può eseguire una o più azioni di sistema a seconda del risultato dell'hit test incluso nel messaggio.</span><span class="sxs-lookup"><span data-stu-id="e4c3b-131">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may perform one or more system actions depending on the hit-test result included in the message.</span></span> <span data-ttu-id="e4c3b-132">In genere, le applicazioni non devono necessariamente gestire questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="e4c3b-132">Typically, applications should not need to handle this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4c3b-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4c3b-133">Requirements</span></span>



| <span data-ttu-id="e4c3b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4c3b-134">Requirement</span></span> | <span data-ttu-id="e4c3b-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e4c3b-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c3b-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4c3b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e4c3b-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e4c3b-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="e4c3b-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4c3b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e4c3b-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e4c3b-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e4c3b-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4c3b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4c3b-141"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4c3b-141"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4c3b-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4c3b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4c3b-143">Messaggi</span><span class="sxs-lookup"><span data-stu-id="e4c3b-143">Messages</span></span>](messages.md)
</dt> </dl>

 

