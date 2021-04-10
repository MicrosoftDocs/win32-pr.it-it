---
title: Utilizzo delle finestre di dialogo
description: Usare le finestre di dialogo per visualizzare le informazioni e richiedere l'input dell'utente.
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Interfaccia utente di Windows, Windowing
- Interfaccia utente di Windows, finestre di dialogo
- finestre, finestre di dialogo
- finestre di dialogo, informazioni
- finestre di dialogo, visualizzazione
- finestre di dialogo modali
- finestre di dialogo non modali
- finestre di dialogo, modali
- finestre di dialogo, non modale
- finestre di dialogo, inizializzazione
- modelli di finestra di dialogo
- finestre di dialogo, modelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21da47d7d59f4cadc21314566bce41a9ef3456a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047173"
---
# <a name="using-dialog-boxes"></a>Utilizzo delle finestre di dialogo

Usare le finestre di dialogo per visualizzare le informazioni e richiedere l'input dell'utente. L'applicazione carica e inizializza la finestra di dialogo, elabora l'input dell'utente ed elimina la finestra di dialogo quando l'utente termina l'attività. Il processo per la gestione delle finestre di dialogo varia a seconda che la finestra di dialogo sia modale o non modale. Per una finestra di dialogo modale è necessario che l'utente chiuda la finestra di dialogo prima di attivare un'altra finestra nell'applicazione. Tuttavia, l'utente può attivare Windows in applicazioni diverse. Una finestra di dialogo non modale non richiede una risposta immediata da parte dell'utente. È simile a una finestra principale contenente i controlli.

Nelle sezioni seguenti viene illustrato come utilizzare entrambi i tipi di finestre di dialogo.

