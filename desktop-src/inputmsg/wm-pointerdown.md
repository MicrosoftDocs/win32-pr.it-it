---
title: WM_POINTERDOWN messaggio
description: Pubblicato quando un puntatore contatta l'area client di una finestra.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac000
keywords:
- WM_POINTERDOWN messaggi di input e notifiche
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
ms.openlocfilehash: 9f94bf4474e208d0b1d29df7a5e2939d7826ca77
ms.sourcegitcommit: 1f917afc149b5cc449a4a25a87de311e4842734b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2021
ms.locfileid: "113689204"
---
# <a name="wm_pointerdown-message"></a><span data-ttu-id="49640-104">WM_POINTERDOWN messaggio</span><span class="sxs-lookup"><span data-stu-id="49640-104">WM_POINTERDOWN message</span></span>

<span data-ttu-id="49640-105">Pubblicato quando un puntatore contatta l'area client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="49640-105">Posted when a pointer makes contact over the client area of a window.</span></span> <span data-ttu-id="49640-106">Questo messaggio di input è destinato alla finestra sulla quale il puntatore contatta e il puntatore viene acquisito in modo implicito nella finestra in modo che la finestra continui a ricevere input per il puntatore fino a quando non interrompe il contatto.</span><span class="sxs-lookup"><span data-stu-id="49640-106">This input message targets the window over which the pointer makes contact, and the pointer is implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact.</span></span>

