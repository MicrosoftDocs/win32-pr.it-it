---
title: Uso degli Appunti
description: Questa sezione contiene esempi di codice per le seguenti attività
ms.assetid: 377fb2cc-5b46-481a-8222-9291e504ae2c
keywords:
- Appunti, taglio di dati
- Appunti, copia di dati
- Appunti, incolla di dati
- Appunti, selezione dei dati
- Appunti, comandi di menu modifica
- Appunti, visualizzatori
- Appunti, finestre del Visualizzatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7c7e7d6db6f25bc1016eefbcc5afc9f5e0db44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337910"
---
# <a name="using-the-clipboard"></a><span data-ttu-id="25402-110">Uso degli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-110">Using the Clipboard</span></span>

<span data-ttu-id="25402-111">Questa sezione contiene esempi di codice per le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="25402-111">This section has code samples for the following tasks:</span></span>

-   [<span data-ttu-id="25402-112">Implementazione dei comandi taglia, copia e incolla</span><span class="sxs-lookup"><span data-stu-id="25402-112">Implementing the Cut, Copy, and Paste Commands</span></span>](#implementing-the-cut-copy-and-paste-commands)
    -   [<span data-ttu-id="25402-113">Selezione dei dati</span><span class="sxs-lookup"><span data-stu-id="25402-113">Selecting Data</span></span>](#selecting-data)
    -   [<span data-ttu-id="25402-114">Creazione di un menu modifica</span><span class="sxs-lookup"><span data-stu-id="25402-114">Creating an Edit Menu</span></span>](#creating-an-edit-menu)
    -   [<span data-ttu-id="25402-115">Elaborazione del \_ messaggio WM INITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="25402-115">Processing the WM\_INITMENUPOPUP Message</span></span>](#processing-the-wm_initmenupopup-message)
    -   [<span data-ttu-id="25402-116">Elaborazione del \_ messaggio di comando WM</span><span class="sxs-lookup"><span data-stu-id="25402-116">Processing the WM\_COMMAND Message</span></span>](#processing-the-wm_command-message)
    -   [<span data-ttu-id="25402-117">Copia delle informazioni negli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-117">Copying Information to the Clipboard</span></span>](#copying-information-to-the-clipboard)
    -   [<span data-ttu-id="25402-118">Incollare le informazioni dagli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-118">Pasting Information from the Clipboard</span></span>](#pasting-information-from-the-clipboard)
    -   [<span data-ttu-id="25402-119">Registrazione di un formato degli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-119">Registering a Clipboard Format</span></span>](#registering-a-clipboard-format)
    -   [<span data-ttu-id="25402-120">Elaborazione dei \_ messaggi WM RENDERFORMAT e WM \_ RENDERALLFORMATS</span><span class="sxs-lookup"><span data-stu-id="25402-120">Processing the WM\_RENDERFORMAT and WM\_RENDERALLFORMATS Messages</span></span>](#processing-the-wm_renderformat-and-wm_renderallformats-messages)
    -   [<span data-ttu-id="25402-121">Elaborazione del \_ messaggio WM DESTROYCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="25402-121">Processing the WM\_DESTROYCLIPBOARD Message</span></span>](#processing-the-wm_destroyclipboard-message)
    -   [<span data-ttu-id="25402-122">Uso del formato degli Appunti Owner-Display</span><span class="sxs-lookup"><span data-stu-id="25402-122">Using the Owner-Display Clipboard Format</span></span>](#using-the-owner-display-clipboard-format)
-   [<span data-ttu-id="25402-123">Monitoraggio del contenuto degli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-123">Monitoring Clipboard Contents</span></span>](#monitoring-clipboard-contents)
-   [<span data-ttu-id="25402-124">Esecuzione di query sul numero di sequenza degli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-124">Querying the Clipboard Sequence Number</span></span>](#querying-the-clipboard-sequence-number)
-   [<span data-ttu-id="25402-125">Creazione di un listener di formato degli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-125">Creating a Clipboard Format Listener</span></span>](#creating-a-clipboard-format-listener)
-   [<span data-ttu-id="25402-126">Creazione di una finestra Visualizzatore Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-126">Creating a Clipboard Viewer Window</span></span>](#creating-a-clipboard-viewer-window)
-   [<span data-ttu-id="25402-127">Aggiunta di una finestra alla catena del visualizzatore degli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-127">Adding a Window to the Clipboard Viewer Chain</span></span>](#adding-a-window-to-the-clipboard-viewer-chain)
    -   [<span data-ttu-id="25402-128">Elaborazione del \_ messaggio WM CHANGECBCHAIN</span><span class="sxs-lookup"><span data-stu-id="25402-128">Processing the WM\_CHANGECBCHAIN Message</span></span>](#processing-the-wm_changecbchain-message)
    -   [<span data-ttu-id="25402-129">Rimozione di una finestra dalla catena del visualizzatore degli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-129">Removing a Window from the Clipboard Viewer Chain</span></span>](#removing-a-window-from-the-clipboard-viewer-chain)
    -   [<span data-ttu-id="25402-130">Elaborazione del \_ messaggio WM DRAWCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="25402-130">Processing the WM\_DRAWCLIPBOARD Message</span></span>](#processing-the-wm_drawclipboard-message)
    -   [<span data-ttu-id="25402-131">Esempio di Visualizzatore Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-131">Example of a Clipboard Viewer</span></span>](#example-of-a-clipboard-viewer)

## <a name="implementing-the-cut-copy-and-paste-commands"></a><span data-ttu-id="25402-132">Implementazione dei comandi taglia, copia e incolla</span><span class="sxs-lookup"><span data-stu-id="25402-132">Implementing the Cut, Copy, and Paste Commands</span></span>

<span data-ttu-id="25402-133">Questa sezione descrive come vengono implementati i comandi **taglia**, **copia** e **Incolla** standard in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="25402-133">This section describes how standard **Cut**, **Copy**, and **Paste** commands are implemented in an application.</span></span> <span data-ttu-id="25402-134">Nell'esempio riportato in questa sezione vengono usati questi metodi per inserire i dati negli appunti usando un formato degli Appunti registrato, il formato **CF \_ OWNERDISPLAY** e il formato di **\_ testo CF** .</span><span class="sxs-lookup"><span data-stu-id="25402-134">The example in this section uses these methods to place data on the clipboard using a registered clipboard format, the **CF\_OWNERDISPLAY** format, and the **CF\_TEXT** format.</span></span> <span data-ttu-id="25402-135">Il formato registrato viene utilizzato per rappresentare le finestre di testo rettangolari o ellittiche, denominate etichette.</span><span class="sxs-lookup"><span data-stu-id="25402-135">The registered format is used to represent rectangular or elliptical text windows, called labels.</span></span>

### <a name="selecting-data"></a><span data-ttu-id="25402-136">Selezione dei dati</span><span class="sxs-lookup"><span data-stu-id="25402-136">Selecting Data</span></span>

<span data-ttu-id="25402-137">Prima che le informazioni possano essere copiate negli Appunti, l'utente deve selezionare informazioni specifiche da copiare o tagliare.</span><span class="sxs-lookup"><span data-stu-id="25402-137">Before information can be copied to the clipboard, the user must select specific information to be copied or cut.</span></span> <span data-ttu-id="25402-138">Un'applicazione deve fornire un mezzo per consentire all'utente di selezionare le informazioni all'interno di un documento e un tipo di feedback visivo per indicare i dati selezionati.</span><span class="sxs-lookup"><span data-stu-id="25402-138">An application should provide a means for the user to select information within a document and some kind of visual feedback to indicate selected data.</span></span>

### <a name="creating-an-edit-menu"></a><span data-ttu-id="25402-139">Creazione di un menu modifica</span><span class="sxs-lookup"><span data-stu-id="25402-139">Creating an Edit Menu</span></span>

<span data-ttu-id="25402-140">Un'applicazione deve caricare una tabella dei tasti di scelta rapida contenente gli acceleratori della tastiera standard per i comandi di menu **modifica** .</span><span class="sxs-lookup"><span data-stu-id="25402-140">An application should load an accelerator table containing the standard keyboard accelerators for the **Edit** menu commands.</span></span> <span data-ttu-id="25402-141">Per rendere effettive le acceleratori, è necessario aggiungere la funzione [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) al ciclo di messaggi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="25402-141">The [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function must be added to the application's message loop for the accelerators to take effect.</span></span> <span data-ttu-id="25402-142">Per ulteriori informazioni sugli acceleratori tastiera, vedere [tasti](/windows/desktop/menurc/keyboard-accelerators)di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="25402-142">For more information about keyboard accelerators, see [Keyboard Accelerators](/windows/desktop/menurc/keyboard-accelerators).</span></span>

### <a name="processing-the-wm_initmenupopup-message"></a><span data-ttu-id="25402-143">Elaborazione del \_ messaggio WM INITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="25402-143">Processing the WM\_INITMENUPOPUP Message</span></span>

<span data-ttu-id="25402-144">Non tutti i comandi degli Appunti sono disponibili per l'utente in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="25402-144">Not all clipboard commands are available to the user at any given time.</span></span> <span data-ttu-id="25402-145">Un'applicazione deve elaborare il messaggio [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) per abilitare le voci di menu per i comandi disponibili e disabilitare i comandi non disponibili.</span><span class="sxs-lookup"><span data-stu-id="25402-145">An application should process the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) message to enable the menu items for available commands and disable unavailable commands.</span></span>

<span data-ttu-id="25402-146">Di seguito è riportato il caso [**\_ INITMENUPOPUP di WM**](/windows/desktop/menurc/wm-initmenupopup) per un'applicazione denominata Label.</span><span class="sxs-lookup"><span data-stu-id="25402-146">Following is the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) case for an application named Label.</span></span>


```
case WM_INITMENUPOPUP:
    InitMenu((HMENU) wParam);
    break;
```



<span data-ttu-id="25402-147">La funzione InitMenu è definita come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="25402-147">The InitMenu function is defined as follows.</span></span>


```
void WINAPI InitMenu(HMENU hmenu) 
{ 
    int  cMenuItems = GetMenuItemCount(hmenu); 
    int  nPos; 
    UINT id; 
    UINT fuFlags; 
    PLABELBOX pbox = (hwndSelected == NULL) ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    for (nPos = 0; nPos < cMenuItems; nPos++) 
    { 
        id = GetMenuItemID(hmenu, nPos); 
 
        switch (id) 
        { 
            case IDM_CUT: 
            case IDM_COPY: 
            case IDM_DELETE: 
                if (pbox == NULL || !pbox->fSelected) 
                    fuFlags = MF_BYCOMMAND | MF_GRAYED; 
                else if (pbox->fEdit) 
                    fuFlags = (id != IDM_DELETE && pbox->ichSel 
                            == pbox->ichCaret) ? 
                        MF_BYCOMMAND | MF_GRAYED : 
                        MF_BYCOMMAND | MF_ENABLED; 
                else 
                    fuFlags = MF_BYCOMMAND | MF_ENABLED; 
 
                EnableMenuItem(hmenu, id, fuFlags); 
                break; 
 
            case IDM_PASTE: 
                if (pbox != NULL && pbox->fEdit) 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable(CF_TEXT) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
                else 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable( 
                                uLabelFormat) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
 
        } 
    } 
}
```



### <a name="processing-the-wm_command-message"></a><span data-ttu-id="25402-148">Elaborazione del \_ messaggio di comando WM</span><span class="sxs-lookup"><span data-stu-id="25402-148">Processing the WM\_COMMAND Message</span></span>

<span data-ttu-id="25402-149">Per elaborare i comandi di menu, aggiungere il case del [**\_ comando WM**](/windows/desktop/menurc/wm-command) alla routine della finestra principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="25402-149">To process menu commands, add the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) case to your application's main window procedure.</span></span> <span data-ttu-id="25402-150">Di seguito è riportato il caso del **\_ comando WM** per la routine della finestra dell'applicazione Label.</span><span class="sxs-lookup"><span data-stu-id="25402-150">Following is the **WM\_COMMAND** case for the Label application's window procedure.</span></span>


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_CUT: 
            if (EditCopy()) 
                EditDelete(); 
            break; 
 
        case IDM_COPY: 
            EditCopy(); 
            break; 
 
        case IDM_PASTE: 
            EditPaste(); 
            break; 
 
        case IDM_DELETE: 
            EditDelete(); 
            break; 
 
        case IDM_EXIT: 
            DestroyWindow(hwnd); 
    } 
    break; 
```



<span data-ttu-id="25402-151">Per eseguire i comandi **Copy** e **Cut** , la routine della finestra chiama la funzione EditCopy definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="25402-151">To carry out the **Copy** and **Cut** commands, the window procedure calls the application-defined EditCopy function.</span></span> <span data-ttu-id="25402-152">Per ulteriori informazioni, vedere [copia di informazioni negli Appunti](#copying-information-to-the-clipboard).</span><span class="sxs-lookup"><span data-stu-id="25402-152">For more information, see [Copying Information to the Clipboard](#copying-information-to-the-clipboard).</span></span> <span data-ttu-id="25402-153">Per eseguire il comando **Incolla** , la routine della finestra chiama la funzione EditPaste definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="25402-153">To carry out the **Paste** command, the window procedure calls the application-defined EditPaste function.</span></span> <span data-ttu-id="25402-154">Per ulteriori informazioni sulla funzione EditPaste, vedere [incollare le informazioni dagli Appunti](#pasting-information-from-the-clipboard).</span><span class="sxs-lookup"><span data-stu-id="25402-154">For more information about the EditPaste function, see [Pasting Information from the Clipboard](#pasting-information-from-the-clipboard).</span></span>

### <a name="copying-information-to-the-clipboard"></a><span data-ttu-id="25402-155">Copia delle informazioni negli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-155">Copying Information to the Clipboard</span></span>

<span data-ttu-id="25402-156">Nell'applicazione Label la funzione EditCopy definita dall'applicazione copia la selezione corrente negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-156">In the Label application, the application-defined EditCopy function copies the current selection to the clipboard.</span></span> <span data-ttu-id="25402-157">Questa funzione esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="25402-157">This function does the following:</span></span>

1.  <span data-ttu-id="25402-158">Apre gli Appunti chiamando la funzione [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .</span><span class="sxs-lookup"><span data-stu-id="25402-158">Opens the clipboard by calling the [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) function.</span></span>
2.  <span data-ttu-id="25402-159">Svuota gli Appunti chiamando la funzione [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) .</span><span class="sxs-lookup"><span data-stu-id="25402-159">Empties the clipboard by calling the [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) function.</span></span>
3.  <span data-ttu-id="25402-160">Chiama la funzione [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) una volta per ogni formato degli Appunti fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="25402-160">Calls the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function once for each clipboard format the application provides.</span></span>
4.  <span data-ttu-id="25402-161">Chiude gli Appunti chiamando la funzione [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .</span><span class="sxs-lookup"><span data-stu-id="25402-161">Closes the clipboard by calling the [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) function.</span></span>

<span data-ttu-id="25402-162">A seconda della selezione corrente, tramite la funzione EditCopy viene copiato un intervallo di testo o viene copiata una struttura definita dall'applicazione che rappresenta un'intera etichetta.</span><span class="sxs-lookup"><span data-stu-id="25402-162">Depending on the current selection, the EditCopy function either copies a range of text or copies an application-defined structure representing an entire label.</span></span> <span data-ttu-id="25402-163">La struttura, denominata LABELBOX, viene definita come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="25402-163">The structure, called LABELBOX, is defined as follows.</span></span>


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



<span data-ttu-id="25402-164">Di seguito è riportata la funzione EditCopy.</span><span class="sxs-lookup"><span data-stu-id="25402-164">Following is the EditCopy function.</span></span>


```
BOOL WINAPI EditCopy(VOID) 
{ 
    PLABELBOX pbox; 
    LPTSTR  lptstrCopy; 
    HGLOBAL hglbCopy; 
    int ich1, ich2, cch; 
 
    if (hwndSelected == NULL) 
        return FALSE; 
 
    // Open the clipboard, and empty it. 
 
    if (!OpenClipboard(hwndMain)) 
        return FALSE; 
    EmptyClipboard(); 
 
    // Get a pointer to the structure for the selected label. 
 
    pbox = (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If text is selected, copy it using the CF_TEXT format. 
 
    if (pbox->fEdit) 
    { 
        if (pbox->ichSel == pbox->ichCaret)     // zero length
        {   
            CloseClipboard();                   // selection 
            return FALSE; 
        } 
 
        if (pbox->ichSel < pbox->ichCaret) 
        { 
            ich1 = pbox->ichSel; 
            ich2 = pbox->ichCaret; 
        } 
        else 
        { 
            ich1 = pbox->ichCaret; 
            ich2 = pbox->ichSel; 
        } 
        cch = ich2 - ich1; 
 
        // Allocate a global memory object for the text. 
 
        hglbCopy = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglbCopy == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
 
        // Lock the handle and copy the text to the buffer. 
 
        lptstrCopy = GlobalLock(hglbCopy); 
        memcpy(lptstrCopy, &pbox->atchLabel[ich1], 
            cch * sizeof(TCHAR)); 
        lptstrCopy[cch] = (TCHAR) 0;    // null character 
        GlobalUnlock(hglbCopy); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglbCopy); 
    } 
 
    // If no text is selected, the label as a whole is copied. 
 
    else 
    { 
        // Save a copy of the selected label as a local memory 
        // object. This copy is used to render data on request. 
        // It is freed in response to the WM_DESTROYCLIPBOARD 
        // message. 
 
        pboxLocalClip = (PLABELBOX) LocalAlloc( 
            LMEM_FIXED, 
            sizeof(LABELBOX) 
        ); 
        if (pboxLocalClip == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
        memcpy(pboxLocalClip, pbox, sizeof(LABELBOX)); 
        pboxLocalClip->fSelected = FALSE; 
        pboxLocalClip->fEdit = FALSE; 
 
        // Place a registered clipboard format, the owner-display 
        // format, and the CF_TEXT format on the clipboard using 
        // delayed rendering. 
 
        SetClipboardData(uLabelFormat, NULL); 
        SetClipboardData(CF_OWNERDISPLAY, NULL); 
        SetClipboardData(CF_TEXT, NULL); 
    } 
 
    // Close the clipboard. 
 
    CloseClipboard(); 
 
    return TRUE; 
}
```



### <a name="pasting-information-from-the-clipboard"></a><span data-ttu-id="25402-165">Incollare le informazioni dagli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-165">Pasting Information from the Clipboard</span></span>

<span data-ttu-id="25402-166">Nell'applicazione Label la funzione EditPaste definita dall'applicazione incolla il contenuto degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-166">In the Label application, the application-defined EditPaste function pastes the content of the clipboard.</span></span> <span data-ttu-id="25402-167">Questa funzione esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="25402-167">This function does the following:</span></span>

1.  <span data-ttu-id="25402-168">Apre gli Appunti chiamando la funzione [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .</span><span class="sxs-lookup"><span data-stu-id="25402-168">Opens the clipboard by calling the [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) function.</span></span>
2.  <span data-ttu-id="25402-169">Determina quale dei formati degli appunti disponibili recuperare.</span><span class="sxs-lookup"><span data-stu-id="25402-169">Determines which of the available clipboard formats to retrieve.</span></span>
3.  <span data-ttu-id="25402-170">Recupera l'handle per i dati nel formato selezionato chiamando la funzione [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="25402-170">Retrieves the handle to the data in the selected format by calling the [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) function.</span></span>
4.  <span data-ttu-id="25402-171">Inserisce una copia dei dati nel documento.</span><span class="sxs-lookup"><span data-stu-id="25402-171">Inserts a copy of the data into the document.</span></span>

    <span data-ttu-id="25402-172">L'handle restituito da [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) è ancora di proprietà degli Appunti, quindi un'applicazione non deve liberarlo o lasciarlo bloccato.</span><span class="sxs-lookup"><span data-stu-id="25402-172">The handle returned by [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) is still owned by the clipboard, so an application must not free it or leave it locked.</span></span>

5.  <span data-ttu-id="25402-173">Chiude gli Appunti chiamando la funzione [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .</span><span class="sxs-lookup"><span data-stu-id="25402-173">Closes the clipboard by calling the [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) function.</span></span>

<span data-ttu-id="25402-174">Se un'etichetta è selezionata e contiene un punto di inserimento, la funzione EditPaste inserisce il testo dagli Appunti nel punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="25402-174">If a label is selected and contains an insertion point, the EditPaste function inserts the text from the clipboard at the insertion point.</span></span> <span data-ttu-id="25402-175">Se non è presente alcuna selezione o se è selezionata un'etichetta, la funzione crea una nuova etichetta, usando la struttura LABELBOX definita dall'applicazione negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-175">If there is no selection or if a label is selected, the function creates a new label, using the application-defined LABELBOX structure on the clipboard.</span></span> <span data-ttu-id="25402-176">La struttura LABELBOX viene posizionata negli Appunti utilizzando un formato degli Appunti registrato.</span><span class="sxs-lookup"><span data-stu-id="25402-176">The LABELBOX structure is placed on the clipboard by using a registered clipboard format.</span></span>

<span data-ttu-id="25402-177">La struttura, denominata LABELBOX, viene definita come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="25402-177">The structure, called LABELBOX, is defined as follows.</span></span>


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



<span data-ttu-id="25402-178">Di seguito è riportata la funzione EditPaste.</span><span class="sxs-lookup"><span data-stu-id="25402-178">Following is the EditPaste function.</span></span>


```
VOID WINAPI EditPaste(VOID) 
{ 
    PLABELBOX pbox; 
    HGLOBAL   hglb; 
    LPTSTR    lptstr; 
    PLABELBOX pboxCopy; 
    int cx, cy; 
    HWND hwnd; 
 
    pbox = hwndSelected == NULL ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If the application is in edit mode, 
    // get the clipboard text. 
 
    if (pbox != NULL && pbox->fEdit) 
    { 
        if (!IsClipboardFormatAvailable(CF_TEXT)) 
            return; 
        if (!OpenClipboard(hwndMain)) 
            return; 
 
        hglb = GetClipboardData(CF_TEXT); 
        if (hglb != NULL) 
        { 
            lptstr = GlobalLock(hglb); 
            if (lptstr != NULL) 
            { 
                // Call the application-defined ReplaceSelection 
                // function to insert the text and repaint the 
                // window. 
 
                ReplaceSelection(hwndSelected, pbox, lptstr); 
                GlobalUnlock(hglb); 
            } 
        } 
        CloseClipboard(); 
 
        return; 
    } 
 
    // If the application is not in edit mode, 
    // create a label window. 
 
    if (!IsClipboardFormatAvailable(uLabelFormat)) 
        return; 
    if (!OpenClipboard(hwndMain)) 
        return; 
 
    hglb = GetClipboardData(uLabelFormat); 
    if (hglb != NULL) 
    { 
        pboxCopy = GlobalLock(hglb); 
        if (pboxCopy != NULL) 
        { 
            cx = pboxCopy->rcText.right + CX_MARGIN; 
            cy = pboxCopy->rcText.top * 2 + cyText; 
 
            hwnd = CreateWindowEx( 
                WS_EX_NOPARENTNOTIFY | WS_EX_TRANSPARENT, 
                atchClassChild, NULL, WS_CHILD, 0, 0, cx, cy, 
                hwndMain, NULL, hinst, NULL 
            ); 
            if (hwnd != NULL) 
            { 
                pbox = (PLABELBOX) GetWindowLong(hwnd, 0); 
                memcpy(pbox, pboxCopy, sizeof(LABELBOX)); 
                ShowWindow(hwnd, SW_SHOWNORMAL); 
                SetFocus(hwnd); 
            } 
            GlobalUnlock(hglb); 
        } 
    } 
    CloseClipboard(); 
}
```



### <a name="registering-a-clipboard-format"></a><span data-ttu-id="25402-179">Registrazione di un formato degli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-179">Registering a Clipboard Format</span></span>

<span data-ttu-id="25402-180">Per registrare un formato degli Appunti, aggiungere una chiamata alla funzione [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) alla funzione di inizializzazione dell'istanza dell'applicazione, come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="25402-180">To register a clipboard format, add a call to the [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) function to your application's instance initialization function, as follows.</span></span>


```
// Register a clipboard format. 
 
// We assume that atchTemp can contain the format name and
// a null-terminator, otherwise it is truncated.
//
LoadString(hinstCurrent, IDS_FORMATNAME, atchTemp, 
    sizeof(atchTemp)/sizeof(TCHAR)); 
uLabelFormat = RegisterClipboardFormat(atchTemp); 
if (uLabelFormat == 0) 
    return FALSE;
```



### <a name="processing-the-wm_renderformat-and-wm_renderallformats-messages"></a><span data-ttu-id="25402-181">Elaborazione dei \_ messaggi WM RENDERFORMAT e WM \_ RENDERALLFORMATS</span><span class="sxs-lookup"><span data-stu-id="25402-181">Processing the WM\_RENDERFORMAT and WM\_RENDERALLFORMATS Messages</span></span>

<span data-ttu-id="25402-182">Se una finestra passa un handle **null** alla funzione [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) , deve elaborare i messaggi [**WM \_ RENDERFORMAT**](wm-renderformat.md) e [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) per eseguire il rendering dei dati su richiesta.</span><span class="sxs-lookup"><span data-stu-id="25402-182">If a window passes a **NULL** handle to the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function, it must process the [**WM\_RENDERFORMAT**](wm-renderformat.md) and [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) messages to render data upon request.</span></span>

<span data-ttu-id="25402-183">Se una finestra ritarda il rendering di un formato specifico e quindi un'altra applicazione richiede dati in tale formato, alla finestra viene inviato un messaggio [**WM \_ RENDERFORMAT**](wm-renderformat.md) .</span><span class="sxs-lookup"><span data-stu-id="25402-183">If a window delays rendering a specific format and then another application requests data in that format, then a [**WM\_RENDERFORMAT**](wm-renderformat.md) message is sent to the window.</span></span> <span data-ttu-id="25402-184">Inoltre, se una finestra ritarda il rendering di uno o più formati e se alcuni di questi formati rimangono senza rendering quando la finestra sta per essere distrutta, viene inviato un messaggio [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) alla finestra prima della sua distruzione.</span><span class="sxs-lookup"><span data-stu-id="25402-184">In addition, if a window delays rendering one or more formats, and if some of those formats remain unrendered when the window is about to be destroyed, then a [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) message is sent to the window before its destruction.</span></span>

<span data-ttu-id="25402-185">Per eseguire il rendering di un formato degli Appunti, la routine della finestra deve inserire un handle di dati non **null** negli Appunti utilizzando la funzione [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="25402-185">To render a clipboard format, the window procedure should place a non-**NULL** data handle on the clipboard using the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function.</span></span> <span data-ttu-id="25402-186">Se la procedura della finestra esegue il rendering di un formato in risposta al messaggio [**WM \_ RENDERFORMAT**](wm-renderformat.md) , non deve aprire gli Appunti prima di chiamare **SetClipboardData**.</span><span class="sxs-lookup"><span data-stu-id="25402-186">If the window procedure is rendering a format in response to the [**WM\_RENDERFORMAT**](wm-renderformat.md) message, it must not open the clipboard before calling **SetClipboardData**.</span></span> <span data-ttu-id="25402-187">Tuttavia, se si esegue il rendering di uno o più formati in risposta al messaggio [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) , è necessario aprire gli appunti e verificare che la finestra sia ancora proprietaria degli Appunti prima di chiamare **SetClipboardData** e chiudere gli Appunti prima di restituire.</span><span class="sxs-lookup"><span data-stu-id="25402-187">But if it is rendering one or more formats in response to the [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) message, it must open the clipboard and check that the window still owns the clipboard before calling **SetClipboardData**, and it must close the clipboard before returning.</span></span>

<span data-ttu-id="25402-188">L'applicazione label elabora i messaggi [**WM \_ RENDERFORMAT**](wm-renderformat.md) e [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="25402-188">The Label application processes the [**WM\_RENDERFORMAT**](wm-renderformat.md) and [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) messages as follows.</span></span>


```
case WM_RENDERFORMAT: 
    RenderFormat((UINT) wParam); 
    break; 
 
case WM_RENDERALLFORMATS:
    if (OpenClipboard(hwnd))
    {
        if (GetClipboardOwner() == hwnd)
        {
            RenderFormat(uLabelFormat);
            RenderFormat(CF_TEXT);
        }
        CloseClipboard();
    }
    break;
```



<span data-ttu-id="25402-189">In entrambi i casi, la routine della finestra chiama la funzione RenderFormat definita dall'applicazione, definita come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="25402-189">In both cases, the window procedure calls the application-defined RenderFormat function, defined as follows.</span></span>

<span data-ttu-id="25402-190">La struttura, denominata LABELBOX, viene definita come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="25402-190">The structure, called LABELBOX, is defined as follows.</span></span>


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```




```
void WINAPI RenderFormat(UINT uFormat) 
{ 
    HGLOBAL hglb; 
    PLABELBOX pbox; 
    LPTSTR  lptstr; 
    int cch; 
 
    if (pboxLocalClip == NULL) 
        return; 
 
    if (uFormat == CF_TEXT) 
    { 
        // Allocate a buffer for the text. 
 
        cch = pboxLocalClip->cchLabel; 
        hglb = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglb == NULL) 
            return; 
 
        // Copy the text from pboxLocalClip. 
 
        lptstr = GlobalLock(hglb); 
        memcpy(lptstr, pboxLocalClip->atchLabel, 
            cch * sizeof(TCHAR)); 
        lptstr[cch] = (TCHAR) 0; 
        GlobalUnlock(hglb); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglb); 
    } 
    else if (uFormat == uLabelFormat) 
    { 
        hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(LABELBOX)); 
        if (hglb == NULL) 
            return; 
        pbox = GlobalLock(hglb); 
        memcpy(pbox, pboxLocalClip, sizeof(LABELBOX)); 
        GlobalUnlock(hglb); 
 
        SetClipboardData(uLabelFormat, hglb); 
    } 
}
```



### <a name="processing-the-wm_destroyclipboard-message"></a><span data-ttu-id="25402-191">Elaborazione del \_ messaggio WM DESTROYCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="25402-191">Processing the WM\_DESTROYCLIPBOARD Message</span></span>

<span data-ttu-id="25402-192">Una finestra può elaborare il messaggio [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) per liberare le risorse riservate per supportare il rendering ritardato.</span><span class="sxs-lookup"><span data-stu-id="25402-192">A window can process the [**WM\_DESTROYCLIPBOARD**](wm-destroyclipboard.md) message in order to free any resources that it set aside to support delayed rendering.</span></span> <span data-ttu-id="25402-193">Ad esempio, l'applicazione Label, quando si copia un'etichetta negli Appunti, alloca un oggetto memoria locale.</span><span class="sxs-lookup"><span data-stu-id="25402-193">For example the Label application, when copying a label to the clipboard, allocates a local memory object.</span></span> <span data-ttu-id="25402-194">Questo oggetto viene quindi liberato in risposta al messaggio **WM \_ DESTROYCLIPBOARD** , come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="25402-194">It then frees this object in response to the **WM\_DESTROYCLIPBOARD** message, as follows.</span></span>


```
case WM_DESTROYCLIPBOARD: 
    if (pboxLocalClip != NULL) 
    { 
        LocalFree(pboxLocalClip); 
        pboxLocalClip = NULL; 
    } 
    break;
```



### <a name="using-the-owner-display-clipboard-format"></a><span data-ttu-id="25402-195">Uso del formato degli Appunti Owner-Display</span><span class="sxs-lookup"><span data-stu-id="25402-195">Using the Owner-Display Clipboard Format</span></span>

<span data-ttu-id="25402-196">Se una finestra inserisce informazioni sugli appunti usando il formato degli **Appunti \_ OWNERDISPLAY di CF** , è necessario eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="25402-196">If a window places information on the clipboard by using the **CF\_OWNERDISPLAY** clipboard format, it must do the following:</span></span>

-   <span data-ttu-id="25402-197">Elaborare il messaggio [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="25402-197">Process the [**WM\_PAINTCLIPBOARD**](wm-paintclipboard.md) message.</span></span> <span data-ttu-id="25402-198">Questo messaggio viene inviato al proprietario degli Appunti quando una parte della finestra Visualizzatore Appunti deve essere ridisegnata.</span><span class="sxs-lookup"><span data-stu-id="25402-198">This message is sent to the clipboard owner when a portion of the clipboard viewer window must be repainted.</span></span>

-   <span data-ttu-id="25402-199">Elaborare il messaggio [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="25402-199">Process the [**WM\_SIZECLIPBOARD**](wm-sizeclipboard.md) message.</span></span> <span data-ttu-id="25402-200">Questo messaggio viene inviato al proprietario degli Appunti quando la finestra Visualizzatore Appunti è stata ridimensionata o il relativo contenuto è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="25402-200">This message is sent to the clipboard owner when the clipboard viewer window has been resized or its content has changed.</span></span>

    <span data-ttu-id="25402-201">In genere, una finestra risponde a questo messaggio impostando le posizioni e gli intervalli di scorrimento per la finestra Visualizzatore Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-201">Typically, a window responds to this message by setting the scroll positions and ranges for the clipboard viewer window.</span></span> <span data-ttu-id="25402-202">In risposta a questo messaggio, l'applicazione label aggiorna anche una struttura di [**dimensioni**](/previous-versions//dd145106(v=vs.85)) per la finestra Visualizzatore Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-202">In response to this message, the Label application also updates a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure for the clipboard viewer window.</span></span>

-   <span data-ttu-id="25402-203">Elaborare i messaggi [**WM \_ HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) e [**WM \_ VSCROLLCLIPBOARD**](wm-vscrollclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="25402-203">Process the [**WM\_HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) and [**WM\_VSCROLLCLIPBOARD**](wm-vscrollclipboard.md) messages.</span></span> <span data-ttu-id="25402-204">Questi messaggi vengono inviati al proprietario degli Appunti quando si verifica un evento della barra di scorrimento nella finestra Visualizzatore Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-204">These messages are sent to the clipboard owner when a scroll bar event occurs in the clipboard viewer window.</span></span>

-   <span data-ttu-id="25402-205">Elaborare il messaggio [**WM \_ ASKCBFORMATNAME**](wm-askcbformatname.md) .</span><span class="sxs-lookup"><span data-stu-id="25402-205">Process the [**WM\_ASKCBFORMATNAME**](wm-askcbformatname.md) message.</span></span> <span data-ttu-id="25402-206">La finestra Visualizzatore Appunti Invia questo messaggio a un'applicazione per recuperare il nome del formato di visualizzazione del proprietario.</span><span class="sxs-lookup"><span data-stu-id="25402-206">The clipboard viewer window sends this message to an application to retrieve the name of the owner-display format.</span></span>

<span data-ttu-id="25402-207">La routine della finestra per l'applicazione label elabora questi messaggi, come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="25402-207">The window procedure for the Label application processes these messages, as follows.</span></span>


```
LRESULT CALLBACK MainWindowProc(hwnd, msg, wParam, lParam) 
HWND hwnd; 
UINT msg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static RECT rcViewer; 
 
    RECT rc; 
    LPRECT lprc; 
    LPPAINTSTRUCT lpps; 
 
    switch (msg) 
    { 
        //
        // Handle other messages.
        //
        case WM_PAINTCLIPBOARD: 
            // Determine the dimensions of the label. 
 
            SetRect(&rc, 0, 0, 
                pboxLocalClip->rcText.right + CX_MARGIN, 
                pboxLocalClip->rcText.top * 2 + cyText 
            ); 
 
            // Center the image in the clipboard viewer window. 
 
            if (rc.right < rcViewer.right) 
            { 
                rc.left = (rcViewer.right - rc.right) / 2; 
                rc.right += rc.left; 
            } 
            if (rc.bottom < rcViewer.bottom) 
            { 
                rc.top = (rcViewer.bottom - rc.bottom) / 2; 
                rc.bottom += rc.top; 
            } 
 
            // Paint the image, using the specified PAINTSTRUCT 
            // structure, by calling the application-defined 
            // PaintLabel function. 
 
            lpps = (LPPAINTSTRUCT) GlobalLock((HGLOBAL) lParam); 
            PaintLabel(lpps, pboxLocalClip, &rc); 
            GlobalUnlock((HGLOBAL) lParam); 
            break; 
 
        case WM_SIZECLIPBOARD: 
            // Save the dimensions of the window in a static 
            // RECT structure. 
 
            lprc = (LPRECT) GlobalLock((HGLOBAL) lParam); 
            memcpy(&rcViewer, lprc, sizeof(RECT)); 
            GlobalUnlock((HGLOBAL) lParam); 
 
            // Set the scroll ranges to zero (thus eliminating 
            // the need to process the WM_HSCROLLCLIPBOARD and 
            // WM_VSCROLLCLIPBOARD messages). 
 
            SetScrollRange((HWND) wParam, SB_HORZ, 0, 0, TRUE); 
            SetScrollRange((HWND) wParam, SB_VERT, 0, 0, TRUE); 
 
            break; 
 
        case WM_ASKCBFORMATNAME: 
            LoadString(hinst, IDS_OWNERDISPLAY, 
                (LPSTR) lParam, wParam); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, msg, wParam, lParam); 
    } 
    return 0; 
}
```



## <a name="monitoring-clipboard-contents"></a><span data-ttu-id="25402-208">Monitoraggio del contenuto degli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-208">Monitoring Clipboard Contents</span></span>

<span data-ttu-id="25402-209">Sono disponibili tre modi per monitorare le modifiche negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-209">There are three ways of monitoring changes to the clipboard.</span></span> <span data-ttu-id="25402-210">Il metodo meno recente consiste nel creare una finestra del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-210">The oldest method is to create a clipboard viewer window.</span></span> <span data-ttu-id="25402-211">In Windows 2000 è stata aggiunta la possibilità di eseguire query sul numero di sequenza degli Appunti e Windows Vista ha aggiunto il supporto per i listener di formato degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-211">Windows 2000 added the ability to query the clipboard sequence number, and Windows Vista added support for clipboard format listeners.</span></span> <span data-ttu-id="25402-212">Le finestre del visualizzatore degli Appunti sono supportate per la compatibilità con le versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="25402-212">Clipboard viewer windows are supported for backward compatibility with earlier versions of Windows.</span></span> <span data-ttu-id="25402-213">I nuovi programmi devono usare i listener di formato degli Appunti o il numero di sequenza degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-213">New programs should use clipboard format listeners or the clipboard sequence number.</span></span>

## <a name="querying-the-clipboard-sequence-number"></a><span data-ttu-id="25402-214">Esecuzione di query sul numero di sequenza degli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-214">Querying the Clipboard Sequence Number</span></span>

<span data-ttu-id="25402-215">Ogni volta che il contenuto degli Appunti viene modificato, un valore a 32 bit noto come numero di sequenza degli Appunti viene incrementato.</span><span class="sxs-lookup"><span data-stu-id="25402-215">Each time the contents of the clipboard change, a 32-bit value known as the clipboard sequence number is incremented.</span></span> <span data-ttu-id="25402-216">Un programma può recuperare il numero di sequenza degli appunti corrente chiamando la funzione [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) .</span><span class="sxs-lookup"><span data-stu-id="25402-216">A program can retrieve the current clipboard sequence number by calling the [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) function.</span></span> <span data-ttu-id="25402-217">Confrontando il valore restituito da un valore restituito da una precedente chiamata a **GetClipboardSequenceNumber**, un programma può determinare se il contenuto degli Appunti è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="25402-217">By comparing the value returned against a value returned by a previous call to **GetClipboardSequenceNumber**, a program can determine whether the clipboard contents have changed.</span></span> <span data-ttu-id="25402-218">Questo metodo è più adatto ai programmi che memorizzano nella cache i risultati in base ai contenuti degli Appunti correnti ed è necessario sapere se i calcoli sono ancora validi prima di utilizzare i risultati della cache.</span><span class="sxs-lookup"><span data-stu-id="25402-218">This method is more suitable to programs which cache results based on the current clipboard contents and need to know whether the calculations are still valid before using the results from that cache.</span></span> <span data-ttu-id="25402-219">Si noti che questo non è un metodo di notifica e non deve essere usato in un ciclo di polling.</span><span class="sxs-lookup"><span data-stu-id="25402-219">Note that this is a not a notification method and should not be used in a polling loop.</span></span> <span data-ttu-id="25402-220">Per ricevere una notifica quando cambiano i contenuti degli Appunti, usare un listener del formato degli Appunti o un visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-220">To be notified when clipboard contents change, use a clipboard format listener or a clipboard viewer.</span></span>

## <a name="creating-a-clipboard-format-listener"></a><span data-ttu-id="25402-221">Creazione di un listener di formato degli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-221">Creating a Clipboard Format Listener</span></span>

<span data-ttu-id="25402-222">Un listener del formato degli Appunti è una finestra che è stata registrata per ricevere una notifica quando il contenuto degli Appunti è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="25402-222">A clipboard format listener is a window which has registered to be notified when the contents of the clipboard has changed.</span></span> <span data-ttu-id="25402-223">Questo metodo è consigliato per la creazione di una finestra del visualizzatore degli appunti perché è più semplice da implementare ed evita problemi se i programmi non riescono a gestire correttamente la catena del visualizzatore degli Appunti o se una finestra nella catena del visualizzatore degli Appunti smette di rispondere ai messaggi.</span><span class="sxs-lookup"><span data-stu-id="25402-223">This method is recommended over creating a clipboard viewer window because it is simpler to implement and avoids problems if programs fail to maintain the clipboard viewer chain properly or if a window in the clipboard viewer chain stops responding to messages.</span></span>

<span data-ttu-id="25402-224">Una finestra viene registrata come listener del formato degli Appunti chiamando la funzione [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) .</span><span class="sxs-lookup"><span data-stu-id="25402-224">A window registers as a clipboard format listener by calling the [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) function.</span></span> <span data-ttu-id="25402-225">Quando il contenuto degli Appunti viene modificato, la finestra viene inviata un messaggio [**WM \_ CLIPBOARDUPDATE**](wm-clipboardupdate.md) .</span><span class="sxs-lookup"><span data-stu-id="25402-225">When the contents of the clipboard change, the window is posted a [**WM\_CLIPBOARDUPDATE**](wm-clipboardupdate.md) message.</span></span> <span data-ttu-id="25402-226">La registrazione rimane valida fino a quando la finestra non viene annullata la registrazione chiamando la funzione [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) .</span><span class="sxs-lookup"><span data-stu-id="25402-226">The registration remains valid until the window unregister itself by calling the [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) function.</span></span>

## <a name="creating-a-clipboard-viewer-window"></a><span data-ttu-id="25402-227">Creazione di una finestra Visualizzatore Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-227">Creating a Clipboard Viewer Window</span></span>

<span data-ttu-id="25402-228">Una finestra del visualizzatore degli Appunti Visualizza il contenuto corrente degli Appunti e riceve i messaggi quando il contenuto degli Appunti viene modificato.</span><span class="sxs-lookup"><span data-stu-id="25402-228">A clipboard viewer window displays the current content of the clipboard, and receives messages when the clipboard content changes.</span></span> <span data-ttu-id="25402-229">Per creare una finestra del visualizzatore degli Appunti, l'applicazione deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="25402-229">To create a clipboard viewer window, your application must do the following:</span></span>

-   <span data-ttu-id="25402-230">Aggiungere la finestra alla catena del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-230">Add the window to the clipboard viewer chain.</span></span>
-   <span data-ttu-id="25402-231">Elaborare il messaggio [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .</span><span class="sxs-lookup"><span data-stu-id="25402-231">Process the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>
-   <span data-ttu-id="25402-232">Elaborare il messaggio [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="25402-232">Process the [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message.</span></span>
-   <span data-ttu-id="25402-233">Rimuovere la finestra dalla catena del visualizzatore degli Appunti prima che venga eliminata definitivamente.</span><span class="sxs-lookup"><span data-stu-id="25402-233">Remove the window from the clipboard viewer chain before it is destroyed.</span></span>

## <a name="adding-a-window-to-the-clipboard-viewer-chain"></a><span data-ttu-id="25402-234">Aggiunta di una finestra alla catena del visualizzatore degli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-234">Adding a Window to the Clipboard Viewer Chain</span></span>

<span data-ttu-id="25402-235">Una finestra si aggiunge alla catena del visualizzatore degli Appunti chiamando la funzione [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="25402-235">A window adds itself to the clipboard viewer chain by calling the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span> <span data-ttu-id="25402-236">Il valore restituito è l'handle per la finestra successiva nella catena.</span><span class="sxs-lookup"><span data-stu-id="25402-236">The return value is the handle to the next window in the chain.</span></span> <span data-ttu-id="25402-237">Una finestra deve tenere traccia di questo valore, ad esempio salvando il valore in una variabile statica denominata *hwndNextViewer*.</span><span class="sxs-lookup"><span data-stu-id="25402-237">A window must keep track of this value — for example, by saving it in a static variable named *hwndNextViewer*.</span></span>

<span data-ttu-id="25402-238">Nell'esempio seguente viene aggiunta una finestra alla catena del visualizzatore degli Appunti in risposta al messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="25402-238">The following example adds a window to the clipboard viewer chain in response to the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span>


```
case WM_CREATE: 
 
    // Add the window to the clipboard viewer chain. 
 
    hwndNextViewer = SetClipboardViewer(hwnd); 
    break;
```



<span data-ttu-id="25402-239">I frammenti di codice vengono visualizzati per le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="25402-239">Code snippets are shown for the following tasks:</span></span>

-   [<span data-ttu-id="25402-240">Elaborazione del \_ messaggio WM CHANGECBCHAIN</span><span class="sxs-lookup"><span data-stu-id="25402-240">Processing the WM\_CHANGECBCHAIN Message</span></span>](/windows)
-   [<span data-ttu-id="25402-241">Rimozione di una finestra dalla catena del visualizzatore degli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-241">Removing a Window from the Clipboard Viewer Chain</span></span>](#removing-a-window-from-the-clipboard-viewer-chain)
-   [<span data-ttu-id="25402-242">Elaborazione del \_ messaggio WM DRAWCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="25402-242">Processing the WM\_DRAWCLIPBOARD Message</span></span>](/windows)
-   [<span data-ttu-id="25402-243">Esempio di Visualizzatore Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-243">Example of a Clipboard Viewer</span></span>](#example-of-a-clipboard-viewer)

### <a name="processing-the-wm_changecbchain-message"></a><span data-ttu-id="25402-244">Elaborazione del \_ messaggio WM CHANGECBCHAIN</span><span class="sxs-lookup"><span data-stu-id="25402-244">Processing the WM\_CHANGECBCHAIN Message</span></span>

<span data-ttu-id="25402-245">Una finestra del visualizzatore degli Appunti riceve il messaggio [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) quando un'altra finestra viene rimossa dalla catena del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-245">A clipboard viewer window receives the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message when another window is removing itself from the clipboard viewer chain.</span></span> <span data-ttu-id="25402-246">Se la finestra da rimuovere è la finestra successiva nella catena, la finestra che riceve il messaggio deve scollegare la finestra successiva dalla catena.</span><span class="sxs-lookup"><span data-stu-id="25402-246">If the window being removed is the next window in the chain, the window receiving the message must unlink the next window from the chain.</span></span> <span data-ttu-id="25402-247">In caso contrario, il messaggio deve essere passato alla finestra successiva nella catena.</span><span class="sxs-lookup"><span data-stu-id="25402-247">Otherwise, this message should be passed to the next window in the chain.</span></span>

<span data-ttu-id="25402-248">Nell'esempio seguente viene illustrata l'elaborazione del messaggio [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .</span><span class="sxs-lookup"><span data-stu-id="25402-248">The following example shows the processing of the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>


```
case WM_CHANGECBCHAIN: 
 
    // If the next window is closing, repair the chain. 
 
    if ((HWND) wParam == hwndNextViewer) 
        hwndNextViewer = (HWND) lParam; 
 
    // Otherwise, pass the message to the next link. 
 
    else if (hwndNextViewer != NULL) 
        SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
    break;
```



### <a name="removing-a-window-from-the-clipboard-viewer-chain"></a><span data-ttu-id="25402-249">Rimozione di una finestra dalla catena del visualizzatore degli Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-249">Removing a Window from the Clipboard Viewer Chain</span></span>

<span data-ttu-id="25402-250">Per rimuovere se stesso dalla catena del visualizzatore degli Appunti, una finestra chiama la funzione [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) .</span><span class="sxs-lookup"><span data-stu-id="25402-250">To remove itself from the clipboard viewer chain, a window calls the [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) function.</span></span> <span data-ttu-id="25402-251">Nell'esempio seguente viene rimossa una finestra dalla catena del visualizzatore degli Appunti in risposta al messaggio [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="25402-251">The following example removes a window from the clipboard viewer chain in response to the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span>


```
case WM_DESTROY: 
    ChangeClipboardChain(hwnd, hwndNextViewer); 
    PostQuitMessage(0); 
    break;
```



### <a name="processing-the-wm_drawclipboard-message"></a><span data-ttu-id="25402-252">Elaborazione del \_ messaggio WM DRAWCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="25402-252">Processing the WM\_DRAWCLIPBOARD Message</span></span>

<span data-ttu-id="25402-253">Il messaggio [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) notifica a una finestra del visualizzatore degli appunti che il contenuto degli Appunti è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="25402-253">The [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message notifies a clipboard viewer window that the content of the clipboard has changed.</span></span> <span data-ttu-id="25402-254">Quando si elabora il messaggio **WM \_ DRAWCLIPBOARD** , una finestra deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="25402-254">A window should do the following when processing the **WM\_DRAWCLIPBOARD** message:</span></span>

1.  <span data-ttu-id="25402-255">Determinare il formato degli appunti disponibili da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="25402-255">Determine which of the available clipboard formats to display.</span></span>
2.  <span data-ttu-id="25402-256">Recuperare i dati degli Appunti e visualizzarli nella finestra.</span><span class="sxs-lookup"><span data-stu-id="25402-256">Retrieve the clipboard data and display it in the window.</span></span> <span data-ttu-id="25402-257">In alternativa, se il formato degli Appunti è **CF \_ OWNERDISPLAY**, inviare un messaggio [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) al proprietario degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-257">Or if the clipboard format is **CF\_OWNERDISPLAY**, send a [**WM\_PAINTCLIPBOARD**](wm-paintclipboard.md) message to the clipboard owner.</span></span>
3.  <span data-ttu-id="25402-258">Inviare il messaggio alla finestra successiva nella catena del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-258">Send the message to the next window in the clipboard viewer chain.</span></span>

<span data-ttu-id="25402-259">Per un esempio di elaborazione del messaggio [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) , vedere l'elenco di esempio [di un visualizzatore degli Appunti](#example-of-a-clipboard-viewer).</span><span class="sxs-lookup"><span data-stu-id="25402-259">For an example of processing the [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message, see the example listing in [Example of a Clipboard Viewer](#example-of-a-clipboard-viewer).</span></span>

### <a name="example-of-a-clipboard-viewer"></a><span data-ttu-id="25402-260">Esempio di Visualizzatore Appunti</span><span class="sxs-lookup"><span data-stu-id="25402-260">Example of a Clipboard Viewer</span></span>

<span data-ttu-id="25402-261">Nell'esempio seguente viene illustrata una semplice applicazione Visualizzatore Appunti.</span><span class="sxs-lookup"><span data-stu-id="25402-261">The following example shows a simple clipboard viewer application.</span></span>


```
HINSTANCE hinst; 
UINT uFormat = (UINT)(-1); 
BOOL fAuto = TRUE; 
 
LRESULT APIENTRY MainWndProc(hwnd, uMsg, wParam, lParam) 
HWND hwnd; 
UINT uMsg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static HWND hwndNextViewer; 
 
    HDC hdc; 
    HDC hdcMem; 
    PAINTSTRUCT ps; 
    LPPAINTSTRUCT lpps; 
    RECT rc; 
    LPRECT lprc; 
    HGLOBAL hglb; 
    LPSTR lpstr; 
    HBITMAP hbm; 
    HENHMETAFILE hemf; 
    HWND hwndOwner; 
 
    switch (uMsg) 
    { 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
 
            // Branch depending on the clipboard format. 
 
            switch (uFormat) 
            { 
                case CF_OWNERDISPLAY: 
                    hwndOwner = GetClipboardOwner(); 
                    hglb = GlobalAlloc(GMEM_MOVEABLE, 
                        sizeof(PAINTSTRUCT)); 
                    lpps = GlobalLock(hglb);
                    memcpy(lpps, &ps, sizeof(PAINTSTRUCT)); 
                    GlobalUnlock(hglb); 
 
                    SendMessage(hwndOwner, WM_PAINTCLIPBOARD, 
                        (WPARAM) hwnd, (LPARAM) hglb); 
 
                    GlobalFree(hglb); 
                    break; 
 
                case CF_BITMAP: 
                    hdcMem = CreateCompatibleDC(hdc); 
                    if (hdcMem != NULL) 
                    { 
                        if (OpenClipboard(hwnd)) 
                        { 
                            hbm = (HBITMAP) 
                                GetClipboardData(uFormat); 
                            SelectObject(hdcMem, hbm); 
                            GetClientRect(hwnd, &rc); 
 
                            BitBlt(hdc, 0, 0, rc.right, rc.bottom, 
                                hdcMem, 0, 0, SRCCOPY); 
                            CloseClipboard(); 
                        } 
                        DeleteDC(hdcMem); 
                    } 
                    break; 
 
                case CF_TEXT: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hglb = GetClipboardData(uFormat); 
                        lpstr = GlobalLock(hglb); 
 
                        GetClientRect(hwnd, &rc); 
                        DrawText(hdc, lpstr, -1, &rc, DT_LEFT); 
 
                        GlobalUnlock(hglb); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case CF_ENHMETAFILE: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hemf = GetClipboardData(uFormat); 
                        GetClientRect(hwnd, &rc); 
                        PlayEnhMetaFile(hdc, hemf, &rc); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case 0: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "The clipboard is empty.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
                    break; 
 
                default: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "Unable to display format.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
            } 
            EndPaint(hwnd, &ps); 
            break; 
 
        case WM_SIZE: 
            if (uFormat == CF_OWNERDISPLAY) 
            { 
                hwndOwner = GetClipboardOwner(); 
                hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(RECT)); 
                lprc = GlobalLock(hglb); 
                GetClientRect(hwnd, lprc); 
                GlobalUnlock(hglb); 
 
                SendMessage(hwndOwner, WM_SIZECLIPBOARD, 
                    (WPARAM) hwnd, (LPARAM) hglb); 
 
                GlobalFree(hglb); 
            } 
            break; 
 
        case WM_CREATE: 
 
            // Add the window to the clipboard viewer chain. 
 
            hwndNextViewer = SetClipboardViewer(hwnd); 
            break; 
 
        case WM_CHANGECBCHAIN: 
 
            // If the next window is closing, repair the chain. 
 
            if ((HWND) wParam == hwndNextViewer) 
                hwndNextViewer = (HWND) lParam; 
 
            // Otherwise, pass the message to the next link. 
 
            else if (hwndNextViewer != NULL) 
                SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
            break; 
 
        case WM_DESTROY: 
            ChangeClipboardChain(hwnd, hwndNextViewer); 
            PostQuitMessage(0); 
            break; 
 
        case WM_DRAWCLIPBOARD:  // clipboard contents changed. 
 
            // Update the window by using Auto clipboard format. 
 
            SetAutoView(hwnd); 
 
            // Pass the message to the next window in clipboard 
            // viewer chain. 
 
            SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
            break; 
 
        case WM_INITMENUPOPUP: 
            if (!HIWORD(lParam)) 
                InitMenu(hwnd, (HMENU) wParam); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_EXIT: 
                    DestroyWindow(hwnd); 
                    break; 
 
                case IDM_AUTO: 
                    SetAutoView(hwnd); 
                    break; 
 
                default: 
                    fAuto = FALSE; 
                    uFormat = LOWORD(wParam); 
                    InvalidateRect(hwnd, NULL, TRUE); 
            } 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return (LRESULT) NULL; 
} 
 
void WINAPI SetAutoView(HWND hwnd) 
{ 
    static UINT auPriorityList[] = { 
        CF_OWNERDISPLAY, 
        CF_TEXT, 
        CF_ENHMETAFILE, 
        CF_BITMAP 
    }; 
 
    uFormat = GetPriorityClipboardFormat(auPriorityList, 4); 
    fAuto = TRUE; 
 
    InvalidateRect(hwnd, NULL, TRUE); 
    UpdateWindow(hwnd); 
} 
 
void WINAPI InitMenu(HWND hwnd, HMENU hmenu) 
{ 
    UINT uFormat; 
    char szFormatName[80]; 
    LPCSTR lpFormatName; 
    UINT fuFlags; 
    UINT idMenuItem; 
 
    // If a menu is not the display menu, no initialization is necessary. 
 
    if (GetMenuItemID(hmenu, 0) != IDM_AUTO) 
        return; 
 
    // Delete all menu items except the first. 
 
    while (GetMenuItemCount(hmenu) > 1) 
        DeleteMenu(hmenu, 1, MF_BYPOSITION); 
 
    // Check or uncheck the Auto menu item. 
 
    fuFlags = fAuto ? MF_BYCOMMAND | MF_CHECKED : 
        MF_BYCOMMAND | MF_UNCHECKED; 
    CheckMenuItem(hmenu, IDM_AUTO, fuFlags); 
 
    // If there are no clipboard formats, return. 
 
    if (CountClipboardFormats() == 0) 
        return; 
 
    // Open the clipboard. 
 
    if (!OpenClipboard(hwnd)) 
        return; 
 
    // Add a separator and then a menu item for each format. 
 
    AppendMenu(hmenu, MF_SEPARATOR, 0, NULL); 
    uFormat = EnumClipboardFormats(0); 
 
    while (uFormat) 
    { 
        // Call an application-defined function to get the name 
        // of the clipboard format. 
 
        lpFormatName = GetPredefinedClipboardFormatName(uFormat); 
 
        // For registered formats, get the registered name. 
 
        if (lpFormatName == NULL) 
        {

        // Note that, if the format name is larger than the
        // buffer, it is truncated. 
            if (GetClipboardFormatName(uFormat, szFormatName, 
                    sizeof(szFormatName))) 
                lpFormatName = szFormatName; 
            else 
                lpFormatName = "(unknown)"; 
        } 
 
        // Add a menu item for the format. For displayable 
        // formats, use the format ID for the menu ID. 
 
        if (IsDisplayableFormat(uFormat)) 
        { 
            fuFlags = MF_STRING; 
            idMenuItem = uFormat; 
        } 
        else 
        { 
            fuFlags = MF_STRING | MF_GRAYED; 
            idMenuItem = 0; 
        } 
        AppendMenu(hmenu, fuFlags, idMenuItem, lpFormatName); 
 
        uFormat = EnumClipboardFormats(uFormat); 
    } 
    CloseClipboard(); 
 
} 
 
BOOL WINAPI IsDisplayableFormat(UINT uFormat) 
{ 
    switch (uFormat) 
    { 
        case CF_OWNERDISPLAY: 
        case CF_TEXT: 
        case CF_ENHMETAFILE: 
        case CF_BITMAP: 
            return TRUE; 
    } 
    return FALSE; 
} 
```



 

 