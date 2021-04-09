---
title: Messaggio WM_POINTERDOWN
description: Inviato quando un puntatore fa contatto sull'area client di una finestra.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac000
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERDOWN
topic_type:
- apiref
api_name:
- WM_POINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 051e7f0aa08305e4c38d7eefec94483fd11f3bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120555"
---
# <a name="wm_pointerdown-message"></a><span data-ttu-id="bda1f-104">Messaggio WM_POINTERDOWN</span><span class="sxs-lookup"><span data-stu-id="bda1f-104">WM_POINTERDOWN message</span></span>

<span data-ttu-id="bda1f-105">Inviato quando un puntatore fa contatto sull'area client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="bda1f-105">Posted when a pointer makes contact over the client area of a window.</span></span> <span data-ttu-id="bda1f-106">Questo messaggio di input è destinato alla finestra su cui il puntatore fa riferimento e il puntatore viene acquisito in modo implicito nella finestra, in modo che la finestra continui a ricevere l'input per il puntatore finché non interrompe il contatto.</span><span class="sxs-lookup"><span data-stu-id="bda1f-106">This input message targets the window over which the pointer makes contact, and the pointer is implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact.</span></span>

<span data-ttu-id="bda1f-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bda1f-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="bda1f-108">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="bda1f-108">\[!Important\]</span></span>  
> <span data-ttu-id="bda1f-109">Le applicazioni desktop devono essere compatibili con DPI.</span><span class="sxs-lookup"><span data-stu-id="bda1f-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="bda1f-110">Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI.</span><span class="sxs-lookup"><span data-stu-id="bda1f-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="bda1f-111">La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo).</span><span class="sxs-lookup"><span data-stu-id="bda1f-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="bda1f-112">Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bda1f-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDOWN                   0x0246
```



## <a name="parameters"></a><span data-ttu-id="bda1f-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="bda1f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bda1f-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bda1f-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bda1f-115">Contiene informazioni sul puntatore.</span><span class="sxs-lookup"><span data-stu-id="bda1f-115">Contains information about the pointer.</span></span> <span data-ttu-id="bda1f-116">Usare le macro seguenti per recuperare le informazioni dal parametro wParam.</span><span class="sxs-lookup"><span data-stu-id="bda1f-116">Use the following macros to retrieve information from the wParam parameter.</span></span>

-   <span data-ttu-id="bda1f-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore.</span><span class="sxs-lookup"><span data-stu-id="bda1f-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): the pointer identifier.</span></span>
-   <span data-ttu-id="bda1f-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il messaggio rappresenta il primo input generato da un nuovo puntatore.</span><span class="sxs-lookup"><span data-stu-id="bda1f-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message represents the first input generated by a new pointer.</span></span>
-   <span data-ttu-id="bda1f-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il messaggio è stato generato da un puntatore durante la relativa durata.</span><span class="sxs-lookup"><span data-stu-id="bda1f-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer during its lifetime.</span></span> <span data-ttu-id="bda1f-120">Questo flag non è impostato per i messaggi che indicano che il puntatore ha un intervallo di rilevamento a sinistra</span><span class="sxs-lookup"><span data-stu-id="bda1f-120">This flag is not set on messages that indicate that the pointer has left detection range</span></span>
-   <span data-ttu-id="bda1f-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il messaggio è stato generato da un puntatore in contatto con l'area della finestra.</span><span class="sxs-lookup"><span data-stu-id="bda1f-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer that is in contact with the window surface.</span></span> <span data-ttu-id="bda1f-122">Questo flag non è impostato per i messaggi che indicano un puntatore al passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="bda1f-122">This flag is not set on messages that indicate a hovering pointer.</span></span>
-   <span data-ttu-id="bda1f-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica che questo puntatore è stato designato come primario.</span><span class="sxs-lookup"><span data-stu-id="bda1f-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indicates that this pointer has been designated as primary.</span></span>
-   <span data-ttu-id="bda1f-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se è presente un'azione primaria.</span><span class="sxs-lookup"><span data-stu-id="bda1f-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a primary action.</span></span>
    -   <span data-ttu-id="bda1f-125">Questo è analogo a un pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="bda1f-125">This is analogous to a mouse left button down.</span></span>
    -   <span data-ttu-id="bda1f-126">Il puntatore a tocco avrà questo set quando sarà in contatto con la superficie del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="bda1f-126">A touch pointer will have this set when it is in contact with the digitizer surface.</span></span>
    -   <span data-ttu-id="bda1f-127">Un puntatore della penna avrà questo set quando sarà in contatto con la superficie del digitalizzatore senza pulsanti premuti.</span><span class="sxs-lookup"><span data-stu-id="bda1f-127">A pen pointer will have this set when it is in contact with the digitizer surface with no buttons pressed.</span></span>
-   <span data-ttu-id="bda1f-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se è presente un'azione secondaria.</span><span class="sxs-lookup"><span data-stu-id="bda1f-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a secondary action.</span></span>
    -   <span data-ttu-id="bda1f-129">Questo è analogo al pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="bda1f-129">This is analogous to a mouse right button down.</span></span>
    -   <span data-ttu-id="bda1f-130">Il puntatore della penna avrà questo set quando sarà in contatto con la superficie del digitalizzatore con il pulsante della penna premuto.</span><span class="sxs-lookup"><span data-stu-id="bda1f-130">A pen pointer will have this set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>
-   <span data-ttu-id="bda1f-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se sono presenti una o più azioni terziarie basate sul tipo di puntatore. le applicazioni che vogliono rispondere a azioni terziarie devono recuperare informazioni specifiche per il tipo di puntatore per determinare quali pulsanti di terziaria vengono premuti.</span><span class="sxs-lookup"><span data-stu-id="bda1f-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there are one or more tertiary actions based on the pointer type; applications that wish to respond to tertiary actions must retrieve information specific to the pointer type to determine which tertiary buttons are pressed.</span></span> <span data-ttu-id="bda1f-132">Ad esempio, un'applicazione può determinare lo stato dei pulsanti di una penna chiamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) ed esaminando i flag che specificano gli Stati dei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="bda1f-132">For example, an application can determine the buttons states of a pen by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>
-   <span data-ttu-id="bda1f-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il puntatore specificato ha avuto una quarta azione.</span><span class="sxs-lookup"><span data-stu-id="bda1f-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether the specified pointer took fourth action.</span></span> <span data-ttu-id="bda1f-134">Le applicazioni che vogliono rispondere a quattro azioni devono recuperare informazioni specifiche del tipo di puntatore per determinare se viene premuto il primo pulsante del mouse esteso (XButton1).</span><span class="sxs-lookup"><span data-stu-id="bda1f-134">Applications that wish to respond to fourth actions must retrieve information specific to the pointer type to determine if the first extended mouse (XButton1) button is pressed.</span></span>
-   <span data-ttu-id="bda1f-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): [**flag**](pointer-flags-contants.md) che indica se il puntatore specificato ha avuto una quinta azione.</span><span class="sxs-lookup"><span data-stu-id="bda1f-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a [**flag**](pointer-flags-contants.md) that indicates whether the specified pointer took fifth action.</span></span> <span data-ttu-id="bda1f-136">Le applicazioni che vogliono rispondere a quinte azioni devono recuperare informazioni specifiche del tipo di puntatore per determinare se viene premuto il secondo pulsante del mouse esteso (XButton2).</span><span class="sxs-lookup"><span data-stu-id="bda1f-136">Applications that wish to respond to fifth actions must retrieve information specific to the pointer type to determine if the second extended mouse (XButton2) button is pressed.</span></span>

    <span data-ttu-id="bda1f-137">Per altri dettagli, vedere [**flag puntatore**](pointer-flags-contants.md) .</span><span class="sxs-lookup"><span data-stu-id="bda1f-137">See [**Pointer Flags**](pointer-flags-contants.md) for more details.</span></span>

    > [!Note]  
    > <span data-ttu-id="bda1f-138">Un puntatore al passaggio del mouse non ha alcun flag dei pulsanti impostato.</span><span class="sxs-lookup"><span data-stu-id="bda1f-138">A hovering pointer has none of the button flags set.</span></span> <span data-ttu-id="bda1f-139">Questa operazione è analoga a uno spostamento del mouse senza pulsanti del mouse.</span><span class="sxs-lookup"><span data-stu-id="bda1f-139">This is analogous to a mouse move with no mouse buttons down.</span></span> <span data-ttu-id="bda1f-140">Un'applicazione può determinare lo stato dei pulsanti di una penna in sospeso, ad esempio chiamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) ed esaminando i flag che specificano gli Stati dei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="bda1f-140">An application can determine the buttons states of a hovering pen, for example, by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>

     

</dd> <dt>

<span data-ttu-id="bda1f-141">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bda1f-141">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bda1f-142">Contiene la posizione del punto del puntatore.</span><span class="sxs-lookup"><span data-stu-id="bda1f-142">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="bda1f-143">Poiché il puntatore può rendere il contatto con il dispositivo su un'area non banale, questa posizione del punto può essere una semplificazione di un'area del puntatore più complessa.</span><span class="sxs-lookup"><span data-stu-id="bda1f-143">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="bda1f-144">Laddove possibile, un'applicazione deve usare le informazioni complete sull'area del puntatore anziché la posizione del punto.</span><span class="sxs-lookup"><span data-stu-id="bda1f-144">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="bda1f-145">Utilizzare le macro seguenti per recuperare le coordinate dello schermo fisico del punto.</span><span class="sxs-lookup"><span data-stu-id="bda1f-145">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="bda1f-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): coordinata X (punto orizzontale).</span><span class="sxs-lookup"><span data-stu-id="bda1f-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="bda1f-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordinata Y (punto verticale).</span><span class="sxs-lookup"><span data-stu-id="bda1f-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bda1f-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bda1f-148">Return value</span></span>

<span data-ttu-id="bda1f-149">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="bda1f-149">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="bda1f-150">Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="bda1f-150">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="bda1f-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="bda1f-151">Remarks</span></span>

> <span data-ttu-id="bda1f-152">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="bda1f-152">\[!Important\]</span></span>  
> <span data-ttu-id="bda1f-153">Quando una finestra perde l'acquisizione di un puntatore e riceve la notifica di [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , in genere non riceverà altre notifiche.</span><span class="sxs-lookup"><span data-stu-id="bda1f-153">When a window loses capture of a pointer and it receives the [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) notification, it typically will not receive any further notifications.</span></span> <span data-ttu-id="bda1f-154">Per questo motivo, è importante non prendere in considerazione le ipotesi basate su WM_POINTERDOWN abbinate in modo uniforme  / [**WM_POINTERUP**](wm-pointerup.md) o [**WM_POINTERENTER**](wm-pointerenter.md) / notifiche [**WM_POINTERLEAVE**](wm-pointerleave.md) .</span><span class="sxs-lookup"><span data-stu-id="bda1f-154">For this reason, it is important that you not make any assumptions based on evenly paired **WM_POINTERDOWN**/[**WM_POINTERUP**](wm-pointerup.md) or [**WM_POINTERENTER**](wm-pointerenter.md)/[**WM_POINTERLEAVE**](wm-pointerleave.md) notifications.</span></span>

 

<span data-ttu-id="bda1f-155">Ogni puntatore ha un identificatore univoco del puntatore durante la relativa durata.</span><span class="sxs-lookup"><span data-stu-id="bda1f-155">Each pointer has a unique pointer identifier during its lifetime.</span></span> <span data-ttu-id="bda1f-156">La durata di un puntatore inizia quando viene rilevata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="bda1f-156">The lifetime of a pointer begins when it is first detected.</span></span>

<span data-ttu-id="bda1f-157">Viene generato un messaggio [**WM_POINTERENTER**](wm-pointerenter.md) se viene rilevato un puntatore al passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="bda1f-157">A [**WM_POINTERENTER**](wm-pointerenter.md) message is generated if a hovering pointer is detected.</span></span> <span data-ttu-id="bda1f-158">Un messaggio di **WM_POINTERDOWN** seguito da un messaggio di **WM_POINTERENTER** viene generato se viene rilevato un puntatore senza passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="bda1f-158">A **WM_POINTERDOWN** message followed by a **WM_POINTERENTER** message is generated if a non-hovering pointer is detected.</span></span>

<span data-ttu-id="bda1f-159">Durante la sua durata, un puntatore può generare una serie di messaggi di [**WM_POINTERUPDATE**](wm-pointerupdate.md) mentre è in corso il passaggio del mouse o il contatto.</span><span class="sxs-lookup"><span data-stu-id="bda1f-159">During its lifetime, a pointer may generate a series of [**WM_POINTERUPDATE**](wm-pointerupdate.md) messages while it is hovering or in contact.</span></span>

<span data-ttu-id="bda1f-160">La durata di un puntatore termina quando non viene più rilevata.</span><span class="sxs-lookup"><span data-stu-id="bda1f-160">The lifetime of a pointer ends when it is no longer detected.</span></span> <span data-ttu-id="bda1f-161">Viene generato un messaggio di [**WM_POINTERLEAVE**](wm-pointerleave.md) .</span><span class="sxs-lookup"><span data-stu-id="bda1f-161">This generates a [**WM_POINTERLEAVE**](wm-pointerleave.md) message.</span></span>

<span data-ttu-id="bda1f-162">Quando un puntatore viene interrotto, viene impostato [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) .</span><span class="sxs-lookup"><span data-stu-id="bda1f-162">When a pointer is aborted, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) is set.</span></span>

<span data-ttu-id="bda1f-163">Un messaggio di [**WM_POINTERLEAVE**](wm-pointerleave.md) può essere generato anche quando un puntatore non acquisito si sposta all'esterno dei limiti di una finestra.</span><span class="sxs-lookup"><span data-stu-id="bda1f-163">A [**WM_POINTERLEAVE**](wm-pointerleave.md) message may also be generated when a non-captured pointer moves outside the bounds of a window.</span></span>

<span data-ttu-id="bda1f-164">Per ottenere la posizione orizzontale e verticale di un puntatore, utilizzare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="bda1f-164">To obtain the horizontal and vertical position of a pointer, use the following:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="bda1f-165">Per convertire il parametro lParam in una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) , usare la macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) .</span><span class="sxs-lookup"><span data-stu-id="bda1f-165">To convert the lParam parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure, use the [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro.</span></span>

<span data-ttu-id="bda1f-166">Per recuperare ulteriori informazioni associate al messaggio, utilizzare la funzione [**GetPointerInfo**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="bda1f-166">To retrieve further information associated with the message, use the [**GetPointerInfo**](/previous-versions/windows/desktop/api) function.</span></span>

<span data-ttu-id="bda1f-167">Per determinare gli Stati dei tasti di modifica della tastiera associati a questo messaggio, usare la funzione [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) .</span><span class="sxs-lookup"><span data-stu-id="bda1f-167">To determine the keyboard modifier key states associated with this message, use the [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) function.</span></span> <span data-ttu-id="bda1f-168">Ad esempio, per rilevare che è stato premuto il tasto ALT, controllare se GetKeyState (VK_MENU) &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="bda1f-168">For example, to detect that the ALT key was pressed, check whether GetKeyState(VK_MENU) &lt; 0.</span></span>

<span data-ttu-id="bda1f-169">Si noti che se l'applicazione non elabora questo messaggio, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) può generare uno o più messaggi di [**WM_GESTURE**](../wintouch/wm-gesture.md) se la sequenza di input da questo e, possibilmente, altri puntatori viene riconosciuta come un movimento.</span><span class="sxs-lookup"><span data-stu-id="bda1f-169">Note that if the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages if the sequence of input from this and, possibly, other pointers is recognized as a gesture.</span></span> <span data-ttu-id="bda1f-170">Se non viene riconosciuto un movimento, **DefWindowProc** potrebbe generare un input del mouse.</span><span class="sxs-lookup"><span data-stu-id="bda1f-170">If a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="bda1f-171">Se un'applicazione usa selettivamente un input del puntatore e passa il resto a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), il comportamento risultante non è definito.</span><span class="sxs-lookup"><span data-stu-id="bda1f-171">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

<span data-ttu-id="bda1f-172">Quando una finestra perde l'acquisizione di un puntatore e riceve la notifica di [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , in genere non riceverà altre notifiche.</span><span class="sxs-lookup"><span data-stu-id="bda1f-172">When a window loses capture of a pointer and receives the [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) notification, it will typically not receive any further notifications.</span></span> <span data-ttu-id="bda1f-173">Pertanto, è importante che una finestra non faccia supposizioni dello stato del puntatore, indipendentemente dal fatto che riceva le notifiche in modo uniforme o in uscita o in ingresso/uscita.</span><span class="sxs-lookup"><span data-stu-id="bda1f-173">Therefore, it is important that a window does not make any assumptions of its pointer status, regardless of whether it receives evenly paired DOWN / UP or ENTER / LEAVE notifications.</span></span>

## <a name="examples"></a><span data-ttu-id="bda1f-174">Esempio</span><span class="sxs-lookup"><span data-stu-id="bda1f-174">Examples</span></span>

<span data-ttu-id="bda1f-175">Nell'esempio di codice seguente viene illustrato come utilizzare [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)e [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)per recuperare le informazioni rilevanti associate al messaggio **WM_POINTERDOWN** .</span><span class="sxs-lookup"><span data-stu-id="bda1f-175">The following code example shows how to use [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), and [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)to retrieve the relevant information associated with the **WM_POINTERDOWN** message.</span></span>


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

if (IS_POINTER_PRIMARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse left button down
}
else if (IS_POINTER_SECONDARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse right button down
}
```



