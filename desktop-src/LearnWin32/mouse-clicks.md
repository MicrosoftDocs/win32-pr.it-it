---
title: Risposta ai clic del mouse
description: Risposta ai clic del mouse
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c37903264ca638aeca1c0b28fb2ea7fa792660
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117730"
---
# <a name="responding-to-mouse-clicks"></a><span data-ttu-id="bbd31-103">Risposta ai clic del mouse</span><span class="sxs-lookup"><span data-stu-id="bbd31-103">Responding to Mouse Clicks</span></span>

<span data-ttu-id="bbd31-104">Se l'utente fa clic su un pulsante del mouse mentre il cursore si trova sull'area client di una finestra, la finestra riceve uno dei messaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="bbd31-104">If the user clicks a mouse button while the cursor is over the client area of a window, the window receives one of the following messages.</span></span>



| <span data-ttu-id="bbd31-105">Messaggio</span><span class="sxs-lookup"><span data-stu-id="bbd31-105">Message</span></span>                                        | <span data-ttu-id="bbd31-106">Significato</span><span class="sxs-lookup"><span data-stu-id="bbd31-106">Meaning</span></span>                   |
|------------------------------------------------|---------------------------|
| [<span data-ttu-id="bbd31-107">**\_LBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="bbd31-107">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown) | <span data-ttu-id="bbd31-108">Pulsante sinistro</span><span class="sxs-lookup"><span data-stu-id="bbd31-108">Left button down</span></span>          |
| [<span data-ttu-id="bbd31-109">**\_LBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="bbd31-109">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)     | <span data-ttu-id="bbd31-110">Pulsante a sinistra in alto</span><span class="sxs-lookup"><span data-stu-id="bbd31-110">Left button up</span></span>            |
| [<span data-ttu-id="bbd31-111">**\_MBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="bbd31-111">**WM\_MBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-mbuttondown) | <span data-ttu-id="bbd31-112">Pulsante centrale verso il basso</span><span class="sxs-lookup"><span data-stu-id="bbd31-112">Middle button down</span></span>        |
| [<span data-ttu-id="bbd31-113">**\_MBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="bbd31-113">**WM\_MBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-mbuttonup)     | <span data-ttu-id="bbd31-114">Pulsante centrale</span><span class="sxs-lookup"><span data-stu-id="bbd31-114">Middle button up</span></span>          |
| [<span data-ttu-id="bbd31-115">**\_RBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="bbd31-115">**WM\_RBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-rbuttondown) | <span data-ttu-id="bbd31-116">Pulsante destro verso il basso</span><span class="sxs-lookup"><span data-stu-id="bbd31-116">Right button down</span></span>         |
| [<span data-ttu-id="bbd31-117">**\_RBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="bbd31-117">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)     | <span data-ttu-id="bbd31-118">Pulsante destro su</span><span class="sxs-lookup"><span data-stu-id="bbd31-118">Right button up</span></span>           |
| [<span data-ttu-id="bbd31-119">**\_XBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="bbd31-119">**WM\_XBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-xbuttondown) | <span data-ttu-id="bbd31-120">XBUTTON1 o XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="bbd31-120">XBUTTON1 or XBUTTON2 down</span></span> |
| [<span data-ttu-id="bbd31-121">**\_XBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="bbd31-121">**WM\_XBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-xbuttonup)     | <span data-ttu-id="bbd31-122">XBUTTON1 o XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="bbd31-122">XBUTTON1 or XBUTTON2 up</span></span>   |



 

<span data-ttu-id="bbd31-123">Si ricordi che l'area client è la parte della finestra che esclude il frame.</span><span class="sxs-lookup"><span data-stu-id="bbd31-123">Recall that the client area is the portion of the window that excludes the frame.</span></span> <span data-ttu-id="bbd31-124">Per ulteriori informazioni sulle aree client, vedere [che cos'è una finestra?](what-is-a-window-.md)</span><span class="sxs-lookup"><span data-stu-id="bbd31-124">For more information about client areas, see [What Is a Window?](what-is-a-window-.md)</span></span>

