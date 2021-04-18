---
description: Negli esempi di codice seguenti viene illustrato come eseguire le attività seguenti associate a messaggi e code di messaggi di Windows.
ms.assetid: 62b4616c-37bf-4d9f-8891-7010c7035d18
title: Utilizzo di messaggi e code di messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a33f422a1a7c77f2c2fcd5913f931168a350a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312486"
---
# <a name="using-messages-and-message-queues"></a>Utilizzo di messaggi e code di messaggi

Negli esempi di codice seguenti viene illustrato come eseguire le attività seguenti associate a messaggi e code di messaggi di Windows.

-   [Creazione di un ciclo di messaggi](#creating-a-message-loop)
-   [Esame di una coda di messaggi](#examining-a-message-queue)
-   [Invio di un messaggio](#posting-a-message)
-   [Invio di un messaggio](#sending-a-message)

## <a name="creating-a-message-loop"></a>Creazione di un ciclo di messaggi

Il sistema non crea automaticamente una coda di messaggi per ogni thread. Il sistema crea invece una coda di messaggi solo per i thread che eseguono operazioni che richiedono una coda di messaggi. Se il thread crea una o più finestre, è necessario fornire un ciclo di messaggi. Questo ciclo di messaggi recupera i messaggi dalla coda di messaggi del thread e li invia alle procedure appropriate della finestra.

Poiché il sistema indirizza i messaggi a singole finestre in un'applicazione, è necessario che un thread crei almeno una finestra prima di avviare il ciclo di messaggi. La maggior parte delle applicazioni contiene un solo thread che crea finestre. Una tipica applicazione registra la classe della finestra principale, crea e Mostra la finestra principale, quindi avvia il ciclo di messaggi, tutto nella funzione [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) .

Per creare un ciclo di messaggi, usare le funzioni [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) e [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) . Se l'applicazione deve ottenere l'input di caratteri dall'utente, includere la funzione [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) nel ciclo. **TranslateMessage** converte i messaggi di chiave virtuale in messaggi di tipo carattere. Nell'esempio seguente viene illustrato il ciclo di messaggi nella funzione [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) di una semplice applicazione basata su Windows.


```
HINSTANCE hinst; 
HWND hwndMain; 
 
int PASCAL WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, 
    LPSTR lpszCmdLine, int nCmdShow) 
{ 
    MSG msg;
    BOOL bRet; 
    WNDCLASS wc; 
    UNREFERENCED_PARAMETER(lpszCmdLine); 
 
    // Register the window class for the main window. 
 
    if (!hPrevInstance) 
    { 
        wc.style = 0; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
        wc.cbClsExtra = 0; 
        wc.cbWndExtra = 0; 
        wc.hInstance = hInstance; 
        wc.hIcon = LoadIcon((HINSTANCE) NULL, 
            IDI_APPLICATION); 
        wc.hCursor = LoadCursor((HINSTANCE) NULL, 
            IDC_ARROW); 
        wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
        wc.lpszMenuName =  "MainMenu"; 
        wc.lpszClassName = "MainWndClass"; 
 
        if (!RegisterClass(&wc)) 
            return FALSE; 
    } 
 
    hinst = hInstance;  // save instance handle 
 
    // Create the main window. 
 
    hwndMain = CreateWindow("MainWndClass", "Sample", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, (HWND) NULL, 
        (HMENU) NULL, hinst, (LPVOID) NULL); 
 
    // If the main window cannot be created, terminate 
    // the application. 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Show the window and paint its contents. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Start the message loop. 
 
    while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
    { 
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
 
    // Return the exit code to the system. 
 
    return msg.wParam; 
} 
```



Nell'esempio seguente viene illustrato un ciclo di messaggi per un thread che utilizza acceleratori e viene visualizzata una finestra di dialogo non modale. Quando [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) o [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) restituisce **true** (che indica che il messaggio è stato elaborato), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) e [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) non vengono chiamati. Il motivo è che **TranslateAccelerator** e **IsDialogMessage** eseguono tutte le operazioni necessarie per la conversione e l'invio dei messaggi.


```
HWND hwndMain; 
HWND hwndDlgModeless = NULL; 
MSG msg;
BOOL bRet; 
HACCEL haccel; 
// 
// Perform initialization and create a main window. 
// 
 
while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
{ 
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else
    {
        if (hwndDlgModeless == (HWND) NULL || 
                !IsDialogMessage(hwndDlgModeless, &msg) && 
                !TranslateAccelerator(hwndMain, haccel, 
                    &msg)) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
} 
```



## <a name="examining-a-message-queue"></a>Esame di una coda di messaggi

Occasionalmente, un'applicazione deve esaminare il contenuto della coda di messaggi di un thread dall'esterno del ciclo di messaggi del thread. Se, ad esempio, la routine della finestra di un'applicazione esegue un'operazione di disegno lunga, potrebbe essere necessario che l'utente sia in grado di interrompere l'operazione. A meno che l'applicazione non esamini periodicamente la coda di messaggi durante l'operazione per i messaggi del mouse e della tastiera, non risponderà all'input dell'utente finché l'operazione non viene completata. Il motivo è che la funzione [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) nel ciclo di messaggi del thread non viene restituita fino al termine dell'elaborazione di un messaggio da parte della routine della finestra.

È possibile utilizzare la funzione [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) per esaminare una coda di messaggi durante un'operazione di lunga durata. **PeekMessage** è simile alla funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) . entrambi controllano una coda di messaggi per un messaggio corrispondente ai criteri di filtro, quindi copiano il messaggio in una struttura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) . La differenza principale tra le due funzioni è che **GetMessage** non restituisce un risultato fino a quando un messaggio corrispondente ai criteri di filtro non viene inserito nella coda, mentre **PeekMessage** viene restituito immediatamente, indipendentemente dal fatto che un messaggio si trovi nella coda.

Nell'esempio seguente viene illustrato come utilizzare [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) per esaminare una coda di messaggi per i clic del mouse e l'input da tastiera durante un'operazione di lunga durata.


```
HWND hwnd; 
BOOL fDone; 
MSG msg; 
 
// Begin the operation and continue until it is complete 
// or until the user clicks the mouse or presses a key. 
 
fDone = FALSE; 
while (!fDone) 
{ 
    fDone = DoLengthyOperation(); // application-defined function 
 
    // Remove any messages that may be in the queue. If the 
    // queue contains any mouse or keyboard 
    // messages, end the operation. 
 
    while (PeekMessage(&msg, hwnd,  0, 0, PM_REMOVE)) 
    { 
        switch(msg.message) 
        { 
            case WM_LBUTTONDOWN: 
            case WM_RBUTTONDOWN: 
            case WM_KEYDOWN: 
                // 
                // Perform any required cleanup. 
                // 
                fDone = TRUE; 
        } 
    } 
} 
```



Altre funzioni, tra cui [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) e [**GetInputState**](/windows/win32/api/winuser/nf-winuser-getinputstate), consentono anche di esaminare il contenuto della coda di messaggi di un thread. **GetQueueStatus** restituisce una matrice di flag che indica i tipi di messaggi nella coda. l'uso di questa soluzione è il modo più rapido per individuare se la coda contiene messaggi. **GetInputState** restituisce **true** se la coda contiene messaggi relativi al mouse o alla tastiera. Entrambe queste funzioni possono essere utilizzate per determinare se la coda contiene messaggi che devono essere elaborati.

## <a name="posting-a-message"></a>Invio di un messaggio

È possibile inviare un messaggio a una coda di messaggi tramite la funzione [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) . **PostMessage** inserisce un messaggio alla fine della coda di messaggi di un thread e viene restituito immediatamente, senza attendere l'elaborazione del messaggio da parte del thread. I parametri della funzione includono un handle di finestra, un identificatore di messaggio e due parametri di messaggio. Il sistema copia questi parametri in una struttura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) , compila i membri **Time** e **PT** della struttura e inserisce la struttura nella coda di messaggi.

Il sistema utilizza l'handle di finestra passato con la funzione [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) per determinare quale coda di messaggi del thread deve ricevere il messaggio. Se l'handle è in primo piano **HWND \_**, il sistema invia il messaggio alle code di messaggi del thread di tutte le finestre di primo livello.

È possibile utilizzare la funzione [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) per inviare un messaggio a una coda di messaggi di thread specifici. **PostThreadMessage** è simile a [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea), eccetto il primo parametro è un identificatore di thread anziché un handle di finestra. È possibile recuperare l'identificatore del thread chiamando la funzione [**GetCurrentThreadID**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) .

Utilizzare la funzione [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) per uscire da un ciclo di messaggi. **PostQuitMessage** invia il messaggio [**WM \_ Quit**](wm-quit.md) al thread attualmente in esecuzione. Il ciclo di messaggi del thread termina e restituisce il controllo al sistema quando rileva il messaggio **WM \_ Quit** . Un'applicazione in genere chiama **PostQuitMessage** in risposta al messaggio [**WM \_ Destroy**](wm-destroy.md) , come illustrato nell'esempio seguente.


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a>Invio di un messaggio

La funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) viene utilizzata per inviare un messaggio direttamente a una routine della finestra. **SendMessage** chiama una routine della finestra e attende che la procedura elabori il messaggio e restituisca un risultato.

Un messaggio può essere inviato a qualsiasi finestra del sistema; è necessario solo un handle di finestra. Il sistema utilizza l'handle per determinare quale routine della finestra deve ricevere il messaggio.

Prima di elaborare un messaggio che potrebbe essere stato inviato da un altro thread, una routine della finestra deve prima chiamare la funzione [**InSendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) . Se questa funzione restituisce **true**, la routine della finestra deve chiamare [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) prima di qualsiasi funzione che induce il thread a produrre il controllo, come illustrato nell'esempio seguente.


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



È possibile inviare un numero di messaggi ai controlli in una finestra di dialogo. Questi messaggi di controllo impostano l'aspetto, il comportamento e il contenuto dei controlli o recuperano informazioni sui controlli. Ad esempio, il messaggio [**CB \_ ADDSTRING**](../controls/cb-addstring.md) può aggiungere una stringa a una casella combinata e il messaggio di controllo [**BM \_**](../controls/bm-setcheck.md) può impostare lo stato di selezione di una casella di controllo o di un pulsante di opzione.

Utilizzare la funzione [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) per inviare un messaggio a un controllo, specificando l'identificatore del controllo e l'handle della finestra di dialogo che contiene il controllo. Nell'esempio seguente, tratto da una routine della finestra di dialogo, copia una stringa dal controllo di modifica di una casella combinata nella relativa casella di riepilogo. Nell'esempio viene usato **SendDlgItemMessage** per inviare un messaggio [**CB \_ ADDSTRING**](../controls/cb-addstring.md) alla casella combinata.


```
HWND hwndCombo; 
int cTxtLen; 
PSTR pszMem; 
 
switch (uMsg) 
{ 
    case WM_COMMAND: 
        switch (LOWORD(wParam)) 
        { 
            case IDD_ADDCBITEM: 
                // Get the handle of the combo box and the 
                // length of the string in the edit control 
                // of the combo box. 
 
                hwndCombo = GetDlgItem(hwndDlg, IDD_COMBO); 
                cTxtLen = GetWindowTextLength(hwndCombo); 
 
                // Allocate memory for the string and copy 
                // the string into the memory. 
 
                pszMem = (PSTR) VirtualAlloc((LPVOID) NULL, 
                    (DWORD) (cTxtLen + 1), MEM_COMMIT, 
                    PAGE_READWRITE); 
                GetWindowText(hwndCombo, pszMem, 
                    cTxtLen + 1); 
 
                // Add the string to the list box of the 
                // combo box and remove the string from the 
                // edit control of the combo box. 
 
                if (pszMem != NULL) 
                { 
                    SendDlgItemMessage(hwndDlg, IDD_COMBO, 
                        CB_ADDSTRING, 0, 
                        (DWORD) ((LPSTR) pszMem)); 
                    SetWindowText(hwndCombo, (LPSTR) NULL); 
                } 
 
                // Free the memory and return. 
 
                VirtualFree(pszMem, 0, MEM_RELEASE); 
                return TRUE; 
            // 
            // Process other dialog box commands. 
            // 
 
        } 
    // 
    // Process other dialog box messages. 
    // 
 
}
```



 

 
