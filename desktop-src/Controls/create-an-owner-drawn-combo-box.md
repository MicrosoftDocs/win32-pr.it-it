---
title: Come creare una Owner-Drawn casella combinata
description: In questo argomento viene illustrato come utilizzare una casella combinata disegnata dal proprietario.
ms.assetid: D866DE82-9734-4E8A-A366-5870C25B7C7B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90d82192e485e4f833157a1c3ab75e8e39446e1e80f7f9cc27baf5444b4e0bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826467"
---
# <a name="how-to-create-an-owner-drawn-combo-box"></a>Come creare una Owner-Drawn casella combinata

In questo argomento viene illustrato come utilizzare una casella combinata disegnata dal proprietario. L'esempio di codice C++ usa una casella di riepilogo a discesa disegnata dal proprietario per visualizzare i quattro gruppi di alimenti, ognuno rappresentato da una bitmap e da un nome. La selezione di un gruppo di alimenti fa sì che gli alimenti in tale gruppo vengano visualizzati in un elenco.

![Screenshot che mostra una finestra di dialogo con una casella di riepilogo e una casella di riepilogo a discesa espansa che mostra un'icona e un'etichetta per ogni elemento](images/cscbx-01.png)

La finestra di dialogo contiene anche una casella di riepilogo (IDLIST) e due pulsanti: **OK** (IDOK) **e Annulla** (IDCANCEL). Le costanti IDOK e IDCANCEL sono definite dai file di intestazione dell'SDK. La costante IDLIST è definita nel file di intestazione dell'applicazione, così come l'identificatore di controllo IDCOMBO. Per altre informazioni sulle finestre di dialogo, vedere [Finestre di dialogo.](/windows/desktop/dlgbox/dialog-boxes)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="step-1-create-the-owner-drawn-dialog-box"></a>Passaggio 1: Creare la finestra Owner-Drawn di dialogo

L'esempio di codice usa [**la funzione DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) per creare una finestra di dialogo modale. Il modello di finestra di dialogo IDD SQMEAL definisce gli stili, i pulsanti e gli identificatori di controllo della finestra per \_ la casella combinata. La casella combinata in questo esempio usa gli stili [**CBS \_ DROPDOWNLIST**](combo-box-styles.md), [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md), [**CBS \_ SORT**](combo-box-styles.md), [**CBS \_ HASSTRINGS,**](combo-box-styles.md) [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)e [**WS \_ TABSTOP.**](/windows/desktop/winmsg/window-styles)


```C++
DialogBox(hInst, MAKEINTRESOURCE(IDD_SQMEAL), 
    hWnd, FoodDlgProc);
```



### <a name="step-2-process-the-wm_initdialog-and-wm_destroy-messages-in-a-dialog-box"></a>Passaggio 2: Elaborare i messaggi \_ WM INITDIALOG e WM \_ DESTROY in una finestra di dialogo.

Quando si usa una casella combinata in una finestra di dialogo, in genere si risponde a un messaggio [**\_ WM INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) inizializzando la casella combinata. L'applicazione carica le bitmap usate per la casella combinata disegnata dal proprietario e quindi chiama la funzione definita dall'applicazione `InitGroupList` per inizializzare la casella combinata. Seleziona anche il primo elemento dell'elenco nella casella combinata e quindi chiama la funzione definita `InitFoodList` dall'applicazione per inizializzare la casella di riepilogo.

Nell'esempio la casella combinata disegnata dal proprietario è una casella di riepilogo a discesa che contiene i nomi di ognuno dei quattro gruppi di alimenti. `InitGroupList` aggiunge il nome di ogni gruppo di alimenti e usa il messaggio [**\_ CB SETITEMDATA**](cb-setitemdata.md) per associare un handle bitmap a ogni elemento dell'elenco che identifica un gruppo di alimenti.

La casella di riepilogo nell'esempio contiene i nomi degli alimenti nel gruppo di alimenti selezionato. **InitFoodList** reimposta il contenuto della casella di riepilogo, quindi aggiunge i nomi della selezione di cibo corrente nella casella di riepilogo a discesa del gruppo di alimenti corrente.


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



Quando riceve il messaggio [**WM \_ DESTROY,**](/windows/desktop/winmsg/wm-destroy) l'applicazione elimina le bitmap nella casella combinata disegnata dal proprietario.


```C++
case WM_DESTROY:

    // Call the application-defined function to free the bitmap resources.
    DeleteIconBitmaps();
    break;
```



### <a name="step-3-process-the-wm_measureitem-message"></a>Passaggio 3: Elaborare il messaggio \_ MEASUREITEM di WM.

Una casella combinata disegnata dal proprietario invia il messaggio [**\_ MEASUREITEM WM**](wm-measureitem.md) alla finestra padre o alla routine della finestra di dialogo in modo che l'applicazione possa impostare le dimensioni di ogni elemento dell'elenco. Poiché la casella combinata di esempio ha [**lo stile CBS \_ OWNERDRAWFIXED,**](combo-box-styles.md) il sistema invia il messaggio **WM \_ MEASUREITEM** una sola volta. Le caselle combinate [**con lo stile \_ CBS OWNERDRAWVARIABLE**](combo-box-styles.md) inviano un **messaggio \_ MEASUREITEM WM** per ogni elemento dell'elenco.