### <a name="mouse-coordinates"></a><span data-ttu-id="bbd31-125">Coordinate del mouse</span><span class="sxs-lookup"><span data-stu-id="bbd31-125">Mouse Coordinates</span></span>

<span data-ttu-id="bbd31-126">In tutti questi messaggi, il parametro *lParam* contiene le coordinate x e y del puntatore del mouse.</span><span class="sxs-lookup"><span data-stu-id="bbd31-126">In all of these messages, the *lParam* parameter contains the x- and y-coordinates of the mouse pointer.</span></span> <span data-ttu-id="bbd31-127">I 16 bit più bassi di *lParam* contengono la coordinata x e i successivi 16 bit contengono la coordinata y.</span><span class="sxs-lookup"><span data-stu-id="bbd31-127">The lowest 16 bits of *lParam* contain the x-coordinate, and the next 16 bits contain the y-coordinate.</span></span> <span data-ttu-id="bbd31-128">Usare le macro [**get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per decomprimere le coordinate da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="bbd31-128">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to unpack the coordinates from *lParam*.</span></span>


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="bbd31-129">Queste macro sono definite nel file di intestazione WindowsX. h.</span><span class="sxs-lookup"><span data-stu-id="bbd31-129">These macros are defined in the header file WindowsX.h.</span></span>

<span data-ttu-id="bbd31-130">In Windows a 64 bit, *lParam* è un valore a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="bbd31-130">On 64-bit Windows, *lParam* is 64-bit value.</span></span> <span data-ttu-id="bbd31-131">Non vengono usati i bit 32 superiori di *lParam* .</span><span class="sxs-lookup"><span data-stu-id="bbd31-131">The upper 32 bits of *lParam* are not used.</span></span> <span data-ttu-id="bbd31-132">Nella documentazione di MSDN sono menzionati la "parola di basso livello" e la "parola più ordinata" di *lParam*.</span><span class="sxs-lookup"><span data-stu-id="bbd31-132">The MSDN documentation mentions the "low-order word" and "high-order word" of *lParam*.</span></span> <span data-ttu-id="bbd31-133">Nel caso di 64 bit, ciò significa che le parole di ordine inferiore e superiore dei 32 bit inferiori.</span><span class="sxs-lookup"><span data-stu-id="bbd31-133">In the 64-bit case, this means the low- and high-order words of the lower 32 bits.</span></span> <span data-ttu-id="bbd31-134">Le macro estraggono i valori corretti, quindi se vengono usati, si sarà sicuri.</span><span class="sxs-lookup"><span data-stu-id="bbd31-134">The macros extract the right values, so if you use them, you will be safe.</span></span>

<span data-ttu-id="bbd31-135">Le coordinate del mouse sono espresse in pixel, non in pixel indipendenti dal dispositivo (DIP) e vengono misurate in relazione all'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="bbd31-135">Mouse coordinates are given in pixels, not device-independent pixels (DIPs), and are measured relative to the client area of the window.</span></span> <span data-ttu-id="bbd31-136">Le coordinate sono valori con segno.</span><span class="sxs-lookup"><span data-stu-id="bbd31-136">Coordinates are signed values.</span></span> <span data-ttu-id="bbd31-137">Le posizioni sopra e a sinistra dell'area client presentano coordinate negative, che è importante se si tiene traccia della posizione del mouse all'esterno della finestra.</span><span class="sxs-lookup"><span data-stu-id="bbd31-137">Positions above and to the left of the client area have negative coordinates, which is important if you track the mouse position outside the window.</span></span> <span data-ttu-id="bbd31-138">Si vedrà come eseguire questa operazione in un argomento successivo, [acquisendo lo spostamento del mouse all'esterno della finestra](mouse-movement.md).</span><span class="sxs-lookup"><span data-stu-id="bbd31-138">We will see how to do that in a later topic, [Capturing Mouse Movement Outside the Window](mouse-movement.md).</span></span>

