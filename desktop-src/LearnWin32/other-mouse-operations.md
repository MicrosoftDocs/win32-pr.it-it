---
title: Operazioni del mouse varie
description: Nelle sezioni precedenti sono stati discussi i clic del mouse e il movimento del mouse. Di seguito sono riportate alcune altre operazioni che possono essere eseguite con il mouse.
ms.assetid: 6A5B953F-7032-4AA6-8B64-2E9CBB8F59F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfba63dce8116d79a557cbbbf8895f17d2a8f1b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337383"
---
# <a name="miscellaneous-mouse-operations"></a><span data-ttu-id="9156a-104">Operazioni del mouse varie</span><span class="sxs-lookup"><span data-stu-id="9156a-104">Miscellaneous Mouse Operations</span></span>

<span data-ttu-id="9156a-105">Nelle sezioni precedenti sono stati discussi i clic del mouse e il movimento del mouse.</span><span class="sxs-lookup"><span data-stu-id="9156a-105">The previous sections have discussed mouse clicks and mouse movement.</span></span> <span data-ttu-id="9156a-106">Di seguito sono riportate alcune altre operazioni che possono essere eseguite con il mouse.</span><span class="sxs-lookup"><span data-stu-id="9156a-106">Here are some other operations that can be performed with the mouse.</span></span>

## <a name="dragging-ui-elements"></a><span data-ttu-id="9156a-107">Trascinamento di elementi dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9156a-107">Dragging UI Elements</span></span>

<span data-ttu-id="9156a-108">Se l'interfaccia utente supporta il trascinamento di elementi dell'interfaccia utente, è necessario chiamare un'altra funzione nel gestore di messaggi del mouse: [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect).</span><span class="sxs-lookup"><span data-stu-id="9156a-108">If your UI supports dragging of UI elements, there is one other function that you should call in your mouse-down message handler: [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect).</span></span> <span data-ttu-id="9156a-109">La funzione **DragDetect** restituisce **true** se l'utente avvia un movimento del mouse da interpretare come trascinamento.</span><span class="sxs-lookup"><span data-stu-id="9156a-109">The **DragDetect** function returns **TRUE** if the user initiates a mouse gesture that should be interpreted as dragging.</span></span> <span data-ttu-id="9156a-110">Il codice seguente illustra come usare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="9156a-110">The following code shows how to use this function.</span></span>


```C++
    case WM_LBUTTONDOWN: 
        {
            POINT pt = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam) };
            if (DragDetect(m_hwnd, pt))
            {
                // Start dragging.
            }
        }
        return 0;
```



<span data-ttu-id="9156a-111">Ecco l'idea: quando un programma supporta il trascinamento della selezione, non è necessario che ogni clic del mouse venga interpretato come un trascinamento.</span><span class="sxs-lookup"><span data-stu-id="9156a-111">Here's the idea: When a program supports drag and drop, you don't want every mouse click to be interpreted as a drag.</span></span> <span data-ttu-id="9156a-112">In caso contrario, l'utente potrebbe trascinare accidentalmente qualcosa quando ha semplicemente intenzione di fare clic su di esso, ad esempio per selezionarlo.</span><span class="sxs-lookup"><span data-stu-id="9156a-112">Otherwise, the user might accidentally drag something when he or she simply meant to click on it (for example, to select it).</span></span> <span data-ttu-id="9156a-113">Tuttavia, se il mouse è particolarmente sensibile, può essere difficile mantenere il mouse ancora in modo ottimale quando si fa clic.</span><span class="sxs-lookup"><span data-stu-id="9156a-113">But if a mouse is particularly sensitive, it can be hard to keep the mouse perfectly still while clicking.</span></span> <span data-ttu-id="9156a-114">Windows definisce pertanto una soglia di trascinamento di pochi pixel.</span><span class="sxs-lookup"><span data-stu-id="9156a-114">Therefore, Windows defines a drag threshold of a few pixels.</span></span> <span data-ttu-id="9156a-115">Quando l'utente preme il pulsante del mouse, non viene considerato un trascinamento, a meno che il mouse non superi questa soglia.</span><span class="sxs-lookup"><span data-stu-id="9156a-115">When the user presses the mouse button, it is not considered a drag unless the mouse crosses this threshold.</span></span> <span data-ttu-id="9156a-116">La funzione [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) verifica se questa soglia viene raggiunta.</span><span class="sxs-lookup"><span data-stu-id="9156a-116">The [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function tests whether this threshold is reached.</span></span> <span data-ttu-id="9156a-117">Se la funzione restituisce **true**, è possibile interpretare il clic del mouse come un trascinamento.</span><span class="sxs-lookup"><span data-stu-id="9156a-117">If the function returns **TRUE**, you can interpret the mouse click as a drag.</span></span> <span data-ttu-id="9156a-118">In caso contrario, non.</span><span class="sxs-lookup"><span data-stu-id="9156a-118">Otherwise, do not.</span></span>

