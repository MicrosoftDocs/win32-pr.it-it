---
description: In questa sezione viene illustrato come eseguire attività associate all'interfaccia a più documenti.
ms.assetid: 024744d3-362f-4162-8d0a-d4dac61de808
title: Uso dell'interfaccia a più documenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e24aed7abc3640b441345520203c8a02e025e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317864"
---
# <a name="using-the-multiple-document-interface"></a>Uso dell'interfaccia a più documenti

In questa sezione viene illustrato come eseguire le attività seguenti:

-   [Registrazione delle classi figlio e della finestra cornice](#registering-child-and-frame-window-classes)
-   [Creazione di finestre cornice e figlio](#creating-frame-and-child-windows)
-   [Scrittura del ciclo di messaggi principale](#writing-the-main-message-loop)
-   [Scrittura della routine della finestra cornice](#writing-the-frame-window-procedure)
-   [Scrittura della routine della finestra figlio](#writing-the-child-window-procedure)
-   [Creazione di una finestra figlio](#creating-a-child-window)

Per illustrare queste attività, in questa sezione sono inclusi esempi di MULTIPAD, un'applicazione con interfaccia a documenti multipli (MDI) tipica.

## <a name="registering-child-and-frame-window-classes"></a>Registrazione delle classi figlio e della finestra cornice

Una tipica applicazione MDI deve registrare due classi finestra: una per la finestra cornice e una per le relative finestre figlio. Se un'applicazione supporta più di un tipo di documento (ad esempio, un foglio di calcolo e un grafico), deve registrare una classe della finestra per ogni tipo.

La struttura della classe per la finestra cornice è simile alla struttura della classe per la finestra principale in applicazioni non MDI. La struttura della classe per le finestre figlio MDI differisce leggermente dalla struttura per le finestre figlio in applicazioni non MDI come indicato di seguito:

-   La struttura della classe deve avere un'icona, in quanto l'utente può ridurre a icona una finestra figlio MDI come se fosse una normale finestra dell'applicazione.
-   Il nome del menu deve essere **null** perché una finestra figlio MDI non può avere un proprio menu.
-   La struttura della classe deve riservare ulteriore spazio nella struttura della finestra. Con questo spazio, l'applicazione può associare dati, ad esempio un nome di file, a una particolare finestra figlio.

Nell'esempio seguente viene illustrato come MultiPad registra le classi della finestra cornice e figlio.


```
BOOL WINAPI InitializeApplication() 
{ 
    WNDCLASS wc; 
 
    // Register the frame window class. 
 
    wc.style         = 0; 
    wc.lpfnWndProc   = (WNDPROC) MPFrameWndProc; 
    wc.cbClsExtra    = 0; 
    wc.cbWndExtra    = 0; 
    wc.hInstance     = hInst; 
    wc.hIcon         = LoadIcon(hInst, IDMULTIPAD); 
    wc.hCursor       = LoadCursor((HANDLE) NULL, IDC_ARROW); 
    wc.hbrBackground = (HBRUSH) (COLOR_APPWORKSPACE + 1); 
    wc.lpszMenuName  = IDMULTIPAD; 
    wc.lpszClassName = szFrame; 
 
    if (!RegisterClass (&wc) ) 
        return FALSE; 
 
    // Register the MDI child window class. 
 
    wc.lpfnWndProc   = (WNDPROC) MPMDIChildWndProc; 
    wc.hIcon         = LoadIcon(hInst, IDNOTE); 
    wc.lpszMenuName  = (LPCTSTR) NULL; 
    wc.cbWndExtra    = CBWNDEXTRA; 
    wc.lpszClassName = szChild; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    return TRUE; 
} 
```



## <a name="creating-frame-and-child-windows"></a>Creazione di finestre cornice e figlio

Una volta registrate le classi della finestra, un'applicazione MDI può crearne le finestre. Innanzitutto, viene creata la finestra cornice usando la funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Dopo aver creato la finestra cornice, l'applicazione crea la finestra del client usando di nuovo **CreateWindow** o **CreateWindowEx**. L'applicazione deve specificare MDICLIENT come nome della classe della finestra client; **MdiClient** è una classe di finestra pre-registrata definita dal sistema. Il parametro *lpvParam* di **CreateWindow** o **CreateWindowEx** deve puntare a una struttura [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) . Questa struttura contiene i membri descritti nella tabella seguente:



| Membro           | Descrizione                                                                                                                                                                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hWindowMenu**  | Handle per il menu finestra utilizzato per il controllo delle finestre figlio MDI. Quando vengono create le finestre figlio, l'applicazione aggiunge i titoli al menu finestra come voci di menu. L'utente può quindi attivare una finestra figlio facendo clic sul relativo titolo nel menu finestra.                                                               |
| **idFirstChild** | Specifica l'identificatore della prima finestra figlio MDI. Alla prima finestra figlio MDI creata viene assegnato questo identificatore. Ulteriori finestre vengono create con identificatori di finestra incrementati. Quando una finestra figlio viene distrutta, il sistema riassegna immediatamente gli identificatori della finestra per mantenendone l'intervallo contiguo. |



 

Quando il titolo di una finestra figlio viene aggiunto al menu finestra, il sistema assegna un identificatore alla finestra figlio. Quando l'utente fa clic sul titolo di una finestra figlio, la finestra cornice riceve un messaggio di [**\_ comando WM**](../menurc/wm-command.md) con l'identificatore nel parametro *wParam* . È necessario specificare un valore per il membro **idFirstChild** che non sia in conflitto con gli identificatori di voce di menu nel menu della finestra cornice.

La routine della finestra cornice di MULTIPAD crea la finestra client MDI durante l'elaborazione del messaggio [**WM \_ create**](wm-create.md) . Nell'esempio seguente viene illustrato come viene creata la finestra del client.


```
case WM_CREATE: 
    { 
        CLIENTCREATESTRUCT ccs; 
 
        // Retrieve the handle to the window menu and assign the 
        // first child window identifier. 
 
        ccs.hWindowMenu = GetSubMenu(GetMenu(hwnd), WINDOWMENU); 
        ccs.idFirstChild = IDM_WINDOWCHILD; 
 
        // Create the MDI client window. 
 
        hwndMDIClient = CreateWindow( "MDICLIENT", (LPCTSTR) NULL, 
            WS_CHILD | WS_CLIPCHILDREN | WS_VSCROLL | WS_HSCROLL, 
            0, 0, 0, 0, hwnd, (HMENU) 0xCAC, hInst, (LPSTR) &ccs); 
 
        ShowWindow(hwndMDIClient, SW_SHOW); 
    } 
    break; 
```



I titoli delle finestre figlio vengono aggiunti nella parte inferiore del menu finestra. Se l'applicazione aggiunge stringhe al menu della finestra usando la funzione [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) , queste stringhe possono essere sovrascritte dai titoli delle finestre figlio quando il menu finestra viene ridisegnato (ogni volta che viene creata o distrutta una finestra figlio). Un'applicazione MDI che aggiunge stringhe al menu della finestra deve usare la funzione [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) e verificare che i titoli delle finestre figlio non abbiano sovrascritto queste nuove stringhe.

Utilizzare lo stile **WS \_ CLIPCHILDREN** per creare la finestra client MDI per evitare che la finestra venga disegnata sulle finestre figlio.

## <a name="writing-the-main-message-loop"></a>Scrittura del ciclo di messaggi principale

Il ciclo di messaggi principale di un'applicazione MDI è simile a quello di un tasto di scelta rapida per la gestione di applicazioni non MDI. La differenza è che il ciclo di messaggi MDI chiama la funzione [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) prima di verificare la presenza di tasti di scelta rapida definiti dall'applicazione o prima di inviare il messaggio.

Nell'esempio seguente viene illustrato il ciclo di messaggi di un'applicazione MDI tipica. Si noti che [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) può restituire-1 se si verifica un errore.


```
MSG msg;
BOOL bRet;

while ((bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else 
    { 
        if (!TranslateMDISysAccel(hwndMDIClient, &msg) && 
                !TranslateAccelerator(hwndFrame, hAccel, &msg))
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



La funzione [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) converte i messaggi di [**WM \_ KeyDown**](../inputdev/wm-keydown.md) in messaggi [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) e li invia alla finestra figlio MDI attiva. Se il messaggio non è un messaggio di accelerazione MDI, la funzione restituisce **false**, nel qual caso l'applicazione usa la funzione [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) per determinare se è stato premuto uno dei tasti di scelta rapida definiti dall'applicazione. In caso contrario, il ciclo invia il messaggio alla procedura appropriata della finestra.

## <a name="writing-the-frame-window-procedure"></a>Scrittura della routine della finestra cornice

La routine della finestra per una finestra cornice MDI è simile a quella della finestra principale di un'applicazione non MDI. La differenza è che una routine della finestra cornice passa tutti i messaggi che non gestisce alla funzione [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) anziché alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Inoltre, la routine della finestra cornice deve passare alcuni messaggi gestiti, inclusi quelli elencati nella tabella seguente.



| Message                                  | Risposta                                                                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_comando WM**](../menurc/wm-command.md)     | Attiva la finestra figlio MDI selezionata dall'utente. Questo messaggio viene inviato quando l'utente sceglie una finestra figlio MDI dal menu finestra della finestra cornice MDI. L'identificatore di finestra associato a questo messaggio identifica la finestra figlio MDI da attivare. |
| [**\_MENUCHAR WM**](../menurc/wm-menuchar.md)   | Apre il menu finestra della finestra figlio MDI attiva quando l'utente preme la combinazione di tasti ALT + – (meno).                                                                                                                                                      |
| [**\_stato attivo WM**](../inputdev/wm-setfocus.md) | Passa lo stato attivo alla finestra client MDI, che a sua volta la passa alla finestra figlio MDI attiva.                                                                                                                                                         |
| [**\_dimensioni WM**](wm-size.md)              | Ridimensiona la finestra del client MDI per adattarla all'area client della nuova finestra cornice. Se la routine della finestra cornice ridimensiona la finestra del client MDI a una dimensione diversa, non dovrebbe passare il messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .                   |



 

La routine della finestra cornice in MultiPad è denominata MPFrameWndProc. La gestione di altri messaggi da parte di MPFrameWndProc è simile a quella delle applicazioni non MDI. [**WM \_**](../menurc/wm-command.md) I messaggi di comando in MultiPad vengono gestiti dalla funzione CommandHandler definita localmente. Per i messaggi di comando MULTIPAD non gestisce, CommandHandler chiama la funzione [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) . Se MULTIPAD non usa **DefFrameProc** per impostazione predefinita, l'utente non può attivare una finestra figlio dal menu finestra perché il messaggio **di \_ comando WM** inviato facendo clic sulla voce di menu della finestra andrebbe perso.

## <a name="writing-the-child-window-procedure"></a>Scrittura della routine della finestra figlio

Analogamente alla routine della finestra cornice, una routine della finestra figlio MDI utilizza una funzione speciale per elaborare i messaggi per impostazione predefinita. Tutti i messaggi non gestiti dalla routine della finestra figlio devono essere passati alla funzione [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) anziché alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Inoltre, alcuni messaggi di gestione delle finestre devono essere passati a **DefMDIChildProc**, anche se l'applicazione gestisce il messaggio, in modo che MDI funzioni correttamente. Di seguito sono riportati i messaggi che l'applicazione deve passare a **DefMDIChildProc**.



| Message                                       | Risposta                                                                                                                                                                                                                                                  |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CHILDACTIVATE WM**](wm-childactivate.md) | Esegue l'elaborazione dell'attivazione quando le finestre figlio MDI vengono ridimensionate, spostate o visualizzate. Questo messaggio deve essere passato.                                                                                                                                        |
| [**\_GETMINMAXINFO WM**](wm-getminmaxinfo.md) | Calcola la dimensione di una finestra figlio MDI ingrandita, in base alle dimensioni correnti della finestra del client MDI.                                                                                                                                                  |
| [**\_MENUCHAR WM**](../menurc/wm-menuchar.md)        | Passa il messaggio alla finestra cornice MDI.                                                                                                                                                                                                               |
| [**\_spostamento WM**](wm-move.md)                   | Ricalcola le barre di scorrimento del client MDI, se presenti.                                                                                                                                                                                                 |
| [**\_stato attivo WM**](../inputdev/wm-setfocus.md)      | Attiva la finestra figlio, se non è la finestra figlio MDI attiva.                                                                                                                                                                                     |
| [**\_dimensioni WM**](wm-size.md)                   | Esegue operazioni necessarie per modificare le dimensioni di una finestra, in particolare per massimizzare o ripristinare una finestra figlio MDI. Il mancato passaggio di questo messaggio alla funzione [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) produce risultati estremamente indesiderati. |
| [**\_SYSCOMMAND WM**](../menurc/wm-syscommand.md)    | Comandi di menu della finestra handle (noto in precedenza come sistema): **SC \_ NEXTWINDOW**, **SC \_ PREVWINDOW**, **SC \_ Move**, **SC \_ size** e **SC \_ ingrandire**.                                                                                                        |



 

## <a name="creating-a-child-window"></a>Creazione di una finestra figlio

Per creare una finestra figlio MDI, un'applicazione può chiamare la funzione [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) o inviare un messaggio [**WM \_ MDICREATE**](wm-mdicreate.md) alla finestra client MDI. L'applicazione può utilizzare la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) con lo stile **WS \_ ex \_ MDIChild** per creare finestre figlio MDI. Un'applicazione MDI a thread singolo può usare entrambi i metodi per creare una finestra figlio. Un thread in un'applicazione MDI multithread deve usare la funzione **CreateMDIWindow** o **CreateWindowEx** per creare una finestra figlio in un thread diverso.

Il parametro *lParam* di un messaggio [**WM \_ MDICREATE**](wm-mdicreate.md) è un puntatore molto lungo a una struttura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) . La struttura include quattro membri della dimensione: **x** e **y**, che indicano le posizioni orizzontali e verticali della finestra e **CX** e **CY**, che indicano gli extent orizzontali e verticali della finestra. Uno di questi membri può essere assegnato in modo esplicito dall'applicazione oppure può essere impostato su **CW \_ usedefault (**, nel qual caso il sistema seleziona una posizione, una dimensione o entrambi, in base a un algoritmo a cascata. In ogni caso, è necessario inizializzare tutti e quattro i membri. MultiPad USA **\_ usedefault (CW** per tutte le dimensioni.

L'ultimo membro della struttura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) è il membro dello **stile** , che può contenere bit di stile per la finestra. Per creare una finestra figlio MDI che può avere qualsiasi combinazione di stili di finestra, specificare lo stile della finestra **\_ ALLCHILDSTYLES di MDI** . Quando questo stile non viene specificato, una finestra figlio MDI dispone degli **stili \_ WS minimizzate**, **WS \_ ingrandite**, **WS \_ HSCROLL** e **WS \_ VSCROLL** come impostazioni predefinite.

MultiPad crea le finestre figlio MDI usando la relativa funzione AddFile definita localmente (che si trova nel file di origine MPFILE. C). La funzione AddFile imposta il titolo della finestra figlio assegnando il membro **szTitle** della struttura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) della finestra al nome del file da modificare o a "Untitled". Il membro **szClass** è impostato sul nome della classe della finestra figlio MDI registrata nella funzione InitializeApplication di MULTIPAD. Il membro **hOwner** è impostato sull'handle di istanza dell'applicazione.

Nell'esempio seguente viene illustrata la funzione AddFile in MultiPad.


```
HWND APIENTRY AddFile(pName) 
TCHAR * pName; 
{ 
    HWND hwnd; 
    TCHAR sz[160]; 
    MDICREATESTRUCT mcs; 
 
    if (!pName) 
    { 
 
        // If the pName parameter is NULL, load the "Untitled" 
        // string from the STRINGTABLE resource and set the szTitle 
        // member of MDICREATESTRUCT. 
 
        LoadString(hInst, IDS_UNTITLED, sz, sizeof(sz)/sizeof(TCHAR)); 
        mcs.szTitle = (LPCTSTR) sz; 
    } 
    else 
 
        // Title the window with the full path and filename, 
        // obtained by calling the OpenFile function with the 
        // OF_PARSE flag, which is called before AddFile(). 
 
        mcs.szTitle = of.szPathName; 
 
    mcs.szClass = szChild; 
    mcs.hOwner  = hInst; 
 
    // Use the default size for the child window. 
 
    mcs.x = mcs.cx = CW_USEDEFAULT; 
    mcs.y = mcs.cy = CW_USEDEFAULT; 
 
    // Give the child window the default style. The styleDefault 
    // variable is defined in MULTIPAD.C. 
 
    mcs.style = styleDefault; 
 
    // Tell the MDI client window to create the child window. 
 
    hwnd = (HWND) SendMessage (hwndMDIClient, WM_MDICREATE, 0, 
        (LONG) (LPMDICREATESTRUCT) &mcs); 
 
    // If the file is found, read its contents into the child 
    // window's client area. 
 
    if (pName) 
    { 
        if (!LoadFile(hwnd, pName)) 
        { 
 
            // Cannot load the file; close the window. 
 
            SendMessage(hwndMDIClient, WM_MDIDESTROY, 
                (DWORD) hwnd, 0L); 
        } 
    } 
    return hwnd; 
} 
```



Il puntatore passato al parametro *lParam* del messaggio [**WM \_ MDICREATE**](wm-mdicreate.md) viene passato alla funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) e viene visualizzato come primo membro nella struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) , passato nel messaggio [**WM \_ create**](wm-create.md) . In MultiPad la finestra figlio si inizializza durante l'elaborazione dei messaggi di **WM \_** , inizializzando le variabili del documento nei dati aggiuntivi e creando la finestra figlio del controllo di modifica.

 

 