### <a name="additional-flags"></a><span data-ttu-id="bbd31-139">Flag aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="bbd31-139">Additional Flags</span></span>

<span data-ttu-id="bbd31-140">Il parametro *wParam* contiene un operatore OR bit per bit di flag, che indica lo stato degli altri **pulsanti del mouse** oltre ai tasti MAIUSC e CTRL.</span><span class="sxs-lookup"><span data-stu-id="bbd31-140">The *wParam* parameter contains a bitwise **OR** of flags, indicating the state of the other mouse buttons plus the SHIFT and CTRL keys.</span></span>



| <span data-ttu-id="bbd31-141">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="bbd31-141">Flag</span></span>             | <span data-ttu-id="bbd31-142">Significato</span><span class="sxs-lookup"><span data-stu-id="bbd31-142">Meaning</span></span>                          |
|------------------|----------------------------------|
| <span data-ttu-id="bbd31-143">**MK ( \_ controllo)**</span><span class="sxs-lookup"><span data-stu-id="bbd31-143">**MK\_CONTROL**</span></span>  | <span data-ttu-id="bbd31-144">Il tasto CTRL è premuto.</span><span class="sxs-lookup"><span data-stu-id="bbd31-144">The CTRL key is down.</span></span>            |
| <span data-ttu-id="bbd31-145">**\_LBUTTON MK**</span><span class="sxs-lookup"><span data-stu-id="bbd31-145">**MK\_LBUTTON**</span></span>  | <span data-ttu-id="bbd31-146">Il pulsante sinistro del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="bbd31-146">The left mouse button is down.</span></span>   |
| <span data-ttu-id="bbd31-147">**\_MBUTTON MK**</span><span class="sxs-lookup"><span data-stu-id="bbd31-147">**MK\_MBUTTON**</span></span>  | <span data-ttu-id="bbd31-148">Il pulsante centrale del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="bbd31-148">The middle mouse button is down.</span></span> |
| <span data-ttu-id="bbd31-149">**\_RBUTTON MK**</span><span class="sxs-lookup"><span data-stu-id="bbd31-149">**MK\_RBUTTON**</span></span>  | <span data-ttu-id="bbd31-150">Il pulsante destro del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="bbd31-150">The right mouse button is down.</span></span>  |
| <span data-ttu-id="bbd31-151">**\_turno MK**</span><span class="sxs-lookup"><span data-stu-id="bbd31-151">**MK\_SHIFT**</span></span>    | <span data-ttu-id="bbd31-152">Il tasto MAIUSC è premuto.</span><span class="sxs-lookup"><span data-stu-id="bbd31-152">The SHIFT key is down.</span></span>           |
| <span data-ttu-id="bbd31-153">**\_XBUTTON1 MK**</span><span class="sxs-lookup"><span data-stu-id="bbd31-153">**MK\_XBUTTON1**</span></span> | <span data-ttu-id="bbd31-154">Il pulsante XBUTTON1 è inattivo.</span><span class="sxs-lookup"><span data-stu-id="bbd31-154">The XBUTTON1 button is down.</span></span>     |
| <span data-ttu-id="bbd31-155">**\_XBUTTON2 MK**</span><span class="sxs-lookup"><span data-stu-id="bbd31-155">**MK\_XBUTTON2**</span></span> | <span data-ttu-id="bbd31-156">Il pulsante XBUTTON2 è inattivo.</span><span class="sxs-lookup"><span data-stu-id="bbd31-156">The XBUTTON2 button is down.</span></span>     |



 

<span data-ttu-id="bbd31-157">L'assenza di un flag indica che non è stato premuto il pulsante o la chiave corrispondente.</span><span class="sxs-lookup"><span data-stu-id="bbd31-157">The absence of a flag means the corresponding button or key was not pressed.</span></span> <span data-ttu-id="bbd31-158">Ad esempio, per verificare se il tasto CTRL è inattivo:</span><span class="sxs-lookup"><span data-stu-id="bbd31-158">For example, to test whether the CTRL key is down:</span></span>