> [!Note]  
> <span data-ttu-id="9156a-119">Se [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) restituisce **false**, Windows elimina il messaggio [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) quando l'utente rilascia il pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="9156a-119">If [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) returns **FALSE**, Windows suppresses the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message when the user releases the mouse button.</span></span> <span data-ttu-id="9156a-120">Pertanto, non chiamare **DragDetect** , a meno che il programma non sia attualmente in una modalità che supporta il trascinamento.</span><span class="sxs-lookup"><span data-stu-id="9156a-120">Therefore, do not call **DragDetect** unless your program is currently in a mode that supports dragging.</span></span> <span data-ttu-id="9156a-121">Se, ad esempio, un elemento dell'interfaccia utente trascinabile è già selezionato. Alla fine di questo modulo, verrà visualizzato un esempio di codice più lungo che usa la funzione **DragDetect** .</span><span class="sxs-lookup"><span data-stu-id="9156a-121">(For example, if a draggable UI element is already selected.) At the end of this module, we will see a longer code example that uses the **DragDetect** function.</span></span>

 

## <a name="confining-the-cursor"></a><span data-ttu-id="9156a-122">Limitazione del cursore</span><span class="sxs-lookup"><span data-stu-id="9156a-122">Confining the Cursor</span></span>

<span data-ttu-id="9156a-123">In alcuni casi potrebbe essere necessario limitare il cursore all'area client o a una parte dell'area client.</span><span class="sxs-lookup"><span data-stu-id="9156a-123">Sometimes you might want to restrict the cursor to the client area or a portion of the client area.</span></span> <span data-ttu-id="9156a-124">La funzione [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) limita lo spostamento del cursore a un rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="9156a-124">The [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) function restricts the movement of the cursor to a specified rectangle.</span></span> <span data-ttu-id="9156a-125">Questo rettangolo viene specificato nelle coordinate dello schermo, anziché nelle coordinate client, quindi il punto (0, 0) indica l'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="9156a-125">This rectangle is given in screen coordinates, rather than client coordinates, so the point (0, 0) means the upper left corner of the screen.</span></span> <span data-ttu-id="9156a-126">Per tradurre le coordinate client nelle coordinate dello schermo, chiamare la funzione [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).</span><span class="sxs-lookup"><span data-stu-id="9156a-126">To translate client coordinates into screen coordinates, call the function [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).</span></span>

<span data-ttu-id="9156a-127">Il codice seguente consente di limitare il cursore all'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="9156a-127">The following code confines the cursor to the client area of the window.</span></span>


```C++
    // Get the window client area.
    RECT rc;
    GetClientRect(m_hwnd, &rc);

    // Convert the client area to screen coordinates.
    POINT pt = { rc.left, rc.top };
    POINT pt2 = { rc.right, rc.bottom };
    ClientToScreen(m_hwnd, &pt);
    ClientToScreen(m_hwnd, &pt2);
    SetRect(&rc, pt.x, pt.y, pt2.x, pt2.y);

    // Confine the cursor.
    ClipCursor(&rc);
```



<span data-ttu-id="9156a-128">[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) accetta una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) , ma [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) accetta una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9156a-128">[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) takes a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure, but [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) takes a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <span data-ttu-id="9156a-129">Un rettangolo viene definito dai punti superiore sinistro e inferiore destro.</span><span class="sxs-lookup"><span data-stu-id="9156a-129">A rectangle is defined by its top-left and bottom-right points.</span></span> <span data-ttu-id="9156a-130">È possibile limitare il cursore a qualsiasi area rettangolare, incluse le aree all'esterno della finestra, ma la limitazione del cursore all'area client è un modo tipico per usare la funzione.</span><span class="sxs-lookup"><span data-stu-id="9156a-130">You can confine the cursor to any rectangular area, including areas outside the window, but confining the cursor to the client area is a typical way to use the function.</span></span> <span data-ttu-id="9156a-131">La limitazione del cursore a un'area completamente esterna alla finestra potrebbe essere insolita e gli utenti probabilmente lo percepiranno come un bug.</span><span class="sxs-lookup"><span data-stu-id="9156a-131">Confining the cursor to a region entirely outside your window would be unusual, and users would probably perceive it as a bug.</span></span>

