---
title: Come creare una finestra di dialogo a schede
description: L'esempio in questa sezione illustra come creare una finestra di dialogo che usa schede per fornire più pagine di controlli.
ms.assetid: DBF7FBDF-AADC-45CE-833E-F893C1129FC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa2ad8ba22c2972c6bdd502728af413d4800dabf0ab5c9196a4033a52267115
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920711"
---
# <a name="how-to-create-a-tabbed-dialog-box"></a>Come creare una finestra di dialogo a schede

L'esempio in questa sezione illustra come creare una finestra di dialogo che usa schede per fornire più pagine di controlli. La finestra di dialogo principale è una finestra di dialogo modale. Ogni pagina di controlli è definita da un modello di finestra di dialogo con lo [**stile \_ WS CHILD.**](/windows/desktop/winmsg/window-styles) Quando si seleziona una scheda, viene creata una finestra di dialogo non modabile per la pagina in ingresso e la finestra di dialogo per la pagina in uscita viene distrutta.

> [!Note]  
> In molti casi, è possibile implementare più facilmente finestre di dialogo a più pagine usando le finestre delle proprietà. Per altre informazioni sulle finestre delle proprietà, vedere [Informazioni sulle finestre delle proprietà](property-sheets.md).

 

Il modello per la finestra di dialogo principale definisce semplicemente due controlli pulsante. Quando si elabora [**il messaggio WM \_ INITDIALOG,**](/windows/desktop/dlgbox/wm-initdialog) la procedura della finestra di dialogo crea un controllo Struttura a schede e carica le risorse del modello di finestra di dialogo per ognuna delle finestre di dialogo figlio.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="create-a-tabbed-dialog-box"></a>Creare una finestra di dialogo a schede

Le informazioni vengono salvate in una struttura definita dall'applicazione denominata DLGHDR. Un puntatore a questa struttura è associato alla finestra di dialogo usando la [**funzione SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) La struttura è definita nel file di intestazione dell'applicazione, come indicato di seguito.


```C++
#define C_PAGES 3 

typedef struct tag_dlghdr { 
    HWND hwndTab;       // tab control 
    HWND hwndDisplay;   // current child dialog box 
    RECT rcDisplay;     // display rectangle for the tab control 
    DLGTEMPLATEEX *apRes[C_PAGES]; 
} DLGHDR; 
```



La funzione seguente elabora il [**messaggio WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) per la finestra di dialogo principale. La funzione alloca la struttura , carica le risorse del modello di finestra di dialogo per le finestre di dialogo figlio `DLGHDR` e crea il controllo Struttura a schede.

Le dimensioni di ogni finestra di dialogo figlio vengono specificate dalla [**struttura DLGTEMPLATEEX.**](/windows/desktop/dlgbox/dlgtemplateex) La funzione esamina le dimensioni di ogni finestra di dialogo e usa la macro per il messaggio [**TCM \_ ADJUSTRECT**](tcm-adjustrect.md) per calcolare le dimensioni appropriate per il controllo Struttura a schede. Ridimensiona quindi la finestra di dialogo e posiziona i due pulsanti di conseguenza. Questo esempio invia **TCM \_ ADJUSTRECT** usando la macro [**TabCtrl \_ AdjustRect.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect)


