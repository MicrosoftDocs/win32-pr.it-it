---
Description: Il \_ messaggio di disegno WM viene inviato quando il sistema o un'altra applicazione esegue una richiesta per disegnare una parte della finestra di un'applicazione.
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: Messaggio WM_PAINT (winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b13e1779fb54a3db7905cb8fc738ef45558400f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982955"
---
# <a name="wm_paint-message"></a><span data-ttu-id="5e778-103">\_Messaggio di disegno WM</span><span class="sxs-lookup"><span data-stu-id="5e778-103">WM\_PAINT message</span></span>

<span data-ttu-id="5e778-104">Il messaggio di **\_ disegno WM** viene inviato quando il sistema o un'altra applicazione esegue una richiesta per disegnare una parte della finestra di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5e778-104">The **WM\_PAINT** message is sent when the system or another application makes a request to paint a portion of an application's window.</span></span> <span data-ttu-id="5e778-105">Il messaggio viene inviato quando viene chiamata la funzione [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) o [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) oppure tramite la funzione [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) quando l'applicazione ottiene un messaggio di **\_ disegno WM** utilizzando la funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="5e778-105">The message is sent when the [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) or [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) function is called, or by the [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) function when the application obtains a **WM\_PAINT** message by using the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span>

<span data-ttu-id="5e778-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5e778-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="5e778-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e778-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e778-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e778-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e778-109">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="5e778-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5e778-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e778-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e778-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="5e778-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e778-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e778-112">Return value</span></span>

<span data-ttu-id="5e778-113">Un'applicazione restituisce zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="5e778-113">An application returns zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="5e778-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="5e778-114">Example</span></span>

```c
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);

            // All painting occurs here, between BeginPaint and EndPaint.
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(hwnd, &ps);
        }
        return 0;
    }

    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}

```

<span data-ttu-id="5e778-115">Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="5e778-115">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e778-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e778-116">Remarks</span></span>

<span data-ttu-id="5e778-117">Il messaggio di **\_ disegno WM** viene generato dal sistema e non deve essere inviato da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5e778-117">The **WM\_PAINT** message is generated by the system and should not be sent by an application.</span></span> <span data-ttu-id="5e778-118">Per forzare una finestra a creare un contesto di dispositivo specifico, usare il messaggio [**WM \_ Print**](wm-print.md) o [**WM \_ PRINTCLIENT**](wm-printclient.md) .</span><span class="sxs-lookup"><span data-stu-id="5e778-118">To force a window to draw into a specific device context, use the [**WM\_PRINT**](wm-print.md) or [**WM\_PRINTCLIENT**](wm-printclient.md) message.</span></span> <span data-ttu-id="5e778-119">Si noti che questa operazione richiede che la finestra di destinazione supporti il messaggio **WM \_ PRINTCLIENT** .</span><span class="sxs-lookup"><span data-stu-id="5e778-119">Note that this requires the target window to support the **WM\_PRINTCLIENT** message.</span></span> <span data-ttu-id="5e778-120">I controlli più comuni supportano il messaggio **WM \_ PRINTCLIENT** .</span><span class="sxs-lookup"><span data-stu-id="5e778-120">Most common controls support the **WM\_PRINTCLIENT** message.</span></span>

<span data-ttu-id="5e778-121">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  convalida l'area di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5e778-121">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function validates the update region.</span></span> <span data-ttu-id="5e778-122">La funzione può anche inviare il messaggio [**WM \_ NCPAINT**](wm-ncpaint.md) alla routine della finestra se è necessario disegnare la cornice della finestra e inviare il messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) se lo sfondo della finestra deve essere cancellato.</span><span class="sxs-lookup"><span data-stu-id="5e778-122">The function may also send the [**WM\_NCPAINT**](wm-ncpaint.md) message to the window procedure if the window frame must be painted and send the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message if the window background must be erased.</span></span>

<span data-ttu-id="5e778-123">Il sistema invia questo messaggio quando non sono presenti altri messaggi nella coda di messaggi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5e778-123">The system sends this message when there are no other messages in the application's message queue.</span></span> <span data-ttu-id="5e778-124">[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) determina la posizione in cui inviare il messaggio. [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) determina il messaggio da inviare.</span><span class="sxs-lookup"><span data-stu-id="5e778-124">[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) determines where to send the message; [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) determines which message to dispatch.</span></span> <span data-ttu-id="5e778-125">**GetMessage** restituisce il messaggio di **\_ disegno WM** quando non sono presenti altri messaggi nella coda di messaggi dell'applicazione e **DispatchMessage** invia il messaggio alla routine della finestra appropriata.</span><span class="sxs-lookup"><span data-stu-id="5e778-125">**GetMessage** returns the **WM\_PAINT** message when there are no other messages in the application's message queue, and **DispatchMessage** sends the message to the appropriate window procedure.</span></span>

<span data-ttu-id="5e778-126">Una finestra può ricevere messaggi di disegno interni in seguito alla chiamata di [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con il \_ flag RDW INTERNALPAINT impostato.</span><span class="sxs-lookup"><span data-stu-id="5e778-126">A window may receive internal paint messages as a result of calling [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the RDW\_INTERNALPAINT flag set.</span></span> <span data-ttu-id="5e778-127">In questo caso, è possibile che la finestra non disponga di un'area di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5e778-127">In this case, the window may not have an update region.</span></span> <span data-ttu-id="5e778-128">Un'applicazione può chiamare la funzione [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) per determinare se la finestra dispone di un'area di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5e778-128">An application may call the [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) function to determine whether the window has an update region.</span></span> <span data-ttu-id="5e778-129">Se **GetUpdateRect** restituisce zero, l'applicazione non deve chiamare le funzioni [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="5e778-129">If **GetUpdateRect** returns zero, the application need not call the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) functions.</span></span>

<span data-ttu-id="5e778-130">Un'applicazione deve verificare la presenza di un disegno interno necessario esaminando le strutture di dati interne per ogni messaggio di **\_ disegno WM** , perché un messaggio di **\_ disegno WM** potrebbe essere stato causato da un'area di aggiornamento non null e da una chiamata a [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con il \_ flag RDW INTERNALPAINT impostato.</span><span class="sxs-lookup"><span data-stu-id="5e778-130">An application must check for any necessary internal painting by looking at its internal data structures for each **WM\_PAINT** message, because a **WM\_PAINT** message may have been caused by both a non-NULL update region and a call to [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the RDW\_INTERNALPAINT flag set.</span></span>

<span data-ttu-id="5e778-131">Il sistema invia un messaggio **di \_ disegno WM** interno una sola volta.</span><span class="sxs-lookup"><span data-stu-id="5e778-131">The system sends an internal **WM\_PAINT** message only once.</span></span> <span data-ttu-id="5e778-132">Dopo che un messaggio di **\_ disegno WM** interno viene restituito da [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) o viene inviato a una finestra da [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), il sistema non pubblica o invia ulteriori messaggi di **\_ disegno WM** fino a quando la finestra non viene invalidata o fino a quando [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) viene richiamato con il \_ flag RDW INTERNALPAINT impostato.</span><span class="sxs-lookup"><span data-stu-id="5e778-132">After an internal **WM\_PAINT** message is returned from [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) or is sent to a window by [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), the system does not post or send further **WM\_PAINT** messages until the window is invalidated or until [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) is called again with the RDW\_INTERNALPAINT flag set.</span></span>

<span data-ttu-id="5e778-133">Per alcuni controlli comuni, l'elaborazione predefinita del messaggio di **\_ disegno WM** controlla il parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="5e778-133">For some common controls, the default **WM\_PAINT** message processing checks the *wParam* parameter.</span></span> <span data-ttu-id="5e778-134">Se *wParam* è diverso da null, il controllo presuppone che il valore sia un HDC e i colori che usano tale contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e778-134">If *wParam* is non-NULL, the control assumes that the value is an HDC and paints using that device context.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e778-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e778-135">Requirements</span></span>



| <span data-ttu-id="5e778-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e778-136">Requirement</span></span> | <span data-ttu-id="5e778-137">Valore</span><span class="sxs-lookup"><span data-stu-id="5e778-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e778-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e778-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5e778-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e778-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5e778-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e778-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5e778-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e778-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5e778-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e778-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e778-143"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e778-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e778-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e778-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e778-145">Cenni preliminari su disegno e disegno</span><span class="sxs-lookup"><span data-stu-id="5e778-145">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="5e778-146">Disegno e creazione di messaggi</span><span class="sxs-lookup"><span data-stu-id="5e778-146">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="5e778-147">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="5e778-147">**BeginPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="5e778-148">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="5e778-148">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="5e778-149">**DispatchMessage**</span><span class="sxs-lookup"><span data-stu-id="5e778-149">**DispatchMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-dispatchmessage)
</dt> <dt>

[<span data-ttu-id="5e778-150">**EndPaint**</span><span class="sxs-lookup"><span data-stu-id="5e778-150">**EndPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[<span data-ttu-id="5e778-151">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="5e778-151">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="5e778-152">**GetUpdateRect**</span><span class="sxs-lookup"><span data-stu-id="5e778-152">**GetUpdateRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)
</dt> <dt>

[<span data-ttu-id="5e778-153">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="5e778-153">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="5e778-154">**RedrawWindow**</span><span class="sxs-lookup"><span data-stu-id="5e778-154">**RedrawWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[<span data-ttu-id="5e778-155">**UpdateWindow**</span><span class="sxs-lookup"><span data-stu-id="5e778-155">**UpdateWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[<span data-ttu-id="5e778-156">**\_ERASEBKGND WM**</span><span class="sxs-lookup"><span data-stu-id="5e778-156">**WM\_ERASEBKGND**</span></span>](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[<span data-ttu-id="5e778-157">**\_NCPAINT WM**</span><span class="sxs-lookup"><span data-stu-id="5e778-157">**WM\_NCPAINT**</span></span>](wm-ncpaint.md)
</dt> <dt>

[<span data-ttu-id="5e778-158">**\_stampa WM**</span><span class="sxs-lookup"><span data-stu-id="5e778-158">**WM\_PRINT**</span></span>](wm-print.md)
</dt> <dt>

[<span data-ttu-id="5e778-159">**\_PRINTCLIENT WM**</span><span class="sxs-lookup"><span data-stu-id="5e778-159">**WM\_PRINTCLIENT**</span></span>](wm-printclient.md)
</dt> </dl>

 

 