<span data-ttu-id="9156a-132">Per rimuovere la restrizione, chiamare [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) con il valore **null**.</span><span class="sxs-lookup"><span data-stu-id="9156a-132">To remove the restriction, call [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) with the value **NULL**.</span></span>


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a><span data-ttu-id="9156a-133">Eventi di rilevamento del mouse: passaggio del mouse e uscita</span><span class="sxs-lookup"><span data-stu-id="9156a-133">Mouse Tracking Events: Hover and Leave</span></span>

<span data-ttu-id="9156a-134">Per impostazione predefinita, altri due messaggi del mouse sono disabilitati, ma possono essere utili per alcune applicazioni:</span><span class="sxs-lookup"><span data-stu-id="9156a-134">Two other mouse messages are disabled by default, but may be useful for some applications:</span></span>

-   <span data-ttu-id="9156a-135">[**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover): il cursore è posizionato sull'area client per un periodo di tempo fisso.</span><span class="sxs-lookup"><span data-stu-id="9156a-135">[**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover): The cursor has hovered over the client area for a fixed period of time.</span></span>
-   <span data-ttu-id="9156a-136">[**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): il cursore ha lasciato l'area client.</span><span class="sxs-lookup"><span data-stu-id="9156a-136">[**WM\_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): The cursor has left the client area.</span></span>

<span data-ttu-id="9156a-137">Per abilitare questi messaggi, chiamare la funzione [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) .</span><span class="sxs-lookup"><span data-stu-id="9156a-137">To enable these messages, call the [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) function.</span></span>


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



<span data-ttu-id="9156a-138">La struttura [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) contiene i parametri per la funzione.</span><span class="sxs-lookup"><span data-stu-id="9156a-138">The [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) structure contains the parameters for the function.</span></span> <span data-ttu-id="9156a-139">Il membro **dwFlags** della struttura contiene flag di bit che specificano i messaggi di rilevamento a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="9156a-139">The **dwFlags** member of the structure contains bit flags that specify which tracking messages you are interested in.</span></span> <span data-ttu-id="9156a-140">È possibile scegliere di ottenere sia [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) che [**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), come illustrato qui, o solo uno dei due.</span><span class="sxs-lookup"><span data-stu-id="9156a-140">You can choose to get both [**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) and [**WM\_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), as shown here, or just one of the two.</span></span> <span data-ttu-id="9156a-141">Il membro **dwHoverTime** specifica la durata del passaggio del mouse prima che il sistema generi un messaggio hover.</span><span class="sxs-lookup"><span data-stu-id="9156a-141">The **dwHoverTime** member specifies how long the mouse needs to hover before the system generates a hover message.</span></span> <span data-ttu-id="9156a-142">Questo valore è espresso in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="9156a-142">This value is given in milliseconds.</span></span> <span data-ttu-id="9156a-143">Per **\_ impostazione predefinita, il valore predefinito di hover** indica l'utilizzo dell'impostazione predefinita del sistema.</span><span class="sxs-lookup"><span data-stu-id="9156a-143">The constant **HOVER\_DEFAULT** means to use the system default.</span></span>