```C++
// Handles the WM_INITDIALOG message for a dialog box that contains 
//   a tab control used to select among three child dialog boxes.
// Returns a result code.
// hwndDlg - handle of the dialog box.
// 
HRESULT OnTabbedDialogInit(HWND hwndDlg) 
{ 
    INITCOMMONCONTROLSEX iccex;
    DWORD dwDlgBase = GetDialogBaseUnits();
    int cxMargin = LOWORD(dwDlgBase) / 4; 
    int cyMargin = HIWORD(dwDlgBase) / 8; 

    TCITEM tie; 
    RECT rcTab; 
    HWND hwndButton; 
    RECT rcButton; 
    int i; 

    // Initialize common controls.
    iccex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    iccex.dwICC = ICC_TAB_CLASSES;
    InitCommonControlsEx(&iccex); 

    // Allocate memory for the DLGHDR structure. Remember to 
    // free this memory before the dialog box is destroyed.
    DLGHDR *pHdr = (DLGHDR *) LocalAlloc(LPTR, sizeof(DLGHDR)); 

    // Save a pointer to the DLGHDR structure in the window
    // data of the dialog box. 
    SetWindowLongPtr(hwndDlg, GWLP_USERDATA, (LONG_PTR) pHdr); 
 
    // Create the tab control. Note that g_hInst is a global 
    // instance handle. 
    pHdr->hwndTab = CreateWindow( 
        WC_TABCONTROL, L"", 
        WS_CHILD | WS_CLIPSIBLINGS | WS_VISIBLE, 
        0, 0, 100, 100, 
        hwndDlg, NULL, g_hInst, NULL 
        ); 
    if (pHdr->hwndTab == NULL) 
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }
 
    // Add a tab for each of the three child dialog boxes. 
    tie.mask = TCIF_TEXT | TCIF_IMAGE; 
    tie.iImage = -1; 
    tie.pszText = L"First"; 
    TabCtrl_InsertItem(pHdr->hwndTab, 0, &tie); 
    tie.pszText = L"Second"; 
    TabCtrl_InsertItem(pHdr->hwndTab, 1, &tie); 
    tie.pszText = L"Third"; 
    TabCtrl_InsertItem(pHdr->hwndTab, 2, &tie); 

    // Lock the resources for the three child dialog boxes. 
    pHdr->apRes[0] = DoLockDlgRes(MAKEINTRESOURCE(IDD_FIRSTDLG)); 
    pHdr->apRes[1] = DoLockDlgRes(MAKEINTRESOURCE(IDD_SECONDDLG)); 
    pHdr->apRes[2] = DoLockDlgRes(MAKEINTRESOURCE(IDD_THIRDDLG)); 

    // Determine a bounding rectangle that is large enough to 
    // contain the largest child dialog box. 
    SetRectEmpty(&rcTab); 
    for (i = 0; i < C_PAGES; i++) 
    { 
        if (pHdr->apRes[i]->cx > rcTab.right) 
            rcTab.right = pHdr->apRes[i]->cx; 
        if (pHdr->apRes[i]->cy > rcTab.bottom) 
            rcTab.bottom = pHdr->apRes[i]->cy; 
    }

    // Map the rectangle from dialog box units to pixels.
    MapDialogRect(hwndDlg, &rcTab);
    
    // Calculate how large to make the tab control, so 
    // the display area can accommodate all the child dialog boxes. 
    TabCtrl_AdjustRect(pHdr->hwndTab, TRUE, &rcTab); 
    OffsetRect(&rcTab, cxMargin - rcTab.left, cyMargin - rcTab.top); 
 
    // Calculate the display rectangle. 
    CopyRect(&pHdr->rcDisplay, &rcTab); 
    TabCtrl_AdjustRect(pHdr->hwndTab, FALSE, &pHdr->rcDisplay); 
 
    // Set the size and position of the tab control, buttons, 
    // and dialog box. 
    SetWindowPos(pHdr->hwndTab, NULL, rcTab.left, rcTab.top, 
            rcTab.right - rcTab.left, rcTab.bottom - rcTab.top, 
            SWP_NOZORDER); 
 
    // Move the first button below the tab control. 
    hwndButton = GetDlgItem(hwndDlg, IDB_CLOSE); 
    SetWindowPos(hwndButton, NULL, 
            rcTab.left, rcTab.bottom + cyMargin, 0, 0, 
            SWP_NOSIZE | SWP_NOZORDER); 
 
    // Determine the size of the button. 
    GetWindowRect(hwndButton, &rcButton); 
    rcButton.right -= rcButton.left; 
    rcButton.bottom -= rcButton.top; 
 
    // Move the second button to the right of the first. 
    hwndButton = GetDlgItem(hwndDlg, IDB_TEST); 
    SetWindowPos(hwndButton, NULL, 
        rcTab.left + rcButton.right + cxMargin, 
        rcTab.bottom + cyMargin, 0, 0, 
        SWP_NOSIZE | SWP_NOZORDER); 
 
    // Size the dialog box. 
    SetWindowPos(hwndDlg, NULL, 0, 0, 
        rcTab.right + cyMargin + (2 * GetSystemMetrics(SM_CXDLGFRAME)), 
        rcTab.bottom + rcButton.bottom + (2 * cyMargin)
        + (2 * GetSystemMetrics(SM_CYDLGFRAME)) 
        + GetSystemMetrics(SM_CYCAPTION), 
        SWP_NOMOVE | SWP_NOZORDER); 
 
    // Simulate selection of the first item. 
    OnSelChanged(hwndDlg); 

    return S_OK;
} 

// Loads and locks a dialog box template resource. 
// Returns the address of the locked dialog box template resource. 
// lpszResName - name of the resource. 
//
DLGTEMPLATEEX* DoLockDlgRes(LPCTSTR lpszResName) 
{ 
    HRSRC hrsrc = FindResource(NULL, lpszResName, RT_DIALOG); 

    // Note that g_hInst is the global instance handle
    HGLOBAL hglb = LoadResource(g_hInst, hrsrc);  
    return (DLGTEMPLATEEX *) LockResource(hglb); 
} 
```