<span data-ttu-id="bda1f-176">Nell'esempio di codice seguente viene illustrato come utilizzare [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) per recuperare l'ID del puntatore dal messaggio di **WM_POINTERDOWN** .</span><span class="sxs-lookup"><span data-stu-id="bda1f-176">The following code example shows how to use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to retrieve the pointer id from the **WM_POINTERDOWN** message.</span></span>


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &amp;pointerInfo))
{
    // failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}
```



<span data-ttu-id="bda1f-177">Nell'esempio di codice seguente viene illustrato come gestire tipi di puntatore diversi, ad esempio touch, Pen o dispositivi di puntamento predefiniti.</span><span class="sxs-lookup"><span data-stu-id="bda1f-177">The following code example shows how to handle different pointer type such as touch, pen, or default pointing devices.</span></span>


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO         pointerInfo;
UINT32               pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE         pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &amp;pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &amp;touchInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process touchInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
case PT_PEN:
    // Retrieve pen information
    if (!GetPointerPenInfo(pointerId, &amp;penInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process penInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
default:
    if (!GetPointerInfo(pointerId, &amp;pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&amp;pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a><span data-ttu-id="bda1f-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bda1f-178">Requirements</span></span>



| <span data-ttu-id="bda1f-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="bda1f-179">Requirement</span></span> | <span data-ttu-id="bda1f-180">Valore</span><span class="sxs-lookup"><span data-stu-id="bda1f-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bda1f-181">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bda1f-181">Minimum supported client</span></span><br/> | <span data-ttu-id="bda1f-182">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bda1f-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="bda1f-183">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bda1f-183">Minimum supported server</span></span><br/> | <span data-ttu-id="bda1f-184">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bda1f-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bda1f-185">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bda1f-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="bda1f-186"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bda1f-186"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bda1f-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bda1f-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bda1f-188">Messaggi</span><span class="sxs-lookup"><span data-stu-id="bda1f-188">Messages</span></span>](messages.md)
</dt> <dt>

<span data-ttu-id="bda1f-189">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="bda1f-189">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bda1f-190">**Flag puntatore**</span><span class="sxs-lookup"><span data-stu-id="bda1f-190">**Pointer Flags**</span></span>](pointer-flags-contants.md)
</dt> <dt>

[<span data-ttu-id="bda1f-191">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bda1f-191">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bda1f-192">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bda1f-192">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bda1f-193">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bda1f-193">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bda1f-194">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bda1f-194">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bda1f-195">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bda1f-195">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bda1f-196">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bda1f-196">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bda1f-197">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bda1f-197">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bda1f-198">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bda1f-198">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bda1f-199">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bda1f-199">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bda1f-200">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bda1f-200">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