<span data-ttu-id="49640-107">Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="49640-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="49640-108">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="49640-108">\[!Important\]</span></span>  
> <span data-ttu-id="49640-109">Le app desktop devono essere in grado di riconoscere DPI.</span><span class="sxs-lookup"><span data-stu-id="49640-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="49640-110">Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi del puntatore e nelle strutture correlate potrebbero apparire inesatte a causa della virtualizzazione DPI.</span><span class="sxs-lookup"><span data-stu-id="49640-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="49640-111">La virtualizzazione DPI offre il supporto automatico del ridimensionamento per le applicazioni che non supportano DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla).</span><span class="sxs-lookup"><span data-stu-id="49640-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="49640-112">Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="49640-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDOWN                   0x0246
```



## <a name="parameters"></a><span data-ttu-id="49640-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="49640-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49640-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49640-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49640-115">Contiene informazioni sul puntatore.</span><span class="sxs-lookup"><span data-stu-id="49640-115">Contains information about the pointer.</span></span> <span data-ttu-id="49640-116">Usare le macro seguenti per recuperare informazioni dal parametro wParam.</span><span class="sxs-lookup"><span data-stu-id="49640-116">Use the following macros to retrieve information from the wParam parameter.</span></span>

-   <span data-ttu-id="49640-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore.</span><span class="sxs-lookup"><span data-stu-id="49640-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): the pointer identifier.</span></span>
-   <span data-ttu-id="49640-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se questo messaggio rappresenta il primo input generato da un nuovo puntatore.</span><span class="sxs-lookup"><span data-stu-id="49640-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message represents the first input generated by a new pointer.</span></span>
-   <span data-ttu-id="49640-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il messaggio è stato generato da un puntatore durante la relativa durata.</span><span class="sxs-lookup"><span data-stu-id="49640-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer during its lifetime.</span></span> <span data-ttu-id="49640-120">Questo flag non è impostato sui messaggi che indicano che il puntatore ha un intervallo di rilevamento a sinistra</span><span class="sxs-lookup"><span data-stu-id="49640-120">This flag is not set on messages that indicate that the pointer has left detection range</span></span>
-   <span data-ttu-id="49640-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il messaggio è stato generato da un puntatore in contatto con la superficie della finestra.</span><span class="sxs-lookup"><span data-stu-id="49640-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer that is in contact with the window surface.</span></span> <span data-ttu-id="49640-122">Questo flag non è impostato sui messaggi che indicano un puntatore al passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="49640-122">This flag is not set on messages that indicate a hovering pointer.</span></span>
-   <span data-ttu-id="49640-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica che questo puntatore è stato designato come primario.</span><span class="sxs-lookup"><span data-stu-id="49640-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indicates that this pointer has been designated as primary.</span></span>
-   <span data-ttu-id="49640-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se è presente un'azione primaria.</span><span class="sxs-lookup"><span data-stu-id="49640-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a primary action.</span></span>
    -   <span data-ttu-id="49640-125">Questo è analogo a un pulsante sinistro del mouse verso il basso.</span><span class="sxs-lookup"><span data-stu-id="49640-125">This is analogous to a mouse left button down.</span></span>
    -   <span data-ttu-id="49640-126">Un puntatore tocco avrà questo set quando è in contatto con la superficie del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="49640-126">A touch pointer will have this set when it is in contact with the digitizer surface.</span></span>
    -   <span data-ttu-id="49640-127">Un puntatore a penna avrà questo set quando è in contatto con la superficie del digitalizzatore senza pulsanti premuti.</span><span class="sxs-lookup"><span data-stu-id="49640-127">A pen pointer will have this set when it is in contact with the digitizer surface with no buttons pressed.</span></span>
-   <span data-ttu-id="49640-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se è presente un'azione secondaria.</span><span class="sxs-lookup"><span data-stu-id="49640-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a secondary action.</span></span>
    -   <span data-ttu-id="49640-129">Questo è analogo a un pulsante destro del mouse verso il basso.</span><span class="sxs-lookup"><span data-stu-id="49640-129">This is analogous to a mouse right button down.</span></span>
    -   <span data-ttu-id="49640-130">Un puntatore a penna avrà questo set quando è in contatto con la superficie del digitalizzatore con il pulsante pentola premuto.</span><span class="sxs-lookup"><span data-stu-id="49640-130">A pen pointer will have this set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>
-   <span data-ttu-id="49640-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se sono presenti una o più azioni terziarie in base al tipo di puntatore. Le applicazioni che vogliono rispondere alle azioni terziarie devono recuperare informazioni specifiche per il tipo di puntatore per determinare quali pulsanti terziari vengono premuti.</span><span class="sxs-lookup"><span data-stu-id="49640-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there are one or more tertiary actions based on the pointer type; applications that wish to respond to tertiary actions must retrieve information specific to the pointer type to determine which tertiary buttons are pressed.</span></span> <span data-ttu-id="49640-132">Ad esempio, un'applicazione può determinare gli stati dei pulsanti di una penna chiamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) ed esaminando i flag che specificano gli stati del pulsante.</span><span class="sxs-lookup"><span data-stu-id="49640-132">For example, an application can determine the buttons states of a pen by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>
-   <span data-ttu-id="49640-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag che indica se il puntatore specificato ha preso la quarta azione.</span><span class="sxs-lookup"><span data-stu-id="49640-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether the specified pointer took fourth action.</span></span> <span data-ttu-id="49640-134">Le applicazioni che vogliono rispondere a quarta azione devono recuperare informazioni specifiche per il tipo di puntatore per determinare se viene premuto il primo pulsante del mouse esteso (XButton1).</span><span class="sxs-lookup"><span data-stu-id="49640-134">Applications that wish to respond to fourth actions must retrieve information specific to the pointer type to determine if the first extended mouse (XButton1) button is pressed.</span></span>
-   <span data-ttu-id="49640-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): flag [**che**](pointer-flags-contants.md) indica se il puntatore specificato ha preso la quinta azione.</span><span class="sxs-lookup"><span data-stu-id="49640-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a [**flag**](pointer-flags-contants.md) that indicates whether the specified pointer took fifth action.</span></span> <span data-ttu-id="49640-136">Le applicazioni che vogliono rispondere a quinta azione devono recuperare informazioni specifiche per il tipo di puntatore per determinare se viene premuto il secondo pulsante del mouse esteso (XButton2).</span><span class="sxs-lookup"><span data-stu-id="49640-136">Applications that wish to respond to fifth actions must retrieve information specific to the pointer type to determine if the second extended mouse (XButton2) button is pressed.</span></span>

    <span data-ttu-id="49640-137">Per [**altri dettagli, vedere Flag**](pointer-flags-contants.md) puntatore.</span><span class="sxs-lookup"><span data-stu-id="49640-137">See [**Pointer Flags**](pointer-flags-contants.md) for more details.</span></span>

    > [!Note]  
    > <span data-ttu-id="49640-138">Per un puntatore al passaggio del mouse non è impostato nessuno dei flag del pulsante.</span><span class="sxs-lookup"><span data-stu-id="49640-138">A hovering pointer has none of the button flags set.</span></span> <span data-ttu-id="49640-139">Questo è analogo a uno spostamento del mouse senza pulsanti del mouse verso il basso.</span><span class="sxs-lookup"><span data-stu-id="49640-139">This is analogous to a mouse move with no mouse buttons down.</span></span> <span data-ttu-id="49640-140">Un'applicazione può determinare gli stati dei pulsanti di una penna al passaggio del mouse, ad esempio chiamando [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) ed esaminando i flag che specificano gli stati del pulsante.</span><span class="sxs-lookup"><span data-stu-id="49640-140">An application can determine the buttons states of a hovering pen, for example, by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>

     

</dd> <dt>

<span data-ttu-id="49640-141">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49640-141">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49640-142">Contiene la posizione del punto del puntatore.</span><span class="sxs-lookup"><span data-stu-id="49640-142">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="49640-143">Poiché il puntatore può contattare il dispositivo su un'area non semplice, questa posizione del punto può essere una semplificazione di un'area del puntatore più complessa.</span><span class="sxs-lookup"><span data-stu-id="49640-143">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="49640-144">Quando possibile, un'applicazione deve usare le informazioni complete sull'area del puntatore anziché la posizione del punto.</span><span class="sxs-lookup"><span data-stu-id="49640-144">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="49640-145">Usare le macro seguenti per recuperare le coordinate fisiche dello schermo del punto.</span><span class="sxs-lookup"><span data-stu-id="49640-145">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="49640-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): coordinata x (punto orizzontale).</span><span class="sxs-lookup"><span data-stu-id="49640-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="49640-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordinata y (punto verticale).</span><span class="sxs-lookup"><span data-stu-id="49640-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49640-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49640-148">Return value</span></span>

<span data-ttu-id="49640-149">Se un'applicazione elabora questo messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="49640-149">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="49640-150">Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="49640-150">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="49640-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="49640-151">Remarks</span></span>

> <span data-ttu-id="49640-152">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="49640-152">\[!Important\]</span></span>  
> <span data-ttu-id="49640-153">Quando una finestra perde l'acquisizione di [](wm-pointercapturechanged.md) un puntatore e riceve la notifica WM_POINTERCAPTURECHANGED, in genere non riceverà altre notifiche.</span><span class="sxs-lookup"><span data-stu-id="49640-153">When a window loses capture of a pointer and it receives the [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) notification, it typically will not receive any further notifications.</span></span> <span data-ttu-id="49640-154">Per questo motivo, è importante non fare ipotesi basate su notifiche di WM_POINTERDOWN WM_POINTERUP o WM_POINTERENTER / [](wm-pointerup.md) [](wm-pointerenter.md) / [**WM_POINTERLEAVE**](wm-pointerleave.md) uniforme.</span><span class="sxs-lookup"><span data-stu-id="49640-154">For this reason, it is important that you not make any assumptions based on evenly paired **WM_POINTERDOWN**/[**WM_POINTERUP**](wm-pointerup.md) or [**WM_POINTERENTER**](wm-pointerenter.md)/[**WM_POINTERLEAVE**](wm-pointerleave.md) notifications.</span></span>

 

<span data-ttu-id="49640-155">Ogni puntatore ha un identificatore di puntatore univoco durante la sua durata.</span><span class="sxs-lookup"><span data-stu-id="49640-155">Each pointer has a unique pointer identifier during its lifetime.</span></span> <span data-ttu-id="49640-156">La durata di un puntatore inizia quando viene rilevato per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="49640-156">The lifetime of a pointer begins when it is first detected.</span></span>

<span data-ttu-id="49640-157">Se [**viene rilevato un puntatore**](wm-pointerenter.md) al passaggio del mouse, viene generato un messaggio WM_POINTERENTER messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="49640-157">A [**WM_POINTERENTER**](wm-pointerenter.md) message is generated if a hovering pointer is detected.</span></span> <span data-ttu-id="49640-158">Un **WM_POINTERDOWN** seguito da un messaggio WM_POINTERENTER **viene** generato se viene rilevato un puntatore non al passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="49640-158">A **WM_POINTERDOWN** message followed by a **WM_POINTERENTER** message is generated if a non-hovering pointer is detected.</span></span>

<span data-ttu-id="49640-159">Durante la durata, un puntatore può generare una serie di WM_POINTERUPDATE [**durante**](wm-pointerupdate.md) il passaggio del mouse o in contatto.</span><span class="sxs-lookup"><span data-stu-id="49640-159">During its lifetime, a pointer may generate a series of [**WM_POINTERUPDATE**](wm-pointerupdate.md) messages while it is hovering or in contact.</span></span>

<span data-ttu-id="49640-160">La durata di un puntatore termina quando non viene più rilevata.</span><span class="sxs-lookup"><span data-stu-id="49640-160">The lifetime of a pointer ends when it is no longer detected.</span></span> <span data-ttu-id="49640-161">Verrà generato un [**WM_POINTERLEAVE**](wm-pointerleave.md) messaggio.</span><span class="sxs-lookup"><span data-stu-id="49640-161">This generates a [**WM_POINTERLEAVE**](wm-pointerleave.md) message.</span></span>

<span data-ttu-id="49640-162">Quando un puntatore viene [**interrotto,**](pointer-flags-contants.md) POINTER_FLAG_CANCELED impostato.</span><span class="sxs-lookup"><span data-stu-id="49640-162">When a pointer is aborted, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) is set.</span></span>

<span data-ttu-id="49640-163">Un [**WM_POINTERLEAVE**](wm-pointerleave.md) può essere generato anche quando un puntatore non acquisito si sposta all'esterno dei limiti di una finestra.</span><span class="sxs-lookup"><span data-stu-id="49640-163">A [**WM_POINTERLEAVE**](wm-pointerleave.md) message may also be generated when a non-captured pointer moves outside the bounds of a window.</span></span>

<span data-ttu-id="49640-164">Per ottenere la posizione orizzontale e verticale di un puntatore, usare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="49640-164">To obtain the horizontal and vertical position of a pointer, use the following:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="49640-165">Per convertire il parametro lParam in una [**struttura POINTS,**](/previous-versions//dd162808(v=vs.85)) usare la macro [**MAKEPOINTS.**](/windows/win32/api/wingdi/nf-wingdi-makepoints)</span><span class="sxs-lookup"><span data-stu-id="49640-165">To convert the lParam parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure, use the [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro.</span></span>

<span data-ttu-id="49640-166">Per recuperare altre informazioni associate al messaggio, usare la [**funzione GetPointerInfo.**](/previous-versions/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="49640-166">To retrieve further information associated with the message, use the [**GetPointerInfo**](/previous-versions/windows/desktop/api) function.</span></span>

<span data-ttu-id="49640-167">Per determinare gli stati dei tasti di modifica della tastiera associati a questo messaggio, usare la [**funzione GetKeyState.**](/windows/win32/api/winuser/nf-winuser-getkeystate)</span><span class="sxs-lookup"><span data-stu-id="49640-167">To determine the keyboard modifier key states associated with this message, use the [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) function.</span></span> <span data-ttu-id="49640-168">Ad esempio, per rilevare che il tasto ALT è stato premuto, controllare se GetKeyState(VK_MENU) &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="49640-168">For example, to detect that the ALT key was pressed, check whether GetKeyState(VK_MENU) &lt; 0.</span></span>

<span data-ttu-id="49640-169">Si noti che se l'applicazione non elabora questo messaggio, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) può generare uno o più messaggi [**WM_GESTURE**](../wintouch/wm-gesture.md) se la sequenza di input da questo e, possibilmente, altri puntatori viene riconosciuta come movimento.</span><span class="sxs-lookup"><span data-stu-id="49640-169">Note that if the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages if the sequence of input from this and, possibly, other pointers is recognized as a gesture.</span></span> <span data-ttu-id="49640-170">Se un movimento non viene riconosciuto, **DefWindowProc** può generare l'input del mouse.</span><span class="sxs-lookup"><span data-stu-id="49640-170">If a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="49640-171">Se un'applicazione utilizza in modo selettivo un input del puntatore e passa il resto a [**DefWindowProc,**](/windows/win32/api/winuser/nf-winuser-defwindowproca)il comportamento risultante non è definito.</span><span class="sxs-lookup"><span data-stu-id="49640-171">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

<span data-ttu-id="49640-172">Quando una finestra perde l'acquisizione di [](wm-pointercapturechanged.md) un puntatore e riceve la notifica WM_POINTERCAPTURECHANGED, in genere non riceverà altre notifiche.</span><span class="sxs-lookup"><span data-stu-id="49640-172">When a window loses capture of a pointer and receives the [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) notification, it will typically not receive any further notifications.</span></span> <span data-ttu-id="49640-173">È quindi importante che una finestra non presunzioni lo stato del puntatore, indipendentemente dal fatto che riceva notifiche DOWN/UP o ENTER/LEAVE abbinate in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="49640-173">Therefore, it is important that a window does not make any assumptions of its pointer status, regardless of whether it receives evenly paired DOWN / UP or ENTER / LEAVE notifications.</span></span>

## <a name="examples"></a><span data-ttu-id="49640-174">Esempio</span><span class="sxs-lookup"><span data-stu-id="49640-174">Examples</span></span>

<span data-ttu-id="49640-175">Nell'esempio di codice seguente viene illustrato come usare IS_POINTER_FIRSTBUTTON_WPARAM [**,**](/previous-versions/windows/desktop/api) [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)e [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)per recuperare le informazioni rilevanti associate al messaggio **WM_POINTERDOWN.**</span><span class="sxs-lookup"><span data-stu-id="49640-175">The following code example shows how to use [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), and [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)to retrieve the relevant information associated with the **WM_POINTERDOWN** message.</span></span>


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



<span data-ttu-id="49640-176">L'esempio di codice seguente illustra come [**usare**](/previous-versions/windows/desktop/api) GET_POINTERID_WPARAM per recuperare l'ID puntatore **dal WM_POINTERDOWN** messaggio.</span><span class="sxs-lookup"><span data-stu-id="49640-176">The following code example shows how to use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to retrieve the pointer id from the **WM_POINTERDOWN** message.</span></span>


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &pointerInfo))
{
    // failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}
```



