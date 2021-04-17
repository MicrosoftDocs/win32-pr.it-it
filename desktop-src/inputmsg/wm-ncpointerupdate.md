---
title: Messaggio WM_NCPOINTERUPDATE
description: Inviato per fornire un aggiornamento su un puntatore che ha effettuato il contatto sull'area non client di una finestra o quando un contatto non acquisito in sospeso passa sull'area non client di una finestra.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704caa1322
keywords:
- Messaggi e notifiche di input del messaggio WM_NCPOINTERUPDATE
topic_type:
- apiref
api_name:
- WM_NCPOINTERUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 09ef5fd6f3b7378a963be4278f1fabdf0f6ab351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400501"
---
# <a name="wm_ncpointerupdate-message"></a><span data-ttu-id="4df37-104">Messaggio WM_NCPOINTERUPDATE</span><span class="sxs-lookup"><span data-stu-id="4df37-104">WM_NCPOINTERUPDATE message</span></span>

<span data-ttu-id="4df37-105">Inviato per fornire un aggiornamento su un puntatore che ha effettuato il contatto sull'area non client di una finestra o quando un contatto non acquisito in sospeso passa sull'area non client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="4df37-105">Posted to provide an update on a pointer that made contact over the non-client area of a window or when a hovering uncaptured contact moves over the non-client area of a window.</span></span> <span data-ttu-id="4df37-106">Mentre il puntatore è posizionato al passaggio del mouse, il messaggio viene indirizzato a qualsiasi finestra su cui si trova il puntatore.</span><span class="sxs-lookup"><span data-stu-id="4df37-106">While the pointer is hovering, the message targets whichever window the pointer happens to be over.</span></span> <span data-ttu-id="4df37-107">Mentre il puntatore è in contatto con la superficie, il puntatore viene acquisito in modo implicito nella finestra su cui il puntatore ha effettuato il contatto e tale finestra continua a ricevere l'input per il puntatore finché non interrompe il contatto.</span><span class="sxs-lookup"><span data-stu-id="4df37-107">While the pointer is in contact with the surface, the pointer is implicitly captured to the window over which the pointer made contact and that window continues to receive input for the pointer until it breaks contact.</span></span>

<span data-ttu-id="4df37-108">Se una finestra ha acquisito questo puntatore, questo messaggio non viene inviato.</span><span class="sxs-lookup"><span data-stu-id="4df37-108">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="4df37-109">Al contrario, viene pubblicato un [**WM_POINTERUPDATE**](wm-pointerupdate.md) nella finestra che ha acquisito il puntatore.</span><span class="sxs-lookup"><span data-stu-id="4df37-109">Instead, a [**WM_POINTERUPDATE**](wm-pointerupdate.md) is posted to the window that has captured this pointer.</span></span>

> <span data-ttu-id="4df37-110">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="4df37-110">\[!Important\]</span></span>  
> <span data-ttu-id="4df37-111">Le applicazioni desktop devono essere compatibili con DPI.</span><span class="sxs-lookup"><span data-stu-id="4df37-111">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="4df37-112">Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI.</span><span class="sxs-lookup"><span data-stu-id="4df37-112">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="4df37-113">La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo).</span><span class="sxs-lookup"><span data-stu-id="4df37-113">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="4df37-114">Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4df37-114">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_NCPOINTERUPDATE                 0x0241
```



## <a name="parameters"></a><span data-ttu-id="4df37-115">Parametri</span><span class="sxs-lookup"><span data-stu-id="4df37-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4df37-116">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4df37-116">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4df37-117">Contiene l'identificatore del puntatore e informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="4df37-117">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="4df37-118">Usare le macro seguenti per recuperare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="4df37-118">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="4df37-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore</span><span class="sxs-lookup"><span data-stu-id="4df37-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="4df37-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): valore hit-test restituito dall'elaborazione del messaggio di [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="4df37-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="4df37-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4df37-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4df37-122">Contiene la posizione del punto del puntatore.</span><span class="sxs-lookup"><span data-stu-id="4df37-122">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="4df37-123">Poiché il puntatore può rendere il contatto con il dispositivo su un'area non banale, questa posizione del punto può essere una semplificazione di un'area del puntatore più complessa.</span><span class="sxs-lookup"><span data-stu-id="4df37-123">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="4df37-124">Laddove possibile, un'applicazione deve usare le informazioni complete sull'area del puntatore anziché la posizione del punto.</span><span class="sxs-lookup"><span data-stu-id="4df37-124">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="4df37-125">Utilizzare le macro seguenti per recuperare le coordinate dello schermo fisico del punto.</span><span class="sxs-lookup"><span data-stu-id="4df37-125">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="4df37-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): coordinata X (punto orizzontale).</span><span class="sxs-lookup"><span data-stu-id="4df37-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="4df37-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordinata Y (punto verticale).</span><span class="sxs-lookup"><span data-stu-id="4df37-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4df37-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4df37-128">Return value</span></span>

<span data-ttu-id="4df37-129">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="4df37-129">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="4df37-130">Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="4df37-130">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="4df37-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="4df37-131">Remarks</span></span>

<span data-ttu-id="4df37-132">Se l'applicazione non elabora questo messaggio, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) può eseguire una o più azioni di sistema a seconda del risultato dell'hit test incluso nel messaggio.</span><span class="sxs-lookup"><span data-stu-id="4df37-132">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may perform one or more system actions depending on the hit-test result included in the message.</span></span> <span data-ttu-id="4df37-133">In genere, le applicazioni non devono necessariamente gestire questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="4df37-133">Typically, applications should not need to handle this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4df37-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4df37-134">Requirements</span></span>



| <span data-ttu-id="4df37-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4df37-135">Requirement</span></span> | <span data-ttu-id="4df37-136">Valore</span><span class="sxs-lookup"><span data-stu-id="4df37-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4df37-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4df37-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4df37-138">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4df37-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="4df37-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4df37-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4df37-140">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4df37-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4df37-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4df37-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="4df37-142"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4df37-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4df37-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4df37-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df37-144">Messaggi</span><span class="sxs-lookup"><span data-stu-id="4df37-144">Messages</span></span>](messages.md)
</dt> </dl>

 

