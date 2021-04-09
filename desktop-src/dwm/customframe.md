---
title: Cornice della finestra personalizzata mediante DWM
description: In questo argomento viene illustrato come utilizzare le API di Gestione finestre desktop (DWM) per creare frame di finestra personalizzati per l'applicazione.
ms.assetid: 7f7dc902-40d3-44e9-adc2-05a39c634eb3
keywords:
- Gestione finestre desktop (DWM), frame di finestra personalizzati
- DWM (Gestione finestre desktop), frame di finestra personalizzati
- frame di finestra personalizzati
- rimozione di frame standard
- estensione di frame client
- Gestione finestre desktop (DWM), estensione di frame client
- DWM (Gestione finestre desktop), estensione di frame client
- Gestione finestre desktop (DWM), rimozione di frame standard
- DWM (Gestione finestre desktop), rimozione di frame standard
- Gestione finestre desktop (DWM), disegno in frame estesi
- DWM (Gestione finestre desktop), disegno in frame estesi
- disegno in frame estesi
- test delle occorrenze
- Gestione finestre desktop (DWM), hit testing
- DWM (Gestione finestre desktop), hit testing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a27a9b71dd2dd91cb000a352ef039de2a71cd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047329"
---
# <a name="custom-window-frame-using-dwm"></a><span data-ttu-id="abafc-118">Cornice della finestra personalizzata mediante DWM</span><span class="sxs-lookup"><span data-stu-id="abafc-118">Custom Window Frame Using DWM</span></span>

<span data-ttu-id="abafc-119">In questo argomento viene illustrato come utilizzare le API di Gestione finestre desktop (DWM) per creare frame di finestra personalizzati per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="abafc-119">This topic demonstrates how to use the Desktop Window Manager (DWM) APIs to create custom window frames for your application.</span></span>