<span data-ttu-id="49640-177">L'esempio di codice seguente illustra come gestire diversi tipi di puntatore, ad esempio tocco, penna o dispositivi di puntamento predefiniti.</span><span class="sxs-lookup"><span data-stu-id="49640-177">The following code example shows how to handle different pointer type such as touch, pen, or default pointing devices.</span></span>


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO         pointerInfo;
UINT32               pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE         pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &touchInfo))
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
    if (!GetPointerPenInfo(pointerId, &penInfo))
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
    if (!GetPointerInfo(pointerId, &pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a><span data-ttu-id="49640-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49640-178">Requirements</span></span>



| <span data-ttu-id="49640-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="49640-179">Requirement</span></span> | <span data-ttu-id="49640-180">Valore</span><span class="sxs-lookup"><span data-stu-id="49640-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49640-181">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49640-181">Minimum supported client</span></span><br/> | <span data-ttu-id="49640-182">\[Windows 8 solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="49640-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="49640-183">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49640-183">Minimum supported server</span></span><br/> | <span data-ttu-id="49640-184">\[Windows Server 2012 solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="49640-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="49640-185">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49640-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="49640-186"><dt>Winuser.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="49640-186"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49640-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49640-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49640-188">Messaggi</span><span class="sxs-lookup"><span data-stu-id="49640-188">Messages</span></span>](messages.md)
</dt> <dt>

<span data-ttu-id="49640-189">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="49640-189">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="49640-190">**Flag puntatore**</span><span class="sxs-lookup"><span data-stu-id="49640-190">**Pointer Flags**</span></span>](pointer-flags-contants.md)
</dt> <dt>

[<span data-ttu-id="49640-191">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="49640-191">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="49640-192">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="49640-192">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="49640-193">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="49640-193">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="49640-194">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="49640-194">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="49640-195">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="49640-195">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="49640-196">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="49640-196">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="49640-197">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="49640-197">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="49640-198">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="49640-198">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="49640-199">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="49640-199">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="49640-200">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="49640-200">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>