<span data-ttu-id="9156a-144">Dopo aver ottenuto uno dei messaggi richiesti, la funzione [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) viene reimpostata.</span><span class="sxs-lookup"><span data-stu-id="9156a-144">After you get one of the messages that you requested, the [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) function resets.</span></span> <span data-ttu-id="9156a-145">Per ottenere un altro messaggio di rilevamento, è necessario chiamarlo di nuovo.</span><span class="sxs-lookup"><span data-stu-id="9156a-145">You must call it again to get another tracking message.</span></span> <span data-ttu-id="9156a-146">Tuttavia, è necessario attendere fino al successivo messaggio di spostamento del mouse prima di chiamare di nuovo **TrackMouseEvent** .</span><span class="sxs-lookup"><span data-stu-id="9156a-146">However, you should wait until the next mouse-move message before calling **TrackMouseEvent** again.</span></span> <span data-ttu-id="9156a-147">In caso contrario, è possibile che la finestra venga sovraccaricata con i messaggi di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="9156a-147">Otherwise, your window might be flooded with tracking messages.</span></span> <span data-ttu-id="9156a-148">Ad esempio, se il mouse viene spostato, il sistema continuerà a generare un flusso di messaggi [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) mentre il mouse è stazionario.</span><span class="sxs-lookup"><span data-stu-id="9156a-148">For example, if the mouse is hovering, the system would continue to generate a stream of [**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) messages while the mouse is stationary.</span></span> <span data-ttu-id="9156a-149">In realtà non si vuole un altro messaggio **WM \_ MOUSEHOVER** fino a quando il mouse si sposta in un altro punto e si passa nuovamente.</span><span class="sxs-lookup"><span data-stu-id="9156a-149">You don't actually want another **WM\_MOUSEHOVER** message until the mouse moves to another spot and hovers again.</span></span>

<span data-ttu-id="9156a-150">Ecco una piccola classe helper che è possibile usare per gestire gli eventi di rilevamento del mouse.</span><span class="sxs-lookup"><span data-stu-id="9156a-150">Here is a small helper class that you can use to manage mouse-tracking events.</span></span>


```C++
class MouseTrackEvents
{
    bool m_bMouseTracking;

public:
    MouseTrackEvents() : m_bMouseTracking(false)
    {
    }
    
    void OnMouseMove(HWND hwnd)
    {
        if (!m_bMouseTracking)
        {
            // Enable mouse tracking.
            TRACKMOUSEEVENT tme;
            tme.cbSize = sizeof(tme);
            tme.hwndTrack = hwnd;
            tme.dwFlags = TME_HOVER | TME_LEAVE;
            tme.dwHoverTime = HOVER_DEFAULT;
            TrackMouseEvent(&tme);
            m_bMouseTracking = true;
        }
    }
    void Reset(HWND hwnd)
    {
        m_bMouseTracking = false;
    }
};
```



<span data-ttu-id="9156a-151">Nell'esempio seguente viene illustrato come utilizzare questa classe nella routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="9156a-151">The next example shows how to use this class in your window procedure.</span></span>


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_MOUSEMOVE:
        mouseTrack.OnMouseMove(m_hwnd);  // Start tracking.

        // TODO: Handle the mouse-move message.

        return 0;

    case WM_MOUSELEAVE:

        // TODO: Handle the mouse-leave message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    case WM_MOUSEHOVER:

        // TODO: Handle the mouse-hover message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="9156a-152">Gli eventi di rilevamento del mouse richiedono un'ulteriore elaborazione da parte del sistema, quindi lasciarli disabilitati se non sono necessari.</span><span class="sxs-lookup"><span data-stu-id="9156a-152">Mouse tracking events require additional processing by the system, so leave them disabled if you do not need them.</span></span>

<span data-ttu-id="9156a-153">Per completezza, di seguito è illustrata una funzione che esegue una query sul sistema per il timeout predefinito del passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="9156a-153">For completeness, here is a function that queries the system for the default hover timeout.</span></span>


```C++
UINT GetMouseHoverTime()
{
    UINT msec; 
    if (SystemParametersInfo(SPI_GETMOUSEHOVERTIME, 0, &msec, 0))
    {   
        return msec;
    }
    else
    {
        return 0;
    }
}
```



## <a name="mouse-wheel"></a><span data-ttu-id="9156a-154">Rotellina del mouse</span><span class="sxs-lookup"><span data-stu-id="9156a-154">Mouse Wheel</span></span>

<span data-ttu-id="9156a-155">La funzione seguente controlla se è presente una rotellina del mouse.</span><span class="sxs-lookup"><span data-stu-id="9156a-155">The following function checks if a mouse wheel is present.</span></span>


```C++
BOOL IsMouseWheelPresent()
{
    return (GetSystemMetrics(SM_MOUSEWHEELPRESENT) != 0);
}
```



