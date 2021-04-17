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
# <a name="using-the-clipboard"></a>Uso degli Appunti

Questa sezione contiene esempi di codice per le attività seguenti:

-   [Implementazione dei comandi taglia, copia e incolla](#implementing-the-cut-copy-and-paste-commands)
    -   [Selezione dei dati](#selecting-data)
    -   [Creazione di un menu modifica](#creating-an-edit-menu)
    -   [Elaborazione del \_ messaggio WM INITMENUPOPUP](#processing-the-wm_initmenupopup-message)
    -   [Elaborazione del \_ messaggio di comando WM](#processing-the-wm_command-message)
    -   [Copia delle informazioni negli Appunti](#copying-information-to-the-clipboard)
    -   [Incollare le informazioni dagli Appunti](#pasting-information-from-the-clipboard)
    -   [Registrazione di un formato degli Appunti](#registering-a-clipboard-format)
    -   [Elaborazione dei \_ messaggi WM RENDERFORMAT e WM \_ RENDERALLFORMATS](#processing-the-wm_renderformat-and-wm_renderallformats-messages)
    -   [Elaborazione del \_ messaggio WM DESTROYCLIPBOARD](#processing-the-wm_destroyclipboard-message)
    -   [Uso del formato degli Appunti Owner-Display](#using-the-owner-display-clipboard-format)
-   [Monitoraggio del contenuto degli Appunti](#monitoring-clipboard-contents)
-   [Esecuzione di query sul numero di sequenza degli Appunti](#querying-the-clipboard-sequence-number)
-   [Creazione di un listener di formato degli Appunti](#creating-a-clipboard-format-listener)
-   [Creazione di una finestra Visualizzatore Appunti](#creating-a-clipboard-viewer-window)
-   [Aggiunta di una finestra alla catena del visualizzatore degli Appunti](#adding-a-window-to-the-clipboard-viewer-chain)
    -   [Elaborazione del \_ messaggio WM CHANGECBCHAIN](#processing-the-wm_changecbchain-message)
    -   [Rimozione di una finestra dalla catena del visualizzatore degli Appunti](#removing-a-window-from-the-clipboard-viewer-chain)
    -   [Elaborazione del \_ messaggio WM DRAWCLIPBOARD](#processing-the-wm_drawclipboard-message)
    -   [Esempio di Visualizzatore Appunti](#example-of-a-clipboard-viewer)

## <a name="implementing-the-cut-copy-and-paste-commands"></a>Implementazione dei comandi taglia, copia e incolla

Questa sezione descrive come vengono implementati i comandi **taglia**, **copia** e **Incolla** standard in un'applicazione. Nell'esempio riportato in questa sezione vengono usati questi metodi per inserire i dati negli appunti usando un formato degli Appunti registrato, il formato **CF \_ OWNERDISPLAY** e il formato di **\_ testo CF** . Il formato registrato viene utilizzato per rappresentare le finestre di testo rettangolari o ellittiche, denominate etichette.

### <a name="selecting-data"></a>Selezione dei dati

Prima che le informazioni possano essere copiate negli Appunti, l'utente deve selezionare informazioni specifiche da copiare o tagliare. Un'applicazione deve fornire un mezzo per consentire all'utente di selezionare le informazioni all'interno di un documento e un tipo di feedback visivo per indicare i dati selezionati.

### <a name="creating-an-edit-menu"></a>Creazione di un menu modifica

Un'applicazione deve caricare una tabella dei tasti di scelta rapida contenente gli acceleratori della tastiera standard per i comandi di menu **modifica** . Per rendere effettive le acceleratori, è necessario aggiungere la funzione [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) al ciclo di messaggi dell'applicazione. Per ulteriori informazioni sugli acceleratori tastiera, vedere [tasti](/windows/desktop/menurc/keyboard-accelerators)di scelta rapida.

### <a name="processing-the-wm_initmenupopup-message"></a>Elaborazione del \_ messaggio WM INITMENUPOPUP

Non tutti i comandi degli Appunti sono disponibili per l'utente in un determinato momento. Un'applicazione deve elaborare il messaggio [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) per abilitare le voci di menu per i comandi disponibili e disabilitare i comandi non disponibili.

Di seguito è riportato il caso [**\_ INITMENUPOPUP di WM**](/windows/desktop/menurc/wm-initmenupopup) per un'applicazione denominata Label.


```
case WM_INITMENUPOPUP:
    InitMenu((HMENU) wParam);
    break;
```



La funzione InitMenu è definita come indicato di seguito.


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



### <a name="processing-the-wm_command-message"></a>Elaborazione del \_ messaggio di comando WM

Per elaborare i comandi di menu, aggiungere il case del [**\_ comando WM**](/windows/desktop/menurc/wm-command) alla routine della finestra principale dell'applicazione. Di seguito è riportato il caso del **\_ comando WM** per la routine della finestra dell'applicazione Label.


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



Per eseguire i comandi **Copy** e **Cut** , la routine della finestra chiama la funzione EditCopy definita dall'applicazione. Per ulteriori informazioni, vedere [copia di informazioni negli Appunti](#copying-information-to-the-clipboard). Per eseguire il comando **Incolla** , la routine della finestra chiama la funzione EditPaste definita dall'applicazione. Per ulteriori informazioni sulla funzione EditPaste, vedere [incollare le informazioni dagli Appunti](#pasting-information-from-the-clipboard).

### <a name="copying-information-to-the-clipboard"></a>Copia delle informazioni negli Appunti

Nell'applicazione Label la funzione EditCopy definita dall'applicazione copia la selezione corrente negli Appunti. Questa funzione esegue le operazioni seguenti:

1.  Apre gli Appunti chiamando la funzione [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .
2.  Svuota gli Appunti chiamando la funzione [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) .
3.  Chiama la funzione [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) una volta per ogni formato degli Appunti fornito dall'applicazione.
4.  Chiude gli Appunti chiamando la funzione [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .

A seconda della selezione corrente, tramite la funzione EditCopy viene copiato un intervallo di testo o viene copiata una struttura definita dall'applicazione che rappresenta un'intera etichetta. La struttura, denominata LABELBOX, viene definita come indicato di seguito.


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



Di seguito è riportata la funzione EditCopy.


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



### <a name="pasting-information-from-the-clipboard"></a>Incollare le informazioni dagli Appunti

Nell'applicazione Label la funzione EditPaste definita dall'applicazione incolla il contenuto degli Appunti. Questa funzione esegue le operazioni seguenti:

1.  Apre gli Appunti chiamando la funzione [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .
2.  Determina quale dei formati degli appunti disponibili recuperare.
3.  Recupera l'handle per i dati nel formato selezionato chiamando la funzione [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) .
4.  Inserisce una copia dei dati nel documento.

    L'handle restituito da [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) è ancora di proprietà degli Appunti, quindi un'applicazione non deve liberarlo o lasciarlo bloccato.

5.  Chiude gli Appunti chiamando la funzione [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .

Se un'etichetta è selezionata e contiene un punto di inserimento, la funzione EditPaste inserisce il testo dagli Appunti nel punto di inserimento. Se non è presente alcuna selezione o se è selezionata un'etichetta, la funzione crea una nuova etichetta, usando la struttura LABELBOX definita dall'applicazione negli Appunti. La struttura LABELBOX viene posizionata negli Appunti utilizzando un formato degli Appunti registrato.

La struttura, denominata LABELBOX, viene definita come indicato di seguito.


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



Di seguito è riportata la funzione EditPaste.


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



### <a name="registering-a-clipboard-format"></a>Registrazione di un formato degli Appunti

Per registrare un formato degli Appunti, aggiungere una chiamata alla funzione [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) alla funzione di inizializzazione dell'istanza dell'applicazione, come indicato di seguito.


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



### <a name="processing-the-wm_renderformat-and-wm_renderallformats-messages"></a>Elaborazione dei \_ messaggi WM RENDERFORMAT e WM \_ RENDERALLFORMATS

Se una finestra passa un handle **null** alla funzione [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) , deve elaborare i messaggi [**WM \_ RENDERFORMAT**](wm-renderformat.md) e [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) per eseguire il rendering dei dati su richiesta.

Se una finestra ritarda il rendering di un formato specifico e quindi un'altra applicazione richiede dati in tale formato, alla finestra viene inviato un messaggio [**WM \_ RENDERFORMAT**](wm-renderformat.md) . Inoltre, se una finestra ritarda il rendering di uno o più formati e se alcuni di questi formati rimangono senza rendering quando la finestra sta per essere distrutta, viene inviato un messaggio [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) alla finestra prima della sua distruzione.

Per eseguire il rendering di un formato degli Appunti, la routine della finestra deve inserire un handle di dati non **null** negli Appunti utilizzando la funzione [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) . Se la procedura della finestra esegue il rendering di un formato in risposta al messaggio [**WM \_ RENDERFORMAT**](wm-renderformat.md) , non deve aprire gli Appunti prima di chiamare **SetClipboardData**. Tuttavia, se si esegue il rendering di uno o più formati in risposta al messaggio [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) , è necessario aprire gli appunti e verificare che la finestra sia ancora proprietaria degli Appunti prima di chiamare **SetClipboardData** e chiudere gli Appunti prima di restituire.

L'applicazione label elabora i messaggi [**WM \_ RENDERFORMAT**](wm-renderformat.md) e [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) come indicato di seguito.


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



In entrambi i casi, la routine della finestra chiama la funzione RenderFormat definita dall'applicazione, definita come indicato di seguito.

La struttura, denominata LABELBOX, viene definita come indicato di seguito.


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



### <a name="processing-the-wm_destroyclipboard-message"></a>Elaborazione del \_ messaggio WM DESTROYCLIPBOARD

Una finestra può elaborare il messaggio [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) per liberare le risorse riservate per supportare il rendering ritardato. Ad esempio, l'applicazione Label, quando si copia un'etichetta negli Appunti, alloca un oggetto memoria locale. Questo oggetto viene quindi liberato in risposta al messaggio **WM \_ DESTROYCLIPBOARD** , come indicato di seguito.


```
case WM_DESTROYCLIPBOARD: 
    if (pboxLocalClip != NULL) 
    { 
        LocalFree(pboxLocalClip); 
        pboxLocalClip = NULL; 
    } 
    break;
```



### <a name="using-the-owner-display-clipboard-format"></a>Uso del formato degli Appunti Owner-Display

Se una finestra inserisce informazioni sugli appunti usando il formato degli **Appunti \_ OWNERDISPLAY di CF** , è necessario eseguire le operazioni seguenti:

-   Elaborare il messaggio [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) . Questo messaggio viene inviato al proprietario degli Appunti quando una parte della finestra Visualizzatore Appunti deve essere ridisegnata.

-   Elaborare il messaggio [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md) . Questo messaggio viene inviato al proprietario degli Appunti quando la finestra Visualizzatore Appunti è stata ridimensionata o il relativo contenuto è stato modificato.

    In genere, una finestra risponde a questo messaggio impostando le posizioni e gli intervalli di scorrimento per la finestra Visualizzatore Appunti. In risposta a questo messaggio, l'applicazione label aggiorna anche una struttura di [**dimensioni**](/previous-versions//dd145106(v=vs.85)) per la finestra Visualizzatore Appunti.

-   Elaborare i messaggi [**WM \_ HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) e [**WM \_ VSCROLLCLIPBOARD**](wm-vscrollclipboard.md) . Questi messaggi vengono inviati al proprietario degli Appunti quando si verifica un evento della barra di scorrimento nella finestra Visualizzatore Appunti.

-   Elaborare il messaggio [**WM \_ ASKCBFORMATNAME**](wm-askcbformatname.md) . La finestra Visualizzatore Appunti Invia questo messaggio a un'applicazione per recuperare il nome del formato di visualizzazione del proprietario.

La routine della finestra per l'applicazione label elabora questi messaggi, come indicato di seguito.


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



## <a name="monitoring-clipboard-contents"></a>Monitoraggio del contenuto degli Appunti

Sono disponibili tre modi per monitorare le modifiche negli Appunti. Il metodo meno recente consiste nel creare una finestra del visualizzatore degli Appunti. In Windows 2000 è stata aggiunta la possibilità di eseguire query sul numero di sequenza degli Appunti e Windows Vista ha aggiunto il supporto per i listener di formato degli Appunti. Le finestre del visualizzatore degli Appunti sono supportate per la compatibilità con le versioni precedenti di Windows. I nuovi programmi devono usare i listener di formato degli Appunti o il numero di sequenza degli Appunti.

## <a name="querying-the-clipboard-sequence-number"></a>Esecuzione di query sul numero di sequenza degli Appunti

Ogni volta che il contenuto degli Appunti viene modificato, un valore a 32 bit noto come numero di sequenza degli Appunti viene incrementato. Un programma può recuperare il numero di sequenza degli appunti corrente chiamando la funzione [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) . Confrontando il valore restituito da un valore restituito da una precedente chiamata a **GetClipboardSequenceNumber**, un programma può determinare se il contenuto degli Appunti è stato modificato. Questo metodo è più adatto ai programmi che memorizzano nella cache i risultati in base ai contenuti degli Appunti correnti ed è necessario sapere se i calcoli sono ancora validi prima di utilizzare i risultati della cache. Si noti che questo non è un metodo di notifica e non deve essere usato in un ciclo di polling. Per ricevere una notifica quando cambiano i contenuti degli Appunti, usare un listener del formato degli Appunti o un visualizzatore degli Appunti.

## <a name="creating-a-clipboard-format-listener"></a>Creazione di un listener di formato degli Appunti

Un listener del formato degli Appunti è una finestra che è stata registrata per ricevere una notifica quando il contenuto degli Appunti è stato modificato. Questo metodo è consigliato per la creazione di una finestra del visualizzatore degli appunti perché è più semplice da implementare ed evita problemi se i programmi non riescono a gestire correttamente la catena del visualizzatore degli Appunti o se una finestra nella catena del visualizzatore degli Appunti smette di rispondere ai messaggi.

Una finestra viene registrata come listener del formato degli Appunti chiamando la funzione [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) . Quando il contenuto degli Appunti viene modificato, la finestra viene inviata un messaggio [**WM \_ CLIPBOARDUPDATE**](wm-clipboardupdate.md) . La registrazione rimane valida fino a quando la finestra non viene annullata la registrazione chiamando la funzione [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) .

## <a name="creating-a-clipboard-viewer-window"></a>Creazione di una finestra Visualizzatore Appunti

Una finestra del visualizzatore degli Appunti Visualizza il contenuto corrente degli Appunti e riceve i messaggi quando il contenuto degli Appunti viene modificato. Per creare una finestra del visualizzatore degli Appunti, l'applicazione deve eseguire le operazioni seguenti:

-   Aggiungere la finestra alla catena del visualizzatore degli Appunti.
-   Elaborare il messaggio [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .
-   Elaborare il messaggio [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) .
-   Rimuovere la finestra dalla catena del visualizzatore degli Appunti prima che venga eliminata definitivamente.

## <a name="adding-a-window-to-the-clipboard-viewer-chain"></a>Aggiunta di una finestra alla catena del visualizzatore degli Appunti

Una finestra si aggiunge alla catena del visualizzatore degli Appunti chiamando la funzione [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) . Il valore restituito è l'handle per la finestra successiva nella catena. Una finestra deve tenere traccia di questo valore, ad esempio salvando il valore in una variabile statica denominata *hwndNextViewer*.

Nell'esempio seguente viene aggiunta una finestra alla catena del visualizzatore degli Appunti in risposta al messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) .


```
case WM_CREATE: 
 
    // Add the window to the clipboard viewer chain. 
 
    hwndNextViewer = SetClipboardViewer(hwnd); 
    break;
```



I frammenti di codice vengono visualizzati per le attività seguenti:

-   [Elaborazione del \_ messaggio WM CHANGECBCHAIN](/windows)
-   [Rimozione di una finestra dalla catena del visualizzatore degli Appunti](#removing-a-window-from-the-clipboard-viewer-chain)
-   [Elaborazione del \_ messaggio WM DRAWCLIPBOARD](/windows)
-   [Esempio di Visualizzatore Appunti](#example-of-a-clipboard-viewer)

### <a name="processing-the-wm_changecbchain-message"></a>Elaborazione del \_ messaggio WM CHANGECBCHAIN

Una finestra del visualizzatore degli Appunti riceve il messaggio [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) quando un'altra finestra viene rimossa dalla catena del visualizzatore degli Appunti. Se la finestra da rimuovere è la finestra successiva nella catena, la finestra che riceve il messaggio deve scollegare la finestra successiva dalla catena. In caso contrario, il messaggio deve essere passato alla finestra successiva nella catena.

Nell'esempio seguente viene illustrata l'elaborazione del messaggio [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .


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



### <a name="removing-a-window-from-the-clipboard-viewer-chain"></a>Rimozione di una finestra dalla catena del visualizzatore degli Appunti

Per rimuovere se stesso dalla catena del visualizzatore degli Appunti, una finestra chiama la funzione [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) . Nell'esempio seguente viene rimossa una finestra dalla catena del visualizzatore degli Appunti in risposta al messaggio [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) .


```
case WM_DESTROY: 
    ChangeClipboardChain(hwnd, hwndNextViewer); 
    PostQuitMessage(0); 
    break;
```



### <a name="processing-the-wm_drawclipboard-message"></a>Elaborazione del \_ messaggio WM DRAWCLIPBOARD

Il messaggio [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) notifica a una finestra del visualizzatore degli appunti che il contenuto degli Appunti è stato modificato. Quando si elabora il messaggio **WM \_ DRAWCLIPBOARD** , una finestra deve eseguire le operazioni seguenti:

1.  Determinare il formato degli appunti disponibili da visualizzare.
2.  Recuperare i dati degli Appunti e visualizzarli nella finestra. In alternativa, se il formato degli Appunti è **CF \_ OWNERDISPLAY**, inviare un messaggio [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) al proprietario degli Appunti.
3.  Inviare il messaggio alla finestra successiva nella catena del visualizzatore degli Appunti.

Per un esempio di elaborazione del messaggio [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) , vedere l'elenco di esempio [di un visualizzatore degli Appunti](#example-of-a-clipboard-viewer).

### <a name="example-of-a-clipboard-viewer"></a>Esempio di Visualizzatore Appunti

Nell'esempio seguente viene illustrata una semplice applicazione Visualizzatore Appunti.


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



 

 