-   [<span data-ttu-id="abafc-120">Introduzione</span><span class="sxs-lookup"><span data-stu-id="abafc-120">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="abafc-121">Estensione del frame client</span><span class="sxs-lookup"><span data-stu-id="abafc-121">Extending the Client Frame</span></span>](#extending-the-client-frame)
-   [<span data-ttu-id="abafc-122">Rimozione del frame standard</span><span class="sxs-lookup"><span data-stu-id="abafc-122">Removing the Standard Frame</span></span>](#removing-the-standard-frame)
-   [<span data-ttu-id="abafc-123">Disegno nella finestra cornice estesa</span><span class="sxs-lookup"><span data-stu-id="abafc-123">Drawing in the Extended Frame Window</span></span>](#drawing-in-the-extended-frame-window)
-   [<span data-ttu-id="abafc-124">Abilitazione dell'hit testing per il frame personalizzato</span><span class="sxs-lookup"><span data-stu-id="abafc-124">Enabling Hit Testing for the Custom Frame</span></span>](#enabling-hit-testing-for-the-custom-frame)
-   [<span data-ttu-id="abafc-125">Appendice A: procedura della finestra di esempio</span><span class="sxs-lookup"><span data-stu-id="abafc-125">Appendix A: Sample Window Procedure</span></span>](#appendix-a-sample-window-procedure)
-   [<span data-ttu-id="abafc-126">Appendice B: disegno del titolo della didascalia</span><span class="sxs-lookup"><span data-stu-id="abafc-126">Appendix B: Painting the Caption Title</span></span>](#appendix-b-painting-the-caption-title)
-   [<span data-ttu-id="abafc-127">Appendice C: funzione HitTestNCA</span><span class="sxs-lookup"><span data-stu-id="abafc-127">Appendix C: HitTestNCA Function</span></span>](#appendix-c-hittestnca-function)
-   [<span data-ttu-id="abafc-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="abafc-128">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="abafc-129">Introduzione</span><span class="sxs-lookup"><span data-stu-id="abafc-129">Introduction</span></span>

<span data-ttu-id="abafc-130">In Windows Vista e versioni successive, l'aspetto delle aree non client delle finestre dell'applicazione (la barra del titolo, l'icona, il bordo della finestra e i pulsanti della didascalia) sono controllati da DWM.</span><span class="sxs-lookup"><span data-stu-id="abafc-130">In Windows Vista and later, the appearance of the non-client areas of application windows (the title bar, icon, window border, and caption buttons) is controlled by the DWM.</span></span> <span data-ttu-id="abafc-131">Utilizzando le API di DWM, è possibile modificare il modo in cui DWM esegue il rendering del frame di una finestra.</span><span class="sxs-lookup"><span data-stu-id="abafc-131">Using the DWM APIs, you can change the way the DWM renders a window's frame.</span></span>

<span data-ttu-id="abafc-132">Una funzionalità delle API di DWM è la possibilità di estendere il frame dell'applicazione nell'area client.</span><span class="sxs-lookup"><span data-stu-id="abafc-132">One feature of the DWM APIs is the ability to extend the application frame into the client area.</span></span> <span data-ttu-id="abafc-133">In questo modo è possibile integrare un elemento dell'interfaccia utente client, ad esempio una barra degli strumenti, nel frame, fornendo ai controlli dell'interfaccia utente una posizione più evidente nell'interfaccia utente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="abafc-133">This enables you to integrate a client UI element—such as a toolbar—into the frame, giving the UI controls a more prominent place in the application UI.</span></span> <span data-ttu-id="abafc-134">Windows Internet Explorer 7 in Windows Vista, ad esempio, integra la barra di spostamento nella cornice della finestra estendendo la parte superiore del frame, come illustrato nello screenshot seguente.</span><span class="sxs-lookup"><span data-stu-id="abafc-134">For example, Windows Internet Explorer 7 on Windows Vista integrates the navigation bar into the window frame by extending the top of the frame as shown in the following screen shot.</span></span>

![barra di spostamento integrata nella cornice della finestra.](images/ie7-extendedborder-boxed.png)

<span data-ttu-id="abafc-136">La possibilità di estendere la cornice della finestra consente anche di creare frame personalizzati mantenendo l'aspetto della finestra.</span><span class="sxs-lookup"><span data-stu-id="abafc-136">The ability to extend the window frame also enables you to create custom frames while maintaining the window's look and feel.</span></span> <span data-ttu-id="abafc-137">Ad esempio, Microsoft Office Word 2007 disegna il pulsante di Office e la barra di accesso rapido all'interno del frame personalizzato, fornendo i pulsanti di riduzione a icona standard, Ingrandisci e Chiudi, come illustrato nello screenshot seguente.</span><span class="sxs-lookup"><span data-stu-id="abafc-137">For example, Microsoft Office Word 2007 draws the Office button and the Quick Access toolbar inside the custom frame while providing the standard Minimize, Maximize, and Close caption buttons, as shown in the following screen shot.</span></span>

![pulsante di Office e barra di accesso rapido in Word 2007](images/word2007-customborder-boxed.png)

## <a name="extending-the-client-frame"></a><span data-ttu-id="abafc-139">Estensione del frame client</span><span class="sxs-lookup"><span data-stu-id="abafc-139">Extending the Client Frame</span></span>

<span data-ttu-id="abafc-140">La funzionalità per estendere il frame nell'area client viene esposta dalla funzione [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .</span><span class="sxs-lookup"><span data-stu-id="abafc-140">The functionality to extend the frame into the client area is exposed by the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) function.</span></span> <span data-ttu-id="abafc-141">Per estendere il frame, passare l'handle della finestra di destinazione insieme ai valori di inserimento dei margini a **DwmExtendFrameIntoClientArea**.</span><span class="sxs-lookup"><span data-stu-id="abafc-141">To extend the frame, pass the handle of the target window together with the margin inset values to **DwmExtendFrameIntoClientArea**.</span></span> <span data-ttu-id="abafc-142">I valori di inserimento dei margini determinano la distanza per estendere il frame nei quattro lati della finestra.</span><span class="sxs-lookup"><span data-stu-id="abafc-142">The margin inset values determine how far to extend the frame on the four sides of the window.</span></span>

<span data-ttu-id="abafc-143">Il codice seguente illustra l'uso di [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) per estendere il frame.</span><span class="sxs-lookup"><span data-stu-id="abafc-143">The following code demonstrates the use of [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) to extend the frame.</span></span>


```
// Handle the window activation.
if (message == WM_ACTIVATE)
{
    // Extend the frame into the client area.
    MARGINS margins;

    margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
    margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
    margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
    margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

    hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

    if (!SUCCEEDED(hr))
    {
        // Handle the error.
    }

    fCallDWP = true;
    lRet = 0;
}
```



<span data-ttu-id="abafc-144">Si noti che l'estensione del frame viene eseguita all'interno del messaggio di [**\_ attivazione WM**](/windows/desktop/inputdev/wm-activate) invece che del messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="abafc-144">Note that the frame extension is done within the [**WM\_ACTIVATE**](/windows/desktop/inputdev/wm-activate) message rather than the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="abafc-145">Ciò garantisce che l'estensione del frame venga gestita correttamente quando la finestra è con le dimensioni predefinite e quando viene ingrandita.</span><span class="sxs-lookup"><span data-stu-id="abafc-145">This ensures that frame extension is handled properly when the window is at its default size and when it is maximized.</span></span>

<span data-ttu-id="abafc-146">Nell'immagine seguente viene mostrata una cornice di finestra standard (a sinistra) e la stessa cornice della finestra estesa (a destra).</span><span class="sxs-lookup"><span data-stu-id="abafc-146">The following image shows a standard window frame (on the left) and the same window frame extended (on the right).</span></span> <span data-ttu-id="abafc-147">Il frame viene esteso usando l'esempio di codice precedente e lo sfondo predefinito Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) / [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) ( \_ finestra dei colori + 1).</span><span class="sxs-lookup"><span data-stu-id="abafc-147">The frame is extended using the previous code example and the default Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)/[**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) background (COLOR\_WINDOW +1).</span></span>

![Screenshot di uno standard (a sinistra) e di un frame esteso (a destra) con sfondo bianco](images/white-sidebyside.png)

<span data-ttu-id="abafc-149">La differenza visiva tra queste due finestre è molto sottile.</span><span class="sxs-lookup"><span data-stu-id="abafc-149">The visual difference between these two windows is very subtle.</span></span> <span data-ttu-id="abafc-150">L'unica differenza tra i due è che il bordo della linea nera sottile dell'area client nella finestra a sinistra non è presente nella finestra a destra.</span><span class="sxs-lookup"><span data-stu-id="abafc-150">The only difference between the two is that the thin black line border of the client region in the window on the left is missing from the window on the right.</span></span> <span data-ttu-id="abafc-151">Il motivo di questo bordo mancante è che è incorporato nel frame esteso, ma il resto dell'area client non lo è.</span><span class="sxs-lookup"><span data-stu-id="abafc-151">The reason for this missing border is that it is incorporated into the extended frame, but the rest of the client area is not.</span></span> <span data-ttu-id="abafc-152">Affinché i frame estesi siano visibili, le aree sottostanti ogni lato dei frame estesi devono contenere dati pixel con un valore alfa pari a 0.</span><span class="sxs-lookup"><span data-stu-id="abafc-152">For the extended frames to be visible, the regions underlying each of the extended frame's sides must have pixel data with an alpha value of 0.</span></span> <span data-ttu-id="abafc-153">Il bordo nero intorno all'area client presenta dati pixel in cui tutti i valori di colore (rosso, verde, blu e alfa) vengono impostati su 0.</span><span class="sxs-lookup"><span data-stu-id="abafc-153">The black border around the client region has pixel data in which all color values (red, green, blue, and alpha) are set to 0.</span></span> <span data-ttu-id="abafc-154">Il resto dello sfondo non ha il valore alfa impostato su 0, quindi il resto del frame esteso non è visibile.</span><span class="sxs-lookup"><span data-stu-id="abafc-154">The rest of the background does not have the alpha value set to 0, so the rest of the extended frame is not visible.</span></span>

<span data-ttu-id="abafc-155">Il modo più semplice per garantire la visibilità dei frame estesi consiste nel disegnare l'intero nero dell'area client.</span><span class="sxs-lookup"><span data-stu-id="abafc-155">The easiest way to ensure that the extended frames are visible is to paint the entire client region black.</span></span> <span data-ttu-id="abafc-156">A tale scopo, inizializzare il membro *hbrBackground* della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) o [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) sull'handle del pennello nero azionario \_ .</span><span class="sxs-lookup"><span data-stu-id="abafc-156">To accomplish this, initialize the *hbrBackground* member of your [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) or [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure to the handle of the stock BLACK\_BRUSH.</span></span> <span data-ttu-id="abafc-157">La figura seguente mostra lo stesso frame standard (a sinistra) e il frame esteso (a destra) mostrati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="abafc-157">The following image shows the same standard frame (left) and extended frame (right) shown previously.</span></span> <span data-ttu-id="abafc-158">Questa volta, tuttavia, *hbrBackground* è impostato sull'handle di \_ pennello nero ottenuto dalla funzione [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) .</span><span class="sxs-lookup"><span data-stu-id="abafc-158">This time, however, *hbrBackground* is set to the BLACK\_BRUSH handle obtained from the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) function.</span></span>

![Screenshot di uno standard (a sinistra) e di un frame esteso (a destra) con sfondo nero](images/standard-extended-sidebyside.png)

## <a name="removing-the-standard-frame"></a><span data-ttu-id="abafc-160">Rimozione del frame standard</span><span class="sxs-lookup"><span data-stu-id="abafc-160">Removing the Standard Frame</span></span>

<span data-ttu-id="abafc-161">Dopo aver esteso il frame dell'applicazione e averlo reso visibile, è possibile rimuovere il frame standard.</span><span class="sxs-lookup"><span data-stu-id="abafc-161">After you have extended the frame of your application and made it visible, you can remove the standard frame.</span></span> <span data-ttu-id="abafc-162">La rimozione del frame standard consente di controllare la larghezza di ogni lato del frame anziché semplicemente di estendere il frame standard.</span><span class="sxs-lookup"><span data-stu-id="abafc-162">Removing the standard frame enables you to control the width of each side of the frame rather than simply extending the standard frame.</span></span>

<span data-ttu-id="abafc-163">Per rimuovere la cornice della finestra standard, è necessario gestire il messaggio [**WM \_ NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) , in particolare quando il valore *wParam* è **true** e il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="abafc-163">To remove the standard window frame, you must handle the [**WM\_NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) message, specifically when its *wParam* value is **TRUE** and the return value is 0.</span></span> <span data-ttu-id="abafc-164">In questo modo, l'applicazione usa l'intera area della finestra come area client, rimuovendo il frame standard.</span><span class="sxs-lookup"><span data-stu-id="abafc-164">By doing so, your application uses the entire window region as the client area, removing the standard frame.</span></span>

<span data-ttu-id="abafc-165">I risultati della gestione del messaggio [**WM \_ NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) non sono visibili fino a quando non è necessario ridimensionare l'area client.</span><span class="sxs-lookup"><span data-stu-id="abafc-165">The results of handling the [**WM\_NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) message are not visible until the client region needs to be resized.</span></span> <span data-ttu-id="abafc-166">Fino a quel momento, la visualizzazione iniziale della finestra viene visualizzata con il frame standard e i bordi estesi.</span><span class="sxs-lookup"><span data-stu-id="abafc-166">Until that time, the initial view of the window appears with the standard frame and extended borders.</span></span> <span data-ttu-id="abafc-167">Per ovviare a questo problema, è necessario ridimensionare la finestra o eseguire un'azione che avvii un messaggio **WM \_ NCCALCSIZE** al momento della creazione della finestra.</span><span class="sxs-lookup"><span data-stu-id="abafc-167">To overcome this, you must either resize your window or perform an action that initiates a **WM\_NCCALCSIZE** message at the time of window creation.</span></span> <span data-ttu-id="abafc-168">Questa operazione può essere eseguita tramite la funzione [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per spostare la finestra e ridimensionarla.</span><span class="sxs-lookup"><span data-stu-id="abafc-168">This can be accomplished by using the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to move your window and resize it.</span></span> <span data-ttu-id="abafc-169">Il codice seguente illustra una chiamata a **SetWindowPos** che impone l'invio di un messaggio **WM \_ NCCALCSIZE** usando gli attributi Rectangle della finestra corrente e il \_ flag FRAMECHANGED di SWP.</span><span class="sxs-lookup"><span data-stu-id="abafc-169">The following code demonstrates a call to **SetWindowPos** that forces a **WM\_NCCALCSIZE** message to be sent using the current window rectangle attributes and the SWP\_FRAMECHANGED flag.</span></span>


```
// Handle window creation.
if (message == WM_CREATE)
{
    RECT rcClient;
    GetWindowRect(hWnd, &rcClient);

    // Inform the application of the frame change.
    SetWindowPos(hWnd, 
                 NULL, 
                 rcClient.left, rcClient.top,
                 RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                 SWP_FRAMECHANGED);

    fCallDWP = true;
    lRet = 0;
}
```



<span data-ttu-id="abafc-170">La figura seguente mostra il frame standard (a sinistra) e il frame appena esteso senza il frame standard (Right).</span><span class="sxs-lookup"><span data-stu-id="abafc-170">The following image shows the standard frame (left) and the newly extended frame without the standard frame (right).</span></span>

![Screenshot di un frame standard (a sinistra) e di un frame personalizzato (a destra)](images/standard-custom-sidebyside.png)

## <a name="drawing-in-the-extended-frame-window"></a><span data-ttu-id="abafc-172">Disegno nella finestra cornice estesa</span><span class="sxs-lookup"><span data-stu-id="abafc-172">Drawing in the Extended Frame Window</span></span>

<span data-ttu-id="abafc-173">Rimuovendo il frame standard, si perde il disegno automatico dell'icona e del titolo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="abafc-173">By removing the standard frame, you lose the automatic drawing of the application icon and title.</span></span> <span data-ttu-id="abafc-174">Per aggiungerli nuovamente all'applicazione, è necessario crearli manualmente.</span><span class="sxs-lookup"><span data-stu-id="abafc-174">To add these back to your application, you must draw them yourself.</span></span> <span data-ttu-id="abafc-175">A tale scopo, esaminare prima di tutto la modifica apportata all'area client.</span><span class="sxs-lookup"><span data-stu-id="abafc-175">To do this, first look at the change that has occurred to your client area.</span></span>

<span data-ttu-id="abafc-176">Con la rimozione del frame standard, l'area client è ora costituita dall'intera finestra, incluso il frame esteso.</span><span class="sxs-lookup"><span data-stu-id="abafc-176">With the removal of the standard frame, your client area now consists of the entire window, including the extended frame.</span></span> <span data-ttu-id="abafc-177">Che include l'area in cui vengono disegnati i pulsanti della didascalia.</span><span class="sxs-lookup"><span data-stu-id="abafc-177">This includes the region where the caption buttons are drawn.</span></span> <span data-ttu-id="abafc-178">Nel confronto affiancato riportato di seguito, l'area client sia per il frame standard che per il frame esteso personalizzato viene evidenziata in rosso.</span><span class="sxs-lookup"><span data-stu-id="abafc-178">In the following side-by-side comparison, the client area for both the standard frame and the custom extended frame is highlighted in red.</span></span> <span data-ttu-id="abafc-179">L'area client per la finestra cornice standard (a sinistra) è l'area nera.</span><span class="sxs-lookup"><span data-stu-id="abafc-179">The client area for the standard frame window (left) is the black region.</span></span> <span data-ttu-id="abafc-180">Nella finestra cornice estesa (a destra) l'area client è l'intera finestra.</span><span class="sxs-lookup"><span data-stu-id="abafc-180">On the extended frame window (right), the client area is the entire window.</span></span>

![Screenshot di un'area client evidenziata in rosso nel frame standard e personalizzato](images/clientarea-sidebyside.png)

<span data-ttu-id="abafc-182">Poiché l'intera finestra è l'area client, è possibile creare semplicemente gli elementi desiderati nel frame esteso.</span><span class="sxs-lookup"><span data-stu-id="abafc-182">Because the entire window is your client area, you can simply draw what you want in the extended frame.</span></span> <span data-ttu-id="abafc-183">Per aggiungere un titolo all'applicazione, è sufficiente creare un testo nell'area appropriata.</span><span class="sxs-lookup"><span data-stu-id="abafc-183">To add a title to your application, just draw text in the appropriate region.</span></span> <span data-ttu-id="abafc-184">La figura seguente mostra il testo con tema disegnato nel frame della didascalia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="abafc-184">The following image shows themed text drawn on the custom caption frame.</span></span> <span data-ttu-id="abafc-185">Il titolo viene disegnato usando la funzione [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) .</span><span class="sxs-lookup"><span data-stu-id="abafc-185">The title is drawn using the [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) function.</span></span> <span data-ttu-id="abafc-186">Per visualizzare il codice che dipinge il titolo, vedere [Appendice B: disegno del titolo della didascalia](#appendix-b-painting-the-caption-title).</span><span class="sxs-lookup"><span data-stu-id="abafc-186">To view the code that paints the title, see [Appendix B: Painting the Caption Title](#appendix-b-painting-the-caption-title).</span></span>

![Screenshot di un frame personalizzato con titolo](images/custom-caption-title.png)

> [!Note]  
> <span data-ttu-id="abafc-188">Quando si disegna nel frame personalizzato, prestare attenzione quando si posizionano i controlli dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="abafc-188">When drawing in your custom frame, be careful when placing UI controls.</span></span> <span data-ttu-id="abafc-189">Poiché l'intera finestra è l'area client, è necessario regolare la posizione del controllo dell'interfaccia utente per ogni larghezza del frame se non si desidera che vengano visualizzate in o nel frame esteso.</span><span class="sxs-lookup"><span data-stu-id="abafc-189">Because the entire window is your client region, you must adjust your UI control placement for each frame width if you do not want them to appear on or in the extended frame.</span></span>

 

## <a name="enabling-hit-testing-for-the-custom-frame"></a><span data-ttu-id="abafc-190">Abilitazione dell'hit testing per il frame personalizzato</span><span class="sxs-lookup"><span data-stu-id="abafc-190">Enabling Hit Testing for the Custom Frame</span></span>

<span data-ttu-id="abafc-191">Un effetto collaterale della rimozione del frame standard è la perdita del comportamento predefinito di ridimensionamento e di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="abafc-191">A side effect of removing the standard frame is the loss of the default resizing and moving behavior.</span></span> <span data-ttu-id="abafc-192">Affinché l'applicazione possa emulare correttamente il comportamento della finestra standard, è necessario implementare la logica per gestire l'hit test del pulsante della didascalia e il ridimensionamento del frame o lo stato di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="abafc-192">For your application to properly emulate standard window behavior, you will need to implement logic to handle caption button hit testing and frame resizing/moving.</span></span>

<span data-ttu-id="abafc-193">Per l'hit test del pulsante della didascalia, DWM fornisce la funzione [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) .</span><span class="sxs-lookup"><span data-stu-id="abafc-193">For caption button hit testing, DWM provides the [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) function.</span></span> <span data-ttu-id="abafc-194">Per eseguire correttamente il test dei pulsanti della didascalia negli scenari di frame personalizzati, i messaggi devono essere prima passati a **DwmDefWindowProc** per la gestione.</span><span class="sxs-lookup"><span data-stu-id="abafc-194">To properly hit test the caption buttons in custom frame scenarios, messages should first be passed to **DwmDefWindowProc** for handling.</span></span> <span data-ttu-id="abafc-195">**DwmDefWindowProc** restituisce **true** se un messaggio viene gestito e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="abafc-195">**DwmDefWindowProc** returns **TRUE** if a message is handled and **FALSE** if it is not.</span></span> <span data-ttu-id="abafc-196">Se il messaggio non viene gestito da **DwmDefWindowProc**, l'applicazione deve gestire il messaggio stesso o passare il messaggio su [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="abafc-196">If the message is not handled by **DwmDefWindowProc**, your application should handle the message itself or pass the message onto [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="abafc-197">Per il ridimensionamento e lo stato del frame, l'applicazione deve fornire la logica di hit testing e gestire i messaggi di hit test del frame.</span><span class="sxs-lookup"><span data-stu-id="abafc-197">For frame resizing and moving, your application must provide the hit testing logic and handle frame hit test messages.</span></span> <span data-ttu-id="abafc-198">I messaggi di hit test del frame vengono inviati all'utente tramite il messaggio [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) , anche se l'applicazione crea un frame personalizzato senza il frame standard.</span><span class="sxs-lookup"><span data-stu-id="abafc-198">Frame hit test messages are sent to you through the [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message, even if your application creates a custom frame without the standard frame.</span></span> <span data-ttu-id="abafc-199">Il codice seguente illustra la gestione del messaggio **WM \_ NCHITTEST** quando [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) non la gestisce.</span><span class="sxs-lookup"><span data-stu-id="abafc-199">The following code demonstrates handling the **WM\_NCHITTEST** message when [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) does not handle it.</span></span> <span data-ttu-id="abafc-200">Per visualizzare il codice della funzione chiamata `HitTestNCA` , vedere [Appendice C: HitTestNCA Function](#appendix-c-hittestnca-function).</span><span class="sxs-lookup"><span data-stu-id="abafc-200">To see the code of the called `HitTestNCA` function, see [Appendix C: HitTestNCA Function](#appendix-c-hittestnca-function).</span></span>


```
// Handle hit testing in the NCA if not handled by DwmDefWindowProc.
if ((message == WM_NCHITTEST) && (lRet == 0))
{
    lRet = HitTestNCA(hWnd, wParam, lParam);

    if (lRet != HTNOWHERE)
    {
        fCallDWP = false;
    }
}
```



## <a name="appendix-a-sample-window-procedure"></a><span data-ttu-id="abafc-201">Appendice A: procedura della finestra di esempio</span><span class="sxs-lookup"><span data-stu-id="abafc-201">Appendix A: Sample Window Procedure</span></span>

<span data-ttu-id="abafc-202">Nell'esempio di codice riportato di seguito viene illustrata una routine della finestra e le funzioni di lavoro di supporto utilizzate per creare un'applicazione cornice personalizzata.</span><span class="sxs-lookup"><span data-stu-id="abafc-202">The following code sample demonstrates a window procedure and its supporting worker functions used to create a custom frame application.</span></span>


```
//
//  Main WinProc.
//
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    bool fCallDWP = true;
    BOOL fDwmEnabled = FALSE;
    LRESULT lRet = 0;
    HRESULT hr = S_OK;

    // Winproc worker for custom frame issues.
    hr = DwmIsCompositionEnabled(&fDwmEnabled);
    if (SUCCEEDED(hr))
    {
        lRet = CustomCaptionProc(hWnd, message, wParam, lParam, &fCallDWP);
    }

    // Winproc worker for the rest of the application.
    if (fCallDWP)
    {
        lRet = AppWinProc(hWnd, message, wParam, lParam);
    }
    return lRet;
}

//
// Message handler for handling the custom caption messages.
//
LRESULT CustomCaptionProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam, bool* pfCallDWP)
{
    LRESULT lRet = 0;
    HRESULT hr = S_OK;
    bool fCallDWP = true; // Pass on to DefWindowProc?

    fCallDWP = !DwmDefWindowProc(hWnd, message, wParam, lParam, &lRet);

    // Handle window creation.
    if (message == WM_CREATE)
    {
        RECT rcClient;
        GetWindowRect(hWnd, &rcClient);

        // Inform application of the frame change.
        SetWindowPos(hWnd, 
                     NULL, 
                     rcClient.left, rcClient.top,
                     RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                     SWP_FRAMECHANGED);

        fCallDWP = true;
        lRet = 0;
    }

    // Handle window activation.
    if (message == WM_ACTIVATE)
    {
        // Extend the frame into the client area.
        MARGINS margins;

        margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
        margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
        margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
        margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

        hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

        if (!SUCCEEDED(hr))
        {
            // Handle error.
        }

        fCallDWP = true;
        lRet = 0;
    }

    if (message == WM_PAINT)
    {
        HDC hdc;
        {
            PAINTSTRUCT ps;
            hdc = BeginPaint(hWnd, &ps);
            PaintCustomCaption(hWnd, hdc);
            EndPaint(hWnd, &ps);
        }

        fCallDWP = true;
        lRet = 0;
    }

    // Handle the non-client size message.
    if ((message == WM_NCCALCSIZE) && (wParam == TRUE))
    {
        // Calculate new NCCALCSIZE_PARAMS based on custom NCA inset.
        NCCALCSIZE_PARAMS *pncsp = reinterpret_cast<NCCALCSIZE_PARAMS*>(lParam);

        pncsp->rgrc[0].left   = pncsp->rgrc[0].left   + 0;
        pncsp->rgrc[0].top    = pncsp->rgrc[0].top    + 0;
        pncsp->rgrc[0].right  = pncsp->rgrc[0].right  - 0;
        pncsp->rgrc[0].bottom = pncsp->rgrc[0].bottom - 0;

        lRet = 0;
        
        // No need to pass the message on to the DefWindowProc.
        fCallDWP = false;
    }

    // Handle hit testing in the NCA if not handled by DwmDefWindowProc.
    if ((message == WM_NCHITTEST) && (lRet == 0))
    {
        lRet = HitTestNCA(hWnd, wParam, lParam);

        if (lRet != HTNOWHERE)
        {
            fCallDWP = false;
        }
    }

    *pfCallDWP = fCallDWP;

    return lRet;
}

//
// Message handler for the application.
//
LRESULT AppWinProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;
    HRESULT hr; 
    LRESULT result = 0;

    switch (message)
    {
        case WM_CREATE:
            {}
            break;
        case WM_COMMAND:
            wmId    = LOWORD(wParam);
            wmEvent = HIWORD(wParam);

            // Parse the menu selections:
            switch (wmId)
            {
                default:
                    return DefWindowProc(hWnd, message, wParam, lParam);
            }
            break;
        case WM_PAINT:
            {
                hdc = BeginPaint(hWnd, &ps);
                PaintCustomCaption(hWnd, hdc);
                
                // Add any drawing code here...
    
                EndPaint(hWnd, &ps);
            }
            break;
        case WM_DESTROY:
            PostQuitMessage(0);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



## <a name="appendix-b-painting-the-caption-title"></a><span data-ttu-id="abafc-203">Appendice B: disegno del titolo della didascalia</span><span class="sxs-lookup"><span data-stu-id="abafc-203">Appendix B: Painting the Caption Title</span></span>

<span data-ttu-id="abafc-204">Il codice seguente illustra come disegnare un titolo di didascalia nel frame esteso.</span><span class="sxs-lookup"><span data-stu-id="abafc-204">The following code demonstrates how to paint a caption title on the extended frame.</span></span> <span data-ttu-id="abafc-205">Questa funzione deve essere chiamata dall'interno delle chiamate a [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="abafc-205">This function must be called from within the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) calls.</span></span>


```
// Paint the title on the custom frame.
void PaintCustomCaption(HWND hWnd, HDC hdc)
{
    RECT rcClient;
    GetClientRect(hWnd, &rcClient);

    HTHEME hTheme = OpenThemeData(NULL, L"CompositedWindow::Window");
    if (hTheme)
    {
        HDC hdcPaint = CreateCompatibleDC(hdc);
        if (hdcPaint)
        {
            int cx = RECTWIDTH(rcClient);
            int cy = RECTHEIGHT(rcClient);

            // Define the BITMAPINFO structure used to draw text.
            // Note that biHeight is negative. This is done because
            // DrawThemeTextEx() needs the bitmap to be in top-to-bottom
            // order.
            BITMAPINFO dib = { 0 };
            dib.bmiHeader.biSize            = sizeof(BITMAPINFOHEADER);
            dib.bmiHeader.biWidth           = cx;
            dib.bmiHeader.biHeight          = -cy;
            dib.bmiHeader.biPlanes          = 1;
            dib.bmiHeader.biBitCount        = BIT_COUNT;
            dib.bmiHeader.biCompression     = BI_RGB;

            HBITMAP hbm = CreateDIBSection(hdc, &dib, DIB_RGB_COLORS, NULL, NULL, 0);
            if (hbm)
            {
                HBITMAP hbmOld = (HBITMAP)SelectObject(hdcPaint, hbm);

                // Setup the theme drawing options.
                DTTOPTS DttOpts = {sizeof(DTTOPTS)};
                DttOpts.dwFlags = DTT_COMPOSITED | DTT_GLOWSIZE;
                DttOpts.iGlowSize = 15;

                // Select a font.
                LOGFONT lgFont;
                HFONT hFontOld = NULL;
                if (SUCCEEDED(GetThemeSysFont(hTheme, TMT_CAPTIONFONT, &lgFont)))
                {
                    HFONT hFont = CreateFontIndirect(&lgFont);
                    hFontOld = (HFONT) SelectObject(hdcPaint, hFont);
                }

                // Draw the title.
                RECT rcPaint = rcClient;
                rcPaint.top += 8;
                rcPaint.right -= 125;
                rcPaint.left += 8;
                rcPaint.bottom = 50;
                DrawThemeTextEx(hTheme, 
                                hdcPaint, 
                                0, 0, 
                                szTitle, 
                                -1, 
                                DT_LEFT | DT_WORD_ELLIPSIS, 
                                &rcPaint, 
                                &DttOpts);

                // Blit text to the frame.
                BitBlt(hdc, 0, 0, cx, cy, hdcPaint, 0, 0, SRCCOPY);

                SelectObject(hdcPaint, hbmOld);
                if (hFontOld)
                {
                    SelectObject(hdcPaint, hFontOld);
                }
                DeleteObject(hbm);
            }
            DeleteDC(hdcPaint);
        }
        CloseThemeData(hTheme);
    }
}
```



## <a name="appendix-c-hittestnca-function"></a><span data-ttu-id="abafc-206">Appendice C: funzione HitTestNCA</span><span class="sxs-lookup"><span data-stu-id="abafc-206">Appendix C: HitTestNCA Function</span></span>

<span data-ttu-id="abafc-207">Il codice seguente illustra la `HitTestNCA` funzione usata nell' [Abilitazione dell'hit testing per il frame personalizzato](#enabling-hit-testing-for-the-custom-frame).</span><span class="sxs-lookup"><span data-stu-id="abafc-207">The following code shows the `HitTestNCA` function used in [Enabling Hit Testing for the Custom Frame](#enabling-hit-testing-for-the-custom-frame).</span></span> <span data-ttu-id="abafc-208">Questa funzione gestisce la logica di hit testing per [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) quando [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) non gestisce il messaggio.</span><span class="sxs-lookup"><span data-stu-id="abafc-208">This function handles the hit testing logic for the [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) when [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) does not handle the message.</span></span>


```
// Hit test the frame for resizing and moving.
LRESULT HitTestNCA(HWND hWnd, WPARAM wParam, LPARAM lParam)
{
    // Get the point coordinates for the hit test.
    POINT ptMouse = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam)};

    // Get the window rectangle.
    RECT rcWindow;
    GetWindowRect(hWnd, &rcWindow);

    // Get the frame rectangle, adjusted for the style without a caption.
    RECT rcFrame = { 0 };
    AdjustWindowRectEx(&rcFrame, WS_OVERLAPPEDWINDOW & ~WS_CAPTION, FALSE, NULL);

    // Determine if the hit test is for resizing. Default middle (1,1).
    USHORT uRow = 1;
    USHORT uCol = 1;
    bool fOnResizeBorder = false;

    // Determine if the point is at the top or bottom of the window.
    if (ptMouse.y >= rcWindow.top && ptMouse.y < rcWindow.top + TOPEXTENDWIDTH)
    {
        fOnResizeBorder = (ptMouse.y < (rcWindow.top - rcFrame.top));
        uRow = 0;
    }
    else if (ptMouse.y < rcWindow.bottom && ptMouse.y >= rcWindow.bottom - BOTTOMEXTENDWIDTH)
    {
        uRow = 2;
    }

    // Determine if the point is at the left or right of the window.
    if (ptMouse.x >= rcWindow.left && ptMouse.x < rcWindow.left + LEFTEXTENDWIDTH)
    {
        uCol = 0; // left side
    }
    else if (ptMouse.x < rcWindow.right && ptMouse.x >= rcWindow.right - RIGHTEXTENDWIDTH)
    {
        uCol = 2; // right side
    }

    // Hit test (HTTOPLEFT, ... HTBOTTOMRIGHT)
    LRESULT hitTests[3][3] = 
    {
        { HTTOPLEFT,    fOnResizeBorder ? HTTOP : HTCAPTION,    HTTOPRIGHT },
        { HTLEFT,       HTNOWHERE,     HTRIGHT },
        { HTBOTTOMLEFT, HTBOTTOM, HTBOTTOMRIGHT },
    };

    return hitTests[uRow][uCol];
}
```



## <a name="related-topics"></a><span data-ttu-id="abafc-209">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="abafc-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abafc-210">Cenni preliminari di Gestione finestre desktop</span><span class="sxs-lookup"><span data-stu-id="abafc-210">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> </dl>

 

 