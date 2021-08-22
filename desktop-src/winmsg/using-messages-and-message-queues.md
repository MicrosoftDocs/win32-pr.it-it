---
description: Gli esempi di codice seguenti illustrano come eseguire le attività seguenti associate Windows messaggi e code di messaggi.
ms.assetid: 62b4616c-37bf-4d9f-8891-7010c7035d18
title: Uso di messaggi e code di messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee617f2c48325eccf5a2fdb07741bb88b47738dea812d372acda1454c9dd3d9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028339"
---
# <a name="using-messages-and-message-queues"></a>Uso di messaggi e code di messaggi

Gli esempi di codice seguenti illustrano come eseguire le attività seguenti associate Windows messaggi e code di messaggi.

-   [Creazione di un ciclo di messaggi](#creating-a-message-loop)
-   [Analisi di una coda di messaggi](#examining-a-message-queue)
-   [Pubblicazione di un messaggio](#posting-a-message)
-   [Invio di un messaggio](#sending-a-message)

## <a name="creating-a-message-loop"></a>Creazione di un ciclo di messaggi

Il sistema non crea automaticamente una coda di messaggi per ogni thread. Al contrario, il sistema crea una coda di messaggi solo per i thread che eseguono operazioni che richiedono una coda di messaggi. Se il thread crea una o più finestre, è necessario fornire un ciclo di messaggi. questo ciclo di messaggi recupera i messaggi dalla coda di messaggi del thread e li invia alle procedure della finestra appropriate.

Poiché il sistema indirizza i messaggi a singole finestre in un'applicazione, un thread deve creare almeno una finestra prima di avviare il ciclo di messaggi. La maggior parte delle applicazioni contiene un singolo thread che crea finestre. Un'applicazione tipica registra la classe window per la finestra principale, crea e mostra la finestra principale e quindi avvia il ciclo di messaggi, tutto nella [**funzione WinMain.**](/windows/win32/api/winbase/nf-winbase-winmain)

Per creare un ciclo di messaggi, usare [**le funzioni GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) e [**DispatchMessage.**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) Se l'applicazione deve ottenere l'input di caratteri dall'utente, includere la [**funzione TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) nel ciclo . **TranslateMessage** converte i messaggi di chiave virtuale in messaggi di tipo carattere. L'esempio seguente illustra il ciclo di messaggi nella [**funzione WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) di una semplice Windows basata su codice.


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



Nell'esempio seguente viene illustrato un ciclo di messaggi per un thread che usa i tasti di scelta rapida e visualizza una finestra di dialogo non modali. Quando [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) o [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) restituisce **TRUE** (a indicare che il messaggio è stato elaborato), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) e [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) non vengono chiamati. Il motivo è che **TranslateAccelerator** e **IsDialogMessage** eseguono tutte le operazioni necessarie per la traduzione e l'invio dei messaggi.


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



## <a name="examining-a-message-queue"></a>Analisi di una coda di messaggi

In alcuni casi, un'applicazione deve esaminare il contenuto della coda di messaggi di un thread dall'esterno del ciclo di messaggi del thread. Ad esempio, se la routine della finestra di un'applicazione esegue un'operazione di disegno lunga, è possibile che l'utente sia in grado di interrompere l'operazione. A meno che l'applicazione non esamini periodicamente la coda di messaggi durante l'operazione per i messaggi del mouse e della tastiera, non risponderà all'input dell'utente fino al termine dell'operazione. Il motivo è che la funzione [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) nel ciclo di messaggi del thread non viene restituita fino al completamento dell'elaborazione di un messaggio da parte della routine della finestra.

È possibile usare la [**funzione PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) per esaminare una coda di messaggi durante un'operazione di lunga durata. **PeekMessage** è simile alla [**funzione GetMessage.**](/windows/win32/api/winuser/nf-winuser-getmessage) entrambi controllano la presenza di un messaggio in una coda di messaggi che corrisponde ai criteri di filtro e quindi copiano il messaggio in una [**struttura MSG.**](/windows/win32/api/winuser/ns-winuser-msg) La differenza principale tra le due funzioni è che **GetMessage** non restituisce finché non viene inserito un messaggio corrispondente ai criteri di filtro nella coda, mentre **PeekMessage** restituisce immediatamente indipendentemente dal fatto che un messaggio si trova nella coda.

L'esempio seguente illustra come usare [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) per esaminare una coda di messaggi per i clic del mouse e l'input da tastiera durante un'operazione di lunga durata.


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



Anche altre funzioni, tra [**cui GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) e [**GetInputState,**](/windows/win32/api/winuser/nf-winuser-getinputstate)consentono di esaminare il contenuto della coda di messaggi di un thread. **GetQueueStatus** restituisce una matrice di flag che indica i tipi di messaggi nella coda. l'uso di è il modo più rapido per individuare se la coda contiene messaggi. **GetInputState restituisce** **TRUE se** la coda contiene messaggi del mouse o della tastiera. Entrambe queste funzioni possono essere usate per determinare se la coda contiene messaggi che devono essere elaborati.

## <a name="posting-a-message"></a>Pubblicazione di un messaggio

È possibile inviare un messaggio a una coda di messaggi usando la [**funzione PostMessage.**](/windows/win32/api/winuser/nf-winuser-postmessagea) **PostMessage** inserisce un messaggio alla fine della coda di messaggi di un thread e restituisce immediatamente, senza attendere l'elaborazione del messaggio da parte del thread. I parametri della funzione includono un handle di finestra, un identificatore di messaggio e due parametri di messaggio. Il sistema copia questi parametri in una struttura  [**MSG,**](/windows/win32/api/winuser/ns-winuser-msg) riempie i membri time e **pt** della struttura e inserisce la struttura nella coda di messaggi.

Il sistema usa l'handle di finestra passato con la [**funzione PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) per determinare quale coda di messaggi del thread deve ricevere il messaggio. Se l'handle **è HWND \_ TOPMOST,** il sistema invia il messaggio alle code di messaggi del thread di tutte le finestre di primo livello.

È possibile usare la [**funzione PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) per pubblicare un messaggio in una coda di messaggi del thread specifica. **PostThreadMessage è** simile a [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea), ad eccezione del fatto che il primo parametro è un identificatore di thread anziché un handle di finestra. È possibile recuperare l'identificatore di thread chiamando la [**funzione GetCurrentThreadId.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid)

Usare la [**funzione PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) per uscire da un ciclo di messaggi. **PostQuitMessage** invia il [**messaggio WM \_ QUIT**](wm-quit.md) al thread attualmente in esecuzione. Il ciclo di messaggi del thread termina e restituisce il controllo al sistema quando rileva il **messaggio WM \_ QUIT.** Un'applicazione chiama **in genere PostQuitMessage** in risposta al [**messaggio WM \_ DESTROY,**](wm-destroy.md) come illustrato nell'esempio seguente.


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a>Invio di un messaggio

La [**funzione SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) viene usata per inviare un messaggio direttamente a una routine della finestra. **SendMessage** chiama una routine della finestra e attende che la routine eserciti il messaggio e restituirà un risultato.

È possibile inviare un messaggio a qualsiasi finestra del sistema. è necessario solo un handle di finestra. Il sistema usa l'handle per determinare quale routine della finestra deve ricevere il messaggio.

Prima di elaborare un messaggio che potrebbe essere stato inviato da un altro thread, una routine della finestra deve chiamare prima [**la funzione InSendMessage.**](/windows/win32/api/winuser/nf-winuser-insendmessage) Se questa funzione restituisce **TRUE,** la routine della finestra deve chiamare [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) prima di qualsiasi funzione che fa sì che il thread restituisca il controllo, come illustrato nell'esempio seguente.


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



È possibile inviare diversi messaggi ai controlli in una finestra di dialogo. Questi messaggi di controllo impostano l'aspetto, il comportamento e il contenuto dei controlli o recuperano informazioni sui controlli. Ad esempio, il messaggio [**CB \_ ADDSTRING**](../controls/cb-addstring.md) può aggiungere una stringa a una casella combinata e il messaggio [**BM \_ SETCHECK**](../controls/bm-setcheck.md) può impostare lo stato di controllo di una casella di controllo o di un pulsante di opzione.

Usare la [**funzione SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) per inviare un messaggio a un controllo, specificando l'identificatore del controllo e l'handle della finestra di dialogo che contiene il controllo. Nell'esempio seguente, tratto da una routine della finestra di dialogo, viene copiata una stringa dal controllo di modifica di una casella combinata nella relativa casella di riepilogo. Nell'esempio viene **utilizzato SendDlgItemMessage** per inviare un [**messaggio \_ CB ADDSTRING**](../controls/cb-addstring.md) alla casella combinata.


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



 

 