La funzione seguente elabora il [codice di notifica TCN \_ SELCHANGE](tcn-selchange.md) per la finestra di dialogo principale. La funzione elimina la finestra di dialogo per la pagina in uscita, se presente. Usa quindi la [**funzione CreateDialogIndirect**](/windows/desktop/api/winuser/nf-winuser-createdialogindirecta) per creare una finestra di dialogo non modala per la pagina in ingresso.


```C++
// Processes the TCN_SELCHANGE notification. 
// hwndDlg - handle to the parent dialog box. 
//
VOID OnSelChanged(HWND hwndDlg) 
{ 
    // Get the dialog header data.
    DLGHDR *pHdr = (DLGHDR *) GetWindowLongPtr( 
        hwndDlg, GWLP_USERDATA); 

    // Get the index of the selected tab.
    int iSel = TabCtrl_GetCurSel(pHdr->hwndTab); 
 
    // Destroy the current child dialog box, if any. 
    if (pHdr->hwndDisplay != NULL) 
        DestroyWindow(pHdr->hwndDisplay); 
 
    // Create the new child dialog box. Note that g_hInst is the
    // global instance handle.
    pHdr->hwndDisplay = CreateDialogIndirect(g_hInst, 
        (DLGTEMPLATE *)pHdr->apRes[iSel], hwndDlg, ChildDialogProc); 

    return;
} 
```



La funzione seguente elabora il [**messaggio WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) per ognuna delle finestre di dialogo figlio. Non è possibile specificare la posizione di una finestra di dialogo creata usando la [**funzione CreateDialogIndirect.**](/windows/desktop/api/winuser/nf-winuser-createdialogindirecta) Questa funzione usa la [**funzione SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per posizionare la finestra di dialogo figlio all'interno dell'area di visualizzazione del controllo Struttura a schede.


```C++
// Positions the child dialog box to occupy the display area of the 
//   tab control. 
// hwndDlg - handle of the dialog box.
//
VOID WINAPI OnChildDialogInit(HWND hwndDlg) 
{ 
    HWND hwndParent = GetParent(hwndDlg);
    DLGHDR *pHdr = (DLGHDR *) GetWindowLongPtr( 
        hwndParent, GWLP_USERDATA); 
    SetWindowPos(hwndDlg, NULL, pHdr->rcDisplay.left,
        pHdr->rcDisplay.top,//-2,
        (pHdr->rcDisplay.right - pHdr->rcDisplay.left),
        (pHdr->rcDisplay.bottom - pHdr->rcDisplay.top),
        SWP_SHOWWINDOW);
        
    return;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli Struttura a schede](using-tab-controls.md)
</dt> <dt>

[Windows di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 