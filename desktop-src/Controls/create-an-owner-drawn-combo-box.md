---
title: Come creare una casella combinata Owner-Drawn
description: In questo argomento viene illustrato come utilizzare una casella combinata creata dal proprietario.
ms.assetid: D866DE82-9734-4E8A-A366-5870C25B7C7B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5355dd33fe0067165308e9e6e5885b76edbe7ceb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047395"
---
# <a name="how-to-create-an-owner-drawn-combo-box"></a><span data-ttu-id="7bf06-103">Come creare una casella combinata Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="7bf06-103">How to Create an Owner-Drawn Combo Box</span></span>

<span data-ttu-id="7bf06-104">In questo argomento viene illustrato come utilizzare una casella combinata creata dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="7bf06-104">This topic demonstrates how to use an owner-drawn combo box.</span></span> <span data-ttu-id="7bf06-105">L'esempio di codice C++ usa una casella di riepilogo a discesa creata dal proprietario per visualizzare i quattro gruppi di alimenti, ognuno rappresentato da una bitmap e un nome.</span><span class="sxs-lookup"><span data-stu-id="7bf06-105">The C++ code example uses an owner-drawn drop-down list box to display the four food groups, each represented by a bitmap and a name.</span></span> <span data-ttu-id="7bf06-106">Se si seleziona un gruppo di alimenti, i cibi del gruppo verranno visualizzati in un elenco.</span><span class="sxs-lookup"><span data-stu-id="7bf06-106">Selecting a food group causes the foods in that group to appear in a list.</span></span>

![cattura di schermata che mostra una finestra di dialogo con una casella di riepilogo e una casella di riepilogo a discesa espansa che mostra un'icona e un'etichetta per ogni elemento](images/cscbx-01.png)

<span data-ttu-id="7bf06-108">La finestra di dialogo contiene anche una casella di riepilogo (IDLIST) e due pulsanti: **OK** (IDOK) e **Cancel** (IDCANCEL).</span><span class="sxs-lookup"><span data-stu-id="7bf06-108">The dialog box also contains a list box (IDLIST) and two buttons: **OK** (IDOK) and **Cancel** (IDCANCEL).</span></span> <span data-ttu-id="7bf06-109">Le costanti IDOK e IDCANCEL sono definite dai file di intestazione dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="7bf06-109">The IDOK and IDCANCEL constants are defined by the SDK header files.</span></span> <span data-ttu-id="7bf06-110">La costante IDLIST è definita nel file di intestazione dell'applicazione, così come l'identificatore del controllo, IDCOMBO.</span><span class="sxs-lookup"><span data-stu-id="7bf06-110">The constant IDLIST is defined in the application's header file, as is the control identifier, IDCOMBO.</span></span> <span data-ttu-id="7bf06-111">Per ulteriori informazioni sulle finestre di dialogo, vedere finestre di [dialogo](/windows/desktop/dlgbox/dialog-boxes).</span><span class="sxs-lookup"><span data-stu-id="7bf06-111">For more information about dialog boxes, see [Dialog Boxes](/windows/desktop/dlgbox/dialog-boxes).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7bf06-112">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="7bf06-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7bf06-113">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="7bf06-113">Technologies</span></span>

