---
title: Uso delle finestre di dialogo
description: Le finestre di dialogo vengono usate per visualizzare informazioni e richiedere l'input dell'utente.
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Windows Interfaccia utente, windowing
- Windows Interfaccia utente,finestre di dialogo
- windowing, finestre di dialogo
- finestre di dialogo, informazioni
- finestre di dialogo, visualizzazione
- finestre di dialogo modali
- finestre di dialogo non modali
- finestre di dialogo, modali
- finestre di dialogo, non modali
- finestre di dialogo, inizializzazione
- modelli di finestre di dialogo
- finestre di dialogo, modelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32ec5e97060697388224ac92f60b6043a188d4259520aaf151fb188c43f6bb64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720795"
---
# <a name="using-dialog-boxes"></a>Uso delle finestre di dialogo

Le finestre di dialogo vengono usate per visualizzare informazioni e richiedere l'input dell'utente. L'applicazione carica e inizializza la finestra di dialogo, elabora l'input dell'utente ed elimina la finestra di dialogo al termine dell'attività. Il processo di gestione delle finestre di dialogo varia a seconda che la finestra di dialogo sia modale o non modale. Una finestra di dialogo modale richiede all'utente di chiudere la finestra di dialogo prima di attivare un'altra finestra nell'applicazione. Tuttavia, l'utente può attivare finestre in applicazioni diverse. Una finestra di dialogo non modabile non richiede una risposta immediata da parte dell'utente. È simile a una finestra principale contenente controlli.

Le sezioni seguenti illustrano come usare entrambi i tipi di finestre di dialogo.

