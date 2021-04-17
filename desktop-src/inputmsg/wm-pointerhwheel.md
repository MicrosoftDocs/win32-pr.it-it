---
title: Messaggio WM_POINTERHWHEEL
description: Inserito nella finestra con lo stato attivo della tastiera in primo piano quando viene ruotata una rotellina di scorrimento orizzontale.
ms.assetid: 6eec37da-2200-4be1-bf0b-44504caa1320
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERHWHEEL
topic_type:
- apiref
api_name:
- WM_NCPOINTERCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5817d5ed243363c82038dc3df2d8f1e337079076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400809"
---
# <a name="wm_pointerhwheel-message"></a><span data-ttu-id="fdc66-104">Messaggio WM_POINTERHWHEEL</span><span class="sxs-lookup"><span data-stu-id="fdc66-104">WM_POINTERHWHEEL message</span></span>

<span data-ttu-id="fdc66-105">Inserito nella finestra con lo stato attivo della tastiera in primo piano quando viene ruotata una rotellina di scorrimento orizzontale.</span><span class="sxs-lookup"><span data-stu-id="fdc66-105">Posted to the window with foreground keyboard focus when a horizontal scroll wheel is rotated.</span></span>

<span data-ttu-id="fdc66-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fdc66-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="fdc66-107">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="fdc66-107">\[!Important\]</span></span>  
> <span data-ttu-id="fdc66-108">Le applicazioni desktop devono essere compatibili con DPI.</span><span class="sxs-lookup"><span data-stu-id="fdc66-108">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="fdc66-109">Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI.</span><span class="sxs-lookup"><span data-stu-id="fdc66-109">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="fdc66-110">La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo).</span><span class="sxs-lookup"><span data-stu-id="fdc66-110">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="fdc66-111">Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fdc66-111">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERHWHEEL            0x024F
```



## <a name="parameters"></a><span data-ttu-id="fdc66-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="fdc66-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdc66-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fdc66-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdc66-114">Contiene l'identificatore del puntatore e il Delta della rotellina.</span><span class="sxs-lookup"><span data-stu-id="fdc66-114">Contains the pointer identifier and wheel delta.</span></span> <span data-ttu-id="fdc66-115">Usare le macro seguenti per recuperare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="fdc66-115">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="fdc66-116">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore.</span><span class="sxs-lookup"><span data-stu-id="fdc66-116">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier.</span></span>

<span data-ttu-id="fdc66-117">[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): Delta della rotellina come valore short con segno.</span><span class="sxs-lookup"><span data-stu-id="fdc66-117">[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): wheel delta as signed short value.</span></span>

</dd> <dt>

<span data-ttu-id="fdc66-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fdc66-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdc66-119">Contiene la posizione del punto del puntatore.</span><span class="sxs-lookup"><span data-stu-id="fdc66-119">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="fdc66-120">Poiché il puntatore può rendere il contatto con il dispositivo su un'area non banale, questa posizione del punto può essere una semplificazione di un'area del puntatore più complessa.</span><span class="sxs-lookup"><span data-stu-id="fdc66-120">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="fdc66-121">Laddove possibile, un'applicazione deve usare le informazioni complete sull'area del puntatore anziché la posizione del punto.</span><span class="sxs-lookup"><span data-stu-id="fdc66-121">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="fdc66-122">Utilizzare le macro seguenti per recuperare le coordinate dello schermo fisico del punto.</span><span class="sxs-lookup"><span data-stu-id="fdc66-122">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="fdc66-123">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): coordinata X (punto orizzontale).</span><span class="sxs-lookup"><span data-stu-id="fdc66-123">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="fdc66-124">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordinata Y (punto verticale).</span><span class="sxs-lookup"><span data-stu-id="fdc66-124">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdc66-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fdc66-125">Return value</span></span>

<span data-ttu-id="fdc66-126">Se l'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="fdc66-126">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="fdc66-127">Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="fdc66-127">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="fdc66-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="fdc66-128">Remarks</span></span>

<span data-ttu-id="fdc66-129">Per recuperare le unità di scorrimento della rotellina, usare il **inputData** archiviato della struttura [**POINTER_INFO**](/previous-versions/windows/desktop/api) restituita chiamando la funzione [**GetPointerInfo**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="fdc66-129">To retrieve the wheel scroll units, use the **inputData** filed of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure returned by calling [**GetPointerInfo**](/previous-versions/windows/desktop/api) function.</span></span> <span data-ttu-id="fdc66-130">Questo campo contiene un valore con segno ed è espresso in un multiplo di **WHEEL_DELTA**.</span><span class="sxs-lookup"><span data-stu-id="fdc66-130">This field contains a signed value and is expressed in a multiple of **WHEEL_DELTA**.</span></span> <span data-ttu-id="fdc66-131">Un valore positivo indica una rotazione in avanti e un valore negativo indica una rotazione indietro.</span><span class="sxs-lookup"><span data-stu-id="fdc66-131">A positive value indicates a rotation forward and a negative value indicates a rotation backward.</span></span>

<span data-ttu-id="fdc66-132">Si noti che gli input della rotellina possono essere recapitati anche se il cursore del mouse si trova all'esterno della finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fdc66-132">Note that the wheel inputs may be delivered even if the mouse cursor is located outside of application s window.</span></span> <span data-ttu-id="fdc66-133">I messaggi della rotellina vengono recapitati in modo molto simile agli input da tastiera.</span><span class="sxs-lookup"><span data-stu-id="fdc66-133">The wheel messages are delivered in a way very similar to the keyboard inputs.</span></span> <span data-ttu-id="fdc66-134">La finestra di stato attivo della coda di messaggi foregournd riceve i messaggi della rotellina.</span><span class="sxs-lookup"><span data-stu-id="fdc66-134">The focus window of the foregournd message queue receives the wheel messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdc66-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdc66-135">Requirements</span></span>



| <span data-ttu-id="fdc66-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdc66-136">Requirement</span></span> | <span data-ttu-id="fdc66-137">Valore</span><span class="sxs-lookup"><span data-stu-id="fdc66-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc66-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdc66-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fdc66-139">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fdc66-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="fdc66-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdc66-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fdc66-141">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fdc66-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fdc66-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fdc66-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdc66-143"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fdc66-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdc66-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fdc66-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdc66-145">Messaggi</span><span class="sxs-lookup"><span data-stu-id="fdc66-145">Messages</span></span>](messages.md)
</dt> </dl>

 