-   [<span data-ttu-id="7bf06-114">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="7bf06-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7bf06-115">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="7bf06-115">Prerequisites</span></span>

-   <span data-ttu-id="7bf06-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="7bf06-116">C/C++</span></span>
-   <span data-ttu-id="7bf06-117">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="7bf06-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7bf06-118">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="7bf06-118">Instructions</span></span>

### <a name="step-1-create-the-owner-drawn-dialog-box"></a><span data-ttu-id="7bf06-119">Passaggio 1: creare la finestra di dialogo Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="7bf06-119">Step 1: Create the Owner-Drawn Dialog Box</span></span>

<span data-ttu-id="7bf06-120">Nell'esempio di codice viene utilizzata la funzione [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) per creare una finestra di dialogo modale.</span><span class="sxs-lookup"><span data-stu-id="7bf06-120">The code example uses the [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) function to create a modal dialog box.</span></span> <span data-ttu-id="7bf06-121">Il modello della finestra di dialogo, IDD \_ SQMEAL, definisce gli stili della finestra, i pulsanti e gli identificatori di controllo per la casella combinata.</span><span class="sxs-lookup"><span data-stu-id="7bf06-121">The dialog box template, IDD\_SQMEAL, defines the window styles, buttons, and control identifiers for the combo box.</span></span> <span data-ttu-id="7bf06-122">Nella casella combinata in questo esempio vengono usati gli stili [**CBS \_ DropDownList**](combo-box-styles.md), [**CBS \_ OwnerDrawFixed**](combo-box-styles.md), CBS [**\_ Sort**](combo-box-styles.md), [**CBS \_ HASSTRINGS**](combo-box-styles.md), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)e [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="7bf06-122">The combo box in this example uses the [**CBS\_DROPDOWNLIST**](combo-box-styles.md), [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md), [**CBS\_SORT**](combo-box-styles.md), [**CBS\_HASSTRINGS**](combo-box-styles.md), [**WS\_VSCROLL**](/windows/desktop/winmsg/window-styles), and [**WS\_TABSTOP**](/windows/desktop/winmsg/window-styles) styles.</span></span>


```C++
DialogBox(hInst, MAKEINTRESOURCE(IDD_SQMEAL), 
    hWnd, FoodDlgProc);
```



### <a name="step-2-process-the-wm_initdialog-and-wm_destroy-messages-in-a-dialog-box"></a><span data-ttu-id="7bf06-123">Passaggio 2: elaborare i \_ messaggi WM INITDIALOG e WM \_ Destroy in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="7bf06-123">Step 2: Process the WM\_INITDIALOG and WM\_DESTROY messages in a dialog box.</span></span>

<span data-ttu-id="7bf06-124">Quando si usa una casella combinata in una finestra di dialogo, in genere si risponde a un messaggio [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) inizializzando la casella combinata.</span><span class="sxs-lookup"><span data-stu-id="7bf06-124">When you use a combo box in a dialog box, you usually respond to a [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message by initializing the combo box.</span></span> <span data-ttu-id="7bf06-125">L'applicazione carica le bitmap utilizzate per la casella combinata creata dal proprietario, quindi chiama la funzione definita dall'applicazione `InitGroupList` per inizializzare la casella combinata.</span><span class="sxs-lookup"><span data-stu-id="7bf06-125">The application loads the bitmaps used for the owner-drawn combo box and then calls the application-defined `InitGroupList` function to initialize the combo box.</span></span> <span data-ttu-id="7bf06-126">Seleziona anche il primo elemento dell'elenco nella casella combinata e quindi chiama la funzione definita dall'applicazione `InitFoodList` per inizializzare la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="7bf06-126">It also selects the first list item in the combo box and then calls the application-defined `InitFoodList` function to initialize the list box.</span></span>

<span data-ttu-id="7bf06-127">Nell'esempio, la casella combinata creata dal proprietario è un elenco a discesa contenente i nomi di ognuno dei quattro gruppi di alimenti.</span><span class="sxs-lookup"><span data-stu-id="7bf06-127">In the example, the owner-drawn combo box is a drop-down list box that contains the names of each of the four food groups.</span></span> <span data-ttu-id="7bf06-128">`InitGroupList` aggiunge il nome di ogni gruppo di alimenti e usa il messaggio [**CB \_ SETITEMDATA**](cb-setitemdata.md) per associare un handle bitmap a ogni elemento dell'elenco che identifica un gruppo di alimenti.</span><span class="sxs-lookup"><span data-stu-id="7bf06-128">`InitGroupList` adds the name of each food group , and uses the [**CB\_SETITEMDATA**](cb-setitemdata.md) message to associate a bitmap handle with each list item that identifies a food group.</span></span>

<span data-ttu-id="7bf06-129">La casella di riepilogo nell'esempio contiene i nomi degli alimenti nel gruppo di alimenti selezionato.</span><span class="sxs-lookup"><span data-stu-id="7bf06-129">The list box in the example contains the names of foods in the selected food group.</span></span> <span data-ttu-id="7bf06-130">**InitFoodList** Reimposta il contenuto della casella di riepilogo, quindi aggiunge i nomi della selezione corrente del cibo nella casella di riepilogo a discesa gruppo di alimenti corrente.</span><span class="sxs-lookup"><span data-stu-id="7bf06-130">**InitFoodList** resets the contents of the list box, then adds the names of the current food selection in the current food group drop-down list box.</span></span>


```C++
case WM_INITDIALOG:

    // Call an application-defined function to load bitmap resources.
    if (!LoadIconBitmaps())
    {
        EndDialog(hDlg, -1);
        break;
    }

    // Initialize the food groups combo box and select the first item.
    InitGroupList(hDlg);
    SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

    // Initialize the food list box and select the first item.
    InitFoodList(hDlg);
    SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

     return (INT_PTR)TRUE;
```



<span data-ttu-id="7bf06-131">Quando riceve il messaggio [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) , l'applicazione elimina le bitmap nella casella combinata creata dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="7bf06-131">When it receives the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, the application deletes the bitmaps in the owner-drawn combo box.</span></span>


```C++
case WM_DESTROY:

    // Call the application-defined function to free the bitmap resources.
    DeleteIconBitmaps();
    break;
```



### <a name="step-3-process-the-wm_measureitem-message"></a><span data-ttu-id="7bf06-132">Passaggio 3: elaborare il \_ messaggio WM MeasureItem.</span><span class="sxs-lookup"><span data-stu-id="7bf06-132">Step 3: Process the WM\_MEASUREITEM message.</span></span>

<span data-ttu-id="7bf06-133">Una casella combinata creata dal proprietario Invia il messaggio [**WM \_ MeasureItem**](wm-measureitem.md) alla finestra padre o alla routine della finestra di dialogo in modo che l'applicazione possa impostare le dimensioni di ogni elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7bf06-133">An owner-drawn combo box sends the [**WM\_MEASUREITEM**](wm-measureitem.md) message to its parent window or dialog box procedure so that the application can set the dimensions of each list item.</span></span> <span data-ttu-id="7bf06-134">Poiché la casella combinata di esempio ha lo stile [**CBS \_ OwnerDrawFixed**](combo-box-styles.md) , il sistema invia il messaggio **WM \_ MeasureItem** una sola volta.</span><span class="sxs-lookup"><span data-stu-id="7bf06-134">Because the example combo box has the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) style, the system sends the **WM\_MEASUREITEM** message only once.</span></span> <span data-ttu-id="7bf06-135">Le caselle combinate con lo stile [**\_ OwnerDrawVariable CBS**](combo-box-styles.md) inviano un messaggio **WM \_ MeasureItem** per ogni elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7bf06-135">Combo boxes with the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style send a **WM\_MEASUREITEM** message for each list item.</span></span>

<span data-ttu-id="7bf06-136">Il parametro *lParam* è un puntatore a una struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) che identifica il controllo e l'elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7bf06-136">The *lParam* parameter is a pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that identifies the control and list item.</span></span> <span data-ttu-id="7bf06-137">Contiene anche le dimensioni predefinite dell'elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7bf06-137">It also contains the default dimensions of the list item.</span></span> <span data-ttu-id="7bf06-138">Nell'esempio viene modificato il membro della struttura **ItemHeight** per assicurarsi che le voci dell'elenco siano sufficientemente elevate da contenere le bitmap del gruppo di alimenti.</span><span class="sxs-lookup"><span data-stu-id="7bf06-138">The example modifies the **itemHeight** structure member to ensure that the list items are high enough to accommodate the food-group bitmaps.</span></span>


```C++
case WM_MEASUREITEM:
    {
    // Set the height of the items in the food groups combo box.
    LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

    if (lpmis->itemHeight < CY_BITMAP + 2)
        lpmis->itemHeight = CY_BITMAP + 2;

    break;
    }
```



### <a name="step-4-process-the-wm_drawitem-message"></a><span data-ttu-id="7bf06-139">Passaggio 4: elaborare il \_ messaggio WM DrawItem.</span><span class="sxs-lookup"><span data-stu-id="7bf06-139">Step 4: Process the WM\_DRAWITEM message.</span></span>

<span data-ttu-id="7bf06-140">Una casella combinata creata dal proprietario Invia il messaggio [**WM \_ DrawItem**](wm-drawitem.md) alla finestra padre o alla relativa routine della finestra di dialogo ogni volta che l'applicazione deve ridisegnare un elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7bf06-140">An owner-drawn combo box sends the [**WM\_DRAWITEM**](wm-drawitem.md) message to its parent window or dialog box procedure each time the application must repaint a list item.</span></span> <span data-ttu-id="7bf06-141">Il parametro *lParam* è un puntatore a una struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) che identifica il controllo e l'elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7bf06-141">The *lParam* parameter is a pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure that identifies the control and list item.</span></span> <span data-ttu-id="7bf06-142">Contiene inoltre le informazioni necessarie per disegnare l'elemento.</span><span class="sxs-lookup"><span data-stu-id="7bf06-142">It also contains information needed to paint the item.</span></span>

<span data-ttu-id="7bf06-143">Nell'applicazione di esempio vengono visualizzati il testo della voce di elenco e la bitmap associata al gruppo di alimenti.</span><span class="sxs-lookup"><span data-stu-id="7bf06-143">The example application displays the list-item text and the bitmap associated with the food group.</span></span> <span data-ttu-id="7bf06-144">Se l'elemento ha lo stato attivo, viene anche disegnato un rettangolo di attivazione.</span><span class="sxs-lookup"><span data-stu-id="7bf06-144">If the item has the focus, it also draws a focus rectangle.</span></span> <span data-ttu-id="7bf06-145">Prima di visualizzare il testo, nell'esempio vengono impostati i colori di primo piano e di sfondo in base all'elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="7bf06-145">Before displaying the text, the example sets the foreground and background colors, based on the item selected.</span></span> <span data-ttu-id="7bf06-146">Poiché la casella combinata ha lo stile [**CBS \_ HASSTRINGS**](combo-box-styles.md) , la casella combinata mantiene il testo per ogni elemento dell'elenco che può essere recuperato usando il messaggio [**CB \_ GETLBTEXT**](cb-getlbtext.md) .</span><span class="sxs-lookup"><span data-stu-id="7bf06-146">Because the combo box has the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the combo box maintains the text for each list item that can be retrieved using the [**CB\_GETLBTEXT**](cb-getlbtext.md) message.</span></span>

<span data-ttu-id="7bf06-147">Le bitmap utilizzate per l'elemento elenco dipendono dal gruppo di alimenti.</span><span class="sxs-lookup"><span data-stu-id="7bf06-147">The bitmaps used for the list item depend on the food group.</span></span> <span data-ttu-id="7bf06-148">`InitGroupList` Usa il messaggio [**CB \_ SETITEMDATA**](cb-setitemdata.md) per associare un handle bitmap a ogni elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7bf06-148">`InitGroupList` uses the [**CB\_SETITEMDATA**](cb-setitemdata.md) message to associate a bitmap handle with each list item.</span></span> <span data-ttu-id="7bf06-149">La routine della finestra Recupera l'handle bitmap dal membro **ItemData** della struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="7bf06-149">The window procedure retrieves the bitmap handle from the **itemData** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span> <span data-ttu-id="7bf06-150">Il sistema usa due bitmap per ogni simbolo del gruppo di alimenti: una bitmap monocromatica con l'operazione SRCAND raster per cancellare l'area irregolare dietro l'immagine e una bitmap di colore con l'operazione raster SRCPAINT per disegnare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="7bf06-150">The system uses two bitmaps for each food group symbol: a monochrome bitmap with the SRCAND raster operation to erase the irregular region behind the image, and a color bitmap with the SRCPAINT raster operation to paint the image.</span></span>


```C++
case WM_DRAWITEM:
    {
    COLORREF clrBackground;
    COLORREF clrForeground;
    TEXTMETRIC tm;
    int x;
    int y;
    HRESULT hr;
    size_t cch;

    LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
       
    if (lpdis->itemID == -1) // Empty item)
        break;

    // Get the food icon from the item data.
    hbmIcon = (HBITMAP) lpdis->itemData;

    // The colors depend on whether the item is selected.
    clrForeground = SetTextColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

    clrBackground = SetBkColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHT : COLOR_WINDOW));

    // Calculate the vertical and horizontal position.
    GetTextMetrics(lpdis->hDC, &tm);
    y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
    x = LOWORD(GetDialogBaseUnits()) / 4;

    // Get and display the text for the list item.
    SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
        lpdis->itemID, (LPARAM) achTemp);

    hr = StringCchLength(achTemp, 256, &cch);
    if (FAILED(hr))
    {
        // TODO: Write error handler.
    }

    ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
        ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
        achTemp, (UINT)cch, NULL);

    // Restore the previous colors.
    SetTextColor(lpdis->hDC, clrForeground);
    SetBkColor(lpdis->hDC, clrBackground);
    
    //  Draw the food icon for the item. 
    HDC hdc = CreateCompatibleDC(lpdis->hDC); 
    if (hdc == NULL) 
        break; 
 
    SelectObject(hdc, hbmMask); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
    SelectObject(hdc, hbmIcon); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
    DeleteDC(hdc); 
  
    // If the item has the focus, draw the focus rectangle.
    if (lpdis->itemState & ODS_FOCUS)
        DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

    break;
    }
```



### <a name="step-5-process-the-wm_command-message"></a><span data-ttu-id="7bf06-151">Passaggio 5: elaborare il \_ messaggio di comando WM.</span><span class="sxs-lookup"><span data-stu-id="7bf06-151">Step 5: Process the WM\_COMMAND message.</span></span>

<span data-ttu-id="7bf06-152">Quando si verifica un evento in un controllo finestra di dialogo, il controllo Invia una notifica alla routine della finestra di dialogo per mezzo di un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="7bf06-152">When an event occurs in a dialog box control, the control notifies the dialog box procedure by means of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="7bf06-153">Nell'esempio vengono elaborati i messaggi di notifica della casella combinata, della casella di riepilogo e del pulsante **OK** .</span><span class="sxs-lookup"><span data-stu-id="7bf06-153">The example processes notification messages from the combo box, the list box, and the **OK** button.</span></span> <span data-ttu-id="7bf06-154">L'identificatore di controllo si trova nella parola più bassa di *wParam* e il codice di notifica si trova nella parola più significativa di *wParam*.</span><span class="sxs-lookup"><span data-stu-id="7bf06-154">The control identifier is in the low-order word of *wParam*, and the notification code is in the high-order word of *wParam*.</span></span>

<span data-ttu-id="7bf06-155">Se l'identificatore di controllo è IDCOMBO, si è verificato un evento nella casella combinata.</span><span class="sxs-lookup"><span data-stu-id="7bf06-155">If the control identifier is IDCOMBO, an event has occurred in the combo box.</span></span> <span data-ttu-id="7bf06-156">In risposta, la routine della finestra di dialogo Ignora tutti gli altri eventi della casella combinata eccetto [**CBN \_ SELENDOK**](cbn-selendok.md), che indica che è stata effettuata una selezione, la casella di riepilogo a discesa è stata chiusa e le modifiche apportate devono essere accettate.</span><span class="sxs-lookup"><span data-stu-id="7bf06-156">In response, the dialog box procedure ignores all other combo box events except [**CBN\_SELENDOK**](cbn-selendok.md), which indicates that a selection was made, the drop down list box was closed, and the changes made should be accepted.</span></span> <span data-ttu-id="7bf06-157">La routine della finestra di dialogo chiama `InitFoodList` per reimpostare il contenuto della casella di riepilogo e per aggiungere i nomi delle selezioni correnti nella casella di riepilogo a discesa.</span><span class="sxs-lookup"><span data-stu-id="7bf06-157">The dialog box procedure calls `InitFoodList` to reset the contents of the list box and to add the names of the current selections in the drop-down list box.</span></span>

<span data-ttu-id="7bf06-158">Se l'identificatore di controllo è IDLIST, si è verificato un evento nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="7bf06-158">If the control identifier is IDLIST, an event has occurred in the list box.</span></span> <span data-ttu-id="7bf06-159">In questo modo, la routine della finestra di dialogo ignorerà tutti gli eventi della casella di riepilogo ad eccezione di [**LBN \_ DBLCLK**](lbn-dblclk.md), che indica che l'utente ha fatto doppio clic su un elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7bf06-159">This causes the dialog box procedure to ignore all list box events except [**LBN\_DBLCLK**](lbn-dblclk.md), which indicates that the user has double-clicked a list item.</span></span> <span data-ttu-id="7bf06-160">Questo evento viene elaborato nello stesso modo in cui è stato scelto un pulsante **OK** .</span><span class="sxs-lookup"><span data-stu-id="7bf06-160">This event is processed in the same way as if an **OK** button had been chosen.</span></span>

<span data-ttu-id="7bf06-161">Se l'identificatore di controllo è IDOK, l'utente ha scelto il pulsante **OK** .</span><span class="sxs-lookup"><span data-stu-id="7bf06-161">If the control identifier is IDOK, the user has chosen the **OK** button.</span></span> <span data-ttu-id="7bf06-162">In risposta, la routine della finestra di dialogo inserisce il nome del cibo selezionato nel controllo di modifica a più righe dell'applicazione, quindi chiama la funzione [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) per chiudere la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="7bf06-162">In response, the dialog box procedure inserts the name of the selected food into the application's multi-line edit control, then calls the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function to close the dialog box.</span></span>

<span data-ttu-id="7bf06-163">Se l'identificatore di controllo è IDCANCEL, l'utente ha fatto clic sul pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="7bf06-163">If the control identifier is IDCANCEL, the user has clicked the **Cancel** button.</span></span> <span data-ttu-id="7bf06-164">In risposta, la routine della finestra di dialogo chiama [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) per chiudere la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="7bf06-164">In response, the dialog box procedure calls [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) to close the dialog box.</span></span>


```C++
case WM_COMMAND:
        switch (LOWORD(wParam)) 
        { 
            case IDCOMBO: 
                if (HIWORD(wParam) == CBN_SELENDOK) 
                { 
                    InitFoodList(hDlg); 
                    SendDlgItemMessage(hDlg, IDLIST, 
                        LB_SETCURSEL, 0, 0); 
                } 
                break; 
 
            case IDLIST: 
                if (HIWORD(wParam) != LBN_DBLCLK) 
                    break; 
 
            // For a double-click, process the OK case. 
            case IDOK: 
 
                // Get the text for the selected list item. 
                hwnd = GetDlgItem(hDlg, IDLIST); 

                // Here it is assumed the text can fit into achTemp.
                // If there is doubt, call LB_GETTEXTLENGTH first.
                SendMessage(hwnd, LB_GETTEXT, 
                    SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                    (LPARAM) achTemp); 
 
                // TODO: Do something with the selected text.
 
                EndDialog(hDlg, 0); 
                break; 
 
            case IDCANCEL: 
                hwnd = GetDlgItem(hDlg, IDCOMBO); 
                if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                    SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                else EndDialog(hDlg, 0); 
        } 
        break; 
```



## <a name="complete-example"></a><span data-ttu-id="7bf06-165">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="7bf06-165">Complete example</span></span>

<span data-ttu-id="7bf06-166">Di seguito sono riportate la routine della finestra di dialogo e le funzioni di supporto per la finestra di dialogo **quadrato pasto** .</span><span class="sxs-lookup"><span data-stu-id="7bf06-166">Following is the dialog box procedure and the supporting functions for the **Square Meal** dialog box.</span></span>


```C++
#define ID_BREAD 0
#define ID_DAIRY 1
#define ID_FRUIT 2
#define ID_MEAT  3

#define CX_BITMAP 24
#define CY_BITMAP 24

HBITMAP hbmBread;
HBITMAP hbmDairy;
HBITMAP hbmMeat;
HBITMAP hbmFruit;
HBITMAP hbmMask;

HBITMAP hbmIcon;
```

```C++
// Message handler for Square Meal dialog box.
INT_PTR CALLBACK FoodDlgProc(HWND hDlg, UINT message, WPARAM wParam, 
    LPARAM lParam)
{
    UNREFERENCED_PARAMETER(lParam);
    TCHAR achTemp[256];
    HWND hwnd;

    switch (message)
    {
    case WM_INITDIALOG:

        // Call an application-defined function to load bitmap resources.
        if (!LoadIconBitmaps())
        {
            EndDialog(hDlg, -1);
            break;
        }

        // Initialize the food groups combo box and select the first item.
        InitGroupList(hDlg);
        SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

        // Initialize the food list box and select the first item.
        InitFoodList(hDlg);
        SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

         return (INT_PTR)TRUE;
   
    case WM_MEASUREITEM:
        {
        // Set the height of the items in the food groups combo box.
        LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

        if (lpmis->itemHeight < CY_BITMAP + 2)
            lpmis->itemHeight = CY_BITMAP + 2;

        break;
        }

    case WM_DRAWITEM:
        {
        COLORREF clrBackground;
        COLORREF clrForeground;
        TEXTMETRIC tm;
        int x;
        int y;
        HRESULT hr;
        size_t cch;

        LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
           
        if (lpdis->itemID == -1) // Empty item)
            break;

        // Get the food icon from the item data.
        hbmIcon = (HBITMAP) lpdis->itemData;

        // The colors depend on whether the item is selected.
        clrForeground = SetTextColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

        clrBackground = SetBkColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHT : COLOR_WINDOW));

        // Calculate the vertical and horizontal position.
        GetTextMetrics(lpdis->hDC, &tm);
        y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
        x = LOWORD(GetDialogBaseUnits()) / 4;

        // Get and display the text for the list item.
        SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
            lpdis->itemID, (LPARAM) achTemp);

        hr = StringCchLength(achTemp, 256, &cch);
        if (FAILED(hr))
        {
            // TODO: Write error handler.
        }

        ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
            ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
            achTemp, (UINT)cch, NULL);

        // Restore the previous colors.
        SetTextColor(lpdis->hDC, clrForeground);
        SetBkColor(lpdis->hDC, clrBackground);
        
        //  Draw the food icon for the item. 
        HDC hdc = CreateCompatibleDC(lpdis->hDC); 
        if (hdc == NULL) 
            break; 
 
        SelectObject(hdc, hbmMask); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
        SelectObject(hdc, hbmIcon); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
        DeleteDC(hdc); 
      
        // If the item has the focus, draw the focus rectangle.
        if (lpdis->itemState & ODS_FOCUS)
            DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

        break;
        }

    case WM_COMMAND:
            switch (LOWORD(wParam)) 
            { 
                case IDCOMBO: 
                    if (HIWORD(wParam) == CBN_SELENDOK) 
                    { 
                        InitFoodList(hDlg); 
                        SendDlgItemMessage(hDlg, IDLIST, 
                            LB_SETCURSEL, 0, 0); 
                    } 
                    break; 
 
                case IDLIST: 
                    if (HIWORD(wParam) != LBN_DBLCLK) 
                        break; 
 
                // For a double-click, process the OK case. 
                case IDOK: 
 
                    // Get the text for the selected list item. 
                    hwnd = GetDlgItem(hDlg, IDLIST); 

                    // Here it is assumed the text can fit into achTemp.
                    // If there is doubt, call LB_GETTEXTLENGTH first.
                    SendMessage(hwnd, LB_GETTEXT, 
                        SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                        (LPARAM) achTemp); 
 
                    // TODO: Do something with the selected text.
 
                    EndDialog(hDlg, 0); 
                    break; 
 
                case IDCANCEL: 
                    hwnd = GetDlgItem(hDlg, IDCOMBO); 
                    if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                        SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                    else EndDialog(hDlg, 0); 
            } 
            break; 

    case WM_DESTROY:

        // Call the application-defined function to free the bitmap resources.
        DeleteIconBitmaps();
        break;
    }
    return (INT_PTR)FALSE;
}

// Loads string resources and adds them as items to the drop-down list of
//   the food groups combo box. The bitmap handle of each item&#39;s icon is
//   stored as item data for easy access when the item needs to be drawn.
// 
void InitGroupList(HWND hDlg)
{
    TCHAR achTemp[256];
    DWORD dwIndex;

    // Get the handle of the food groups combo box.
    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);

    LoadString(hInst, IDS_BREAD, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmBread);
    
    LoadString(hInst, IDS_DAIRY, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmDairy);

    LoadString(hInst, IDS_FRUIT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmFruit); 

    LoadString(hInst, IDS_MEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmMeat);

    return;
}

// Fills the food list based on the selected item in the food groups
//   combo box.
void InitFoodList(HWND hDlg)
{
    TCHAR achTemp[256];

    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);
    HWND hwndFoodList = GetDlgItem(hDlg, IDLIST);

    // Clear the list contents.
    SendMessage(hwndFoodList, LB_RESETCONTENT, 0, 0);

    // Find out which food group is selected.
    int idFoodGroup = SendMessage(hwndGroupsBox, CB_GETCURSEL, 0, 0);

    switch (idFoodGroup)
    {
    case ID_BREAD:
        LoadString(hInst, IDS_OAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_WHEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_RYE, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        break;

    case ID_DAIRY:
        LoadString(hInst, IDS_CHEDDAR, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_MILK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PROCESSED, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_SWISS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        
        break;

    case ID_FRUIT:
        LoadString(hInst, IDS_APPLES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_BANANAS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_ORANGES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    case ID_MEAT:
        LoadString(hInst, IDS_BEEF, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_CHICKEN, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PORK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    default:
        break;
    }

    return;
}

// Loads the food icon bitmaps from the application resources.
//
BOOL LoadIconBitmaps(void)
{
    hbmBread = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_BREAD));

    if (hbmBread != NULL)
         hbmDairy = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_DAIRY));

    if (hbmDairy != NULL)
         hbmMeat = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MEAT));

    if (hbmMeat != NULL)
        hbmFruit = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_FRUIT));
    
    if (hbmFruit != NULL)
        hbmMask = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MASK));

    if (hbmMask != NULL)
        return TRUE;
        
    return FALSE;
}

// Frees the icon bitmps.
//
void DeleteIconBitmaps(void)
{
    FreeResource(reinterpret_cast<HGLOBAL>(hbmBread));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmDairy));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMeat));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmFruit));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMask));
}
```


## <a name="related-topics"></a><span data-ttu-id="7bf06-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7bf06-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bf06-168">Uso di caselle combinate</span><span class="sxs-lookup"><span data-stu-id="7bf06-168">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> </dl>

 

 