```C++
if (wParam & MK_CONTROL) { ...
```



<span data-ttu-id="bbd31-159">Se è necessario trovare lo stato di altre chiavi oltre a CTRL e MAIUSC, usare la funzione [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) , descritta in input da [tastiera](keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="bbd31-159">If you need to find the state of other keys besides CTRL and SHIFT, use the [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function, which is described in [Keyboard Input](keyboard-input.md).</span></span>

<span data-ttu-id="bbd31-160">I messaggi della finestra [**WM \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) e [**WM \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) si applicano sia a XBUTTON1 che a XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="bbd31-160">The [**WM\_XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) and [**WM\_XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) window messages apply to both XBUTTON1 and XBUTTON2.</span></span> <span data-ttu-id="bbd31-161">Il parametro *wParam* indica il pulsante su cui è stato fatto clic.</span><span class="sxs-lookup"><span data-stu-id="bbd31-161">The *wParam* parameter indicates which button was clicked.</span></span>


```C++
UINT button = GET_XBUTTON_WPARAM(wParam);  
if (button == XBUTTON1)
{
    // XBUTTON1 was clicked.
}
else if (button == XBUTTON2)
{
    // XBUTTON2 was clicked.
}
```



## <a name="double-clicks"></a><span data-ttu-id="bbd31-162">Doppio clic</span><span class="sxs-lookup"><span data-stu-id="bbd31-162">Double Clicks</span></span>

<span data-ttu-id="bbd31-163">Per impostazione predefinita, una finestra non riceve notifiche di doppio clic.</span><span class="sxs-lookup"><span data-stu-id="bbd31-163">A window does not receive double-click notifications by default.</span></span> <span data-ttu-id="bbd31-164">Per ricevere i doppi clic, impostare il flag **cs \_ DBLCLKS** nella struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) quando si registra la classe Window.</span><span class="sxs-lookup"><span data-stu-id="bbd31-164">To receive double clicks, set the **CS\_DBLCLKS** flag in the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure when you register the window class.</span></span>


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



<span data-ttu-id="bbd31-165">Se si imposta il flag **cs \_ DBLCLKS** come illustrato, la finestra riceverà le notifiche di doppio clic.</span><span class="sxs-lookup"><span data-stu-id="bbd31-165">If you set the **CS\_DBLCLKS** flag as shown, the window will receive double-click notifications.</span></span> <span data-ttu-id="bbd31-166">Un doppio clic è indicato da un messaggio della finestra con "DBLCLK" nel nome.</span><span class="sxs-lookup"><span data-stu-id="bbd31-166">A double click is indicated by a window message with "DBLCLK" in the name.</span></span> <span data-ttu-id="bbd31-167">Ad esempio, un doppio clic sul pulsante sinistro del mouse produce la seguente sequenza di messaggi:</span><span class="sxs-lookup"><span data-stu-id="bbd31-167">For example, a double click on the left mouse button produces the following sequence of messages:</span></span>

<dl>

[<span data-ttu-id="bbd31-168">**\_LBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="bbd31-168">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown)  
[<span data-ttu-id="bbd31-169">**\_LBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="bbd31-169">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)  
[<span data-ttu-id="bbd31-170">**\_LBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="bbd31-170">**WM\_LBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-lbuttondblclk)  
[<span data-ttu-id="bbd31-171">**\_LBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="bbd31-171">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

<span data-ttu-id="bbd31-172">In effetti, il secondo messaggio [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) che verrebbe normalmente generato diventa un messaggio [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) .</span><span class="sxs-lookup"><span data-stu-id="bbd31-172">In effect, the second [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message that would normally be generated becomes a [**WM\_LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) message.</span></span> <span data-ttu-id="bbd31-173">I messaggi equivalenti vengono definiti per i pulsanti right, Middle e XBUTTON.</span><span class="sxs-lookup"><span data-stu-id="bbd31-173">Equivalent messages are defined for right, middle, and XBUTTON buttons.</span></span>

<span data-ttu-id="bbd31-174">Fino a quando non si riceve il messaggio di doppio clic, non esiste alcun modo per indicare che il primo clic del mouse è l'inizio di un doppio clic.</span><span class="sxs-lookup"><span data-stu-id="bbd31-174">Until you get the double-click message, there is no way to tell that the first mouse click is the start of a double click.</span></span> <span data-ttu-id="bbd31-175">Pertanto, un'azione di doppio clic deve continuare un'azione che inizia con il primo clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="bbd31-175">Therefore, a double-click action should continue an action that begins with the first mouse click.</span></span> <span data-ttu-id="bbd31-176">Nella shell di Windows, ad esempio, un singolo clic Seleziona una cartella, mentre un doppio clic apre la cartella.</span><span class="sxs-lookup"><span data-stu-id="bbd31-176">For example, in the Windows Shell, a single click selects a folder, while a double click opens the folder.</span></span>

## <a name="non-client-mouse-messages"></a><span data-ttu-id="bbd31-177">Messaggi del mouse non client</span><span class="sxs-lookup"><span data-stu-id="bbd31-177">Non-client Mouse Messages</span></span>

<span data-ttu-id="bbd31-178">Per gli eventi del mouse che si verificano all'interno dell'area non client della finestra viene definito un set separato di messaggi.</span><span class="sxs-lookup"><span data-stu-id="bbd31-178">A separate set of messages are defined for mouse events that occur within the non-client area of the window.</span></span> <span data-ttu-id="bbd31-179">Questi messaggi contengono le lettere "NC" nel nome.</span><span class="sxs-lookup"><span data-stu-id="bbd31-179">These messages have the letters "NC" in the name.</span></span> <span data-ttu-id="bbd31-180">Ad esempio, [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) è l'equivalente non client di [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span><span class="sxs-lookup"><span data-stu-id="bbd31-180">For example, [**WM\_NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) is the non-client equivalent of [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span></span> <span data-ttu-id="bbd31-181">Una tipica applicazione non intercetta questi messaggi perché la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gestisce correttamente questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="bbd31-181">A typical application will not intercept these messages, because the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function handles these messages correctly.</span></span> <span data-ttu-id="bbd31-182">Tuttavia, possono essere utili per alcune funzioni avanzate.</span><span class="sxs-lookup"><span data-stu-id="bbd31-182">However, they can be useful for certain advanced functions.</span></span> <span data-ttu-id="bbd31-183">Ad esempio, è possibile usare questi messaggi per implementare un comportamento personalizzato nella barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="bbd31-183">For example, you could use these messages to implement custom behavior in the title bar.</span></span> <span data-ttu-id="bbd31-184">Se si gestiscono questi messaggi, è in genere necessario passarli a **DefWindowProc** in seguito.</span><span class="sxs-lookup"><span data-stu-id="bbd31-184">If you do handle these messages, you should generally pass them to **DefWindowProc** afterward.</span></span> <span data-ttu-id="bbd31-185">In caso contrario, l'applicazione interrompe le funzionalità standard, ad esempio il trascinamento o la riduzione a icona della finestra.</span><span class="sxs-lookup"><span data-stu-id="bbd31-185">Otherwise, your application will break standard functionality such as dragging or minimizing the window.</span></span>

## <a name="next"></a><span data-ttu-id="bbd31-186">Prossima</span><span class="sxs-lookup"><span data-stu-id="bbd31-186">Next</span></span>

[<span data-ttu-id="bbd31-187">Spostamento del mouse</span><span class="sxs-lookup"><span data-stu-id="bbd31-187">Mouse Movement</span></span>](mouse-movement.md)

 

 