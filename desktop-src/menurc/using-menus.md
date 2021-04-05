---
title: Uso di menu
description: In questa sezione vengono forniti esempi di codice per le attività correlate ai menu.
ms.assetid: b1391e37-a146-46ec-a329-aa57cfcfd351
keywords:
- risorse, menu
- menu, creazione
- menu-risorse modello
- risorse, menu-modello
- menu esteso-formato modello
- formato vecchio modello di menu
- caricamento dei menu-risorse modello
- menu, classe
- menu, collegamento
- creazione di menu
- menu della classe
- menu di scelta rapida
- bitmap delle voci di menu
- menu, proprietario disegnato
- menu creati dal proprietario
- bitmap di segno di spunta personalizzati
- menu, caselle di controllo
- menu, tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d216b5fe5e6c25a98b5bdf3abe9d55b4bb0b34f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726751"
---
# <a name="using-menus"></a><span data-ttu-id="a4241-121">Uso di menu</span><span class="sxs-lookup"><span data-stu-id="a4241-121">Using Menus</span></span>

<span data-ttu-id="a4241-122">In questa sezione vengono descritte le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4241-122">This section describes the following tasks:</span></span>

-   [<span data-ttu-id="a4241-123">Uso di una risorsa Menu-Template</span><span class="sxs-lookup"><span data-stu-id="a4241-123">Using a Menu-Template Resource</span></span>](#using-a-menu-template-resource)
    -   [<span data-ttu-id="a4241-124">Formato Menu-Template esteso</span><span class="sxs-lookup"><span data-stu-id="a4241-124">Extended Menu-Template Format</span></span>](#extended-menu-template-format)
    -   [<span data-ttu-id="a4241-125">Vecchio formato Menu-Template</span><span class="sxs-lookup"><span data-stu-id="a4241-125">Old Menu-Template Format</span></span>](#old-menu-template-format)
    -   [<span data-ttu-id="a4241-126">Caricamento di una risorsa Menu-Template</span><span class="sxs-lookup"><span data-stu-id="a4241-126">Loading a Menu-Template Resource</span></span>](#loading-a-menu-template-resource)
    -   [<span data-ttu-id="a4241-127">Creazione di un menu classe</span><span class="sxs-lookup"><span data-stu-id="a4241-127">Creating a Class Menu</span></span>](#creating-a-class-menu)
-   [<span data-ttu-id="a4241-128">Creazione di un menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="a4241-128">Creating a Shortcut Menu</span></span>](#creating-a-shortcut-menu)
    -   [<span data-ttu-id="a4241-129">Elaborazione del \_ messaggio WM ContextMenu</span><span class="sxs-lookup"><span data-stu-id="a4241-129">Processing the WM\_CONTEXTMENU Message</span></span>](/windows)
    -   [<span data-ttu-id="a4241-130">Creazione di un menu di scelta rapida Font-Attributes</span><span class="sxs-lookup"><span data-stu-id="a4241-130">Creating a Shortcut Font-Attributes Menu</span></span>](#creating-a-shortcut-font-attributes-menu)
    -   [<span data-ttu-id="a4241-131">Visualizzazione di un menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="a4241-131">Displaying a Shortcut Menu</span></span>](#displaying-a-shortcut-menu)
-   [<span data-ttu-id="a4241-132">Uso di bitmap Menu-Item</span><span class="sxs-lookup"><span data-stu-id="a4241-132">Using Menu-Item Bitmaps</span></span>](#using-menu-item-bitmaps)
    -   [<span data-ttu-id="a4241-133">Impostazione del flag di tipo bitmap</span><span class="sxs-lookup"><span data-stu-id="a4241-133">Setting the Bitmap Type Flag</span></span>](#setting-the-bitmap-type-flag)
    -   [<span data-ttu-id="a4241-134">Creazione della bitmap</span><span class="sxs-lookup"><span data-stu-id="a4241-134">Creating the Bitmap</span></span>](#creating-the-bitmap)
    -   [<span data-ttu-id="a4241-135">Aggiunta di linee e grafici a un menu</span><span class="sxs-lookup"><span data-stu-id="a4241-135">Adding Lines and Graphs to a Menu</span></span>](#adding-lines-and-graphs-to-a-menu)
    -   [<span data-ttu-id="a4241-136">Esempio di bitmap Menu-Item</span><span class="sxs-lookup"><span data-stu-id="a4241-136">Example of Menu-Item Bitmaps</span></span>](#example-of-menu-item-bitmaps)
-   [<span data-ttu-id="a4241-137">Creazione di voci di menu Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="a4241-137">Creating Owner-Drawn Menu Items</span></span>](#creating-owner-drawn-menu-items)
    -   [<span data-ttu-id="a4241-138">Impostazione del flag di Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="a4241-138">Setting the Owner-Drawn Flag</span></span>](#setting-the-owner-drawn-flag)
    -   [<span data-ttu-id="a4241-139">Menu creati dal proprietario e il \_ messaggio WM MeasureItem</span><span class="sxs-lookup"><span data-stu-id="a4241-139">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>](/windows)
    -   [<span data-ttu-id="a4241-140">Menu creati dal proprietario e messaggio di WM \_ DrawItem</span><span class="sxs-lookup"><span data-stu-id="a4241-140">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>](/windows)
    -   [<span data-ttu-id="a4241-141">Menu creati dal proprietario e il \_ messaggio WM MENUCHAR</span><span class="sxs-lookup"><span data-stu-id="a4241-141">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>](/windows)
    -   [<span data-ttu-id="a4241-142">Impostazione dei tipi di carattere per le stringhe di testo Menu-Item</span><span class="sxs-lookup"><span data-stu-id="a4241-142">Setting Fonts for Menu-Item Text Strings</span></span>](#setting-fonts-for-menu-item-text-strings)
    -   [<span data-ttu-id="a4241-143">Esempio di voci di menu Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="a4241-143">Example of Owner-Drawn Menu Items</span></span>](#example-of-owner-drawn-menu-items)
-   [<span data-ttu-id="a4241-144">Uso di bitmap con segno di spunta personalizzato</span><span class="sxs-lookup"><span data-stu-id="a4241-144">Using Custom Check Mark Bitmaps</span></span>](#using-custom-check-mark-bitmaps)
    -   [<span data-ttu-id="a4241-145">Creazione di bitmap di segno di spunta personalizzati</span><span class="sxs-lookup"><span data-stu-id="a4241-145">Creating Custom Check Mark Bitmaps</span></span>](#creating-custom-check-mark-bitmaps)
    -   [<span data-ttu-id="a4241-146">Associazione di bitmap a una voce di menu</span><span class="sxs-lookup"><span data-stu-id="a4241-146">Associating Bitmaps with a Menu Item</span></span>](#associating-bitmaps-with-a-menu-item)
    -   [<span data-ttu-id="a4241-147">Impostazione dell'attributo Check-Mark</span><span class="sxs-lookup"><span data-stu-id="a4241-147">Setting the Check-mark Attribute</span></span>](#setting-the-check-mark-attribute)
    -   [<span data-ttu-id="a4241-148">Simulazione di caselle di controllo in un menu</span><span class="sxs-lookup"><span data-stu-id="a4241-148">Simulating Check Boxes in a Menu</span></span>](#simulating-check-boxes-in-a-menu)
    -   [<span data-ttu-id="a4241-149">Esempio di utilizzo di bitmap di segno di spunta personalizzate</span><span class="sxs-lookup"><span data-stu-id="a4241-149">Example of Using Custom Check-mark Bitmaps</span></span>](#example-of-using-custom-check-mark-bitmaps)

## <a name="using-a-menu-template-resource"></a><span data-ttu-id="a4241-150">Uso di una risorsa Menu-Template</span><span class="sxs-lookup"><span data-stu-id="a4241-150">Using a Menu-Template Resource</span></span>

<span data-ttu-id="a4241-151">In genere si include un menu in un'applicazione creando una risorsa modello di menu e quindi caricando il menu in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a4241-151">You typically include a menu in an application by creating a menu-template resource and then loading the menu at run time.</span></span> <span data-ttu-id="a4241-152">In questa sezione viene descritto il formato di un modello di menu e viene illustrato come caricare una risorsa modello di menu e utilizzarla nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-152">This section describes the format of a menu template, and explains how to load a menu-template resource and use it in your application.</span></span> <span data-ttu-id="a4241-153">Per informazioni sulla creazione di una risorsa modello di menu, vedere la documentazione inclusa con gli strumenti di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="a4241-153">For information about creating a menu-template resource, see the documentation included with your development tools.</span></span>

-   [<span data-ttu-id="a4241-154">Formato Menu-Template esteso</span><span class="sxs-lookup"><span data-stu-id="a4241-154">Extended Menu-Template Format</span></span>](#extended-menu-template-format)
-   [<span data-ttu-id="a4241-155">Vecchio formato Menu-Template</span><span class="sxs-lookup"><span data-stu-id="a4241-155">Old Menu-Template Format</span></span>](#old-menu-template-format)
-   [<span data-ttu-id="a4241-156">Caricamento di una risorsa Menu-Template</span><span class="sxs-lookup"><span data-stu-id="a4241-156">Loading a Menu-Template Resource</span></span>](#loading-a-menu-template-resource)
-   [<span data-ttu-id="a4241-157">Creazione di un menu classe</span><span class="sxs-lookup"><span data-stu-id="a4241-157">Creating a Class Menu</span></span>](#creating-a-class-menu)

### <a name="extended-menu-template-format"></a><span data-ttu-id="a4241-158">Formato Menu-Template esteso</span><span class="sxs-lookup"><span data-stu-id="a4241-158">Extended Menu-Template Format</span></span>

<span data-ttu-id="a4241-159">Il formato di modello del menu esteso supporta funzionalità di menu aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="a4241-159">The extended menu-template format supports additional menu functionality.</span></span> <span data-ttu-id="a4241-160">Analogamente ai menu standard, le risorse del modello menu esteso hanno il tipo di risorsa **\_ menu RT** .</span><span class="sxs-lookup"><span data-stu-id="a4241-160">Like standard menu-template resources, extended menu-template resources have the **RT\_MENU** resource type.</span></span> <span data-ttu-id="a4241-161">Il sistema distingue i due formati di risorse in base al numero di versione, che è il primo membro dell'intestazione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a4241-161">The system distinguishes the two resource formats by the version number, which is the first member of the resource header.</span></span>

<span data-ttu-id="a4241-162">Un modello di menu esteso è costituito da una struttura di [**\_ \_ intestazione del modello menuex**](menuex-template-header.md) seguita da una o più strutture di definizione degli elementi dell' [**\_ \_ elemento modello menuex**](menuex-template-item.md) .</span><span class="sxs-lookup"><span data-stu-id="a4241-162">An extended menu template consists of a [**MENUEX\_TEMPLATE\_HEADER**](menuex-template-header.md) structure followed by one more [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) item definition structures.</span></span>

### <a name="old-menu-template-format"></a><span data-ttu-id="a4241-163">Vecchio formato Menu-Template</span><span class="sxs-lookup"><span data-stu-id="a4241-163">Old Menu-Template Format</span></span>

<span data-ttu-id="a4241-164">Un modello di menu obsoleto (Microsoft Windows NT 3,51 e versioni precedenti) definisce un menu, ma non supporta la nuova funzionalità di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-164">An old menu template (Microsoft Windows NT 3.51 and earlier) defines a menu, but does not support the new menu functionality.</span></span> <span data-ttu-id="a4241-165">Una risorsa del modello di menu precedente presenta il tipo di risorsa **\_ menu RT** .</span><span class="sxs-lookup"><span data-stu-id="a4241-165">An old menu-template resource has the **RT\_MENU** resource type.</span></span>

<span data-ttu-id="a4241-166">Un modello di menu obsoleto è costituito da una struttura [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) seguita da una o più strutture [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) .</span><span class="sxs-lookup"><span data-stu-id="a4241-166">An old menu template consists of a [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) structure followed by one or more [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) structures.</span></span>

### <a name="loading-a-menu-template-resource"></a><span data-ttu-id="a4241-167">Caricamento di una risorsa Menu-Template</span><span class="sxs-lookup"><span data-stu-id="a4241-167">Loading a Menu-Template Resource</span></span>

<span data-ttu-id="a4241-168">Per caricare una risorsa modello di menu, usare la funzione [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) , specificando un handle per il modulo che contiene la risorsa e l'identificatore del modello di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-168">To load a menu-template resource, use the [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) function, specifying a handle to the module that contains the resource and the menu template's identifier.</span></span> <span data-ttu-id="a4241-169">La funzione **LoadMenu** restituisce un handle di menu che è possibile usare per assegnare il menu a una finestra.</span><span class="sxs-lookup"><span data-stu-id="a4241-169">The **LoadMenu** function returns a menu handle that you can use to assign the menu to a window.</span></span> <span data-ttu-id="a4241-170">Questa finestra diventa la finestra proprietaria del menu che riceve tutti i messaggi generati dal menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-170">This window becomes the menu's owner window, receiving all the messages generated by the menu.</span></span>

<span data-ttu-id="a4241-171">Per creare un menu da un modello di menu già in memoria, usare la funzione [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .</span><span class="sxs-lookup"><span data-stu-id="a4241-171">To create a menu from a menu template that is already in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span> <span data-ttu-id="a4241-172">Questa operazione è utile se l'applicazione genera dinamicamente modelli di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-172">This is useful if your application generates menu templates dynamically.</span></span>

<span data-ttu-id="a4241-173">Per assegnare un menu a una finestra, usare la funzione [**semenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) o specificare l'handle del menu nel parametro *HMenu* della funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) durante la creazione di una finestra.</span><span class="sxs-lookup"><span data-stu-id="a4241-173">To assign a menu to a window, use the [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) function or specify the menu's handle in the *hMenu* parameter of the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function when creating a window.</span></span> <span data-ttu-id="a4241-174">Un altro modo per assegnare un menu a una finestra consiste nel specificare un modello di menu quando si registra una classe della finestra; il modello identifica il menu specificato come menu della classe per la classe della finestra.</span><span class="sxs-lookup"><span data-stu-id="a4241-174">Another way you can assign a menu to a window is to specify a menu template when you register a window class; the template identifies the specified menu as the class menu for that window class.</span></span>

<span data-ttu-id="a4241-175">Per fare in modo che il sistema assegni automaticamente un menu specifico a una finestra, specificare il modello del menu quando si registra la classe della finestra.</span><span class="sxs-lookup"><span data-stu-id="a4241-175">To have the system automatically assign a specific menu to a window, specify the menu's template when you register the window's class.</span></span> <span data-ttu-id="a4241-176">Il modello identifica il menu specificato come menu della classe per la classe della finestra.</span><span class="sxs-lookup"><span data-stu-id="a4241-176">The template identifies the specified menu as the class menu for that window class.</span></span> <span data-ttu-id="a4241-177">Quindi, quando si crea una finestra della classe specificata, il sistema assegna automaticamente il menu specificato alla finestra.</span><span class="sxs-lookup"><span data-stu-id="a4241-177">Then, when you create a window of the specified class, the system automatically assigns the specified menu to the window.</span></span>

<span data-ttu-id="a4241-178">Non è possibile assegnare un menu a una finestra che rappresenta una finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="a4241-178">You cannot assign a menu to a window that is a child window.</span></span>

<span data-ttu-id="a4241-179">Per creare un menu di classe, includere l'identificatore della risorsa del modello di menu come membro **lpszMenuName** di una struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) e quindi passare un puntatore alla struttura alla funzione [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) .</span><span class="sxs-lookup"><span data-stu-id="a4241-179">To create a class menu, include the identifier of the menu-template resource as the **lpszMenuName** member of a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure and then pass a pointer to the structure to the [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function.</span></span>

### <a name="creating-a-class-menu"></a><span data-ttu-id="a4241-180">Creazione di un menu classe</span><span class="sxs-lookup"><span data-stu-id="a4241-180">Creating a Class Menu</span></span>

<span data-ttu-id="a4241-181">Nell'esempio seguente viene illustrato come creare un menu di classe per un'applicazione, creare una finestra che utilizza il menu classe ed elaborare i comandi di menu nella procedura della finestra.</span><span class="sxs-lookup"><span data-stu-id="a4241-181">The following example shows how to create a class menu for an application, create a window that uses the class menu, and process menu commands in the window procedure.</span></span>

<span data-ttu-id="a4241-182">Di seguito è riportata la parte pertinente del file di intestazione dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="a4241-182">Following is the relevant portion of the application's header file:</span></span>


```
// Menu-template resource identifier 
 
#define IDM_MYMENURESOURCE   3
```



<span data-ttu-id="a4241-183">Di seguito sono riportate le parti pertinenti dell'applicazione stessa:</span><span class="sxs-lookup"><span data-stu-id="a4241-183">Following are the relevant portions of the application itself:</span></span>


```
HINSTANCE hinst; 
 
int APIENTRY WinMain(HINSTANCE hinstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg = { };  // message 
    WNDCLASS wc;    // windowclass data 
    HWND hwnd;      // handle to the main window 
 
    // Create the window class for the main window. Specify 
    // the identifier of the menu-template resource as the 
    // lpszMenuName member of the WNDCLASS structure to create 
    // the class menu. 
 
    wc.style = 0; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  MAKEINTRESOURCE(IDM_MYMENURESOURCE); 
    wc.lpszClassName = "MainWClass"; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    hinst = hinstance; 
 
    // Create the main window. Set the hmenu parameter to NULL so 
    // that the system uses the class menu for the window. 
 
    hwnd = CreateWindow("MainWClass", "Sample Application", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, hinstance, 
        NULL); 
 
    if (hwnd == NULL) 
        return FALSE; 
 
    // Make the window visible and send a WM_PAINT message to the 
    // window procedure. 
 
    ShowWindow(hwnd, nCmdShow); 
    UpdateWindow(hwnd); 
 
    // Start the main message loop. 
 
    while (GetMessage(&msg, NULL, 0, 0)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
    return msg.wParam; 
        UNREFERENCED_PARAMETER(hPrevInstance); 
} 
 
 
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    switch (uMsg) 
    { 
        // Process other window messages. 
 
        case WM_COMMAND: 
 
            // Test for the identifier of a command item. 
 
            switch(LOWORD(wParam)) 
            { 
                case IDM_FI_OPEN: 
                    DoFileOpen();   // application-defined 
                    break; 
 
                case IDM_FI_CLOSE: 
                    DoFileClose();  // application-defined 
                    break; 
                // Process other menu commands. 
 
                default: 
                    break; 
 
            } 
            return 0; 
 
        // Process other window messages. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="creating-a-shortcut-menu"></a><span data-ttu-id="a4241-184">Creazione di un menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="a4241-184">Creating a Shortcut Menu</span></span>

<span data-ttu-id="a4241-185">Per usare un menu di scelta rapida in un'applicazione, passare il relativo handle alla funzione [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .</span><span class="sxs-lookup"><span data-stu-id="a4241-185">To use a shortcut menu in an application, pass its handle to the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function.</span></span> <span data-ttu-id="a4241-186">Un'applicazione in genere chiama **TrackPopupMenuEx** in una routine di finestra in risposta a un messaggio generato dall'utente, ad esempio [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) o [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown).</span><span class="sxs-lookup"><span data-stu-id="a4241-186">An application typically calls **TrackPopupMenuEx** in a window procedure in response to a user-generated message, such as [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) or [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown).</span></span>

<span data-ttu-id="a4241-187">Oltre all'handle del menu popup, [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) richiede di specificare un handle per la finestra proprietaria, la posizione del menu di scelta rapida (in coordinate dello schermo) e il pulsante del mouse che l'utente può usare per scegliere un elemento.</span><span class="sxs-lookup"><span data-stu-id="a4241-187">In addition to the pop-up menu handle, [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) requires that you specify a handle to the owner window, the position of the shortcut menu (in screen coordinates), and the mouse button that the user can use to choose an item.</span></span>

<span data-ttu-id="a4241-188">La funzione [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) precedente è ancora supportata, ma le nuove applicazioni devono usare la funzione [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .</span><span class="sxs-lookup"><span data-stu-id="a4241-188">The older [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function is still supported, but new applications should use the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function.</span></span> <span data-ttu-id="a4241-189">La funzione **TrackPopupMenuEx** richiede gli stessi parametri di **TrackPopupMenu**, ma consente anche di specificare una parte della schermata che non deve essere nascosta nel menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-189">The **TrackPopupMenuEx** function requires the same parameters as **TrackPopupMenu**, but also lets you specify a portion of the screen that the menu should not obscure.</span></span> <span data-ttu-id="a4241-190">Un'applicazione in genere chiama queste funzioni in una routine della finestra durante l'elaborazione del messaggio del [**\_ ContextMenu di WM**](wm-contextmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="a4241-190">An application typically calls these functions in a window procedure when processing the [**WM\_CONTEXTMENU**](wm-contextmenu.md) message.</span></span>

<span data-ttu-id="a4241-191">È possibile specificare la posizione di un menu di scelta rapida fornendo le coordinate x e y insieme al flag **TPM \_ CENTERALIGN**, **TPM \_ LEFTALIGN** o **TPM \_ RIGHTALIGN** .</span><span class="sxs-lookup"><span data-stu-id="a4241-191">You can specify the position of a shortcut menu by providing x- and y-coordinates along with the **TPM\_CENTERALIGN**, **TPM\_LEFTALIGN**, or **TPM\_RIGHTALIGN** flag.</span></span> <span data-ttu-id="a4241-192">Il flag specifica la posizione del menu di scelta rapida rispetto alle coordinate x e y.</span><span class="sxs-lookup"><span data-stu-id="a4241-192">The flag specifies the position of the shortcut menu relative to the x- and y-coordinates.</span></span>

<span data-ttu-id="a4241-193">È necessario consentire all'utente di scegliere un elemento da un menu di scelta rapida utilizzando lo stesso pulsante del mouse utilizzato per visualizzare il menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-193">You should permit the user to choose an item from a shortcut menu by using the same mouse button used to display the menu.</span></span> <span data-ttu-id="a4241-194">A tale scopo, specificare il flag **TPM \_ LEFTBUTTON** o **TPM \_ RIGHTBUTTON** per indicare quale pulsante del mouse può essere utilizzato dall'utente per scegliere una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-194">To do this, specify either **TPM\_LEFTBUTTON** or **TPM\_RIGHTBUTTON** flag to indicate which mouse button the user can use to choose a menu item.</span></span>

-   [<span data-ttu-id="a4241-195">Elaborazione del \_ messaggio WM ContextMenu</span><span class="sxs-lookup"><span data-stu-id="a4241-195">Processing the WM\_CONTEXTMENU Message</span></span>](/windows)
-   [<span data-ttu-id="a4241-196">Creazione di un menu di scelta rapida Font-Attributes</span><span class="sxs-lookup"><span data-stu-id="a4241-196">Creating a Shortcut Font-Attributes Menu</span></span>](#creating-a-shortcut-font-attributes-menu)
-   [<span data-ttu-id="a4241-197">Visualizzazione di un menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="a4241-197">Displaying a Shortcut Menu</span></span>](#displaying-a-shortcut-menu)

### <a name="processing-the-wm_contextmenu-message"></a><span data-ttu-id="a4241-198">Elaborazione del \_ messaggio WM ContextMenu</span><span class="sxs-lookup"><span data-stu-id="a4241-198">Processing the WM\_CONTEXTMENU Message</span></span>

<span data-ttu-id="a4241-199">Il [**messaggio WM \_ ContextMenu**](wm-contextmenu.md) viene generato quando la routine della finestra di un'applicazione passa il messaggio [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) o [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="a4241-199">The [**WM\_CONTEXTMENU**](wm-contextmenu.md) message is generated when an application's window procedure passes the [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) or [**WM\_NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="a4241-200">L'applicazione può elaborare questo messaggio per visualizzare un menu di scelta rapida appropriato per una parte specifica dello schermo.</span><span class="sxs-lookup"><span data-stu-id="a4241-200">The application can process this message to display a shortcut menu appropriate to a specific portion of its screen.</span></span> <span data-ttu-id="a4241-201">Se l'applicazione non visualizza un menu di scelta rapida, deve passare il messaggio a **DefWindowProc** per la gestione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a4241-201">If the application does not display a shortcut menu, it should pass the message to **DefWindowProc** for default handling.</span></span>

<span data-ttu-id="a4241-202">Di seguito è riportato un esempio di elaborazione dei messaggi di [**WM \_ ContextMenu**](wm-contextmenu.md) come potrebbe apparire nella procedura della finestra di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-202">Following is an example of [**WM\_CONTEXTMENU**](wm-contextmenu.md) message processing as it might appear in an application's window procedure.</span></span> <span data-ttu-id="a4241-203">Le parole di ordine inferiore e superiore del parametro *lParam* specificano le coordinate dello schermo del mouse quando viene rilasciato il pulsante destro del mouse (si noti che queste coordinate possono richiedere valori negativi nei sistemi con più monitoraggi).</span><span class="sxs-lookup"><span data-stu-id="a4241-203">The low-order and high-order words of the *lParam* parameter specify the screen coordinates of the mouse when the right mouse button is released (note that these coordinates can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="a4241-204">La funzione **oncontextmenu** definita dall'applicazione restituisce **true** se Visualizza un menu di scelta rapida; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="a4241-204">The application-defined **OnContextMenu** function returns **TRUE** if it displays a context menu, or **FALSE** if it does not.</span></span>


```
case WM_CONTEXTMENU: 
    if (!OnContextMenu(hwnd, GET_X_LPARAM(lParam),
              GET_Y_LPARAM(lParam))) 
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    break; 
```



<span data-ttu-id="a4241-205">La funzione OnContextMenu definita dall'applicazione seguente visualizza un menu di scelta rapida se la posizione del mouse specificata si trova all'interno dell'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="a4241-205">The following application-defined OnContextMenu function displays a shortcut menu if the specified mouse position is within the window's client area.</span></span> <span data-ttu-id="a4241-206">Una funzione più sofisticata potrebbe visualizzare uno dei diversi menu, a seconda della parte dell'area client specificata.</span><span class="sxs-lookup"><span data-stu-id="a4241-206">A more sophisticated function might display one of several different menus, depending on which portion of the client area is specified.</span></span> <span data-ttu-id="a4241-207">Per visualizzare effettivamente il menu di scelta rapida, in questo esempio viene chiamata una funzione definita dall'applicazione denominata DisplayContextMenu.</span><span class="sxs-lookup"><span data-stu-id="a4241-207">To actually display the shortcut menu, this example calls an application-defined function called DisplayContextMenu.</span></span> <span data-ttu-id="a4241-208">Per una descrizione di questa funzione, vedere [visualizzazione di un menu di scelta rapida](#displaying-a-shortcut-menu).</span><span class="sxs-lookup"><span data-stu-id="a4241-208">For a description of this function, see [Displaying a Shortcut Menu](#displaying-a-shortcut-menu).</span></span>


```
BOOL WINAPI OnContextMenu(HWND hwnd, int x, int y) 
{ 
    RECT rc;                    // client area of window 
    POINT pt = { x, y };        // location of mouse click 
 
    // Get the bounding rectangle of the client area. 
 
    GetClientRect(hwnd, &rc); 
 
    // Convert the mouse position to client coordinates. 
 
    ScreenToClient(hwnd, &pt); 
 
    // If the position is in the client area, display a  
    // shortcut menu. 
 
    if (PtInRect(&rc, pt)) 
    { 
        ClientToScreen(hwnd, &pt); 
        DisplayContextMenu(hwnd, pt); 
        return TRUE; 
    } 
 
    // Return FALSE if no menu is displayed. 
 
    return FALSE; 
} 
```



### <a name="creating-a-shortcut-font-attributes-menu"></a><span data-ttu-id="a4241-209">Creazione di un menu di scelta rapida Font-Attributes</span><span class="sxs-lookup"><span data-stu-id="a4241-209">Creating a Shortcut Font-Attributes Menu</span></span>

<span data-ttu-id="a4241-210">Nell'esempio riportato in questa sezione sono contenute parti del codice di un'applicazione che consente di creare e visualizzare un menu di scelta rapida che consente all'utente di impostare tipi di carattere e attributi del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="a4241-210">The example in this section contains portions of code from an application that creates and displays a shortcut menu that enables the user to set fonts and font attributes.</span></span> <span data-ttu-id="a4241-211">L'applicazione Visualizza il menu nell'area client della finestra principale ogni volta che l'utente fa clic con il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="a4241-211">The application displays the menu in the client area of its main window whenever the user clicks the left mouse button.</span></span>

<span data-ttu-id="a4241-212">Ecco il modello di menu per il menu di scelta rapida fornito nel file di definizione delle risorse dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-212">Here is the menu template for the shortcut menu that is provided in the application's resource-definition file.</span></span>


```
PopupMenu MENU 
BEGIN 
  POPUP "Dummy Popup" 
    BEGIN 
      POPUP "Fonts" 
        BEGIN 
          MENUITEM "Courier",     IDM_FONT_COURIER 
          MENUITEM "Times Roman", IDM_FONT_TMSRMN 
          MENUITEM "Swiss",       IDM_FONT_SWISS 
          MENUITEM "Helvetica",   IDM_FONT_HELV 
          MENUITEM "Old English", IDM_FONT_OLDENG 
        END 
      POPUP "Sizes" 
        BEGIN 
          MENUITEM "7",  IDM_SIZE_7 
          MENUITEM "8",  IDM_SIZE_8 
          MENUITEM "9",  IDM_SIZE_9 
          MENUITEM "10", IDM_SIZE_10 
          MENUITEM "11", IDM_SIZE_11 
          MENUITEM "12", IDM_SIZE_12 
          MENUITEM "14", IDM_SIZE_14 
        END 
      POPUP "Styles" 
        BEGIN 
          MENUITEM "Bold",        IDM_STYLE_BOLD 
          MENUITEM "Italic",      IDM_STYLE_ITALIC 
          MENUITEM "Strike Out",  IDM_STYLE_SO 
          MENUITEM "Superscript", IDM_STYLE_SUPER 
          MENUITEM "Subscript",   IDM_STYLE_SUB 
        END 
    END 
 
END 
```



<span data-ttu-id="a4241-213">Nell'esempio seguente vengono fornite le funzioni di supporto e di routine della finestra utilizzate per creare e visualizzare il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="a4241-213">The following example gives the window procedure and supporting functions used to create and display the shortcut menu.</span></span>


```
LRESULT APIENTRY MenuWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rc;    // client area             
    POINT pt;   // location of mouse click  
 
    switch (uMsg) 
    { 
        case WM_LBUTTONDOWN: 
 
            // Get the bounding rectangle of the client area. 
 
            GetClientRect(hwnd, (LPRECT) &rc); 
 
            // Get the client coordinates for the mouse click.  
 
            pt.x = GET_X_LPARAM(lParam); 
            pt.y = GET_Y_LPARAM(lParam); 
 
            // If the mouse click took place inside the client 
            // area, execute the application-defined function 
            // that displays the shortcut menu. 
 
            if (PtInRect((LPRECT) &rc, pt)) 
                HandlePopupMenu(hwnd, pt); 
            break; 
        // Process other window messages.  
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
 
VOID APIENTRY HandlePopupMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // menu template          
    HMENU hmenuTrackPopup;  // shortcut menu   
 
    //  Load the menu template containing the shortcut menu from the 
    //  application's resources. 
 
    hmenu = LoadMenu(hinst, "PopupMenu"); 
    if (hmenu == NULL) 
        return; 
 
    // Get the first shortcut menu in the menu template. This is the 
    // menu that TrackPopupMenu displays. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // TrackPopup uses screen coordinates, so convert the 
    // coordinates of the mouse click to screen coordinates. 
 
    ClientToScreen(hwnd, (LPPOINT) &pt); 
 
    // Draw and track the shortcut menu.  
 
    TrackPopupMenu(hmenuTrackPopup, TPM_LEFTALIGN | TPM_LEFTBUTTON, 
        pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



### <a name="displaying-a-shortcut-menu"></a><span data-ttu-id="a4241-214">Visualizzazione di un menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="a4241-214">Displaying a Shortcut Menu</span></span>

<span data-ttu-id="a4241-215">La funzione mostrata nell'esempio seguente visualizza un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="a4241-215">The function shown in the following example displays a shortcut menu.</span></span>

<span data-ttu-id="a4241-216">L'applicazione include una risorsa di menu identificata dalla stringa "ShortcutExample".</span><span class="sxs-lookup"><span data-stu-id="a4241-216">The application includes a menu resource identified by the string "ShortcutExample."</span></span> <span data-ttu-id="a4241-217">La barra dei menu contiene semplicemente un nome di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-217">The menu bar simply contains a menu name.</span></span> <span data-ttu-id="a4241-218">L'applicazione usa la funzione [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) per visualizzare il menu associato a questa voce di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-218">The application uses the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function to display the menu associated with this menu item.</span></span> <span data-ttu-id="a4241-219">La barra dei menu non viene visualizzata perché **TrackPopupMenu** richiede un handle a un menu, un sottomenu o un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="a4241-219">(The menu bar itself is not displayed because **TrackPopupMenu** requires a handle to a menu, submenu, or shortcut menu.)</span></span>


```
VOID APIENTRY DisplayContextMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // top-level menu 
    HMENU hmenuTrackPopup;  // shortcut menu 
 
    // Load the menu resource. 
 
    if ((hmenu = LoadMenu(hinst, "ShortcutExample")) == NULL) 
        return; 
 
    // TrackPopupMenu cannot display the menu bar so get 
    // a handle to the first shortcut menu. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // Display the shortcut menu. Track the right mouse 
    // button. 
 
    TrackPopupMenu(hmenuTrackPopup, 
            TPM_LEFTALIGN | TPM_RIGHTBUTTON, 
            pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



## <a name="using-menu-item-bitmaps"></a><span data-ttu-id="a4241-220">Uso di bitmap Menu-Item</span><span class="sxs-lookup"><span data-stu-id="a4241-220">Using Menu-Item Bitmaps</span></span>

<span data-ttu-id="a4241-221">Il sistema può utilizzare una bitmap anziché una stringa di testo per visualizzare una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-221">The system can use a bitmap instead of a text string to display a menu item.</span></span> <span data-ttu-id="a4241-222">Per usare una bitmap, è necessario impostare il **flag \_ bitmap MIIm** per la voce di menu e specificare un handle per la bitmap che il sistema deve visualizzare per la voce di menu nel membro **hbmpItem** della struttura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="a4241-222">To use a bitmap, you must set the **MIIM\_BITMAP** flag for the menu item and specify a handle to the bitmap that the system should display for the menu item in the **hbmpItem** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="a4241-223">In questa sezione viene descritto come utilizzare le bitmap per le voci di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-223">This section describes how to use bitmaps for menu items.</span></span>

-   [<span data-ttu-id="a4241-224">Impostazione del flag di tipo bitmap</span><span class="sxs-lookup"><span data-stu-id="a4241-224">Setting the Bitmap Type Flag</span></span>](#setting-the-bitmap-type-flag)
-   [<span data-ttu-id="a4241-225">Creazione della bitmap</span><span class="sxs-lookup"><span data-stu-id="a4241-225">Creating the Bitmap</span></span>](#creating-the-bitmap)
-   [<span data-ttu-id="a4241-226">Aggiunta di linee e grafici a un menu</span><span class="sxs-lookup"><span data-stu-id="a4241-226">Adding Lines and Graphs to a Menu</span></span>](#adding-lines-and-graphs-to-a-menu)
-   [<span data-ttu-id="a4241-227">Esempio di bitmap Menu-Item</span><span class="sxs-lookup"><span data-stu-id="a4241-227">Example of Menu-Item Bitmaps</span></span>](#example-of-menu-item-bitmaps)

### <a name="setting-the-bitmap-type-flag"></a><span data-ttu-id="a4241-228">Impostazione del flag di tipo bitmap</span><span class="sxs-lookup"><span data-stu-id="a4241-228">Setting the Bitmap Type Flag</span></span>

<span data-ttu-id="a4241-229">Il **flag \_ bitmap MIIm** o **MF \_ bitmap** indica al sistema di usare una bitmap anziché una stringa di testo per visualizzare una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-229">The **MIIM\_BITMAP** or **MF\_BITMAP** flag tells the system to use a bitmap rather than a text string to display a menu item.</span></span> <span data-ttu-id="a4241-230">È necessario impostare la **\_ bitmap MIIm** della voce di menu o il flag **MF \_ bitmap** in fase di esecuzione. non è possibile impostarlo nel file di definizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="a4241-230">A menu item's **MIIM\_BITMAP** or **MF\_BITMAP** flag must be set at run time; you cannot set it in the resource-definition file.</span></span>

<span data-ttu-id="a4241-231">Per le nuove applicazioni, è possibile usare la funzione [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) o [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) per impostare il flag di tipo **\_ bitmap MIIm** .</span><span class="sxs-lookup"><span data-stu-id="a4241-231">For new applications, you can use the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) or [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) function to set the **MIIM\_BITMAP** type flag.</span></span> <span data-ttu-id="a4241-232">Per modificare una voce di menu da un elemento di testo in un elemento bitmap, usare **SetMenuItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="a4241-232">To change a menu item from a text item to a bitmap item, use **SetMenuItemInfo**.</span></span> <span data-ttu-id="a4241-233">Per aggiungere un nuovo elemento bitmap a un menu, usare la funzione **InsertMenuItem** .</span><span class="sxs-lookup"><span data-stu-id="a4241-233">To add a new bitmap item to a menu, use the **InsertMenuItem** function.</span></span>

<span data-ttu-id="a4241-234">Le applicazioni scritte per le versioni precedenti del sistema possono continuare a usare le funzioni [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)o [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) per impostare il flag della **\_ bitmap MF** .</span><span class="sxs-lookup"><span data-stu-id="a4241-234">Applications written for earlier versions of the system can continue to use the [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), or [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) functions to set the **MF\_BITMAP** flag.</span></span> <span data-ttu-id="a4241-235">Per modificare una voce di menu da un elemento stringa di testo in un elemento bitmap, usare **ModifyMenu**.</span><span class="sxs-lookup"><span data-stu-id="a4241-235">To change a menu item from a text string item to a bitmap item, use **ModifyMenu**.</span></span> <span data-ttu-id="a4241-236">Per aggiungere un nuovo elemento bitmap a un menu, usare il flag di **\_ bitmap MF** con la funzione **InsertMenu** o **AppendMenu** .</span><span class="sxs-lookup"><span data-stu-id="a4241-236">To add a new bitmap item to a menu, use the **MF\_BITMAP** flag with the **InsertMenu** or **AppendMenu** function.</span></span>

### <a name="creating-the-bitmap"></a><span data-ttu-id="a4241-237">Creazione della bitmap</span><span class="sxs-lookup"><span data-stu-id="a4241-237">Creating the Bitmap</span></span>

<span data-ttu-id="a4241-238">Quando si imposta il flag **MIIm \_ bitmap** o **MF \_ bitmap** Type per una voce di menu, è necessario specificare anche un handle per la bitmap che il sistema deve visualizzare per la voce di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-238">When you set the **MIIM\_BITMAP** or **MF\_BITMAP** type flag for a menu item, you must also specify a handle to the bitmap that the system should display for the menu item.</span></span> <span data-ttu-id="a4241-239">È possibile specificare la bitmap come risorsa bitmap o creare la bitmap in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a4241-239">You can provide the bitmap as a bitmap resource or create the bitmap at run time.</span></span> <span data-ttu-id="a4241-240">Se si usa una risorsa bitmap, è possibile usare la funzione [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) per caricare la bitmap e ottenere il relativo handle.</span><span class="sxs-lookup"><span data-stu-id="a4241-240">If you use a bitmap resource, you can use the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function to load the bitmap and obtain its handle.</span></span>

<span data-ttu-id="a4241-241">Per creare la bitmap in fase di esecuzione, utilizzare le funzioni di Windows Graphics Device Interface (GDI).</span><span class="sxs-lookup"><span data-stu-id="a4241-241">To create the bitmap at run time, use Windows Graphics Device Interface (GDI) functions.</span></span> <span data-ttu-id="a4241-242">GDI offre diversi modi per creare una bitmap in fase di esecuzione, ma gli sviluppatori in genere usano il metodo seguente:</span><span class="sxs-lookup"><span data-stu-id="a4241-242">GDI provides several ways to create a bitmap at run time, but developers typically use the following method:</span></span>

1.  <span data-ttu-id="a4241-243">Usare la funzione [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) per creare un contesto di dispositivo compatibile con il contesto di dispositivo usato dalla finestra principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-243">Use the [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) function to create a device context compatible with the device context used by the application's main window.</span></span>
2.  <span data-ttu-id="a4241-244">Usare la funzione [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) per creare una bitmap compatibile con la finestra principale dell'applicazione oppure usare la funzione [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) per creare una bitmap monocromatica.</span><span class="sxs-lookup"><span data-stu-id="a4241-244">Use the [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) function to create a bitmap compatible with the application's main window or use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) function to create a monochrome bitmap.</span></span>
3.  <span data-ttu-id="a4241-245">Usare la funzione [**SelezionaOggetto**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) per selezionare la bitmap nel contesto di dispositivo compatibile.</span><span class="sxs-lookup"><span data-stu-id="a4241-245">Use the [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) function to select the bitmap into the compatible device context.</span></span>
4.  <span data-ttu-id="a4241-246">Utilizzare le funzioni di disegno GDI, ad esempio [**ellisse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) e [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), per disegnare un'immagine nella bitmap.</span><span class="sxs-lookup"><span data-stu-id="a4241-246">Use GDI drawing functions, such as [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) and [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), to draw an image into the bitmap.</span></span>

<span data-ttu-id="a4241-247">Per ulteriori informazioni, vedere [bitmap](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="a4241-247">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

### <a name="adding-lines-and-graphs-to-a-menu"></a><span data-ttu-id="a4241-248">Aggiunta di linee e grafici a un menu</span><span class="sxs-lookup"><span data-stu-id="a4241-248">Adding Lines and Graphs to a Menu</span></span>

<span data-ttu-id="a4241-249">Nell'esempio di codice riportato di seguito viene illustrato come creare un menu che contiene bitmap di voci di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-249">The following code sample shows how to create a menu that contains menu-item bitmaps.</span></span> <span data-ttu-id="a4241-250">Vengono creati due menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-250">It creates two menus.</span></span> <span data-ttu-id="a4241-251">Il primo è un menu del grafico che contiene tre bitmap di voci di menu: un grafico a torta, un grafico a linee e un grafico a barre.</span><span class="sxs-lookup"><span data-stu-id="a4241-251">The first is a Chart menu that contains three menu-item bitmaps: a pie chart, a line chart, and a bar chart.</span></span> <span data-ttu-id="a4241-252">Nell'esempio viene illustrato come caricare queste bitmap dal file di risorse dell'applicazione e quindi utilizzare le funzioni [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) e [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) per creare il menu e le voci di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-252">The example demonstrates how to load these bitmaps from the application's resource file, and then use the [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) and [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) functions to create the menu and menu items.</span></span>

<span data-ttu-id="a4241-253">Il secondo menu è un menu righe.</span><span class="sxs-lookup"><span data-stu-id="a4241-253">The second menu is a Lines menu.</span></span> <span data-ttu-id="a4241-254">Contiene bitmap che mostrano gli stili di linea forniti dalla penna predefinita nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a4241-254">It contains bitmaps showing the line styles provided by the predefined pen in the system.</span></span> <span data-ttu-id="a4241-255">Le bitmap di tipo riga vengono create in fase di esecuzione utilizzando le funzioni GDI.</span><span class="sxs-lookup"><span data-stu-id="a4241-255">The line-style bitmaps are created at run time by using GDI functions.</span></span>

<span data-ttu-id="a4241-256">Di seguito sono riportate le definizioni delle risorse bitmap nel file di definizione delle risorse dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-256">Here are the definitions of the bitmap resources in the application's resource-definition file.</span></span>


```
PIE BITMAP pie.bmp 
LINE BITMAP line.bmp 
BAR BITMAP bar.bmp 
 
```



<span data-ttu-id="a4241-257">Di seguito sono riportate le parti rilevanti del file di intestazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-257">Here are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers 
 
#define IDM_SOLID       PS_SOLID 
#define IDM_DASH        PS_DASH 
#define IDM_DASHDOT     PS_DASHDOT 
#define IDM_DASHDOTDOT  PS_DASHDOTDOT 
 
#define IDM_PIE  1 
#define IDM_LINE 2 
#define IDM_BAR  3 
 
// Line-type flags  
 
#define SOLID       0 
#define DOT         1 
#define DASH        2 
#define DASHDOT     3 
#define DASHDOTDOT  4 
 
// Count of pens  
 
#define CPENS 5 
 
// Chart-type flags  
 
#define PIE  1 
#define LINE 2 
#define BAR  3 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
VOID MakeChartMenu(HWND); 
VOID MakeLineMenu(HWND, HPEN, HBITMAP); 
```



<span data-ttu-id="a4241-258">Nell'esempio seguente viene illustrato come vengono creati i menu e le bitmap degli elementi di menu in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-258">The following example shows how menus and menu-item bitmaps are created in an application.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HPEN hpen[CPENS]; 
    static HBITMAP hbmp[CPENS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Create the Chart and Line menus.  
 
            MakeChartMenu(hwnd); 
            MakeLineMenu(hwnd, hpen, hbmp); 
            return 0; 
 
        // Process other window messages. 
 
        case WM_DESTROY: 
 
            for (i = 0; i < CPENS; i++) 
            { 
                DeleteObject(hbmp[i]); 
                DeleteObject(hpen[i]); 
            } 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
VOID MakeChartMenu(HWND hwnd) 
{ 
    HBITMAP hbmpPie;    // handle to pie chart bitmap   
    HBITMAP hbmpLine;   // handle to line chart bitmap  
    HBITMAP hbmpBar;    // handle to bar chart bitmap   
    HMENU hmenuMain;    // handle to main menu          
    HMENU hmenuChart;   // handle to Chart menu  
 
    // Load the pie, line, and bar chart bitmaps from the 
    // resource-definition file. 
 
    hbmpPie = LoadBitmap(hinst, MAKEINTRESOURCE(PIE)); 
    hbmpLine = LoadBitmap(hinst, MAKEINTRESOURCE(LINE)); 
    hbmpBar = LoadBitmap(hinst, MAKEINTRESOURCE(BAR)); 
 
    // Create the Chart menu and add it to the menu bar. 
    // Append the Pie, Line, and Bar menu items to the Chart 
    // menu. 
 
    hmenuMain = GetMenu(hwnd); 
    hmenuChart = CreatePopupMenu(); 
    AppendMenu(hmenuMain, MF_STRING | MF_POPUP, (UINT) hmenuChart, 
        "Chart"); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_PIE, (LPCTSTR) hbmpPie); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_LINE, 
        (LPCTSTR) hbmpLine); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_BAR, (LPCTSTR) hbmpBar); 
 
    return; 
} 
 
VOID MakeLineMenu(HWND hwnd, HPEN phpen, HBITMAP phbmp) 
{ 
    HMENU hmenuLines;       // handle to Lines menu      
    HMENU hmenu;            // handle to main menu              
    COLORREF crMenuClr;     // menu-item background color       
    HBRUSH hbrBackground;   // handle to background brush       
    HBRUSH hbrOld;          // handle to previous brush         
    WORD wLineX;            // width of line bitmaps            
    WORD wLineY;            // height of line bitmaps           
    HDC hdcMain;            // handle to main window's DC       
    HDC hdcLines;           // handle to compatible DC          
    HBITMAP hbmpOld;        // handle to previous bitmap        
    int i;                  // loop counter                     
 
    // Create the Lines menu. Add it to the menu bar.  
 
    hmenu = GetMenu(hwnd); 
    hmenuLines = CreatePopupMenu(); 
    AppendMenu(hmenu, MF_STRING | MF_POPUP, 
        (UINT) hmenuLines, "&Lines"); 
 
    // Create a brush for the menu-item background color.  
 
    crMenuClr = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crMenuClr); 
 
    // Create a compatible device context for the line bitmaps, 
    // and then select the background brush into it. 
 
    hdcMain = GetDC(hwnd); 
    hdcLines = CreateCompatibleDC(hdcMain); 
    hbrOld = SelectObject(hdcLines, hbrBackground); 
 
    // Get the dimensions of the check-mark bitmap. The width of 
    // the line bitmaps will be five times the width of the 
    // check-mark bitmap. 
 
    wLineX = GetSystemMetrics(SM_CXMENUCHECK) * (WORD) 5; 
    wLineY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    // Create the bitmaps and select them, one at a time, into the 
    // compatible device context. Initialize each bitmap by 
    // filling it with the menu-item background color. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        phbmp[i] = CreateCompatibleBitmap(hdcMain, wLineX, wLineY); 
        if (i == 0) 
            hbmpOld = SelectObject(hdcLines, phbmp[i]); 
        else 
            SelectObject(hdcLines, phbmp[i]); 
        ExtFloodFill(hdcLines, 0, 0, crMenuClr, FLOODFILLBORDER); 
    } 
 
    // Create the pens.  
 
    phpen[0] = CreatePen(PS_SOLID, 1, RGB(0, 0, 0)); 
    phpen[1] = CreatePen(PS_DOT, 1, RGB(0, 0, 0)); 
    phpen[2] = CreatePen(PS_DASH, 1, RGB(0, 0, 0)); 
    phpen[3] = CreatePen(PS_DASHDOT, 1, RGB(0, 0, 0)); 
    phpen[4] = CreatePen(PS_DASHDOTDOT, 1, RGB(0, 0, 0)); 
 
    // Select a pen and a bitmap into the compatible device 
    // context, draw a line into the bitmap, and then append 
    // the bitmap as an item in the Lines menu. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        SelectObject(hdcLines, phbmp[i]); 
        SelectObject(hdcLines, phpen[i]); 
        MoveToEx(hdcLines, 0, wLineY / 2, NULL); 
        LineTo(hdcLines, wLineX, wLineY / 2); 
        AppendMenu(hmenuLines, MF_BITMAP, i + 1, 
            (LPCTSTR) phbmp[i]); 
    } 
 
    // Release the main window's device context and destroy the 
    // compatible device context. Also, destroy the background 
    // brush. 
 
    ReleaseDC(hwnd, hdcMain); 
    SelectObject(hdcLines, hbrOld); 
    DeleteObject(hbrBackground); 
    SelectObject(hdcLines, hbmpOld); 
    DeleteDC(hdcLines); 
 
    return; 
} 
```



### <a name="example-of-menu-item-bitmaps"></a><span data-ttu-id="a4241-259">Esempio di bitmap Menu-Item</span><span class="sxs-lookup"><span data-stu-id="a4241-259">Example of Menu-Item Bitmaps</span></span>

<span data-ttu-id="a4241-260">Nell'esempio riportato in questo argomento vengono creati due menu, ognuno dei quali contiene diverse voci di menu bitmap.</span><span class="sxs-lookup"><span data-stu-id="a4241-260">The example in this topic creates two menus, each containing several bitmap menu items.</span></span> <span data-ttu-id="a4241-261">Per ogni menu, l'applicazione aggiunge un nome di menu corrispondente alla barra dei menu della finestra principale.</span><span class="sxs-lookup"><span data-stu-id="a4241-261">For each menu, the application adds a corresponding menu name to the main window's menu bar.</span></span>

<span data-ttu-id="a4241-262">Il primo menu contiene voci di menu che mostrano ognuno dei tre tipi di grafico, ovvero a torta, a linee e a barre.</span><span class="sxs-lookup"><span data-stu-id="a4241-262">The first menu contains menu items showing each of three chart types: pie, line, and bar.</span></span> <span data-ttu-id="a4241-263">Le bitmap per queste voci di menu sono definite come risorse e vengono caricate tramite la funzione [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) .</span><span class="sxs-lookup"><span data-stu-id="a4241-263">The bitmaps for these menu items are defined as resources and are loaded by using the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function.</span></span> <span data-ttu-id="a4241-264">Associato a questo menu è un nome di menu "Chart" sulla barra dei menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-264">Associated with this menu is a "Chart" menu name on the menu bar.</span></span>

<span data-ttu-id="a4241-265">Il secondo menu contiene voci di menu che mostrano ognuno dei cinque stili di linea usati con la funzione [**CreatePen**](/windows/desktop/api/wingdi/nf-wingdi-createpen) : **PS \_ Solid**, **PS \_ Dash**, **PS \_ dot**, **PS \_ DASHDOT** e **PS \_ TrattoPuntoPunto**.</span><span class="sxs-lookup"><span data-stu-id="a4241-265">The second menu contains menu items showing each of the five line styles used with the [**CreatePen**](/windows/desktop/api/wingdi/nf-wingdi-createpen) function: **PS\_SOLID**, **PS\_DASH**, **PS\_DOT**, **PS\_DASHDOT**, and **PS\_DASHDOTDOT**.</span></span> <span data-ttu-id="a4241-266">L'applicazione crea le bitmap per queste voci di menu in fase di esecuzione usando le funzioni di disegno GDI.</span><span class="sxs-lookup"><span data-stu-id="a4241-266">The application creates the bitmaps for these menu items at run time using GDI drawing functions.</span></span> <span data-ttu-id="a4241-267">Associato a questo menu è un nome di menu **linee** sulla barra dei menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-267">Associated with this menu is a **Lines** menu name on the menu bar.</span></span>

<span data-ttu-id="a4241-268">Definito nella procedura della finestra dell'applicazione sono due matrici statiche di handle bitmap.</span><span class="sxs-lookup"><span data-stu-id="a4241-268">Defined in the application's window procedure are two static arrays of bitmap handles.</span></span> <span data-ttu-id="a4241-269">Una matrice contiene gli handle delle tre bitmap utilizzate per il menu del **grafico** .</span><span class="sxs-lookup"><span data-stu-id="a4241-269">One array contains the handles of the three bitmaps used for the **Chart** menu.</span></span> <span data-ttu-id="a4241-270">L'altra contiene gli handle delle cinque bitmap utilizzate per il menu **righe** .</span><span class="sxs-lookup"><span data-stu-id="a4241-270">The other contains the handles of the five bitmaps used for the **Lines** menu.</span></span> <span data-ttu-id="a4241-271">Quando si elabora il messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) , la procedura della finestra Carica le bitmap del grafico, crea le bitmap della riga e quindi aggiunge le voci di menu corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="a4241-271">When processing the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, the window procedure loads the chart bitmaps, creates the line bitmaps, and then adds the corresponding menu items.</span></span> <span data-ttu-id="a4241-272">Quando si elabora il messaggio [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) , la routine della finestra Elimina tutte le bitmap.</span><span class="sxs-lookup"><span data-stu-id="a4241-272">When processing the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, the window procedure deletes all of the bitmaps.</span></span>

<span data-ttu-id="a4241-273">Di seguito sono riportate le parti rilevanti del file di intestazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-273">Following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers 
 
#define IDM_PIE         1 
#define IDM_LINE        2 
#define IDM_BAR         3 
 
#define IDM_SOLID       4 
#define IDM_DASH        5 
#define IDM_DASHDOT     6 
#define IDM_DASHDOTDOT  7 
 
// Number of items on the Chart and Lines menus 
 
#define C_LINES         5 
#define C_CHARTS        3 
 
// Bitmap resource identifiers 
 
#define IDB_PIE         1 
#define IDB_LINE        2 
#define IDB_BAR         3 
 
// Dimensions of the line bitmaps 
 
#define CX_LINEBMP      40 
#define CY_LINEBMP      10 
```



<span data-ttu-id="a4241-274">Di seguito sono riportate le parti pertinenti della routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="a4241-274">Following are the relevant portions of the window procedure.</span></span> <span data-ttu-id="a4241-275">La procedura della finestra esegue la maggior parte dell'inizializzazione chiamando le funzioni LoadChartBitmaps, CreateLineBitmaps e AddBitmapMenu definite dall'applicazione, descritte più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="a4241-275">The window procedure performs most of its initialization by calling the application-defined LoadChartBitmaps, CreateLineBitmaps, and AddBitmapMenu functions, described later in this topic.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    static HBITMAP aHbmLines[C_LINES]; 
    static HBITMAP aHbmChart[C_CHARTS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
             // Call application-defined functions to load the 
             // bitmaps for the Chart menu and create those for 
             // the Lines menu. 
 
            LoadChartBitmaps(aHbmChart); 
            CreateLineBitmaps(aHbmLines); 
 
             // Call an application-defined function to create 
             // menus containing the bitmap menu items. The function 
             // also adds a menu name to the window's menu bar. 
 
            AddBitmapMenu( 
                    hwnd,      // menu bar's owner window 
                    "&Chart",  // text of menu name on menu bar 
                    IDM_PIE,   // ID of first item on menu 
                    aHbmChart, // array of bitmap handles 
                    C_CHARTS   // number of items on menu 
                    ); 
            AddBitmapMenu(hwnd, "&Lines", IDM_SOLID, 
                    aHbmLines, C_LINES); 
            break; 
 
        case WM_DESTROY: 
            for (i = 0; i < C_LINES; i++) 
                DeleteObject(aHbmLines[i]); 
            for (i = 0; i < C_CHARTS; i++) 
                DeleteObject(aHbmChart[i]); 
            PostQuitMessage(0); 
            break; 
 
        // Process additional messages here. 
 
        default: 
            return (DefWindowProc(hwnd, uMsg, wParam, lParam)); 
    } 
    return 0; 
} 
```



<span data-ttu-id="a4241-276">La funzione LoadChartBitmaps definita dall'applicazione carica le risorse bitmap per il menu Chart chiamando la funzione [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) , come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="a4241-276">The application-defined LoadChartBitmaps function loads the bitmap resources for the chart menu by calling the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function, as follows.</span></span>


```
VOID WINAPI LoadChartBitmaps(HBITMAP *paHbm) 
{ 
    paHbm[0] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_PIE)); 
    paHbm[1] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_LINE)); 
    paHbm[2] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_BAR)); 
} 
```



<span data-ttu-id="a4241-277">La funzione CreateLineBitmaps definita dall'applicazione crea le bitmap per il menu righe usando le funzioni di disegno GDI.</span><span class="sxs-lookup"><span data-stu-id="a4241-277">The application-defined CreateLineBitmaps function creates the bitmaps for the Lines menu by using GDI drawing functions.</span></span> <span data-ttu-id="a4241-278">La funzione crea un contesto di dispositivo di memoria (DC) con le stesse proprietà del controller di dominio della finestra desktop.</span><span class="sxs-lookup"><span data-stu-id="a4241-278">The function creates a memory device context (DC) with the same properties as the desktop window's DC.</span></span> <span data-ttu-id="a4241-279">Per ogni stile di linea, la funzione crea una bitmap, la seleziona nel controller di dominio di memoria e la disegna.</span><span class="sxs-lookup"><span data-stu-id="a4241-279">For each line style, the function creates a bitmap, selects it into the memory DC, and draws in it.</span></span>


```
VOID WINAPI CreateLineBitmaps(HBITMAP *paHbm) 
{ 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
    COLORREF clrMenu = GetSysColor(COLOR_MENU); 
    HBRUSH hbrOld; 
    HPEN hpenOld; 
    HBITMAP hbmOld; 
    int fnDrawMode; 
    int i; 
 
     // Create a brush using the menu background color, 
     // and select it into the memory DC. 
 
    hbrOld = SelectObject(hdcMem, CreateSolidBrush(clrMenu)); 
 
     // Create the bitmaps. Select each one into the memory 
     // DC that was created and draw in it. 
 
    for (i = 0; i < C_LINES; i++) 
    { 
        // Create the bitmap and select it into the DC. 
 
        paHbm[i] = CreateCompatibleBitmap(hdcDesktop, 
                CX_LINEBMP, CY_LINEBMP); 
        hbmOld = SelectObject(hdcMem, paHbm[i]); 
 
        // Fill the background using the brush. 
 
        PatBlt(hdcMem, 0, 0, CX_LINEBMP, CY_LINEBMP, PATCOPY); 
 
        // Create the pen and select it into the DC. 
 
        hpenOld = SelectObject(hdcMem, 
                CreatePen(PS_SOLID + i, 1, RGB(0, 0, 0))); 
 
         // Draw the line. To preserve the background color where 
         // the pen is white, use the R2_MASKPEN drawing mode. 
 
        fnDrawMode = SetROP2(hdcMem, R2_MASKPEN); 
        MoveToEx(hdcMem, 0, CY_LINEBMP / 2, NULL); 
        LineTo(hdcMem, CX_LINEBMP, CY_LINEBMP / 2); 
        SetROP2(hdcMem, fnDrawMode); 
 
        // Delete the pen, and select the old pen and bitmap. 
 
        DeleteObject(SelectObject(hdcMem, hpenOld)); 
        SelectObject(hdcMem, hbmOld); 
    } 
 
    // Delete the brush and select the original brush. 
 
    DeleteObject(SelectObject(hdcMem, hbrOld)); 
 
    // Delete the memory DC and release the desktop DC. 
 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
} 
```



<span data-ttu-id="a4241-280">La funzione AddBitmapMenu definita dall'applicazione crea un menu e vi aggiunge il numero specificato di voci di menu bitmap.</span><span class="sxs-lookup"><span data-stu-id="a4241-280">The application-defined AddBitmapMenu function creates a menu and adds the specified number of bitmap menu items to it.</span></span> <span data-ttu-id="a4241-281">Aggiunge quindi un nome di menu corrispondente alla barra dei menu della finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="a4241-281">Then it adds a corresponding menu name to the specified window's menu bar.</span></span>


```
VOID WINAPI AddBitmapMenu( 
        HWND hwnd,          // window that owned the menu bar 
        LPSTR lpszText,     // text of menu name on menu bar 
        UINT uID,           // ID of first bitmap menu item 
        HBITMAP *paHbm,     // bitmaps for the menu items 
        int cItems)         // number bitmap menu items 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup = CreatePopupMenu(); 
    MENUITEMINFO mii; 
    int i; 
 
    // Add the bitmap menu items to the menu. 
 
    for (i = 0; i < cItems; i++) 
    { 
        mii.fMask = MIIM_ID | MIIM_BITMAP | MIIM_DATA; 
        mii.wID = uID + i; 
        mii.hbmpItem = &paHbm[i]; 
        InsertMenuItem(hmenuPopup, i, TRUE, &mii); 
    } 
 
    // Add a menu name to the menu bar. 
 
    mii.fMask = MIIM_STRING | MIIM_DATA | MIIM_SUBMENU; 
    mii.fType = MFT_STRING; 
    mii.hSubMenu = hmenuPopup; 
    mii.dwTypeData = lpszText; 
    InsertMenuItem(hmenuBar, 
        GetMenuItemCount(hmenuBar), TRUE, &mii); 
} 
```



## <a name="creating-owner-drawn-menu-items"></a><span data-ttu-id="a4241-282">Creazione di voci di menu Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="a4241-282">Creating Owner-Drawn Menu Items</span></span>

<span data-ttu-id="a4241-283">Se è necessario un controllo completo sull'aspetto di una voce di menu, è possibile usare una voce di menu creata dal proprietario nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-283">If you need complete control over the appearance of a menu item, you can use an owner-drawn menu item in your application.</span></span> <span data-ttu-id="a4241-284">In questa sezione vengono descritti i passaggi necessari per la creazione e l'utilizzo di una voce di menu creata dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="a4241-284">This section describes the steps involved in creating and using an owner-drawn menu item.</span></span>

-   [<span data-ttu-id="a4241-285">Impostazione del flag di Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="a4241-285">Setting the Owner-Drawn Flag</span></span>](#setting-the-owner-drawn-flag)
-   [<span data-ttu-id="a4241-286">Menu creati dal proprietario e il \_ messaggio WM MeasureItem</span><span class="sxs-lookup"><span data-stu-id="a4241-286">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>](/windows)
-   [<span data-ttu-id="a4241-287">Menu creati dal proprietario e messaggio di WM \_ DrawItem</span><span class="sxs-lookup"><span data-stu-id="a4241-287">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>](/windows)
-   [<span data-ttu-id="a4241-288">Menu creati dal proprietario e il \_ messaggio WM MENUCHAR</span><span class="sxs-lookup"><span data-stu-id="a4241-288">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>](/windows)
-   [<span data-ttu-id="a4241-289">Impostazione dei tipi di carattere per le stringhe di testo Menu-Item</span><span class="sxs-lookup"><span data-stu-id="a4241-289">Setting Fonts for Menu-Item Text Strings</span></span>](#setting-fonts-for-menu-item-text-strings)
-   [<span data-ttu-id="a4241-290">Esempio di voci di menu Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="a4241-290">Example of Owner-Drawn Menu Items</span></span>](#example-of-owner-drawn-menu-items)

### <a name="setting-the-owner-drawn-flag"></a><span data-ttu-id="a4241-291">Impostazione del flag di Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="a4241-291">Setting the Owner-Drawn Flag</span></span>

<span data-ttu-id="a4241-292">Non è possibile definire una voce di menu creata dal proprietario nel file di definizione delle risorse dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-292">You cannot define an owner-drawn menu item in your application's resource-definition file.</span></span> <span data-ttu-id="a4241-293">È invece necessario creare una nuova voce di menu o modificarne una esistente usando il flag di menu **\_ OWNERDRAW di MFT** .</span><span class="sxs-lookup"><span data-stu-id="a4241-293">Instead, you must create a new menu item or modify an existing one by using the **MFT\_OWNERDRAW** menu flag.</span></span>

<span data-ttu-id="a4241-294">È possibile usare la funzione [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) o [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) per specificare una voce di menu creata dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="a4241-294">You can use the [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) or [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function to specify an owner-drawn menu item.</span></span> <span data-ttu-id="a4241-295">Usare **InsertMenuItem** per inserire una nuova voce di menu in corrispondenza della posizione specificata in una barra dei menu o in un menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-295">Use **InsertMenuItem** to insert a new menu item at the specified position in a menu bar or menu.</span></span> <span data-ttu-id="a4241-296">Usare **SetMenuItemInfo** per modificare il contenuto di un menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-296">Use **SetMenuItemInfo** to change the contents of a menu.</span></span>

<span data-ttu-id="a4241-297">Quando si chiamano queste due funzioni, è necessario specificare un puntatore a una struttura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) , che specifica le proprietà della nuova voce di menu o le proprietà che si desidera modificare per una voce di menu esistente.</span><span class="sxs-lookup"><span data-stu-id="a4241-297">When calling these two functions, you must specify a pointer to a [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure, which specifies the properties of the new menu item or the properties you want to change for an existing menu item.</span></span> <span data-ttu-id="a4241-298">Per impostare un elemento come elemento creato dal proprietario, specificare il **valore MIIm \_ ftype** per il membro **fmask** e il **valore \_ OWNERDRAW di MFT** per il membro **ftype** .</span><span class="sxs-lookup"><span data-stu-id="a4241-298">To make an item an owner-drawn item, specify the **MIIM\_FTYPE** value for the **fMask** member and the **MFT\_OWNERDRAW** value for the **fType** member.</span></span>

<span data-ttu-id="a4241-299">Impostando i membri appropriati della struttura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) , è possibile associare un valore definito dall'applicazione, denominato **dati elemento**, con ogni voce di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-299">By setting the appropriate members of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure, you can associate an application-defined value, which is called **item data**, with each menu item.</span></span> <span data-ttu-id="a4241-300">A tale scopo, specificare il valore di **\_ dati MIIm** per il membro **fmask** e il valore definito dall'applicazione per il membro **dwItemData** .</span><span class="sxs-lookup"><span data-stu-id="a4241-300">To do so, specify the **MIIM\_DATA** value for the **fMask** member and the application-defined value for the **dwItemData** member.</span></span>

<span data-ttu-id="a4241-301">È possibile utilizzare i dati degli elementi con qualsiasi tipo di voce di menu, ma è particolarmente utile per gli elementi creati dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="a4241-301">You can use item data with any type of menu item, but it is particularly useful for owner-drawn items.</span></span> <span data-ttu-id="a4241-302">Si supponga, ad esempio, che una struttura includa le informazioni utilizzate per tracciare una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-302">For example, suppose a structure contains information used to draw a menu item.</span></span> <span data-ttu-id="a4241-303">Un'applicazione può usare i dati dell'elemento per una voce di menu per archiviare un puntatore alla struttura.</span><span class="sxs-lookup"><span data-stu-id="a4241-303">An application might use the item data for a menu item to store a pointer to the structure.</span></span> <span data-ttu-id="a4241-304">I dati dell'elemento vengono inviati alla finestra proprietaria del menu con i messaggi [**WM \_ MeasureItem**](../controls/wm-measureitem.md) e [**WM \_ DrawItem**](../controls/wm-drawitem.md) .</span><span class="sxs-lookup"><span data-stu-id="a4241-304">The item data is sent to the menu's owner window with the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) and [**WM\_DRAWITEM**](../controls/wm-drawitem.md) messages.</span></span> <span data-ttu-id="a4241-305">Per recuperare i dati dell'elemento per un menu in qualsiasi momento, utilizzare la funzione [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="a4241-305">To retrieve the item data for a menu at any time, use the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function.</span></span>

<span data-ttu-id="a4241-306">Le applicazioni scritte per le versioni precedenti del sistema possono continuare a chiamare [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)o [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) per assegnare il flag **MF \_ OWNERDRAW** a una voce di menu creata dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="a4241-306">Applications written for earlier versions of the system can continue to call [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), or [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) to assign the **MF\_OWNERDRAW** flag to an owner-drawn menu item.</span></span>

<span data-ttu-id="a4241-307">Quando si chiama una di queste tre funzioni, è possibile passare un valore come parametro *lpNewItem* .</span><span class="sxs-lookup"><span data-stu-id="a4241-307">When you call any of these three functions, you can pass a value as the *lpNewItem* parameter.</span></span> <span data-ttu-id="a4241-308">Questo valore può rappresentare tutte le informazioni significative per l'applicazione e che saranno disponibili per l'applicazione quando l'elemento deve essere visualizzato.</span><span class="sxs-lookup"><span data-stu-id="a4241-308">This value can represent any information that is meaningful to your application, and that will be available to your application when the item is to be displayed.</span></span> <span data-ttu-id="a4241-309">Ad esempio, il valore può contenere un puntatore a una struttura; la struttura, a sua volta, può contenere una stringa di testo e un handle per il tipo di carattere logico che l'applicazione userà per creare la stringa.</span><span class="sxs-lookup"><span data-stu-id="a4241-309">For example, the value could contain a pointer to a structure; the structure, in turn, might contain a text string and a handle to the logical font your application will use to draw the string.</span></span>

### <a name="owner-drawn-menus-and-the-wm_measureitem-message"></a><span data-ttu-id="a4241-310">Menu Owner-Drawn e il \_ messaggio WM MeasureItem</span><span class="sxs-lookup"><span data-stu-id="a4241-310">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>

<span data-ttu-id="a4241-311">Prima che il sistema visualizzi una voce di menu creata dal proprietario per la prima volta, invia il messaggio [**WM \_ MeasureItem**](../controls/wm-measureitem.md) alla routine della finestra che possiede il menu dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a4241-311">Before the system displays an owner-drawn menu item for the first time, it sends the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message to the window procedure of the window that owns the item's menu.</span></span> <span data-ttu-id="a4241-312">Questo messaggio contiene un puntatore a una struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) che identifica l'elemento e contiene i dati dell'elemento che possono essere stati assegnati a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-312">This message contains a pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that identifies the item and contains the item data that an application may have assigned to it.</span></span> <span data-ttu-id="a4241-313">La routine della finestra deve riempire i membri **itemWidth** e **ItemHeight** della struttura prima di tornare dall'elaborazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="a4241-313">The window procedure must fill the **itemWidth** and **itemHeight** members of the structure before returning from processing the message.</span></span> <span data-ttu-id="a4241-314">Il sistema usa le informazioni contenute in questi membri quando crea il rettangolo di delimitazione in cui un'applicazione disegna la voce di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-314">The system uses the information in these members when creating the bounding rectangle in which an application draws the menu item.</span></span> <span data-ttu-id="a4241-315">USA inoltre le informazioni per rilevare quando l'utente sceglie l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a4241-315">It also uses the information to detect when the user chooses the item.</span></span>

### <a name="owner-drawn-menus-and-the-wm_drawitem-message"></a><span data-ttu-id="a4241-316">Menu Owner-Drawn e il \_ messaggio WM DrawItem</span><span class="sxs-lookup"><span data-stu-id="a4241-316">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>

<span data-ttu-id="a4241-317">Ogni volta che è necessario disegnare l'elemento (ad esempio, quando viene visualizzato per la prima volta o quando l'utente lo seleziona), il sistema invia il messaggio [**WM \_ DrawItem**](../controls/wm-drawitem.md) alla procedura della finestra proprietaria del menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-317">Whenever the item must be drawn (for example, when it is first displayed or when the user selects it), the system sends the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message to the window procedure of the menu's owner window.</span></span> <span data-ttu-id="a4241-318">Questo messaggio contiene un puntatore a una struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) che contiene informazioni sull'elemento, inclusi i dati dell'elemento che possono essere stati assegnati a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-318">This message contains a pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure, which contains information about the item, including the item data that an application may have assigned to it.</span></span> <span data-ttu-id="a4241-319">Inoltre, **DRAWITEMSTRUCT** contiene flag che indicano lo stato dell'elemento (ad esempio, se è grigio o selezionato), nonché un rettangolo di delimitazione e un contesto di dispositivo usato dall'applicazione per tracciare l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a4241-319">In addition, **DRAWITEMSTRUCT** contains flags that indicate the state of the item (such as whether it is grayed or selected) as well as a bounding rectangle and a device context that the application uses to draw the item.</span></span>

<span data-ttu-id="a4241-320">Durante l'elaborazione del messaggio [**WM \_ DrawItem**](../controls/wm-drawitem.md) , un'applicazione deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4241-320">An application must do the following while processing the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message:</span></span>

-   <span data-ttu-id="a4241-321">Determinare il tipo di disegno necessario.</span><span class="sxs-lookup"><span data-stu-id="a4241-321">Determine the type of drawing that is necessary.</span></span> <span data-ttu-id="a4241-322">A tale scopo, controllare il membro **itemAction** della struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="a4241-322">To do so, check the **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span>
-   <span data-ttu-id="a4241-323">Tracciare la voce di menu in modo appropriato, usando il rettangolo di delimitazione e il contesto di dispositivo ottenuti dalla struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="a4241-323">Draw the menu item appropriately, using the bounding rectangle and device context obtained from the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span> <span data-ttu-id="a4241-324">L'applicazione deve essere disegnato solo all'interno del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-324">The application must draw only within the bounding rectangle.</span></span> <span data-ttu-id="a4241-325">Per motivi di prestazioni, il sistema non Ritaglia le parti dell'immagine disegnate all'esterno del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="a4241-325">For performance reasons, the system does not clip portions of the image that are drawn outside the rectangle.</span></span>
-   <span data-ttu-id="a4241-326">Ripristina tutti gli oggetti GDI selezionati per il contesto di dispositivo della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-326">Restore all GDI objects selected for the menu item's device context.</span></span>

<span data-ttu-id="a4241-327">Se l'utente seleziona la voce di menu, il sistema imposta il membro **itemAction** della [**struttura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) sul valore **di \_ selezione Oda** e imposta il valore **ODS \_ selezionato** nel membro **ItemState** .</span><span class="sxs-lookup"><span data-stu-id="a4241-327">If the user selects the menu item, the system sets the **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure to the **ODA\_SELECT** value and sets the **ODS\_SELECTED** value in the **itemState** member.</span></span> <span data-ttu-id="a4241-328">Si tratta di un suggerimento di un'applicazione per ricreare la voce di menu per indicare che è selezionata.</span><span class="sxs-lookup"><span data-stu-id="a4241-328">This is an application's cue to redraw the menu item to indicate that it is selected.</span></span>

### <a name="owner-drawn-menus-and-the-wm_menuchar-message"></a><span data-ttu-id="a4241-329">Menu Owner-Drawn e il \_ messaggio WM MENUCHAR</span><span class="sxs-lookup"><span data-stu-id="a4241-329">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>

<span data-ttu-id="a4241-330">Per i menu diversi dai menu creati dal proprietario è possibile specificare un tasto di scelta inserendo un carattere di sottolineatura accanto a un carattere nella stringa di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-330">Menus other than owner-drawn menus can specify a menu mnemonic by inserting an underscore next to a character in the menu string.</span></span> <span data-ttu-id="a4241-331">Ciò consente all'utente di selezionare il menu premendo ALT e premendo il tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="a4241-331">This allows the user to select the menu by pressing ALT and pressing the menu mnemonic character.</span></span> <span data-ttu-id="a4241-332">Nei menu creati dal proprietario, tuttavia, non è possibile specificare un tasto di scelta di menu in questo modo.</span><span class="sxs-lookup"><span data-stu-id="a4241-332">In owner-drawn menus, however, you cannot specify a menu mnemonic in this manner.</span></span> <span data-ttu-id="a4241-333">Al contrario, l'applicazione deve elaborare il messaggio [**WM \_ MENUCHAR**](wm-menuchar.md) per fornire menu creati dal proprietario con tasti di scelta.</span><span class="sxs-lookup"><span data-stu-id="a4241-333">Instead, your application must process the [**WM\_MENUCHAR**](wm-menuchar.md) message to provide owner-drawn menus with menu mnemonics.</span></span>

<span data-ttu-id="a4241-334">Il messaggio [**WM \_ MENUCHAR**](wm-menuchar.md) viene inviato quando l'utente digita un tasto di scelta di menu che non corrisponde ad alcuno dei tasti di scelta predefiniti del menu corrente.</span><span class="sxs-lookup"><span data-stu-id="a4241-334">The [**WM\_MENUCHAR**](wm-menuchar.md) message is sent when the user types a menu mnemonic that does not match any of the predefined mnemonics of the current menu.</span></span> <span data-ttu-id="a4241-335">Il valore contenuto in *wParam* specifica il carattere ASCII che corrisponde alla chiave che l'utente ha premuto con il tasto ALT.</span><span class="sxs-lookup"><span data-stu-id="a4241-335">The value contained in *wParam* specifies the ASCII character that corresponds to the key the user pressed with the ALT key.</span></span> <span data-ttu-id="a4241-336">La parola di ordine inferiore di *wParam* specifica il tipo del menu selezionato. i possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4241-336">The low-order word of *wParam* specifies the type of the selected menu and can be one of the following values:</span></span>

-   <span data-ttu-id="a4241-337">**MF \_ POPUP** se il menu corrente è un sottomenu.</span><span class="sxs-lookup"><span data-stu-id="a4241-337">**MF\_POPUP** if the current menu is a submenu.</span></span>
-   <span data-ttu-id="a4241-338">**MF \_ SYSMENU** se il menu è il menu di sistema.</span><span class="sxs-lookup"><span data-stu-id="a4241-338">**MF\_SYSMENU** if the menu is the system menu.</span></span>

<span data-ttu-id="a4241-339">La parola più ordinata di *wParam* contiene l'handle di menu per il menu corrente.</span><span class="sxs-lookup"><span data-stu-id="a4241-339">The high-order word of *wParam* contains the menu handle to the current menu.</span></span> <span data-ttu-id="a4241-340">La finestra con i menu creati dal proprietario può elaborare [**WM \_ MENUCHAR**](wm-menuchar.md) nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="a4241-340">The window with the owner-drawn menus can process [**WM\_MENUCHAR**](wm-menuchar.md) as follows:</span></span>


```
   case WM_MENUCHAR:
      nIndex = Determine index of menu item to be selected from
               character that was typed and handle to the current
               menu.
      return MAKELRESULT(nIndex, 2);
```



<span data-ttu-id="a4241-341">I due elementi nella parola più ordinata del valore restituito segnalano al sistema che la parola di basso livello del valore restituito contiene l'indice in base zero della voce di menu da selezionare.</span><span class="sxs-lookup"><span data-stu-id="a4241-341">The two in the high-order word of the return value informs the system that the low-order word of the return value contains the zero-based index of the menu item to be selected.</span></span>

<span data-ttu-id="a4241-342">Le costanti seguenti corrispondono ai possibili valori restituiti dal messaggio [**WM \_ MENUCHAR**](wm-menuchar.md) .</span><span class="sxs-lookup"><span data-stu-id="a4241-342">The following constants correspond to the possible return values from the [**WM\_MENUCHAR**](wm-menuchar.md) message.</span></span>



| <span data-ttu-id="a4241-343">Costante</span><span class="sxs-lookup"><span data-stu-id="a4241-343">Constant</span></span>         | <span data-ttu-id="a4241-344">Valore</span><span class="sxs-lookup"><span data-stu-id="a4241-344">Value</span></span> | <span data-ttu-id="a4241-345">Significato</span><span class="sxs-lookup"><span data-stu-id="a4241-345">Meaning</span></span>                                                                                                                                                       |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4241-346">**\_Ignora**</span><span class="sxs-lookup"><span data-stu-id="a4241-346">**MNC\_IGNORE**</span></span>  | <span data-ttu-id="a4241-347">0</span><span class="sxs-lookup"><span data-stu-id="a4241-347">0</span></span>     | <span data-ttu-id="a4241-348">Il sistema deve rimuovere il carattere premuto dall'utente e creare un breve beep sull'altoparlante del sistema.</span><span class="sxs-lookup"><span data-stu-id="a4241-348">The system should discard the character the user pressed and create a short beep on the system speaker.</span></span>                                                       |
| <span data-ttu-id="a4241-349">**\_Close**</span><span class="sxs-lookup"><span data-stu-id="a4241-349">**MNC\_CLOSE**</span></span>   | <span data-ttu-id="a4241-350">1</span><span class="sxs-lookup"><span data-stu-id="a4241-350">1</span></span>     | <span data-ttu-id="a4241-351">Il sistema deve chiudere il menu attivo.</span><span class="sxs-lookup"><span data-stu-id="a4241-351">The system should close the active menu.</span></span>                                                                                                                      |
| <span data-ttu-id="a4241-352">**esecuzione di multipagina \_**</span><span class="sxs-lookup"><span data-stu-id="a4241-352">**MNC\_EXECUTE**</span></span> | <span data-ttu-id="a4241-353">2</span><span class="sxs-lookup"><span data-stu-id="a4241-353">2</span></span>     | <span data-ttu-id="a4241-354">Il sistema deve scegliere l'elemento specificato nella parola di ordine inferiore del valore restituito.</span><span class="sxs-lookup"><span data-stu-id="a4241-354">The system should choose the item specified in the low-order word of the return value.</span></span> <span data-ttu-id="a4241-355">La finestra proprietaria riceve un messaggio di [**\_ comando WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="a4241-355">The owner window receives a [**WM\_COMMAND**](wm-command.md) message.</span></span> |
| <span data-ttu-id="a4241-356">**\_selezione**</span><span class="sxs-lookup"><span data-stu-id="a4241-356">**MNC\_SELECT**</span></span>  | <span data-ttu-id="a4241-357">3</span><span class="sxs-lookup"><span data-stu-id="a4241-357">3</span></span>     | <span data-ttu-id="a4241-358">Il sistema deve selezionare l'elemento specificato nella parola di ordine inferiore del valore restituito.</span><span class="sxs-lookup"><span data-stu-id="a4241-358">The system should select the item specified in the low-order word of the return value.</span></span>                                                                        |



 

### <a name="setting-fonts-for-menu-item-text-strings"></a><span data-ttu-id="a4241-359">Impostazione dei tipi di carattere per le stringhe di testo Menu-Item</span><span class="sxs-lookup"><span data-stu-id="a4241-359">Setting Fonts for Menu-Item Text Strings</span></span>

<span data-ttu-id="a4241-360">Questo argomento contiene un esempio di un'applicazione che usa voci di menu create dal proprietario in un menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-360">This topic contains an example from an application that uses owner-drawn menu items in a menu.</span></span> <span data-ttu-id="a4241-361">Il menu contiene gli elementi che impostano gli attributi del tipo di carattere corrente e gli elementi vengono visualizzati utilizzando l'attributo del tipo di carattere appropriato.</span><span class="sxs-lookup"><span data-stu-id="a4241-361">The menu contains items that set the attributes of the current font, and the items are displayed using the appropriate font attribute.</span></span>

<span data-ttu-id="a4241-362">Ecco come viene definito il menu nel file di definizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="a4241-362">Here is how the menu is defined in the resource-definition file.</span></span> <span data-ttu-id="a4241-363">Si noti che le stringhe per le voci di menu Regular, Bold, Italic e Underline vengono assegnate in fase di esecuzione, quindi le stringhe sono vuote nel file di definizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="a4241-363">Note that the strings for the Regular, Bold, Italic, and Underline menu items are assigned at run time, so their strings are empty in the resource-definition file.</span></span>


```
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "",    IDM_REGULAR 
        MENUITEM SEPARATOR 
        MENUITEM    "",    IDM_BOLD 
        MENUITEM    "",    IDM_ITALIC 
        MENUITEM    "",    IDM_ULINE 
    END 
END 
```



<span data-ttu-id="a4241-364">La procedura della finestra dell'applicazione elabora i messaggi coinvolti nell'utilizzo delle voci di menu create dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="a4241-364">The application's window procedure processes the messages involved in using owner-drawn menu items.</span></span> <span data-ttu-id="a4241-365">L'applicazione usa il messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4241-365">The application uses the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to do the following:</span></span>

-   <span data-ttu-id="a4241-366">Impostare il flag **MF \_ OWNERDRAW** per le voci di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-366">Set the **MF\_OWNERDRAW** flag for the menu items.</span></span>
-   <span data-ttu-id="a4241-367">Impostare le stringhe di testo per le voci di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-367">Set the text strings for the menu items.</span></span>
-   <span data-ttu-id="a4241-368">Ottenere gli handle dei tipi di carattere utilizzati per creare gli elementi.</span><span class="sxs-lookup"><span data-stu-id="a4241-368">Obtain handles of the fonts used to draw the items.</span></span>
-   <span data-ttu-id="a4241-369">Ottiene i valori del colore di sfondo e di testo per le voci di menu selezionate.</span><span class="sxs-lookup"><span data-stu-id="a4241-369">Obtain the text and background color values for selected menu items.</span></span>

<span data-ttu-id="a4241-370">Le stringhe di testo e gli handle dei tipi di carattere vengono archiviati in una matrice di strutture di elementi definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-370">The text strings and font handles are stored in an array of application-defined MYITEM structures.</span></span> <span data-ttu-id="a4241-371">La funzione GetAFont definita dall'applicazione crea un tipo di carattere che corrisponde all'attributo del tipo di carattere specificato e restituisce un handle per il tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="a4241-371">The application-defined GetAFont function creates a font that corresponds to the specified font attribute and returns a handle to the font.</span></span> <span data-ttu-id="a4241-372">Gli handle vengono eliminati definitivamente durante l'elaborazione del messaggio [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="a4241-372">The handles are destroyed during the processing of the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span>

<span data-ttu-id="a4241-373">Durante l'elaborazione del messaggio [**WM \_ MeasureItem**](../controls/wm-measureitem.md) , nell'esempio vengono ottenute la larghezza e l'altezza di una stringa di voce di menu e tali valori vengono copiati nella struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="a4241-373">During the processing of the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message, the example gets the width and height of a menu-item string and copies these values into the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure.</span></span> <span data-ttu-id="a4241-374">Il sistema usa i valori di larghezza e altezza per calcolare le dimensioni del menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-374">The system uses the width and height values to calculate the size of the menu.</span></span>

<span data-ttu-id="a4241-375">Durante l'elaborazione del messaggio [**WM \_ DrawItem**](../controls/wm-drawitem.md) , la stringa della voce di menu viene disegnata con la posizione sinistra accanto alla stringa per la bitmap di segno di spunta.</span><span class="sxs-lookup"><span data-stu-id="a4241-375">During the processing of the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message, the menu item's string is drawn with room left next to the string for the check-mark bitmap.</span></span> <span data-ttu-id="a4241-376">Se l'utente seleziona l'elemento, verranno utilizzati i colori di sfondo e di testo selezionati per tracciare l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a4241-376">If the user selects the item, the selected text and background colors are used to draw the item.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    typedef struct _MYITEM 
    { 
        HFONT hfont; 
        LPSTR psz; 
    } MYITEM;             // structure for item font and string  
 
    MYITEM *pmyitem;      // pointer to item's font and string        
    static MYITEM myitem[CITEMS];   // array of MYITEMS               
    static HMENU hmenu;             // handle to main menu            
    static COLORREF crSelText;  // text color of selected item        
    static COLORREF crSelBkgnd; // background color of selected item  
    COLORREF crText;            // text color of unselected item      
    COLORREF crBkgnd;           // background color unselected item   
    LPMEASUREITEMSTRUCT lpmis;  // pointer to item of data             
    LPDRAWITEMSTRUCT lpdis;     // pointer to item drawing data        
    HDC hdc;                    // handle to screen DC                
    SIZE size;                  // menu-item text extents             
    WORD wCheckX;               // check-mark width                   
    int nTextX;                 // width of menu item                 
    int nTextY;                 // height of menu item                
    int i;                      // loop counter                       
    HFONT hfontOld;             // handle to old font                 
    BOOL fSelected = FALSE;     // menu-item selection flag
    size_t * pcch;
    HRESULT hResult;           
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Modify the Regular, Bold, Italic, and Underline 
            // menu items to make them owner-drawn items. Associate 
            // a MYITEM structure with each item to contain the 
            // string for and font handle to each item. 
 
            hmenu = GetMenu(hwnd); 
            ModifyMenu(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED | MF_OWNERDRAW, IDM_REGULAR, 
                (LPTSTR) &myitem[REGULAR]); 
            ModifyMenu(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_BOLD, (LPTSTR) &myitem[BOLD]); 
            ModifyMenu(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ITALIC, 
                (LPTSTR) &myitem[ITALIC]); 
            ModifyMenu(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ULINE, (LPTSTR) &myitem[ULINE]); 
 
            // Retrieve each item's font handle and copy it into 
            // the hfont member of each item's MYITEM structure. 
            // Also, copy each item's string into the structures. 
 
            myitem[REGULAR].hfont = GetAFont(REGULAR); 
            myitem[REGULAR].psz = "Regular"; 
            myitem[BOLD].hfont = GetAFont(BOLD); 
            myitem[BOLD].psz = "Bold"; 
            myitem[ITALIC].hfont = GetAFont(ITALIC); 
            myitem[ITALIC].psz = "Italic"; 
            myitem[ULINE].hfont = GetAFont(ULINE); 
            myitem[ULINE].psz = "Underline"; 
 
            // Retrieve the text and background colors of the 
            // selected menu text. 
 
            crSelText = GetSysColor(COLOR_HIGHLIGHTTEXT); 
            crSelBkgnd = GetSysColor(COLOR_HIGHLIGHT); 
 
            return 0; 
 
        case WM_MEASUREITEM: 
 
            // Retrieve a device context for the main window.  
 
            hdc = GetDC(hwnd); 
 
            // Retrieve pointers to the menu item's 
            // MEASUREITEMSTRUCT structure and MYITEM structure. 
 
            lpmis = (LPMEASUREITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpmis->itemData; 
 
            // Select the font associated with the item into 
            // the main window's device context. 
 
            hfontOld = SelectObject(hdc, pmyitem->hfont); 
 
            // Retrieve the width and height of the item's string, 
            // and then copy the width and height into the 
            // MEASUREITEMSTRUCT structure's itemWidth and 
            // itemHeight members.
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            GetTextExtentPoint32(hdc, pmyitem->psz, 
                *pcch, &size); 
            lpmis->itemWidth = size.cx; 
            lpmis->itemHeight = size.cy; 
 
            // Select the old font back into the device context, 
            // and then release the device context. 
 
            SelectObject(hdc, hfontOld); 
            ReleaseDC(hwnd, hdc); 
 
            return TRUE; 
 
            break; 
 
        case WM_DRAWITEM: 
 
            // Get pointers to the menu item's DRAWITEMSTRUCT 
            // structure and MYITEM structure. 
 
            lpdis = (LPDRAWITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpdis->itemData; 
 
            // If the user has selected the item, use the selected 
            // text and background colors to display the item. 
 
            if (lpdis->itemState & ODS_SELECTED) 
            { 
                crText = SetTextColor(lpdis->hDC, crSelText); 
                crBkgnd = SetBkColor(lpdis->hDC, crSelBkgnd); 
                fSelected = TRUE; 
            } 
 
            // Remember to leave space in the menu item for the 
            // check-mark bitmap. Retrieve the width of the bitmap 
            // and add it to the width of the menu item. 
 
            wCheckX = GetSystemMetrics(SM_CXMENUCHECK); 
            nTextX = wCheckX + lpdis->rcItem.left; 
            nTextY = lpdis->rcItem.top; 
 
            // Select the font associated with the item into the 
            // item's device context, and then draw the string. 
 
            hfontOld = SelectObject(lpdis->hDC, pmyitem->hfont);
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            ExtTextOut(lpdis->hDC, nTextX, nTextY, ETO_OPAQUE, 
                &lpdis->rcItem, pmyitem->psz, 
                *pcch, NULL); 
 
            // Select the previous font back into the device 
            // context. 
 
            SelectObject(lpdis->hDC, hfontOld); 
 
            // Return the text and background colors to their 
            // normal state (not selected). 
 
            if (fSelected) 
            { 
                SetTextColor(lpdis->hDC, crText); 
                SetBkColor(lpdis->hDC, crBkgnd); 
            } 
 
            return TRUE; 
 
        // Process other messages.  
 
        case WM_DESTROY: 
 
            // Destroy the menu items' font handles.  
 
            for (i = 0; i < CITEMS; i++) 
                DeleteObject(myitem[i].hfont); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HFONT GetAFont(int fnFont) 
{ 
    static LOGFONT lf;  // structure for font information  
 
    // Get a handle to the ANSI fixed-pitch font, and copy 
    // information about the font to a LOGFONT structure. 
 
    GetObject(GetStockObject(ANSI_FIXED_FONT), sizeof(LOGFONT), 
        &lf); 
 
    // Set the font attributes, as appropriate.  
 
    if (fnFont == BOLD) 
        lf.lfWeight = FW_BOLD; 
    else 
        lf.lfWeight = FW_NORMAL; 
 
    lf.lfItalic = (fnFont == ITALIC); 
    lf.lfItalic = (fnFont == ULINE); 
 
    // Create the font, and then return its handle.  
 
    return CreateFont(lf.lfHeight, lf.lfWidth, 
        lf.lfEscapement, lf.lfOrientation, lf.lfWeight, 
        lf.lfItalic, lf.lfUnderline, lf.lfStrikeOut, lf.lfCharSet, 
        lf.lfOutPrecision, lf.lfClipPrecision, lf.lfQuality, 
        lf.lfPitchAndFamily, lf.lfFaceName); 
} 
```



### <a name="example-of-owner-drawn-menu-items"></a><span data-ttu-id="a4241-377">Esempio di voci di menu Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="a4241-377">Example of Owner-Drawn Menu Items</span></span>

<span data-ttu-id="a4241-378">Nell'esempio riportato in questo argomento vengono utilizzate voci di menu create dal proprietario in un menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-378">The example in this topic uses owner-drawn menu items in a menu.</span></span> <span data-ttu-id="a4241-379">Le voci di menu selezionano attributi del tipo di carattere specifici e l'applicazione Visualizza ogni voce di menu usando un tipo di carattere con l'attributo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="a4241-379">The menu items select specific font attributes, and the application displays each menu item using a font that has the corresponding attribute.</span></span> <span data-ttu-id="a4241-380">Ad esempio, la voce di menu **corsivo** viene visualizzata in un tipo di carattere corsivo.</span><span class="sxs-lookup"><span data-stu-id="a4241-380">For example, the **Italic** menu item is displayed in an italic font.</span></span> <span data-ttu-id="a4241-381">Il menu **carattere** sulla barra dei menu apre il menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-381">The **Character** menu name on the menu bar opens the menu.</span></span>

<span data-ttu-id="a4241-382">La barra dei menu e il menu a discesa vengono definiti inizialmente da una risorsa modello di menu esteso.</span><span class="sxs-lookup"><span data-stu-id="a4241-382">The menu bar and drop-down menu are defined initially by an extended menu-template resource.</span></span> <span data-ttu-id="a4241-383">Poiché un modello di menu non può specificare elementi creati dal proprietario, il menu contiene inizialmente quattro voci di menu di testo con le seguenti stringhe: "regular", "Bold", "Italic" e "underline".</span><span class="sxs-lookup"><span data-stu-id="a4241-383">Because a menu template cannot specify owner-drawn items, the menu initially contains four text menu items with the following strings: "Regular," "Bold," "Italic," and "Underline."</span></span> <span data-ttu-id="a4241-384">La procedura della finestra dell'applicazione modifica questi elementi in elementi creati dal proprietario quando elabora il messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="a4241-384">The application's window procedure changes these to owner-drawn items when it processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="a4241-385">Quando riceve il messaggio **WM \_ create** , la routine della finestra chiama la funzione OnCreate definita dall'applicazione, che esegue i passaggi seguenti per ciascuna voce di menu:</span><span class="sxs-lookup"><span data-stu-id="a4241-385">When it receives the **WM\_CREATE** message, the window procedure calls the application-defined OnCreate function, which performs the following steps for each menu item:</span></span>

-   <span data-ttu-id="a4241-386">Alloca una struttura di elemento definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-386">Allocates an application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="a4241-387">Ottiene il testo della voce di menu e lo salva nella struttura di elemento definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-387">Gets the text of the menu item and saves it in the application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="a4241-388">Crea il tipo di carattere utilizzato per visualizzare la voce di menu e salva il relativo handle nella struttura di elemento definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-388">Creates the font used to display the menu item and saves its handle in the application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="a4241-389">Consente di modificare il tipo di voce di menu in **MFT \_ OWNERDRAW** e di salvare un puntatore alla struttura di elemento definito dall'applicazione come dati dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a4241-389">Changes the menu item type to **MFT\_OWNERDRAW** and saves a pointer to the application-defined MYITEM structure as item data.</span></span>

<span data-ttu-id="a4241-390">Poiché un puntatore a ogni struttura di elemento definito dall'applicazione viene salvato come dati degli elementi, viene passato alla routine della finestra insieme ai messaggi [**WM \_ MeasureItem**](../controls/wm-measureitem.md) e [**WM \_ DrawItem**](../controls/wm-drawitem.md) per la voce di menu corrispondente.</span><span class="sxs-lookup"><span data-stu-id="a4241-390">Because a pointer to each application-defined MYITEM structure is saved as item data, it is passed to the window procedure in conjunction with the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) and [**WM\_DRAWITEM**](../controls/wm-drawitem.md) messages for the corresponding menu item.</span></span> <span data-ttu-id="a4241-391">Il puntatore è contenuto nel membro **ItemData** delle strutture [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) e [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="a4241-391">The pointer is contained in the **itemData** member of both the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) and [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structures.</span></span>

<span data-ttu-id="a4241-392">Viene inviato un messaggio [**WM \_ MeasureItem**](../controls/wm-measureitem.md) per ogni voce di menu creata dal proprietario la prima volta che viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="a4241-392">A [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message is sent for each owner-drawn menu item the first time it is displayed.</span></span> <span data-ttu-id="a4241-393">L'applicazione elabora questo messaggio selezionando il tipo di carattere per la voce di menu in un contesto di dispositivo e quindi determinando lo spazio necessario per visualizzare il testo della voce di menu in tale tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="a4241-393">The application processes this message by selecting the font for the menu item into a device context and then determining the space required to display the menu item text in that font.</span></span> <span data-ttu-id="a4241-394">Il tipo di carattere e il testo della voce di menu sono entrambi specificati dalla struttura della voce di menu `MYITEM` (la struttura definita dall'applicazione).</span><span class="sxs-lookup"><span data-stu-id="a4241-394">The font and menu item text are both specified by the menu item's `MYITEM` structure (the structure defined by the application).</span></span> <span data-ttu-id="a4241-395">Tramite l'applicazione vengono determinate le dimensioni del testo utilizzando la funzione [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) .</span><span class="sxs-lookup"><span data-stu-id="a4241-395">The application determines the size of the text by using the [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) function.</span></span>

<span data-ttu-id="a4241-396">La routine della finestra elabora il messaggio [**WM \_ DrawItem**](../controls/wm-drawitem.md) visualizzando il testo della voce di menu nel tipo di carattere appropriato.</span><span class="sxs-lookup"><span data-stu-id="a4241-396">The window procedure processes the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message by displaying the menu item text in the appropriate font.</span></span> <span data-ttu-id="a4241-397">Il tipo di carattere e il testo della voce di menu sono entrambi specificati dalla struttura della voce di menu `MYITEM` .</span><span class="sxs-lookup"><span data-stu-id="a4241-397">The font and menu item text are both specified by the menu item's `MYITEM` structure.</span></span> <span data-ttu-id="a4241-398">L'applicazione seleziona il testo e i colori di sfondo appropriati per lo stato della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-398">The application selects text and background colors appropriate to the menu item's state.</span></span>

<span data-ttu-id="a4241-399">La procedura della finestra elabora il messaggio [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) per eliminare i caratteri e liberare memoria.</span><span class="sxs-lookup"><span data-stu-id="a4241-399">The window procedure processes the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message to destroy fonts and free memory.</span></span> <span data-ttu-id="a4241-400">Tramite l'applicazione viene eliminato il tipo di carattere e viene liberata la struttura dell'elemento definita dall'applicazione per ciascuna voce di menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-400">The application deletes the font and frees the application-defined MYITEM structure for each menu item.</span></span>

<span data-ttu-id="a4241-401">Di seguito sono riportate le parti rilevanti del file di intestazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-401">The following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_REGULAR   11 
#define IDM_BOLD      12 
#define IDM_ITALIC    13 
#define IDM_UNDERLINE 14 
 
// Structure associated with menu items 
 
typedef struct tagMYITEM 
{ 
    HFONT hfont; 
    int   cchItemText; 
    char  szItemText[1]; 
} MYITEM; 
 
#define CCH_MAXITEMTEXT 256 
 
```



<span data-ttu-id="a4241-402">Di seguito sono riportate le parti rilevanti della routine della finestra dell'applicazione e delle relative funzioni associate.</span><span class="sxs-lookup"><span data-stu-id="a4241-402">The following are the relevant portions of the application's window procedure and its associated functions.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_MEASUREITEM: 
            OnMeasureItem(hwnd, (LPMEASUREITEMSTRUCT) lParam); 
            return TRUE; 
 
        case WM_DRAWITEM: 
            OnDrawItem(hwnd, (LPDRAWITEMSTRUCT) lParam); 
            return TRUE; 
 
        // Additional message processing goes here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Modify each menu item. Assume that the IDs IDM_REGULAR 
    // through IDM_UNDERLINE are consecutive numbers. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
         // Allocate an item structure, leaving space for a 
         // string of up to CCH_MAXITEMTEXT characters. 
 
        pMyItem = (MYITEM *) LocalAlloc(LMEM_FIXED, 
                sizeof(MYITEM) + CCH_MAXITEMTEXT); 
 
        // Save the item text in the item structure. 
 
        mii.fMask = MIIM_STRING; 
        mii.dwTypeData = pMyItem->szItemText; 
        mii.cch = CCH_MAXITEMTEXT; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem->cchItemText = mii.cch; 
 
        // Reallocate the structure to the minimum required size. 
 
        pMyItem = (MYITEM *) LocalReAlloc(pMyItem, 
                sizeof(MYITEM) + mii.cch, LMEM_MOVEABLE); 
 
        // Create the font used to draw the item. 
 
        pMyItem->hfont = CreateMenuItemFont(uID); 
 
        // Change the item to an owner-drawn item, and save 
        // the address of the item structure as item data. 
 
        mii.fMask = MIIM_FTYPE | MIIM_DATA; 
        mii.fType = MFT_OWNERDRAW; 
        mii.dwItemData = (ULONG_PTR) pMyItem; 
        SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
    } 
    return TRUE; 
} 
 
HFONT CreateMenuItemFont(UINT uID) 
{ 
    LOGFONT lf;
    HRESULT hr; 
 
    ZeroMemory(&lf, sizeof(lf)); 
    lf.lfHeight = 20; 
    hr = StringCchCopy(lf.lfFaceName, 32, "Times New Roman");
    if (FAILED(hr))
    {
    // TODO: writer error handler
    } 
 
    switch (uID) 
    { 
        case IDM_BOLD: 
            lf.lfWeight = FW_HEAVY; 
            break; 
 
        case IDM_ITALIC: 
            lf.lfItalic = TRUE; 
            break; 
 
        case IDM_UNDERLINE: 
            lf.lfUnderline = TRUE; 
            break; 
    } 
    return CreateFontIndirect(&lf); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get  
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Free resources associated with each menu item. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
        // Get the item data. 
 
        mii.fMask = MIIM_DATA; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem = (MYITEM *) mii.dwItemData; 
 
        // Destroy the font and free the item structure. 
 
        DeleteObject(pMyItem->hfont); 
        LocalFree(pMyItem); 
    } 
} 
 
VOID WINAPI OnMeasureItem(HWND hwnd, LPMEASUREITEMSTRUCT lpmis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpmis->itemData; 
    HDC hdc = GetDC(hwnd); 
    HFONT hfntOld = (HFONT)SelectObject(hdc, pMyItem->hfont); 
    SIZE size; 
 
    GetTextExtentPoint32(hdc, pMyItem->szItemText, 
            pMyItem->cchItemText, &size); 
 
    lpmis->itemWidth = size.cx; 
    lpmis->itemHeight = size.cy; 
 
    SelectObject(hdc, hfntOld); 
    ReleaseDC(hwnd, hdc); 
} 
 
VOID WINAPI OnDrawItem(HWND hwnd, LPDRAWITEMSTRUCT lpdis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpdis->itemData; 
    COLORREF clrPrevText, clrPrevBkgnd; 
    HFONT hfntPrev; 
    int x, y; 
 
    // Set the appropriate foreground and background colors. 
 
    if (lpdis->itemState & ODS_SELECTED) 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHTTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHT)); 
    } 
    else 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_MENUTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_MENU)); 
    } 
 
    // Determine where to draw and leave space for a check mark. 
 
    x = lpdis->rcItem.left; 
    y = lpdis->rcItem.top; 
    x += GetSystemMetrics(SM_CXMENUCHECK); 
 
    // Select the font and draw the text. 
 
    hfntPrev = (HFONT)SelectObject(lpdis->hDC, pMyItem->hfont); 
    ExtTextOut(lpdis->hDC, x, y, ETO_OPAQUE, 
            &lpdis->rcItem, pMyItem->szItemText, 
            pMyItem->cchItemText, NULL); 
 
    // Restore the original font and colors. 
 
    SelectObject(lpdis->hDC, hfntPrev); 
    SetTextColor(lpdis->hDC, clrPrevText); 
    SetBkColor(lpdis->hDC, clrPrevBkgnd); 
} 
```



## <a name="using-custom-check-mark-bitmaps"></a><span data-ttu-id="a4241-403">Uso di bitmap con segno di spunta personalizzato</span><span class="sxs-lookup"><span data-stu-id="a4241-403">Using Custom Check Mark Bitmaps</span></span>

<span data-ttu-id="a4241-404">Il sistema fornisce una bitmap di segno di spunta predefinita per la visualizzazione accanto a una voce di menu selezionata.</span><span class="sxs-lookup"><span data-stu-id="a4241-404">The system provides a default check-mark bitmap for displaying next to a menu item that is selected.</span></span> <span data-ttu-id="a4241-405">È possibile personalizzare una singola voce di menu fornendo una coppia di bitmap per sostituire la bitmap di segno di spunta predefinita.</span><span class="sxs-lookup"><span data-stu-id="a4241-405">You can customize an individual menu item by providing a pair of bitmaps to replace the default check-mark bitmap.</span></span> <span data-ttu-id="a4241-406">Il sistema Visualizza una bitmap quando l'elemento è selezionato e l'altro quando è chiaro.</span><span class="sxs-lookup"><span data-stu-id="a4241-406">The system displays one bitmap when the item is selected and the other when it is clear.</span></span> <span data-ttu-id="a4241-407">In questa sezione vengono descritti i passaggi necessari per la creazione e l'utilizzo di bitmap di segno di spunta personalizzate.</span><span class="sxs-lookup"><span data-stu-id="a4241-407">This section describes the steps involved in creating and using custom check-mark bitmaps.</span></span>

-   [<span data-ttu-id="a4241-408">Creazione di bitmap di segno di spunta personalizzati</span><span class="sxs-lookup"><span data-stu-id="a4241-408">Creating Custom Check Mark Bitmaps</span></span>](#creating-custom-check-mark-bitmaps)
-   [<span data-ttu-id="a4241-409">Associazione di bitmap a una voce di menu</span><span class="sxs-lookup"><span data-stu-id="a4241-409">Associating Bitmaps with a Menu Item</span></span>](#associating-bitmaps-with-a-menu-item)
-   [<span data-ttu-id="a4241-410">Impostazione dell'attributo Check-Mark</span><span class="sxs-lookup"><span data-stu-id="a4241-410">Setting the Check-mark Attribute</span></span>](#setting-the-check-mark-attribute)
-   [<span data-ttu-id="a4241-411">Simulazione di caselle di controllo in un menu</span><span class="sxs-lookup"><span data-stu-id="a4241-411">Simulating Check Boxes in a Menu</span></span>](#simulating-check-boxes-in-a-menu)
-   [<span data-ttu-id="a4241-412">Esempio di utilizzo di bitmap di segno di spunta personalizzate</span><span class="sxs-lookup"><span data-stu-id="a4241-412">Example of Using Custom Check-mark Bitmaps</span></span>](#example-of-using-custom-check-mark-bitmaps)

### <a name="creating-custom-check-mark-bitmaps"></a><span data-ttu-id="a4241-413">Creazione di bitmap di segno di spunta personalizzati</span><span class="sxs-lookup"><span data-stu-id="a4241-413">Creating Custom Check Mark Bitmaps</span></span>

<span data-ttu-id="a4241-414">Una bitmap di segno di spunta personalizzata deve avere le stesse dimensioni dell'immagine bitmap di segno di spunta predefinita.</span><span class="sxs-lookup"><span data-stu-id="a4241-414">A custom check-mark bitmap must be the same size as the default check-mark bitmap.</span></span> <span data-ttu-id="a4241-415">È possibile recuperare le dimensioni di segno di spunta predefinite della bitmap chiamando la funzione [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="a4241-415">You can retrieve the default check-mark size of the bitmap by calling the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="a4241-416">La parola di ordine inferiore del valore restituito di questa funzione specifica la larghezza; la parola di ordine superiore specifica l'altezza.</span><span class="sxs-lookup"><span data-stu-id="a4241-416">The low-order word of this function's return value specifies the width; the high-order word specifies the height.</span></span>

<span data-ttu-id="a4241-417">È possibile usare le risorse bitmap per fornire bitmap di segno di spunta.</span><span class="sxs-lookup"><span data-stu-id="a4241-417">You can use bitmap resources to provide check-mark bitmaps.</span></span> <span data-ttu-id="a4241-418">Tuttavia, poiché le dimensioni bitmap richieste variano a seconda del tipo di visualizzazione, potrebbe essere necessario ridimensionare la bitmap in fase di esecuzione tramite la funzione [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) .</span><span class="sxs-lookup"><span data-stu-id="a4241-418">However, because the required bitmap size varies depending on the display type, you may need to resize the bitmap at run time by using the [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) function.</span></span> <span data-ttu-id="a4241-419">A seconda della bitmap, la distorsione causata dal dimensionamento potrebbe produrre risultati inaccettabili.</span><span class="sxs-lookup"><span data-stu-id="a4241-419">Depending on the bitmap, the distortion caused by sizing could produce unacceptable results.</span></span>

<span data-ttu-id="a4241-420">Anziché utilizzare una risorsa bitmap, è possibile creare una bitmap in fase di esecuzione utilizzando le funzioni GDI.</span><span class="sxs-lookup"><span data-stu-id="a4241-420">Instead of using a bitmap resource, you can create a bitmap at run time by using GDI functions.</span></span>

<span data-ttu-id="a4241-421">**Per creare una bitmap in fase di esecuzione**</span><span class="sxs-lookup"><span data-stu-id="a4241-421">**To create a bitmap at run time**</span></span>

1.  <span data-ttu-id="a4241-422">Usare la funzione [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) per creare un contesto di dispositivo compatibile con quello usato dalla finestra principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-422">Use the [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) function to create a device context compatible with the one used by the application's main window.</span></span>

    <span data-ttu-id="a4241-423">Il parametro *HDC* della funzione può specificare **null** o il valore restituito dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="a4241-423">The function's *hdc* parameter can specify either **NULL** or the return value from the function.</span></span> <span data-ttu-id="a4241-424">[**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) restituisce un handle per il contesto di dispositivo compatibile.</span><span class="sxs-lookup"><span data-stu-id="a4241-424">[**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) returns a handle to the compatible device context.</span></span>

2.  <span data-ttu-id="a4241-425">Usare la funzione [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) per creare una bitmap compatibile con la finestra principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-425">Use the [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) function to create a bitmap compatible with the application's main window.</span></span>

    <span data-ttu-id="a4241-426">I parametri *nWidth* e *nHeight* di questa funzione impostano le dimensioni della bitmap; devono specificare le informazioni su larghezza e altezza restituite dalla funzione [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="a4241-426">This function's *nWidth* and *nHeight* parameters set the size of the bitmap; they should specify the width and height information returned by the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span>

    > [!Note]  
    > <span data-ttu-id="a4241-427">È anche possibile usare la funzione [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) per creare una bitmap monocromatica.</span><span class="sxs-lookup"><span data-stu-id="a4241-427">You can also use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) function to create a monochrome bitmap.</span></span>

     

3.  <span data-ttu-id="a4241-428">Usare la funzione [**SelezionaOggetto**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) per selezionare la bitmap nel contesto di dispositivo compatibile.</span><span class="sxs-lookup"><span data-stu-id="a4241-428">Use the [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) function to select the bitmap into the compatible device context.</span></span>
4.  <span data-ttu-id="a4241-429">Usare le funzioni di disegno GDI, ad esempio [**ellisse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) e [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), per disegnare un'immagine nella bitmap o usare funzioni quali [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) e [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) per copiare un'immagine nella bitmap.</span><span class="sxs-lookup"><span data-stu-id="a4241-429">Use GDI drawing functions, such as [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) and [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), to draw an image into the bitmap, or use functions such as [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) and [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) to copy an image into the bitmap.</span></span>

<span data-ttu-id="a4241-430">Per ulteriori informazioni, vedere [bitmap](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="a4241-430">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

### <a name="associating-bitmaps-with-a-menu-item"></a><span data-ttu-id="a4241-431">Associazione di bitmap a una voce di menu</span><span class="sxs-lookup"><span data-stu-id="a4241-431">Associating Bitmaps with a Menu Item</span></span>

<span data-ttu-id="a4241-432">Associare una coppia di bitmap di segno di spunta a una voce di menu passando gli handle delle bitmap alla funzione [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) .</span><span class="sxs-lookup"><span data-stu-id="a4241-432">You associate a pair of check-mark bitmaps with a menu item by passing the handles of the bitmaps to the [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) function.</span></span> <span data-ttu-id="a4241-433">Il parametro *hBitmapUnchecked* identifica la bitmap cancellata e il parametro *hBitmapChecked* identifica la bitmap selezionata.</span><span class="sxs-lookup"><span data-stu-id="a4241-433">The *hBitmapUnchecked* parameter identifies the clear bitmap, and the *hBitmapChecked* parameter identifies the selected bitmap.</span></span> <span data-ttu-id="a4241-434">Se si desidera rimuovere uno o entrambi i segni di spunta da una voce di menu, è possibile impostare il parametro *hBitmapUnchecked* o *hBitmapChecked* , o entrambi, su **null**.</span><span class="sxs-lookup"><span data-stu-id="a4241-434">If you want to remove one or both check marks from a menu item, you can set the *hBitmapUnchecked* or *hBitmapChecked* parameter, or both, to **NULL**.</span></span>

### <a name="setting-the-check-mark-attribute"></a><span data-ttu-id="a4241-435">Impostazione dell'attributo Check-Mark</span><span class="sxs-lookup"><span data-stu-id="a4241-435">Setting the Check-mark Attribute</span></span>

<span data-ttu-id="a4241-436">La funzione [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) imposta l'attributo Check-Mark di una voce di menu su Selected o decleared.</span><span class="sxs-lookup"><span data-stu-id="a4241-436">The [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) function sets a menu item's check-mark attribute to either selected or cleared.</span></span> <span data-ttu-id="a4241-437">È possibile specificare il valore **MF \_ checked** per impostare l'attributo check-mark su Selected e il valore **MF \_ unchecked** per impostarlo su Clear.</span><span class="sxs-lookup"><span data-stu-id="a4241-437">You can specify the **MF\_CHECKED** value to set the check-mark attribute to selected and the **MF\_UNCHECKED** value to set it to clear.</span></span>

<span data-ttu-id="a4241-438">È inoltre possibile impostare lo stato di selezione di una voce di menu tramite la funzione [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="a4241-438">You can also set the check state of a menu item by using the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function.</span></span>

<span data-ttu-id="a4241-439">Talvolta un gruppo di voci di menu rappresenta un set di opzioni che si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="a4241-439">Sometimes a group of menu items represents a set of mutually exclusive options.</span></span> <span data-ttu-id="a4241-440">Utilizzando la funzione [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) , è possibile selezionare una voce di menu rimuovendo contemporaneamente il segno di spunta da tutte le altre voci di menu del gruppo.</span><span class="sxs-lookup"><span data-stu-id="a4241-440">By using the [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) function, you can check one menu item while simultaneously removing the check mark from all other menu items in the group.</span></span>

### <a name="simulating-check-boxes-in-a-menu"></a><span data-ttu-id="a4241-441">Simulazione di caselle di controllo in un menu</span><span class="sxs-lookup"><span data-stu-id="a4241-441">Simulating Check Boxes in a Menu</span></span>

<span data-ttu-id="a4241-442">Questo argomento contiene un esempio che illustra come simulare le caselle di controllo in un menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-442">This topic contains an example that shows how to simulate check boxes in a menu.</span></span> <span data-ttu-id="a4241-443">Nell'esempio è contenuto un menu carattere i cui elementi consentono all'utente di impostare gli attributi grassetto, corsivo e sottolineato del tipo di carattere corrente.</span><span class="sxs-lookup"><span data-stu-id="a4241-443">The example contains a Character menu whose items allow the user to set the bold, italic, and underline attributes of the current font.</span></span> <span data-ttu-id="a4241-444">Quando un attributo del tipo di carattere è attivo, nella casella di controllo accanto alla voce di menu corrispondente viene visualizzato un segno di spunta. in caso contrario, viene visualizzata una casella di controllo vuota accanto all'elemento.</span><span class="sxs-lookup"><span data-stu-id="a4241-444">When a font attribute is in effect, a check mark is displayed in the check box next to the corresponding menu item; otherwise, an empty check box is displayed next to the item.</span></span>

<span data-ttu-id="a4241-445">Nell'esempio viene sostituita la bitmap di segno di spunta predefinita con due bitmap, ovvero una bitmap con una casella di controllo selezionata e la bitmap con una casella vuota.</span><span class="sxs-lookup"><span data-stu-id="a4241-445">The example replaces the default check-mark bitmap with two bitmaps: a bitmap with a selected check box and the bitmap with an empty box.</span></span> <span data-ttu-id="a4241-446">La bitmap della casella di controllo selezionata viene visualizzata accanto alla voce di menu grassetto, corsivo o sottolineato quando l'attributo Check-Mark dell'elemento è impostato su **MF \_ selezionato**.</span><span class="sxs-lookup"><span data-stu-id="a4241-446">The selected check box bitmap is displayed next to the Bold, Italic, or Underline menu item when the item's check-mark attribute is set to **MF\_CHECKED**.</span></span> <span data-ttu-id="a4241-447">La bitmap della casella di controllo Clear o Empty viene visualizzata quando l'attributo Check-Mark è impostato su **MF \_ deselezionato**.</span><span class="sxs-lookup"><span data-stu-id="a4241-447">The clear or empty check box bitmap is displayed when the check-mark attribute is set to **MF\_UNCHECKED**.</span></span>

<span data-ttu-id="a4241-448">Il sistema fornisce una bitmap predefinita che contiene le immagini utilizzate per le caselle di controllo e i pulsanti di opzione.</span><span class="sxs-lookup"><span data-stu-id="a4241-448">The system provides a predefined bitmap that contains the images used for check boxes and radio buttons.</span></span> <span data-ttu-id="a4241-449">L'esempio isola le caselle di controllo selezionate e vuote, le copia in due bitmap separate, quindi le usa come bitmap selezionate e deselezionate per gli elementi del menu **carattere** .</span><span class="sxs-lookup"><span data-stu-id="a4241-449">The example isolates the selected and empty check boxes, copies them to two separate bitmaps, and then uses them as the selected and cleared bitmaps for items in the **Character** menu.</span></span>

<span data-ttu-id="a4241-450">Per recuperare un handle per la bitmap della casella di controllo definita dal sistema, nell'esempio viene chiamata la funzione [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) , specificando **null** come parametro *HINSTANCE* e le **\_ caselle** di controllo OBM come parametro *lpBitmapName* .</span><span class="sxs-lookup"><span data-stu-id="a4241-450">To retrieve a handle to the system-defined check box bitmap, the example calls the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function, specifying **NULL** as the *hInstance* parameter and **OBM\_CHECKBOXES** as the *lpBitmapName* parameter.</span></span> <span data-ttu-id="a4241-451">Poiché le immagini nella bitmap hanno tutte le stesse dimensioni, l'esempio può isolarle dividendo la larghezza e l'altezza della bitmap per il numero di immagini nelle righe e nelle colonne.</span><span class="sxs-lookup"><span data-stu-id="a4241-451">Because the images in the bitmap are all the same size, the example can isolate them by dividing the bitmap width and height by the number of images in its rows and columns.</span></span>

<span data-ttu-id="a4241-452">La parte seguente di un file di definizione delle risorse Mostra come vengono definite le voci di menu nel menu **carattere** .</span><span class="sxs-lookup"><span data-stu-id="a4241-452">The following portion of a resource-definition file shows how the menu items in the **Character** menu are defined.</span></span> <span data-ttu-id="a4241-453">Si noti che inizialmente non sono presenti attributi del tipo di carattere, pertanto l'attributo Check-Mark per l'elemento **Regular** è impostato su Selected e, per impostazione predefinita, l'attributo Check-Mark degli elementi rimanenti è impostato su Clear.</span><span class="sxs-lookup"><span data-stu-id="a4241-453">Note that no font attributes are in effect initially, so the check-mark attribute for the **Regular** item is set to selected and, by default, the check-mark attribute of the remaining items is set to clear.</span></span>


```
#include "men3.h" 
 
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "&Regular",     IDM_REGULAR, CHECKED 
        MENUITEM SEPARATOR 
        MENUITEM    "&Bold",        IDM_BOLD 
        MENUITEM    "&Italic",      IDM_ITALIC 
        MENUITEM    "&Underline",   IDM_ULINE 
    END 
END
```



<span data-ttu-id="a4241-454">Ecco il contenuto pertinente del file di intestazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-454">Here are the relevant contents of the application's header file.</span></span>


```
// Menu-item identifiers  
 
#define IDM_REGULAR 0x1 
#define IDM_BOLD    0x2 
#define IDM_ITALIC  0x4 
#define IDM_ULINE   0x8 
 
// Check-mark flags  
 
#define CHECK   1 
#define UNCHECK 2 
 
// Font-attribute mask  
 
#define ATTRIBMASK 0xe 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
HBITMAP GetMyCheckBitmaps(UINT); 
BYTE CheckOrUncheckMenuItem(BYTE, HMENU); 
```



<span data-ttu-id="a4241-455">Nell'esempio seguente vengono illustrate le parti della routine della finestra che creano le bitmap di segno di spunta; impostare l'attributo Check-Mark delle voci di menu **grassetto**, **corsivo** e **sottolineatura** . e distruggi le bitmap di segno di spunta.</span><span class="sxs-lookup"><span data-stu-id="a4241-455">The following example shows the portions of the window procedure that create the check-mark bitmaps; set the check-mark attribute of the **Bold**, **Italic**, and **Underline** menu items; and destroy check-mark bitmaps.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HBITMAP hbmpCheck;   // handle to checked bitmap    
    static HBITMAP hbmpUncheck; // handle to unchecked bitmap  
    static HMENU hmenu;         // handle to main menu         
    BYTE fbFontAttrib;          // font-attribute flags        
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Call the application-defined GetMyCheckBitmaps 
            // function to get the predefined checked and 
            // unchecked check box bitmaps. 
 
            hbmpCheck = GetMyCheckBitmaps(CHECK); 
            hbmpUncheck = GetMyCheckBitmaps(UNCHECK); 
 
            // Set the checked and unchecked bitmaps for the menu 
            // items. 
 
            hmenu = GetMenu(hwndMain); 
            SetMenuItemBitmaps(hmenu, IDM_BOLD, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ITALIC, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ULINE, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the menu commands.  
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // CheckOrUncheckMenuItem is an application- 
                    // defined function that sets the menu item 
                    // checkmarks and returns the user-selected 
                    // font attributes. 
 
                    fbFontAttrib = CheckOrUncheckMenuItem( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // Set the font attributes.  
 
                    return 0; 
 
                // Process other command messages.  
 
                default: 
                    break; 
            } 
 
            break; 
 
        // Process other window messages.  
 
        case WM_DESTROY: 
 
            // Destroy the checked and unchecked bitmaps.  
 
            DeleteObject(hbmpCheck); 
            DeleteObject(hbmpUncheck); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HBITMAP GetMyCheckBitmaps(UINT fuCheck) 
{ 
    COLORREF crBackground;  // background color                  
    HBRUSH hbrBackground;   // background brush                  
    HBRUSH hbrTargetOld;    // original background brush         
    HDC hdcSource;          // source device context             
    HDC hdcTarget;          // target device context             
    HBITMAP hbmpCheckboxes; // handle to check-box bitmap        
    BITMAP bmCheckbox;      // structure for bitmap data         
    HBITMAP hbmpSourceOld;  // handle to original source bitmap  
    HBITMAP hbmpTargetOld;  // handle to original target bitmap  
    HBITMAP hbmpCheck;      // handle to check-mark bitmap       
    RECT rc;                // rectangle for check-box bitmap    
    WORD wBitmapX;          // width of check-mark bitmap        
    WORD wBitmapY;          // height of check-mark bitmap       
 
    // Get the menu background color and create a solid brush 
    // with that color. 
 
    crBackground = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crBackground); 
 
    // Create memory device contexts for the source and 
    // destination bitmaps. 
 
    hdcSource = CreateCompatibleDC((HDC) NULL); 
    hdcTarget = CreateCompatibleDC(hdcSource); 
 
    // Get the size of the system default check-mark bitmap and 
    // create a compatible bitmap of the same size. 
 
    wBitmapX = GetSystemMetrics(SM_CXMENUCHECK); 
    wBitmapY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    hbmpCheck = CreateCompatibleBitmap(hdcSource, wBitmapX, 
        wBitmapY); 
 
    // Select the background brush and bitmap into the target DC. 
 
    hbrTargetOld = SelectObject(hdcTarget, hbrBackground); 
    hbmpTargetOld = SelectObject(hdcTarget, hbmpCheck); 
 
    // Use the selected brush to initialize the background color 
    // of the bitmap in the target device context. 
 
    PatBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, PATCOPY); 
 
    // Load the predefined check box bitmaps and select it 
    // into the source DC. 
 
    hbmpCheckboxes = LoadBitmap((HINSTANCE) NULL, 
        (LPTSTR) OBM_CHECKBOXES); 
 
    hbmpSourceOld = SelectObject(hdcSource, hbmpCheckboxes); 
 
    // Fill a BITMAP structure with information about the 
    // check box bitmaps, and then find the upper-left corner of 
    // the unchecked check box or the checked check box. 
 
    GetObject(hbmpCheckboxes, sizeof(BITMAP), &bmCheckbox); 
 
    if (fuCheck == UNCHECK) 
    { 
        rc.left = 0; 
        rc.right = (bmCheckbox.bmWidth / 4); 
    } 
    else 
    { 
        rc.left = (bmCheckbox.bmWidth / 4); 
        rc.right = (bmCheckbox.bmWidth / 4) * 2; 
    } 
 
    rc.top = 0; 
    rc.bottom = (bmCheckbox.bmHeight / 3); 
 
    // Copy the appropriate bitmap into the target DC. If the 
    // check-box bitmap is larger than the default check-mark 
    // bitmap, use StretchBlt to make it fit; otherwise, just 
    // copy it. 
 
    if (((rc.right - rc.left) > (int) wBitmapX) || 
            ((rc.bottom - rc.top) > (int) wBitmapY)) 
    {
        StretchBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, 
            hdcSource, rc.left, rc.top, rc.right - rc.left, 
            rc.bottom - rc.top, SRCCOPY); 
    }
 
    else 
    {
        BitBlt(hdcTarget, 0, 0, rc.right - rc.left, 
            rc.bottom - rc.top, 
            hdcSource, rc.left, rc.top, SRCCOPY); 
    }
 
    // Select the old source and destination bitmaps into the 
    // source and destination DCs, and then delete the DCs and 
    // the background brush. 
 
    SelectObject(hdcSource, hbmpSourceOld); 
    SelectObject(hdcTarget, hbrTargetOld); 
    hbmpCheck = SelectObject(hdcTarget, hbmpTargetOld); 
 
    DeleteObject(hbrBackground); 
    DeleteObject(hdcSource); 
    DeleteObject(hdcTarget); 
 
    // Return a handle to the new check-mark bitmap.  
 
    return hbmpCheck; 
} 
 
 
BYTE CheckOrUncheckMenuItem(BYTE bMenuItemID, HMENU hmenu) 
{ 
    DWORD fdwMenu; 
    static BYTE fbAttributes; 
 
    switch (bMenuItemID) 
    { 
        case IDM_REGULAR: 
 
            // Whenever the Regular menu item is selected, add a 
            // check mark to it and then remove checkmarks from 
            // any font-attribute menu items. 
 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
            } 
            fbAttributes = IDM_REGULAR; 
            return fbAttributes; 
 
        case IDM_BOLD: 
        case IDM_ITALIC: 
        case IDM_ULINE: 
 
            // Toggle the check mark for the selected menu item and 
            // set the font attribute flags appropriately. 
 
            fdwMenu = GetMenuState(hmenu, (UINT) bMenuItemID, 
                MF_BYCOMMAND); 
            if (!(fdwMenu & MF_CHECKED)) 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes |= bMenuItemID; 
            }
            else 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes ^= bMenuItemID; 
            } 
 
            // If any font attributes are currently selected, 
            // remove the check mark from the Regular menu item; 
            // if no attributes are selected, add a check mark 
            // to the Regular menu item. 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes &= (BYTE) ~IDM_REGULAR; 
            }
            else 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes = IDM_REGULAR; 
            } 
 
            return fbAttributes; 
    } 
} 
```



### <a name="example-of-using-custom-check-mark-bitmaps"></a><span data-ttu-id="a4241-456">Esempio di utilizzo di bitmap di segno di spunta personalizzate</span><span class="sxs-lookup"><span data-stu-id="a4241-456">Example of Using Custom Check-mark Bitmaps</span></span>

<span data-ttu-id="a4241-457">Nell'esempio riportato in questo argomento vengono assegnate bitmap di segno di spunta personalizzate alle voci di menu di due menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-457">The example in this topic assigns custom check-mark bitmaps to menu items in two menus.</span></span> <span data-ttu-id="a4241-458">Le voci di menu nel primo menu specificano gli attributi dei caratteri: grassetto, corsivo e sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="a4241-458">The menu items in the first menu specify character attributes: bold, italic, and underline.</span></span> <span data-ttu-id="a4241-459">Ogni voce di menu può essere selezionata o deselezionata.</span><span class="sxs-lookup"><span data-stu-id="a4241-459">Each menu item can be either selected or cleared.</span></span> <span data-ttu-id="a4241-460">Per queste voci di menu, nell'esempio vengono utilizzate bitmap di segno di spunta simili agli stati selezionati e cancellati di un controllo casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="a4241-460">For these menu items, the example uses check-mark bitmaps that resemble the selected and cleared states of a check box control.</span></span>

<span data-ttu-id="a4241-461">Le voci di menu nel secondo menu specificano le impostazioni di allineamento del paragrafo: Left, centrato e Right.</span><span class="sxs-lookup"><span data-stu-id="a4241-461">The menu items in the second menu specify paragraph alignment settings: left, centered, and right.</span></span> <span data-ttu-id="a4241-462">Solo una di queste voci di menu viene selezionata in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="a4241-462">Only one of these menu items is selected at any time.</span></span> <span data-ttu-id="a4241-463">Per queste voci di menu, nell'esempio vengono utilizzate bitmap di segno di spunta che assomigliano agli stati selezionati e cancellati di un controllo pulsante di opzione.</span><span class="sxs-lookup"><span data-stu-id="a4241-463">For these menu items, the example uses check-mark bitmaps that resemble the selected and clear states of a radio button control.</span></span>

<span data-ttu-id="a4241-464">La routine della finestra elabora il messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) chiamando la funzione OnCreate definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-464">The window procedure processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message by calling the application-defined OnCreate function.</span></span> <span data-ttu-id="a4241-465">`OnCreate` Crea le quattro bitmap di segno di spunta e le assegna alle voci di menu appropriate tramite la funzione [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) .</span><span class="sxs-lookup"><span data-stu-id="a4241-465">`OnCreate` creates the four check-mark bitmaps and then assigns them to their appropriate menu items by using the [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) function.</span></span>

<span data-ttu-id="a4241-466">Per creare ogni bitmap, OnCreate chiama la funzione CreateMenuBitmaps definita dall'applicazione, specificando un puntatore a una funzione di disegno specifica della bitmap.</span><span class="sxs-lookup"><span data-stu-id="a4241-466">To create each bitmap, OnCreate calls the application-defined CreateMenuBitmaps function, specifying a pointer to a bitmap-specific drawing function.</span></span> <span data-ttu-id="a4241-467">CreateMenuBitmaps crea una bitmap monocromatica della dimensione richiesta, la seleziona in un contesto di dispositivo di memoria e cancella lo sfondo.</span><span class="sxs-lookup"><span data-stu-id="a4241-467">CreateMenuBitmaps creates a monochrome bitmap of the required size, selects it into a memory device context, and erases the background.</span></span> <span data-ttu-id="a4241-468">Chiama quindi la funzione di disegno specificata per compilare in primo piano.</span><span class="sxs-lookup"><span data-stu-id="a4241-468">Then it calls the specified drawing function to fill in the foreground.</span></span>

<span data-ttu-id="a4241-469">Le quattro funzioni di disegno definite dall'applicazione sono DrawCheck, DrawUncheck, **DrawRadioCheck** e DrawRadioUncheck.</span><span class="sxs-lookup"><span data-stu-id="a4241-469">The four application-defined drawing functions are DrawCheck, DrawUncheck, **DrawRadioCheck**, and DrawRadioUncheck.</span></span> <span data-ttu-id="a4241-470">Vengono disegnato un rettangolo con una X, un rettangolo vuoto, un'ellisse contenente un'ellisse riempita più piccola e un'ellisse vuota, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="a4241-470">They draw a rectangle with an X, an empty rectangle, an ellipse containing a smaller filled ellipse, and an empty ellipse, respectively.</span></span>

<span data-ttu-id="a4241-471">La routine della finestra elabora il messaggio [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) eliminando le bitmap di segno di spunta.</span><span class="sxs-lookup"><span data-stu-id="a4241-471">The window procedure processes the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message by deleting the check-mark bitmaps.</span></span> <span data-ttu-id="a4241-472">Recupera ogni handle bitmap usando la funzione [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) e quindi passa un handle alla funzione.</span><span class="sxs-lookup"><span data-stu-id="a4241-472">It retrieves each bitmap handle by using the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function and then passes a handle to the function.</span></span>

<span data-ttu-id="a4241-473">Quando l'utente sceglie una voce di menu, viene inviato un messaggio di [**\_ comando WM**](wm-command.md) alla finestra proprietaria.</span><span class="sxs-lookup"><span data-stu-id="a4241-473">When the user chooses a menu item, a [**WM\_COMMAND**](wm-command.md) message is sent to the owner window.</span></span> <span data-ttu-id="a4241-474">Per le voci di menu del menu **carattere** , la routine della finestra chiama la funzione CheckCharacterItem definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-474">For menu items on the **Character** menu, the window procedure calls the application-defined CheckCharacterItem function.</span></span> <span data-ttu-id="a4241-475">Per gli elementi del menu di **paragrafo** , la routine della finestra chiama la funzione CheckParagraphItem definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-475">For items on the **Paragraph** menu, the window procedure calls the application-defined CheckParagraphItem function.</span></span>

<span data-ttu-id="a4241-476">Ogni elemento del menu **carattere** può essere selezionato e cancellato in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="a4241-476">Each item on the **Character** menu can be selected and cleared independently.</span></span> <span data-ttu-id="a4241-477">Pertanto, CheckCharacterItem passa semplicemente lo stato di selezione della voce di menu specificata.</span><span class="sxs-lookup"><span data-stu-id="a4241-477">Therefore, CheckCharacterItem simply switches the specified menu item's check state.</span></span> <span data-ttu-id="a4241-478">Per prima cosa, la funzione chiama la funzione [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) per ottenere lo stato della voce di menu corrente.</span><span class="sxs-lookup"><span data-stu-id="a4241-478">First, the function calls the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function to get the current menu item state.</span></span> <span data-ttu-id="a4241-479">Passa quindi il flag di stato di **\_ selezione di MFS** e imposta il nuovo stato chiamando la funzione [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="a4241-479">Then it switches the **MFS\_CHECKED** state flag and sets the new state by calling the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function.</span></span>

<span data-ttu-id="a4241-480">A differenza degli attributi carattere, è possibile selezionare un solo allineamento paragrafo alla volta.</span><span class="sxs-lookup"><span data-stu-id="a4241-480">Unlike character attributes, only one paragraph alignment can be selected at a time.</span></span> <span data-ttu-id="a4241-481">CheckParagraphItem controlla quindi la voce di menu specificata e rimuove il segno di spunta da tutti gli altri elementi nel menu.</span><span class="sxs-lookup"><span data-stu-id="a4241-481">Therefore, CheckParagraphItem checks the specified menu item and removes the check mark from all other items on the menu.</span></span> <span data-ttu-id="a4241-482">A tale scopo, viene chiamata la funzione [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) .</span><span class="sxs-lookup"><span data-stu-id="a4241-482">To do so, it calls the [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) function.</span></span>

<span data-ttu-id="a4241-483">Di seguito sono riportate le parti rilevanti del file di intestazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4241-483">Following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_BOLD      11 
#define IDM_ITALIC    12 
#define IDM_UNDERLINE 13 
 
// Menu-item identifiers for the Paragraph menu 
 
#define IDM_PARAGRAPH 20 
#define IDM_LEFT      21 
#define IDM_CENTER    22 
#define IDM_RIGHT     23 
 
// Function-pointer type for drawing functions 
 
typedef VOID (WINAPI * DRAWFUNC)(HDC hdc, SIZE size); 
 
```



<span data-ttu-id="a4241-484">Di seguito sono riportate le parti pertinenti della routine della finestra dell'applicazione e delle relative funzioni.</span><span class="sxs-lookup"><span data-stu-id="a4241-484">The following are the relevant portions of the application's window procedure and related functions.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_UNDERLINE: 
                    CheckCharacterItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                case IDM_LEFT: 
                case IDM_CENTER: 
                case IDM_RIGHT: 
                    CheckParagraphItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                // Process other commands here. 
 
            } 
            break; 
 
        // Process other messages here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
VOID WINAPI CheckCharacterItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the state of the specified menu item. 
 
    mii.fMask = MIIM_STATE;    // information to get 
    GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
 
    // Toggle the checked state. 
 
    mii.fState ^= MFS_CHECKED; 
    SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
} 
 
VOID WINAPI CheckParagraphItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Check the specified item and uncheck all the others. 
 
    CheckMenuRadioItem( 
            hmenuPopup,         // handle to menu 
            IDM_LEFT,           // first item in range 
            IDM_RIGHT,          // last item in range 
            uID,                // item to check 
            MF_BYCOMMAND        // IDs, not positions 
            ); 
} 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    HBITMAP hbmChecked; 
    HBITMAP hbmUnchecked; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_BOLD; uID <= IDM_UNDERLINE; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Get a handle to the Paragraph pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawRadioCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawRadioUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_LEFT; uID <= IDM_RIGHT; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Initially check the IDM_LEFT paragraph item. 
 
    CheckMenuRadioItem(hmenuPopup, IDM_LEFT, IDM_RIGHT, 
            IDM_LEFT, MF_BYCOMMAND); 
    return TRUE; 
} 
 
HBITMAP WINAPI CreateMenuBitmap(DRAWFUNC lpfnDraw) 
{ 
    // Create a DC compatible with the desktop window's DC. 
 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
 
    // Determine the required bitmap size. 
 
    SIZE size = { GetSystemMetrics(SM_CXMENUCHECK), 
                  GetSystemMetrics(SM_CYMENUCHECK) }; 
 
    // Create a monochrome bitmap and select it. 
 
    HBITMAP hbm = CreateBitmap(size.cx, size.cy, 1, 1, NULL); 
    HBITMAP hbmOld = SelectObject(hdcMem, hbm); 
 
    // Erase the background and call the drawing function. 
 
    PatBlt(hdcMem, 0, 0, size.cx, size.cy, WHITENESS); 
    (*lpfnDraw)(hdcMem, size); 
 
    // Clean up. 
 
    SelectObject(hdcMem, hbmOld); 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
    return hbm; 
} 
 
VOID WINAPI DrawCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    MoveToEx(hdc, 0, 0, NULL); 
    LineTo(hdc, size.cx, size.cy); 
    MoveToEx(hdc, 0, size.cy - 1, NULL); 
    LineTo(hdc, size.cx - 1, 0); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, GetStockObject(BLACK_BRUSH)); 
    Ellipse(hdc, 2, 2, size.cx - 2, size.cy - 2); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_BOLD, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_LEFT, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
} 
```



 

 