Il *parametro lParam* è un puntatore a una [**struttura MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) che identifica il controllo e l'elemento dell'elenco. Contiene anche le dimensioni predefinite dell'elemento dell'elenco. Nell'esempio viene modificato il membro della struttura **itemHeight** per assicurarsi che gli elementi dell'elenco siano sufficientemente elevati da contenere le bitmap del gruppo di alimenti.


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



### <a name="step-4-process-the-wm_drawitem-message"></a>Passaggio 4: Elaborare il messaggio WM \_ DRAWITEM.

Una casella combinata disegnata dal proprietario invia il messaggio [**WM \_ DRAWITEM**](wm-drawitem.md) alla finestra padre o alla routine della finestra di dialogo ogni volta che l'applicazione deve ridisegnare un elemento dell'elenco. Il *parametro lParam* è un puntatore a una [**struttura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) che identifica il controllo e l'elemento dell'elenco. Contiene anche le informazioni necessarie per disegnare l'elemento.

L'applicazione di esempio visualizza il testo dell'elemento elenco e la bitmap associata al gruppo di alimenti. Se l'elemento ha lo stato attivo, disegna anche un rettangolo di attivazione. Prima di visualizzare il testo, l'esempio imposta i colori di primo piano e di sfondo in base all'elemento selezionato. Poiché la casella combinata ha lo stile [**\_ CBS HASSTRINGS,**](combo-box-styles.md) la casella combinata mantiene il testo per ogni elemento dell'elenco che può essere recuperato utilizzando il [**messaggio \_ CB GETLBTEXT.**](cb-getlbtext.md)

Le bitmap usate per l'elemento dell'elenco dipendono dal gruppo di alimenti. `InitGroupList` usa il [**messaggio \_ CB SETITEMDATA**](cb-setitemdata.md) per associare un handle di bitmap a ogni elemento dell'elenco. La routine della finestra recupera l'handle della bitmap dal **membro itemData** della [**struttura DRAWITEMSTRUCT.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Il sistema usa due bitmap per ogni simbolo del gruppo di alimenti: una bitmap monocromatica con l'operazione raster SRCAND per cancellare l'area irregolare dietro l'immagine e una bitmap di colore con l'operazione raster SRCPAINT per disegnare l'immagine.


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



### <a name="step-5-process-the-wm_command-message"></a>Passaggio 5: Elaborare il messaggio WM \_ COMMAND.

Quando si verifica un evento in un controllo della finestra di dialogo, il controllo invia una notifica alla routine della finestra di dialogo tramite un [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) L'esempio elabora i messaggi di notifica dalla casella combinata, dalla casella di riepilogo e dal **pulsante OK.** L'identificatore di controllo è nella parola di ordine più basso di *wParam* e il codice di notifica è nella parola di ordine superiore *di wParam*.

Se l'identificatore del controllo è IDCOMBO, si è verificato un evento nella casella combinata. In risposta, la procedura della finestra di dialogo ignora tutti gli altri eventi della casella combinata ad eccezione di [**CBN \_ SELENDOK,**](cbn-selendok.md)che indica che è stata effettuata una selezione, che la casella di riepilogo a discesa è stata chiusa e che le modifiche apportate devono essere accettate. La routine della finestra di dialogo chiama per reimpostare il contenuto della casella di riepilogo e per aggiungere i nomi delle selezioni correnti nella casella `InitFoodList` di riepilogo a discesa.

Se l'identificatore del controllo è IDLIST, si è verificato un evento nella casella di riepilogo. In questo modo la routine della finestra di dialogo ignora tutti gli eventi della casella di riepilogo ad eccezione di [**LBN \_ DBLCLK,**](lbn-dblclk.md)che indica che l'utente ha fatto doppio clic su un elemento dell'elenco. Questo evento viene elaborato come se fosse stato scelto un pulsante **OK.**

Se l'identificatore del controllo è IDOK, l'utente ha scelto **il pulsante OK.** In risposta, la routine della finestra di dialogo inserisce il nome dell'alimento selezionato nel controllo di modifica su più righe dell'applicazione, quindi chiama la [**funzione EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) per chiudere la finestra di dialogo.

Se l'identificatore del controllo è IDCANCEL, l'utente ha fatto clic sul **pulsante** Annulla. In risposta, la routine della finestra di dialogo chiama [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) per chiudere la finestra di dialogo.


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



## <a name="complete-example"></a>Esempio completo

Di seguito è riportata la procedura della finestra di dialogo e le funzioni di supporto per la finestra di dialogo **Square Meal.**


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


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle caselle combinate](using-combo-boxes.md)
</dt> </dl>

 

 