-   [Visualizzazione di una finestra di messaggio](#displaying-a-message-box)
-   [Creazione di una finestra di dialogo modale](#creating-a-modal-dialog-box)
-   [Creazione di una finestra di dialogo non modabile](#creating-a-modeless-dialog-box)
-   [Inizializzazione di una finestra di dialogo](#initializing-a-dialog-box)
-   [Creazione di un modello in memoria](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a>Visualizzazione di una finestra di messaggio

La forma più semplice di finestra di dialogo modale è la finestra di messaggio. La maggior parte delle applicazioni usa finestre di messaggio per avvisare l'utente di errori e per richiedere indicazioni su come procedere dopo che si è verificato un errore. È possibile creare una finestra di messaggio usando la funzione [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) o [**MessageBoxEx,**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) specificando il messaggio e il numero e il tipo di pulsanti da visualizzare. Il sistema crea una finestra di dialogo modale, fornendo un modello di finestra di dialogo e una procedura propri. Dopo che l'utente chiude la finestra di messaggio, **MessageBox** o **MessageBoxEx** restituisce un valore che identifica il pulsante scelto dall'utente per chiudere la finestra di messaggio.

Nell'esempio seguente l'applicazione visualizza una finestra di messaggio che richiede all'utente di eseguire un'azione dopo che si è verificata una condizione di errore. Nella finestra di messaggio viene visualizzato il messaggio che descrive la condizione di errore e come risolverla. Lo **stile MB \_ YESNO** indica a [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) di fornire due pulsanti con cui l'utente può scegliere come procedere:


```
int DisplayConfirmSaveAsMessageBox()
{
    int msgboxID = MessageBox(
        NULL,
        L"temp.txt already exists.\nDo you want to replace it?",
        L"Confirm Save As",
        MB_ICONEXCLAMATION | MB_YESNO
    );

    if (msgboxID == IDYES)
    {
        // TODO: add code
    }

    return msgboxID;    
}
```



L'immagine seguente mostra l'output dell'esempio di codice precedente:

![finestra di messaggio](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a>Creazione di una finestra di dialogo modale

È possibile creare una finestra di dialogo modale usando la [**funzione DialogBox.**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) È necessario specificare l'identificatore o il nome di una risorsa modello di finestra di dialogo e un puntatore alla routine della finestra di dialogo. La **funzione DialogBox** carica il modello, visualizza la finestra di dialogo ed elabora tutto l'input dell'utente fino a quando l'utente non chiude la finestra di dialogo.

Nell'esempio seguente l'applicazione visualizza una finestra di dialogo modale quando l'utente fa clic su **Elimina elemento** dal menu di un'applicazione. La finestra di dialogo contiene un controllo di modifica (in cui l'utente immette il nome di un elemento) e i pulsanti **OK** **e Annulla.** Gli identificatori di controllo per questi controlli sono rispettivamente ID \_ ITEMNAME, IDOK e IDCANCEL.

La prima parte dell'esempio è costituita dalle istruzioni che creano la finestra di dialogo modale. Queste istruzioni, nella routine della finestra per la finestra principale dell'applicazione, creano la finestra di dialogo quando il sistema riceve un messaggio [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) con l'identificatore di menu IDM \_ DELETEITEM. La seconda parte dell'esempio è la routine della finestra di dialogo, che recupera il contenuto del controllo di modifica e chiude la finestra di dialogo alla ricezione di un **messaggio WM \_ COMMAND.**

Le istruzioni seguenti creano la finestra di dialogo modale. Il modello di finestra di dialogo è una risorsa nel file eseguibile dell'applicazione e ha l'identificatore di risorsa DLG \_ DELETEITEM.


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_DELETEITEM: 
            if (DialogBox(hinst, 
                          MAKEINTRESOURCE(DLG_DELETEITEM), 
                          hwnd, 
                          (DLGPROC)DeleteItemProc)==IDOK) 
            {
                // Complete the command; szItemName contains the 
                // name of the item to delete. 
            }

            else 
            {
                // Cancel the command. 
            } 
            break; 
    } 
    return 0L; 
```



In questo esempio, l'applicazione specifica la finestra principale come finestra proprietaria per la finestra di dialogo. Quando il sistema visualizza inizialmente la finestra di dialogo, la relativa posizione è relativa all'angolo superiore sinistro dell'area client della finestra proprietaria. L'applicazione usa il valore restituito da [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) per determinare se procedere con l'operazione o annullarla. Le istruzioni seguenti definiscono la routine della finestra di dialogo.


```
char szItemName[80]; // receives name of item to delete. 
 
BOOL CALLBACK DeleteItemProc(HWND hwndDlg, 
                             UINT message, 
                             WPARAM wParam, 
                             LPARAM lParam) 
{ 
    switch (message) 
    { 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    if (!GetDlgItemText(hwndDlg, ID_ITEMNAME, szItemName, 80)) 
                         *szItemName=0; 
 
                    // Fall through. 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, wParam); 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



In questo esempio la procedura usa [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) per recuperare il testo corrente dal controllo di modifica identificato dall'ID \_ ITEMNAME. La procedura chiama quindi la [**funzione EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) per impostare il valore restituito della finestra di dialogo su IDOK o IDCANCEL, a seconda del messaggio ricevuto, e per avviare il processo di chiusura della finestra di dialogo. Gli identificatori IDOK e IDCANCEL corrispondono ai pulsanti **OK** **e** Annulla. Dopo che la routine chiama **EndDialog**, il sistema invia messaggi aggiuntivi alla procedura per eliminare la finestra di dialogo e restituisce il valore restituito della finestra di dialogo alla funzione che ha creato la finestra di dialogo.

## <a name="creating-a-modeless-dialog-box"></a>Creazione di una finestra di dialogo non modabile

Per creare una finestra di dialogo non modabile, usare la funzione [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) , specificando l'identificatore o il nome di una risorsa modello di finestra di dialogo e un puntatore alla routine della finestra di dialogo. **CreateDialog** carica il modello, crea la finestra di dialogo e facoltativamente lo visualizza. L'applicazione è responsabile del recupero e dell'invio dei messaggi di input dell'utente alla procedura della finestra di dialogo.

Nell'esempio seguente l'applicazione visualizza una finestra di dialogo non modali, se non è già visualizzata, quando l'utente fa clic su **Vai** a dal menu di un'applicazione. La finestra di dialogo contiene un controllo di modifica, una casella di controllo e **i pulsanti OK** **e** Annulla. Il modello di finestra di dialogo è una risorsa nel file eseguibile dell'applicazione e ha l'identificatore di risorsa DLG \_ GOTO. L'utente immette un numero di riga nel controllo di modifica e seleziona la casella di controllo per specificare che il numero di riga è relativo alla riga corrente. Gli identificatori di controllo sono ID \_ LINE, ID \_ ABSREL, IDOK e IDCANCEL.

Le istruzioni nella prima parte dell'esempio creano la finestra di dialogo non modali. Queste istruzioni, nella routine della finestra per la finestra principale dell'applicazione, creano la finestra di dialogo quando la routine della finestra riceve un messaggio [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) con l'identificatore di menu GOTO IDM, ma solo se la variabile globale non contiene già un \_ handle valido. La seconda parte dell'esempio è il ciclo di messaggi principale dell'applicazione. Il ciclo include la [**funzione IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) per garantire che l'utente possa usare l'interfaccia della tastiera della finestra di dialogo in questa finestra di dialogo non modabile. La terza parte dell'esempio è la procedura della finestra di dialogo. La procedura recupera il contenuto del controllo di modifica e della casella di controllo quando l'utente fa clic sul **pulsante OK.** La procedura elimina la finestra di dialogo quando l'utente fa clic sul **pulsante** Annulla.


```
HWND hwndGoto = NULL;  // Window handle of dialog box 
                
...

case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_GOTO: 
            if (!IsWindow(hwndGoto)) 
            { 
                hwndGoto = CreateDialog(hinst, 
                                        MAKEINTRESOURCE(DLG_GOTO), 
                                        hwnd, 
                                        (DLGPROC)GoToProc); 
                ShowWindow(hwndGoto, SW_SHOW); 
            } 
            break; 
    } 
    return 0L; 
```



Nelle istruzioni precedenti [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) viene chiamato solo se `hwndGoto` non contiene un handle di finestra valido. Ciò garantisce che l'applicazione non visualizza due finestre di dialogo contemporaneamente. Per supportare questo metodo di controllo, la routine della finestra di dialogo deve essere impostata su **NULL** quando elimina la finestra di dialogo.

Il ciclo di messaggi per un'applicazione è costituito dalle istruzioni seguenti.


```
BOOL bRet;

while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0) 
{ 
    if (bRet == -1)
    {
        // Handle the error and possibly exit
    }
    else if (!IsWindow(hwndGoto) || !IsDialogMessage(hwndGoto, &msg)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
} 
```



Il ciclo controlla la validità dell'handle di finestra nella finestra di dialogo e chiama la [**funzione IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) solo se l'handle è valido. **IsDialogMessage** elabora il messaggio solo se appartiene alla finestra di dialogo. In caso contrario, **restituisce FALSE** e il ciclo invia il messaggio alla finestra appropriata.

Le istruzioni seguenti definiscono la routine della finestra di dialogo.


```
int iLine;             // Receives line number.
BOOL fRelative;        // Receives check box status. 
 
BOOL CALLBACK GoToProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    BOOL fError; 
 
    switch (message) 
    { 
        case WM_INITDIALOG: 
            CheckDlgButton(hwndDlg, ID_ABSREL, fRelative); 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    fRelative = IsDlgButtonChecked(hwndDlg, ID_ABSREL); 
                    iLine = GetDlgItemInt(hwndDlg, ID_LINE, &fError, fRelative); 
                    if (fError) 
                    { 
                        MessageBox(hwndDlg, SZINVALIDNUMBER, SZGOTOERR, MB_OK); 
                        SendDlgItemMessage(hwndDlg, ID_LINE, EM_SETSEL, 0, -1L); 
                    } 
                    else 

                    // Notify the owner window to carry out the task. 
 
                    return TRUE; 
 
                case IDCANCEL: 
                    DestroyWindow(hwndDlg); 
                    hwndGoto = NULL; 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



Nelle istruzioni precedenti la procedura elabora i messaggi [**WM \_ INITDIALOG**](wm-initdialog.md) e [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) Durante **\_ l'elaborazione di WM INITDIALOG,** la procedura inizializza la casella di controllo passando il valore corrente della variabile globale a [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx). La routine restituisce quindi **TRUE per** indirizzare il sistema all'impostazione dello stato attivo per l'input predefinito.

Durante [**\_ l'elaborazione**](/windows/desktop/menurc/wm-command) di WM COMMAND, la procedura chiude la finestra di dialogo solo se l'utente fa clic sul pulsante **Annulla,** ovvero il pulsante con l'identificatore IDCANCEL. La procedura deve chiamare [**DestroyWindow per**](/windows/desktop/api/winuser/nf-winuser-destroywindow) chiudere una finestra di dialogo non modale. Si noti che la routine imposta anche la variabile su **NULL** per garantire il corretto funzionamento delle altre istruzioni che dipendono da questa variabile.

Se l'utente fa clic sul pulsante **OK,** la procedura recupera lo stato corrente della casella di controllo e lo assegna alla **variabile fRelative.** Usa quindi la variabile per recuperare il numero di riga dal controllo di modifica. [**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) converte il testo nel controllo di modifica in un numero intero. Il valore **di fRelative** determina se la funzione interpreta il numero come valore con segno o senza segno. Se il testo del controllo di modifica non è un numero valido, **GetDlgItemInt** imposta il valore della **variabile fError** su un valore diverso da zero. La procedura controlla questo valore per determinare se visualizzare un messaggio di errore o eseguire l'attività. In caso di errore, la routine della finestra di dialogo invia un messaggio al controllo di modifica, indicando di selezionare il testo nel controllo in modo che l'utente possa sostituirlo facilmente. Se **GetDlgItemInt** non restituisce un errore, la procedura può eseguire l'attività richiesta o inviare un messaggio alla finestra proprietaria, indicando l'esecuzione dell'operazione.

## <a name="initializing-a-dialog-box"></a>Inizializzazione di una finestra di dialogo

Inizializzare la finestra di dialogo e il relativo contenuto durante l'elaborazione [**del messaggio \_ WM INITDIALOG.**](wm-initdialog.md) L'attività più comune è inizializzare i controlli in modo che riflettano le impostazioni correnti della finestra di dialogo. Un'altra attività comune è centrare una finestra di dialogo sullo schermo o all'interno della finestra proprietaria. Un'attività utile per alcune finestre di dialogo è impostare lo stato attivo per l'input su un controllo specificato anziché accettare lo stato attivo per l'input predefinito.

Nell'esempio seguente la routine della finestra di dialogo centra la finestra di dialogo e imposta lo stato attivo per l'input durante l'elaborazione [**del messaggio \_ WM INITDIALOG.**](wm-initdialog.md) Per centrare la finestra di dialogo, la procedura recupera i rettangoli della finestra per la finestra di dialogo e la finestra proprietaria e calcola una nuova posizione per la finestra di dialogo. Per impostare lo stato attivo per l'input, la procedura controlla *il parametro wParam* per determinare l'identificatore dello stato attivo per l'input predefinito.


```
HWND hwndOwner; 
RECT rc, rcDlg, rcOwner; 

....
 
case WM_INITDIALOG: 

    // Get the owner window and dialog box rectangles. 

    if ((hwndOwner = GetParent(hwndDlg)) == NULL) 
    {
        hwndOwner = GetDesktopWindow(); 
    }

    GetWindowRect(hwndOwner, &rcOwner); 
    GetWindowRect(hwndDlg, &rcDlg); 
    CopyRect(&rc, &rcOwner); 

    // Offset the owner and dialog box rectangles so that right and bottom 
    // values represent the width and height, and then offset the owner again 
    // to discard space taken up by the dialog box. 

    OffsetRect(&rcDlg, -rcDlg.left, -rcDlg.top); 
    OffsetRect(&rc, -rc.left, -rc.top); 
    OffsetRect(&rc, -rcDlg.right, -rcDlg.bottom); 

    // The new position is the sum of half the remaining space and the owner's 
    // original position. 

    SetWindowPos(hwndDlg, 
                 HWND_TOP, 
                 rcOwner.left + (rc.right / 2), 
                 rcOwner.top + (rc.bottom / 2), 
                 0, 0,          // Ignores size arguments. 
                 SWP_NOSIZE); 

    if (GetDlgCtrlID((HWND) wParam) != ID_ITEMNAME) 
    { 
        SetFocus(GetDlgItem(hwndDlg, ID_ITEMNAME)); 
        return FALSE; 
    } 
    return TRUE; 
```



Nelle istruzioni precedenti la procedura usa la funzione [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) per recuperare l'handle della finestra proprietaria in una finestra di dialogo. La funzione restituisce l'handle della finestra proprietaria alle finestre di dialogo e l'handle della finestra padre alle finestre figlio. Poiché un'applicazione può creare una finestra di dialogo senza proprietario, la procedura controlla l'handle restituito e usa la funzione [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) per recuperare l'handle della finestra del desktop, se necessario. Dopo aver calcolato la nuova posizione, la procedura usa la funzione [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per spostare la finestra di dialogo, specificando il valore HWND TOP per assicurarsi che la finestra di dialogo rimanga sopra la finestra \_ proprietaria.

Prima di impostare lo stato attivo per l'input, la procedura controlla l'identificatore di controllo dello stato attivo per l'input predefinito. Il sistema passa l'handle della finestra dello stato attivo di input predefinito nel *parametro wParam.* La [**funzione GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) restituisce l'identificatore per il controllo identificato dall'handle di finestra. Se l'identificatore non corrisponde all'identificatore corretto, la procedura usa la [**funzione SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) per impostare lo stato attivo per l'input. La [**funzione GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) è necessaria per recuperare l'handle della finestra del controllo desiderato.

## <a name="creating-a-template-in-memory"></a>Creazione di un modello in memoria

Le applicazioni talvolta adattano o modificano il contenuto delle finestre di dialogo a seconda dello stato corrente dei dati elaborati. In questi casi, non è pratico fornire tutti i modelli di finestra di dialogo possibili come risorse nel file eseguibile dell'applicazione. Tuttavia, la creazione di modelli in memoria offre all'applicazione una maggiore flessibilità da adattare a qualsiasi circostanza.

Nell'esempio seguente l'applicazione crea un modello in memoria per una finestra di dialogo modale contenente un messaggio e **i pulsanti OK** **e** Guida.

In un modello di finestra di dialogo tutte le stringhe di caratteri, ad esempio i titoli delle finestre di dialogo e dei pulsanti, devono essere stringhe Unicode. Questo esempio usa la [**funzione MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) per generare queste stringhe Unicode.

Le [**strutture DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) in un modello di finestra di dialogo devono essere allineate in base **ai limiti DWORD.** Per allineare queste strutture, questo esempio usa una routine helper che accetta un puntatore di input e restituisce il puntatore più vicino allineato su un **limite DWORD.**


```
#define ID_HELP   150
#define ID_TEXT   200

LPWORD lpwAlign(LPWORD lpIn)
{
    ULONG ul;

    ul = (ULONG)lpIn;
    ul ++;
    ul >>=1;
    ul <<=1;
    return (LPWORD)ul;
}

LRESULT DisplayMyMessage(HINSTANCE hinst, HWND hwndOwner, LPSTR lpszMessage)
{
    HGLOBAL hgbl;
    LPDLGTEMPLATE lpdt;
    LPDLGITEMTEMPLATE lpdit;
    LPWORD lpw;
    LPWSTR lpwsz;
    LRESULT ret;
    int nchar;

    hgbl = GlobalAlloc(GMEM_ZEROINIT, 1024);
    if (!hgbl)
        return -1;
 
    lpdt = (LPDLGTEMPLATE)GlobalLock(hgbl);
 
    // Define a dialog box.
 
    lpdt->style = WS_POPUP | WS_BORDER | WS_SYSMENU | DS_MODALFRAME | WS_CAPTION;
    lpdt->cdit = 3;         // Number of controls
    lpdt->x  = 10;  lpdt->y  = 10;
    lpdt->cx = 100; lpdt->cy = 100;

    lpw = (LPWORD)(lpdt + 1);
    *lpw++ = 0;             // No menu
    *lpw++ = 0;             // Predefined dialog box class (by default)

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "My Dialog", -1, lpwsz, 50);
    lpw += nchar;

    //-----------------------
    // Define an OK button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 70;
    lpdit->cx = 80; lpdit->cy = 20;
    lpdit->id = IDOK;       // OK button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_DEFPUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "OK", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a Help button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 55; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_HELP;    // Help button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_PUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class atom

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "Help", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a static text control.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_TEXT;    // Text identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | SS_LEFT;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0082;        // Static class

    for (lpwsz = (LPWSTR)lpw; *lpwsz++ = (WCHAR)*lpszMessage++;);
    lpw = (LPWORD)lpwsz;
    *lpw++ = 0;             // No creation data

    GlobalUnlock(hgbl); 
    ret = DialogBoxIndirect(hinst, 
                           (LPDLGTEMPLATE)hgbl, 
                           hwndOwner, 
                           (DLGPROC)DialogProc); 
    GlobalFree(hgbl); 
    return ret; 
}
```



 

 