<span data-ttu-id="9156a-156">Se l'utente ruota la rotellina del mouse, la finestra con lo stato attivo riceve un messaggio [**WM \_ MOUSEWHEEL**](/windows/desktop/inputdev/wm-mousewheel) .</span><span class="sxs-lookup"><span data-stu-id="9156a-156">If the user rotates the mouse wheel, the window with focus receives a [**WM\_MOUSEWHEEL**](/windows/desktop/inputdev/wm-mousewheel) message.</span></span> <span data-ttu-id="9156a-157">Il parametro *wParam* di questo messaggio contiene un valore integer denominato *Delta* che misura la distanza con cui è stata ruotata la rotellina.</span><span class="sxs-lookup"><span data-stu-id="9156a-157">The *wParam* parameter of this message contains an integer value called the *delta* that measures how far the wheel was rotated.</span></span> <span data-ttu-id="9156a-158">Il Delta USA unità arbitrarie, in cui 120 unità è definita come rotazione necessaria per eseguire una "azione".</span><span class="sxs-lookup"><span data-stu-id="9156a-158">The delta uses arbitrary units, where 120 units is defined as the rotation needed to perform one "action."</span></span> <span data-ttu-id="9156a-159">Naturalmente, la definizione di un'azione dipende dal programma.</span><span class="sxs-lookup"><span data-stu-id="9156a-159">Of course, the definition of an action depends on your program.</span></span> <span data-ttu-id="9156a-160">Se ad esempio si usa la rotellina del mouse per scorrere il testo, ogni 120 unità di rotazione scorrerà una riga di testo.</span><span class="sxs-lookup"><span data-stu-id="9156a-160">For example, if the mouse wheel is used to scroll text, each 120 units of rotation would scroll one line of text.</span></span>

<span data-ttu-id="9156a-161">Il segno del Delta indica la direzione di rotazione:</span><span class="sxs-lookup"><span data-stu-id="9156a-161">The sign of the delta indicates the direction of rotation:</span></span>

-   <span data-ttu-id="9156a-162">Positivo: ruotare in orizzontale, lontano dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9156a-162">Positive: Rotate forward, away from the user.</span></span>
-   <span data-ttu-id="9156a-163">Negativo: ruotare indietro verso l'utente.</span><span class="sxs-lookup"><span data-stu-id="9156a-163">Negative: Rotate backward, toward the user.</span></span>

<span data-ttu-id="9156a-164">Il valore del Delta viene inserito in *wParam* insieme ad alcuni flag aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="9156a-164">The value of the delta is placed in *wParam* along with some additional flags.</span></span> <span data-ttu-id="9156a-165">Usare la macro [**get \_ Wheel \_ Delta \_ wParam**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) per ottenere il valore del Delta.</span><span class="sxs-lookup"><span data-stu-id="9156a-165">Use the [**GET\_WHEEL\_DELTA\_WPARAM**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) macro to get the value of the delta.</span></span>


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="9156a-166">Se la rotellina del mouse ha una risoluzione elevata, il valore assoluto del Delta potrebbe essere minore di 120.</span><span class="sxs-lookup"><span data-stu-id="9156a-166">If the mouse wheel has a high resolution, the absolute value of the delta might be less than 120.</span></span> <span data-ttu-id="9156a-167">In tal caso, se è opportuno che l'azione venga eseguita con incrementi più piccoli, è possibile farlo.</span><span class="sxs-lookup"><span data-stu-id="9156a-167">In that case, if it makes sense for the action to occur in smaller increments, you can do so.</span></span> <span data-ttu-id="9156a-168">Ad esempio, il testo potrebbe scorrere in base a incrementi di meno di una riga.</span><span class="sxs-lookup"><span data-stu-id="9156a-168">For example, text could scroll by increments of less than one line.</span></span> <span data-ttu-id="9156a-169">In caso contrario, accumulare il Delta totale finché la rotellina non ruota abbastanza per eseguire l'azione.</span><span class="sxs-lookup"><span data-stu-id="9156a-169">Otherwise, accumulate the total delta until the wheel rotates enough to perform the action.</span></span> <span data-ttu-id="9156a-170">Archiviare il Delta non usato in una variabile e quando si accumulano 120 unità (positive o negative), eseguire l'azione.</span><span class="sxs-lookup"><span data-stu-id="9156a-170">Store the unused delta in a variable, and when 120 units accumulate (either positive or negative), perform the action.</span></span>

## <a name="next"></a><span data-ttu-id="9156a-171">Prossima</span><span class="sxs-lookup"><span data-stu-id="9156a-171">Next</span></span>

[<span data-ttu-id="9156a-172">Input da tastiera</span><span class="sxs-lookup"><span data-stu-id="9156a-172">Keyboard Input</span></span>](keyboard-input.md)

 

 