-   [Visualizzazione di una finestra di messaggio](#displaying-a-message-box)
-   [Creazione di una finestra di dialogo modale](#creating-a-modal-dialog-box)
-   [Creazione di una finestra di dialogo non modale](#creating-a-modeless-dialog-box)
-   [Inizializzazione di una finestra di dialogo](#initializing-a-dialog-box)
-   [Creazione di un modello in memoria](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a>Visualizzazione di una finestra di messaggio

Il formato più semplice della finestra di dialogo modale è la finestra di messaggio. La maggior parte delle applicazioni usa le finestre di messaggio per avvisare l'utente degli errori e per richiedere indicazioni su come procedere in seguito a un errore. Per creare una finestra di messaggio, è possibile utilizzare la funzione [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) o [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) , specificando il messaggio e il numero e il tipo di pulsanti da visualizzare. Il sistema crea una finestra di dialogo modale che fornisce il proprio modello di finestra di dialogo e la relativa procedura. Dopo che l'utente ha chiuso la finestra di messaggio **MessageBox** o **MessageBoxEx** restituisce un valore che identifica il pulsante scelto dall'utente per chiudere la finestra di messaggio.

Nell'esempio seguente, l'applicazione visualizza una finestra di messaggio che richiede all'utente di un'azione dopo che si è verificata una condizione di errore. Nella finestra di messaggio viene visualizzato il messaggio che descrive la condizione di errore e come risolverlo. Lo stile **MB \_ YesNo** indica a [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) di fornire due pulsanti con cui l'utente può scegliere come procedere:


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



La figura seguente mostra l'output dell'esempio di codice precedente:

![MessageBox](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a>Creazione di una finestra di dialogo modale

Per creare una finestra di dialogo modale, utilizzare la funzione [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) . È necessario specificare l'identificatore o il nome di una risorsa modello di finestra di dialogo e un puntatore alla routine della finestra di dialogo. La funzione **DialogBox** carica il modello, Visualizza la finestra di dialogo ed elabora tutti gli input utente fino a quando l'utente non chiude la finestra di dialogo.

Nell'esempio seguente, l'applicazione visualizza una finestra di dialogo modale quando l'utente fa clic su **Elimina elemento** dal menu di un'applicazione. La finestra di dialogo contiene un controllo di modifica (in cui l'utente immette il nome di un elemento) e i pulsanti **OK** e **Annulla** . Gli identificatori di controllo per questi controlli sono \_ rispettivamente ID itemName, IDOK e IDCANCEL.

La prima parte dell'esempio è costituita dalle istruzioni che creano la finestra di dialogo modale. Queste istruzioni, nella procedura della finestra principale dell'applicazione, creano la finestra di dialogo quando il sistema riceve un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) con l'identificatore del \_ menu IDM DeleteItem. La seconda parte dell'esempio è la routine della finestra di dialogo, che recupera il contenuto del controllo di modifica e chiude la finestra di dialogo al momento della ricezione di un messaggio di **\_ comando WM** .

Nelle istruzioni seguenti viene creata la finestra di dialogo modale. Il modello della finestra di dialogo è una risorsa nel file eseguibile dell'applicazione e ha l'identificatore di risorsa DLG \_ DeleteItem.


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



In questo esempio, l'applicazione specifica la finestra principale come finestra proprietaria per la finestra di dialogo. Quando il sistema visualizza inizialmente la finestra di dialogo, la relativa posizione è relativa all'angolo superiore sinistro dell'area client della finestra proprietaria. L'applicazione usa il valore restituito da [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) per determinare se procedere con l'operazione o annullarlo. Le istruzioni seguenti definiscono la routine della finestra di dialogo.


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



In questo esempio, la procedura usa [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) per recuperare il testo corrente dal controllo di modifica identificato da ID \_ ItemName. La procedura chiama quindi la funzione [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) per impostare il valore restituito della finestra di dialogo su IDOK o IDCANCEL, a seconda del messaggio ricevuto e per iniziare il processo di chiusura della finestra di dialogo. Gli identificatori IDOK e IDCANCEL corrispondono ai pulsanti **OK** e **Annulla** . Dopo che la stored procedure ha chiamato **EndDialog**, il sistema invia messaggi aggiuntivi alla procedura per eliminare la finestra di dialogo e restituisce nuovamente il valore restituito della finestra di dialogo alla funzione che ha creato la finestra di dialogo.

## <a name="creating-a-modeless-dialog-box"></a>Creazione di una finestra di dialogo non modale

Per creare una finestra di dialogo non modale, utilizzare la funzione [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) , specificando l'identificatore o il nome di una risorsa modello di finestra di dialogo e un puntatore alla routine della finestra di dialogo. **CreateDialog** carica il modello, crea la finestra di dialogo e, facoltativamente, lo Visualizza. L'applicazione è responsabile del recupero e dell'invio di messaggi di input utente alla routine della finestra di dialogo.

Nell'esempio seguente, l'applicazione visualizza una finestra di dialogo non modale, se non è già visualizzata, quando l'utente fa clic **su Vai a** dal menu di un'applicazione. La finestra di dialogo contiene un controllo di modifica, una casella di controllo e pulsanti **OK** e **Annulla** . Il modello della finestra di dialogo è una risorsa nel file eseguibile dell'applicazione e ha l'identificatore di risorsa DLG \_ goto. L'utente immette un numero di riga nel controllo di modifica e controlla la casella di controllo per specificare che il numero di riga è relativo alla riga corrente. Gli identificatori di controllo sono ID \_ line, ID \_ ABSREL, IDOK e IDCANCEL.

Le istruzioni nella prima parte dell'esempio creano la finestra di dialogo non modale. Queste istruzioni, nella procedura della finestra principale dell'applicazione, creano la finestra di dialogo quando la routine della finestra riceve un messaggio [**di \_ comando WM**](/windows/desktop/menurc/wm-command) con l' \_ identificatore del menu IDM goto, ma solo se la variabile globale non contiene già un handle valido. La seconda parte dell'esempio è il ciclo di messaggi principale dell'applicazione. Il ciclo include la funzione [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) per garantire che l'utente possa usare l'interfaccia della tastiera della finestra di dialogo in questa finestra di dialogo non modale. La terza parte dell'esempio è la routine della finestra di dialogo. La procedura consente di recuperare il contenuto del controllo di modifica e della casella di controllo quando l'utente fa clic sul pulsante **OK** . La procedura elimina la finestra di dialogo quando l'utente fa clic sul pulsante **Annulla** .


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



Nelle istruzioni precedenti, [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) viene chiamato solo se `hwndGoto` non contiene un handle di finestra valido. In questo modo si garantisce che l'applicazione non visualizzi due finestre di dialogo nello stesso momento. Per supportare questo metodo di controllo, la routine della finestra di dialogo deve impostare su **null** quando elimina la finestra di dialogo.

Il ciclo di messaggi di un'applicazione è costituito dalle istruzioni seguenti.


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



Il ciclo controlla la validità dell'handle di finestra nella finestra di dialogo e chiama solo la funzione [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) se l'handle è valido. **IsDialogMessage** elabora il messaggio solo se appartiene alla finestra di dialogo. In caso contrario, restituisce **false** e il ciclo invia il messaggio alla finestra appropriata.

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



Nelle istruzioni precedenti, la procedura elabora i messaggi di [**\_ comando**](/windows/desktop/menurc/wm-command) [**WM \_ INITDIALOG**](wm-initdialog.md) e WM. Durante l'elaborazione di **WM \_ INITDIALOG** , la routine inizializza la casella di controllo passando il valore corrente della variabile globale a [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx). La procedura restituisce **true** per indicare al sistema di impostare lo stato attivo per l'input predefinito.

Durante l'elaborazione del [**\_ comando WM**](/windows/desktop/menurc/wm-command) , la procedura chiude la finestra di dialogo solo se l'utente fa clic sul pulsante **Annulla** , ovvero il pulsante con l'identificatore IDCANCEL. Per chiudere una finestra di dialogo non modale, è necessario che la stored procedure chiami [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) . Si noti che la procedura imposta anche la variabile su **null** per assicurarsi che altre istruzioni che dipendono da questa variabile funzionino correttamente.

Se l'utente fa clic sul pulsante **OK** , la procedura recupera lo stato corrente della casella di controllo e la assegna alla variabile **fRelative** . USA quindi la variabile per recuperare il numero di riga dal controllo di modifica. [**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) converte il testo nel controllo di modifica in un intero. Il valore di **fRelative** determina se la funzione interpreta il numero come valore con segno o senza segno. Se il testo del controllo di modifica non è un numero valido, **GetDlgItemInt** imposta il valore della variabile **ferritor** su un valore diverso da zero. La procedura controlla questo valore per determinare se visualizzare o meno un messaggio di errore o eseguire l'attività. In caso di errore, la routine della finestra di dialogo Invia un messaggio al controllo di modifica, indirizzando la selezione del testo nel controllo in modo che l'utente possa sostituirlo facilmente. Se **GetDlgItemInt** non restituisce un errore, la procedura può eseguire l'attività richiesta o inviare un messaggio alla finestra proprietaria, indirizzando l'operazione in modo da eseguire l'operazione.

## <a name="initializing-a-dialog-box"></a>Inizializzazione di una finestra di dialogo

È possibile inizializzare la finestra di dialogo e il relativo contenuto durante l'elaborazione del messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) . L'attività più comune consiste nell'inizializzare i controlli in modo da riflettere le impostazioni correnti della finestra di dialogo. Un'altra attività comune consiste nell'incentrare una finestra di dialogo sullo schermo o all'interno della finestra proprietaria. Un'attività utile per alcune finestre di dialogo consiste nell'impostare lo stato attivo per l'input su un controllo specificato anziché accettare lo stato attivo per l'input predefinito.

Nell'esempio seguente, la routine della finestra di dialogo centra la finestra di dialogo e imposta lo stato attivo per l'input durante l'elaborazione del messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) . Per centrare la finestra di dialogo, la procedura recupera i rettangoli della finestra di dialogo e la finestra proprietaria e calcola una nuova posizione per la finestra di dialogo. Per impostare lo stato attivo per l'input, la procedura controlla il parametro *wParam* per determinare l'identificatore dello stato attivo per l'input predefinito.


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



Nelle istruzioni precedenti, la procedura usa la funzione [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) per recuperare l'handle della finestra proprietaria in una finestra di dialogo. La funzione restituisce l'handle della finestra proprietaria alle finestre di dialogo e l'handle della finestra padre per le finestre figlio. Poiché un'applicazione può creare una finestra di dialogo senza proprietario, la procedura controlla l'handle restituito e usa la funzione [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) per recuperare l'handle della finestra desktop, se necessario. Dopo aver calcolato la nuova posizione, la procedura utilizza la funzione [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per spostare la finestra di dialogo, specificando il \_ valore principale di HWND per assicurarsi che la finestra di dialogo rimanga nella parte superiore della finestra proprietaria.

Prima di impostare lo stato attivo per l'input, la procedura controlla l'identificatore di controllo dello stato attivo per l'input predefinito. Il sistema passa l'handle di finestra dello stato attivo per l'input predefinito nel parametro *wParam* . La funzione [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) restituisce l'identificatore per il controllo identificato dall'handle della finestra. Se l'identificatore non corrisponde all'identificatore corretto, nella procedura viene utilizzata la funzione [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) per impostare lo stato attivo per l'input. Per recuperare l'handle della finestra del controllo desiderato, è necessaria la funzione [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) .

## <a name="creating-a-template-in-memory"></a>Creazione di un modello in memoria

Le applicazioni a volte adattano o modificano il contenuto delle finestre di dialogo a seconda dello stato corrente dei dati in fase di elaborazione. In questi casi, non è pratico fornire tutti i possibili modelli di finestra di dialogo come risorse nel file eseguibile dell'applicazione. Tuttavia, la creazione di modelli in memoria garantisce maggiore flessibilità all'applicazione per adattarsi a qualsiasi circostanza.

Nell'esempio seguente, l'applicazione crea un modello in memoria per una finestra di dialogo modale che contiene un messaggio e i pulsanti **OK** e **Guida** .

In un modello di finestra di dialogo tutte le stringhe di caratteri, ad esempio la finestra di dialogo e i titoli dei pulsanti, devono essere stringhe Unicode. In questo esempio viene usata la funzione [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) per generare queste stringhe Unicode.

Le strutture [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) in un modello di finestra di dialogo devono essere allineate sui limiti **DWORD** . Per allineare queste strutture, in questo esempio viene utilizzata una routine helper che accetta un puntatore di input e restituisce il puntatore più vicino allineato a un limite **DWORD** .


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



 

 