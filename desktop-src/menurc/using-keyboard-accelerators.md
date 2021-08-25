---
title: Uso dei tasti di scelta rapida
description: Questa sezione illustra le attività associate ai tasti di scelta rapida.
ms.assetid: 11c42d69-7454-43e6-9f44-c14a283814ce
keywords:
- input utente, tasti di scelta rapida
- acquisizione di input dell'utente, tasti di scelta rapida
- tasti di scelta rapida
- Acceleratori
- tabelle dei tasti di scelta rapida
- risorse accelerator-table
- Funzione di conversione dei tasti di scelta rapida
- WM_COMMAND messaggio
- WM_SYS messaggio COMMAND
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecbb16c92b986cbe73aababc7edc24518cf59ce5009322e3a006bac827427c45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886566"
---
# <a name="using-keyboard-accelerators"></a>Uso dei tasti di scelta rapida

Questa sezione illustra le attività associate ai tasti di scelta rapida.

-   [Uso di una risorsa tabella dei tasti di scelta rapida](#using-an-accelerator-table-resource)
    -   [Creazione della risorsa tabella dei tasti di scelta rapida](#creating-the-accelerator-table-resource)
    -   [Caricamento della risorsa tabella dei tasti di scelta rapida](#loading-the-accelerator-table-resource)
    -   [Chiamata della funzione Translate Accelerator](#calling-the-translate-accelerator-function)
    -   [Elaborazione di messaggi WM \_ COMMAND](/windows)
    -   [Eliminazione della risorsa tabella dei tasti di scelta rapida](#destroying-the-accelerator-table-resource)
    -   [Creazione di tasti di scelta rapida per gli attributi dei tipi di carattere](#creating-accelerators-for-font-attributes)
-   [Uso di una tabella dei tasti di scelta rapida creata in fase di esecuzione](#using-an-accelerator-table-created-at-run-time)
    -   [Creazione di una Run-Time di tasti di scelta rapida](#creating-a-run-time-accelerator-table)
    -   [Acceleratori di elaborazione](#processing-accelerators)
    -   [Eliminazione di una tabella Run-Time tasti di scelta rapida](#destroying-a-run-time-accelerator-table)
    -   [Creazione di acceleratori modificabili dall'utente](#creating-user-editable-accelerators)

## <a name="using-an-accelerator-table-resource"></a>Uso di una risorsa tabella dei tasti di scelta rapida

Il modo più comune per aggiungere il supporto dell'acceleratore a un'applicazione è includere una risorsa accelerator-table con il file eseguibile dell'applicazione e quindi caricare la risorsa in fase di esecuzione.

In questa sezione vengono trattati gli argomenti seguenti.

-   [Creazione della risorsa tabella dei tasti di scelta rapida](#creating-the-accelerator-table-resource)
-   [Caricamento della risorsa tabella dei tasti di scelta rapida](#loading-the-accelerator-table-resource)
-   [Chiamata della funzione Translate Accelerator](#calling-the-translate-accelerator-function)
-   [Elaborazione di messaggi WM \_ COMMAND](/windows)
-   [Eliminazione della risorsa tabella dei tasti di scelta rapida](#destroying-the-accelerator-table-resource)
-   [Creazione di tasti di scelta rapida per gli attributi dei tipi di carattere](#creating-accelerators-for-font-attributes)

### <a name="creating-the-accelerator-table-resource"></a>Creazione della risorsa tabella dei tasti di scelta rapida

È possibile creare una risorsa accelerator-table usando [l'istruzione ACCELERATORS](./accelerators-resource.md) nel file di definizione delle risorse dell'applicazione. È necessario assegnare un nome o un identificatore di risorsa alla tabella dei tasti di scelta rapida, preferibilmente a differenza di qualsiasi altra risorsa. Il sistema usa questo identificatore per caricare la risorsa in fase di esecuzione.

Ogni tasto di scelta rapida definito richiede una voce separata nella tabella dei tasti di scelta rapida. In ogni voce si definisce la sequenza di tasti (un codice carattere ASCII o un codice tasto virtuale) che genera l'acceleratore e l'identificatore del tasto di scelta rapida. È inoltre necessario specificare se la sequenza di tasti deve essere utilizzata in combinazione con i tasti ALT, MAIUSC o CTRL. Per altre informazioni sui tasti virtuali, vedere [Input da tastiera.](/windows/desktop/inputdev/keyboard-input)

Una sequenza di tasti ASCII viene specificata racchiudendo il carattere ASCII tra virgolette doppie o usando il valore intero del carattere in combinazione con il flag ASCII. Negli esempi seguenti viene illustrato come definire tasti di scelta rapida ASCII.

``` syntax
"A", ID_ACCEL1         ; SHIFT+A 
65,  ID_ACCEL2, ASCII  ; SHIFT+A 
```

Una sequenza di tasti del codice virtuale viene specificata in modo diverso a seconda che la sequenza di tasti sia un tasto alfanumerico o un tasto non alfanumerico. Per una chiave alfanumerica, la lettera o il numero della chiave, racchiuso tra virgolette doppie, viene combinato con il flag **VIRTKEY.** Per una chiave non alfanumerica, il codice della chiave virtuale per la chiave specifica viene combinato con il flag **VIRTKEY.** Gli esempi seguenti illustrano come definire gli acceleratori di codice dei tasti di scelta rapida virtuali.

``` syntax
"a",       ID_ACCEL3, VIRTKEY   ; A (caps-lock on) or a 
VK_INSERT, ID_ACCEL4, VIRTKEY   ; INSERT key 
```

L'esempio seguente illustra una risorsa accelerator-table che definisce i tasti di scelta rapida per le operazioni sui file. Il nome della risorsa è *FileAccel.*

``` syntax
FileAccel ACCELERATORS 
BEGIN 
    VK_F12, IDM_OPEN, CONTROL, VIRTKEY  ; CTRL+F12 
    VK_F4,  IDM_CLOSE, ALT, VIRTKEY     ; ALT+F4 
    VK_F12, IDM_SAVE, SHIFT, VIRTKEY    ; SHIFT+F12 
    VK_F12, IDM_SAVEAS, VIRTKEY         ; F12 
END 
```

Se si vuole che l'utente premuti i tasti ALT, MAIUSC o CTRL in combinazione con la combinazione di tasti di scelta rapida, specificare i flag ALT, MAIUSC e CTRL nella definizione del tasto di scelta rapida. Di seguito sono riportati alcuni esempi.

``` syntax
"B",   ID_ACCEL5, ALT                   ; ALT_SHIFT+B 
"I",   ID_ACCEL6, CONTROL, VIRTKEY      ; CTRL+I 
VK_F5, ID_ACCEL7, CONTROL, ALT, VIRTKEY ; CTRL+ALT+F5 
```

Per impostazione predefinita, quando un tasto di scelta rapida corrisponde a una voce di menu, il sistema evidenzia la voce di menu. È possibile usare il flag **NOINVERT** per impedire l'evidenziazione per un singolo acceleratore. L'esempio seguente illustra come usare il flag **NOINVERT:**

``` syntax
VK_DELETE, ID_ACCEL8, VIRTKEY, SHIFT, NOINVERT  ; SHIFT+DELETE 
```

Per definire i tasti di scelta rapida che corrispondono alle voci di menu nell'applicazione, includere i tasti di scelta rapida nel testo delle voci di menu. L'esempio seguente illustra come includere i tasti di scelta rapida nel testo delle voci di menu in un file di definizione delle risorse.

``` syntax
FilePopup MENU 
BEGIN 
    POPUP   "&File" 
    BEGIN 
        MENUITEM    "&New..",           IDM_NEW 
        MENUITEM    "&Open\tCtrl+F12",  IDM_OPEN 
        MENUITEM    "&Close\tAlt+F4"    IDM_CLOSE 
        MENUITEM    "&Save\tShift+F12", IDM_SAVE 
        MENUITEM    "Save &As...\tF12", IDM_SAVEAS 
    END 
END 
```

### <a name="loading-the-accelerator-table-resource"></a>Caricamento della risorsa tabella dei tasti di scelta rapida

Un'applicazione carica una risorsa accelerator-table chiamando la funzione [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) e specificando l'handle di istanza per l'applicazione il cui file eseguibile contiene la risorsa e il nome o l'identificatore della risorsa. **LoadAccelerators carica** la tabella dei tasti di scelta rapida specificata in memoria e restituisce l'handle alla tabella dei tasti di scelta rapida.

Un'applicazione può caricare una risorsa accelerator-table in qualsiasi momento. In genere, un'applicazione a thread singolo carica la tabella dei tasti di scelta rapida prima di entrare nel ciclo di messaggi principale. Un'applicazione che usa più thread carica in genere la risorsa della tabella di tasti di scelta rapida per un thread prima di entrare nel ciclo di messaggi per il thread. Un'applicazione o un thread può anche usare più tabelle dei tasti di scelta rapida, ognuna associata a una determinata finestra nell'applicazione. Un'applicazione di questo tipo carica la tabella dei tasti di scelta rapida per la finestra ogni volta che l'utente attiva la finestra. Per altre informazioni sui thread, vedere [Processi e thread.](/windows/desktop/ProcThread/processes-and-threads)

### <a name="calling-the-translate-accelerator-function"></a>Chiamata della funzione Translate Accelerator

Per elaborare gli acceleratori, il ciclo di messaggi di un'applicazione (o del thread) deve contenere una chiamata alla [**funzione TranslateAccelerator.**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) **TranslateAccelerator** confronta le sequenze di tasti con una tabella dei tasti di scelta rapida e, se trova una corrispondenza, converte le sequenze di tasti in un messaggio [**WM \_ COMMAND**](wm-command.md) (o [**WM \_ SYSCOMMAND).**](wm-syscommand.md) La funzione invia quindi il messaggio a una routine della finestra. I parametri della funzione **TranslateAccelerator** includono l'handle per la finestra che deve ricevere i messaggi **WM \_ COMMAND,** l'handle alla tabella dei tasti di scelta rapida usata per convertire i tasti di scelta rapida e un puntatore a una struttura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) contenente un messaggio dalla coda. Nell'esempio seguente viene illustrato come chiamare **TranslateAccelerator dall'interno** di un ciclo di messaggi.


```
MSG msg;
BOOL bRet;

while ( (bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1) 
    {
        // handle the error and possibly exit
    }
    else
    { 
        // Check for accelerator keystrokes. 
     
        if (!TranslateAccelerator( 
                hwndMain,      // handle to receiving window 
                haccel,        // handle to active accelerator table 
                &msg))         // message data 
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



### <a name="processing-wm_command-messages"></a>Elaborazione di messaggi WM \_ COMMAND

Quando si usa un tasto di scelta rapida, la finestra specificata nella funzione [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) riceve un messaggio [**WM \_ COMMAND**](wm-command.md) o [**WM \_ SYSCOMMAND.**](wm-syscommand.md) La parola più bassa del parametro *wParam* contiene l'identificatore del tasto di scelta rapida. La routine della finestra esamina l'identificatore per determinare l'origine del **messaggio WM \_ COMMAND** ed elabora il messaggio di conseguenza.

In genere, se un tasto di scelta rapida corrisponde a una voce di menu nell'applicazione, all'acceleratore e alla voce di menu viene assegnato lo stesso identificatore. Se è necessario sapere se un messaggio [**WM \_ COMMAND**](wm-command.md) è stato generato da un tasto di scelta rapida o da una voce di menu, è possibile esaminare la parola più alta del *parametro wParam.* Se il messaggio è stato generato da un acceleratore, la parola più importante è 1. Se il messaggio è stato generato da una voce di menu, la parola più importante è 0.

### <a name="destroying-the-accelerator-table-resource"></a>Eliminazione della risorsa tabella dei tasti di scelta rapida

Il sistema elimina automaticamente le risorse della tabella dei tasti di scelta rapida caricate dalla funzione [**LoadAccelerators,**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) rimuovendo la risorsa dalla memoria dopo la chiusura dell'applicazione.

### <a name="creating-accelerators-for-font-attributes"></a>Creazione di tasti di scelta rapida per gli attributi dei tipi di carattere

L'esempio in questa sezione illustra come eseguire le attività seguenti:

-   Creare una risorsa accelerator-table.
-   Caricare la tabella dei tasti di scelta rapida in fase di esecuzione.
-   Convertire i tasti di scelta rapida in un ciclo di messaggi.
-   Elaborare [**i messaggi WM \_ COMMAND**](wm-command.md) generati dagli acceleratori.

Queste attività vengono illustrate nel contesto di un'applicazione che include un menu **Carattere** e i tasti di scelta rapida corrispondenti che consentono all'utente di selezionare gli attributi del tipo di carattere corrente.

La parte seguente di un file di definizione delle risorse definisce il menu **Carattere e** la tabella dei tasti di scelta rapida associata. Si noti che le voci di menu mostrano le sequenze di tasti di scelta rapida e che ogni tasto di scelta rapida ha lo stesso identificatore della voce di menu associata.


```
#include <windows.h> 
#include "acc.h" 
 
MainMenu MENU 
{ 
    POPUP   "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```



Le sezioni seguenti del file di origine dell'applicazione illustrano come implementare gli acceleratori.


```
HWND hwndMain;      // handle to main window 
HANDLE hinstAcc;    // handle to application instance 
int WINAPI WinMain(HINSTANCE hinst, HINSTANCE hinstPrev, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg;            // application messages 
    BOOL bRet;          // for return value of GetMessage
    HACCEL haccel;      // handle to accelerator table 
 
    // Perform the initialization procedure. 
 
    // Create a main window for this application instance. 
 
    hwndMain = CreateWindowEx(0L, "MainWindowClass", 
        "Sample Application", WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, 
        hinst, NULL ); 
 
    // If a window cannot be created, return "failure." 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Make the window visible and update its client area. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Load the accelerator table. 
 
    haccel = LoadAccelerators(hinstAcc, "FontAccel"); 
    if (haccel == NULL) 
        HandleAccelErr(ERR_LOADING);     // application defined 
 
    // Get and dispatch messages until a WM_QUIT message is 
    // received. 
 
    while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        { 
            // Check for accelerator keystrokes. 
     
            if (!TranslateAccelerator( 
                    hwndMain,  // handle to receiving window 
                    haccel,    // handle to active accelerator table 
                    &msg))         // message data 
            {
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
        } 
    }
    return msg.wParam; 
} 
 
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    BYTE fbFontAttrib;        // array of font-attribute flags 
    static HMENU hmenu;       // handle to main menu 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Add a check mark to the Regular menu item to 
            // indicate that it is the default. 
 
            hmenu = GetMenu(hwndMain); 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the accelerator and menu commands. 
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // GetFontAttributes is an application-defined 
                    // function that sets the menu-item check marks 
                    // and returns the user-selected font attributes. 
 
                    fbFontAttrib = GetFontAttributes( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // SetFontAttributes is an application-defined 
                    // function that creates a font with the 
                    // user-specified attributes the font with 
                    // the main window's device context. 
 
                    SetFontAttributes(fbFontAttrib); 
                    break; 
 
                default: 
                    break; 
            } 
            break; 
 
            // Process other messages. 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="using-an-accelerator-table-created-at-run-time"></a>Uso di una tabella dei tasti di scelta rapida creata in fase di esecuzione

Questo argomento illustra come usare le tabelle dei tasti di scelta rapida create in fase di esecuzione.

-   [Creazione di una Run-Time di tasti di scelta rapida](#creating-a-run-time-accelerator-table)
-   [Acceleratori di elaborazione](#processing-accelerators)
-   [Eliminazione di una tabella Run-Time tasti di scelta rapida](#destroying-a-run-time-accelerator-table)
-   [Creazione di acceleratori modificabili dall'utente](#creating-user-editable-accelerators)

### <a name="creating-a-run-time-accelerator-table"></a>Creazione di una Run-Time di tasti di scelta rapida

Il primo passaggio per la creazione di una tabella dei tasti di scelta rapida in fase di esecuzione consiste nel riempire una matrice di [**strutture ACCEL.**](/windows/win32/api/winuser/ns-winuser-accel) Ogni struttura nella matrice definisce un acceleratore nella tabella. La definizione di un acceleratore include i flag, la chiave e il relativo identificatore. La **struttura ACCEL** ha il formato seguente.

``` syntax
typedef struct tagACCEL { // accl 
    BYTE   fVirt; 
    WORD   key; 
    WORD   cmd; 
} ACCEL;
```

È possibile definire la sequenza di tasti di scelta rapida specificando un  codice carattere ASCII o un codice tasto virtuale nel membro chiave della [**struttura ACCEL.**](/windows/win32/api/winuser/ns-winuser-accel) Se si specifica un codice di chiave virtuale, è prima necessario includere il flag **FVIRTKEY** nel **membro fVirt.** In caso contrario, il sistema interpreta il codice come codice di caratteri ASCII. È possibile includere il flag **FCONTROL,** **FALT** o **FSHIFT** o tutti e tre per combinare ctrl, ALT o MAIUSC con la sequenza di tasti.

Per creare la tabella dei tasti di scelta rapida, passare un puntatore alla matrice di [**strutture ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) alla [**funzione CreateAcceleratorTable.**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) **CreateAcceleratorTable crea** la tabella dei tasti di scelta rapida e restituisce l'handle alla tabella.

### <a name="processing-accelerators"></a>Acceleratori di elaborazione

Il processo di caricamento e chiamata degli acceleratori forniti da una tabella dei tasti di scelta rapida creata in fase di esecuzione è lo stesso dell'elaborazione di quelli forniti da una risorsa della tabella dei tasti di scelta rapida. Per altre informazioni, vedere [Caricamento della risorsa tabella dei tasti di scelta rapida](#loading-the-accelerator-table-resource) tramite [l'elaborazione di messaggi WM \_ COMMAND.](/windows)

### <a name="destroying-a-run-time-accelerator-table"></a>Eliminazione di una tabella Run-Time acceleratore

Il sistema elimina automaticamente le tabelle dei tasti di scelta rapida create in fase di esecuzione, rimuovendo le risorse dalla memoria dopo la chiusura dell'applicazione. È possibile eliminare una tabella dei tasti di scelta rapida e rimuoverla dalla memoria in precedenza passando l'handle della tabella alla [**funzione DestroyAcceleratorTable.**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable)

### <a name="creating-user-editable-accelerators"></a>Creazione di acceleratori modificabili dall'utente

Questo esempio illustra come costruire una finestra di dialogo che consente all'utente di modificare il tasto di scelta rapida associato a una voce di menu. La finestra di dialogo è costituita da una casella combinata contenente voci di menu, da una casella combinata contenente i nomi dei tasti e da caselle di controllo per la selezione dei tasti CTRL, ALT e MAIUSC. Nella figura seguente viene illustrata la finestra di dialogo .

![finestra di dialogo con caselle combinate e caselle di controllo](images/useredit.gif)

Nell'esempio seguente viene illustrato come viene definita la finestra di dialogo nel file di definizione delle risorse.

``` syntax
EdAccelBox DIALOG 5, 17, 193, 114 
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Edit Accelerators" 
BEGIN 
    COMBOBOX        IDD_MENUITEMS, 10, 22, 52, 53, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    CONTROL         "Control", IDD_CNTRL, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 35, 40, 10 
    CONTROL         "Alt", IDD_ALT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 48, 40, 10 
    CONTROL         "Shift", IDD_SHIFT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 61, 40, 10 
    COMBOBOX        IDD_KEYSTROKES, 124, 22, 58, 58, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    PUSHBUTTON      "Ok", IDOK, 43, 92, 40, 14 
    PUSHBUTTON      "Cancel", IDCANCEL, 103, 92, 40, 14 
    LTEXT           "Select Item:", 101, 10, 12, 43, 8 
    LTEXT           "Select Keystroke:", 102, 123, 12, 60, 8 
END
```

La barra dei menu dell'applicazione contiene un sottomenu **Carattere** i cui elementi hanno tasti di scelta rapida associati.

``` syntax
MainMenu MENU 
{ 
    POPUP "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```

I valori delle voci di menu per il modello di menu sono costanti definite come indicato di seguito nel file di intestazione dell'applicazione.

``` syntax
#define IDM_REGULAR    1100
#define IDM_BOLD       1200
#define IDM_ITALIC     1300
#define IDM_ULINE      1400
```

La finestra di dialogo usa una matrice di strutture VKEY definite dall'applicazione, ognuna delle quali contiene una stringa di tasti di scelta rapida e una stringa di testo dell'acceleratore. Quando viene creata la finestra di dialogo, analizza la matrice e aggiunge ogni stringa di sequenza di tasti alla casella combinata **Seleziona sequenza** di tasti. Quando l'utente fa clic sul **pulsante OK,** la finestra di dialogo cerca la stringa di sequenza di tasti selezionata e recupera la stringa di tasti di scelta rapida corrispondente. La finestra di dialogo aggiunge la stringa accelerator-text al testo della voce di menu selezionata dall'utente. L'esempio seguente illustra la matrice di strutture VKEY:


```
// VKey Lookup Support 
 
#define MAXKEYS 25 
 
typedef struct _VKEYS { 
    char *pKeyName; 
    char *pKeyString; 
} VKEYS; 
 
VKEYS vkeys[MAXKEYS] = { 
    "BkSp",     "Back Space", 
    "PgUp",     "Page Up", 
    "PgDn",     "Page Down", 
    "End",      "End", 
    "Home",     "Home", 
    "Lft",      "Left", 
    "Up",       "Up", 
    "Rgt",      "Right", 
    "Dn",       "Down", 
    "Ins",      "Insert", 
    "Del",      "Delete", 
    "Mult",     "Multiply", 
    "Add",      "Add", 
    "Sub",      "Subtract", 
    "DecPt",    "Decimal Point", 
    "Div",      "Divide", 
    "F2",       "F2", 
    "F3",       "F3", 
    "F5",       "F5", 
    "F6",       "F6", 
    "F7",       "F7", 
    "F8",       "F8", 
    "F9",       "F9", 
    "F11",      "F11", 
    "F12",      "F12" 
};
```



La procedura di inizializzazione della finestra di dialogo riempie **le caselle** combinate Seleziona elemento e **Seleziona sequenza di** tasti. Dopo che l'utente ha selezionato una voce di menu e un acceleratore associato, la finestra di dialogo esamina i controlli nella finestra di dialogo per ottenere la selezione dell'utente, aggiorna il testo della voce di menu e quindi crea una nuova tabella dei tasti di scelta rapida contenente il nuovo acceleratore definito dall'utente. Nell'esempio seguente viene illustrata la procedura della finestra di dialogo. Si noti che è necessario inizializzare nella routine della finestra.


```
// Global variables 
 
HWND hwndMain;      // handle to main window 
HACCEL haccel;      // handle to accelerator table 
 
// Dialog-box procedure 
 
BOOL CALLBACK EdAccelProc(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    int nCurSel;            // index of list box item 
    UINT idItem;            // menu-item identifier 
    UINT uItemPos;          // menu-item position 
    UINT i, j = 0;          // loop counters 
    static UINT cItems;     // count of items in menu 
    char szTemp[32];        // temporary buffer 
    char szAccelText[32];   // buffer for accelerator text 
    char szKeyStroke[16];   // buffer for keystroke text 
    static char szItem[32]; // buffer for menu-item text 
    HWND hwndCtl;           // handle to control window 
    static HMENU hmenu;     // handle to "Character" menu 
    PCHAR pch, pch2;        // pointers for string copying 
    WORD wVKCode;           // accelerator virtual-key code 
    BYTE fAccelFlags;       // fVirt flags for ACCEL structure 
    LPACCEL lpaccelNew;     // pointer to new accelerator table 
    HACCEL haccelOld;       // handle to old accelerator table 
    int cAccelerators;      // number of accelerators in table 
    static BOOL fItemSelected = FALSE; // item selection flag 
    static BOOL fKeySelected = FALSE;  // key selection flag 
    HRESULT hr;
    INT numTCHAR;           // TCHARs in listbox text
 
    switch (uMsg) 
    { 
        case WM_INITDIALOG: 
 
            // Get the handle to the menu-item combo box. 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_MENUITEMS); 
 
            // Get the handle to the Character submenu and
            // count the number of items it has. In this example, 
            // the menu has position 0. You must alter this value 
            // if you add additional menus. 
            hmenu = GetSubMenu(GetMenu(hwndMain), 0); 
            cItems = GetMenuItemCount(hmenu); 
 
            // Get the text of each item, strip out the '&' and 
            // the accelerator text, and add the text to the 
            // menu-item combo box. 
 
            for (i = 0; i < cItems; i++) 
            { 
                if (!(GetMenuString(hmenu, i, szTemp, 
                        sizeof(szTemp)/sizeof(TCHAR), MF_BYPOSITION))) 
                    continue; 
                for (pch = szTemp, pch2 = szItem; *pch != '\0'; ) 
                { 
                    if (*pch != '&') 
                    { 
                        if (*pch == '\t') 
                        { 
                            *pch = '\0'; 
                            *pch2 = '\0'; 
                        } 
                        else *pch2++ = *pch++; 
                    } 
                    else pch++; 
                } 
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) szItem); 
            } 
 
            // Now fill the keystroke combo box with the list of 
            // keystrokes that will be allowed for accelerators. 
            // The list of keystrokes is in the application-defined 
            // structure called "vkeys". 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
            for (i = 0; i < MAXKEYS; i++) 
            {
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) vkeys[i].pKeyString); 
            }
 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDD_MENUITEMS: 
 
                    // The user must select an item from the combo 
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fItemSelected = TRUE; 
                    return 0; 
 
                case IDD_KEYSTROKES: 
 
                    // The user must select an item from the combo
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fKeySelected = TRUE; 
 
                    return 0; 
 
                case IDOK: 
 
                    // If the user has not selected a menu item 
                    // and a keystroke, display a reminder in a 
                    // message box. 
 
                    if (!fItemSelected || !fKeySelected) 
                    { 
                        MessageBox(hwndDlg, 
                            "Item or key not selected.", NULL, 
                            MB_OK); 
                        return 0; 
                    } 
 
                    // Determine whether the CTRL, ALT, and SHIFT 
                    // keys are selected. Concatenate the 
                    // appropriate strings to the accelerator- 
                    // text buffer, and set the appropriate 
                    // accelerator flags. 
 
                    szAccelText[0] = '\0'; 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_CNTRL); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Ctl+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FCONTROL; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_ALT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Alt+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FALT; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_SHIFT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    {
                        hr = StringCchCat(szAccelText, 32, "Shft+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FSHIFT; 
                    } 
 
                    // Get the selected keystroke, and look up the 
                    // accelerator text and the virtual-key code 
                    // for the keystroke in the vkeys structure. 
 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
                    nCurSel = (int) SendMessage(hwndCtl, 
                        CB_GETCURSEL, 0, 0);
                    numTCHAR = SendMessage(hwndCtl, CB_GETLBTEXTLEN, 
                        nCursel, 0); 
                    if (numTCHAR <= 15)
                        {                   
                        SendMessage(hwndCtl, CB_GETLBTEXT, 
                            nCurSel, (LONG) (LPSTR) szKeyStroke);
                        }
                    else
                        {
                        // TODO: writer error handler
                        }
                         
                    for (i = 0; i < MAXKEYS; i++) 
                    {
                    //
                    // lstrcmp requires that both parameters are
                    // null-terminated.
                    //
                        if(lstrcmp(vkeys[i].pKeyString, szKeyStroke) 
                            == 0) 
                        { 
                            hr = StringCchCopy(szKeyStroke, 16, vkeys[i].pKeyName);
                            if (FAILED(hr))
                            {
                            // TODO: write error handler
                            }
                            break; 
                        } 
                    } 
 
                    // Concatenate the keystroke text to the 
                    // "Ctl+","Alt+", or "Shft+" string. 
 
                        hr = StringCchCat(szAccelText, 32, szKeyStroke);
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
 
                    // Determine the position in the menu of the 
                    // selected menu item. Menu items in the 
                    // "Character" menu have positions 0,2,3, and 4.
                    // Note: the lstrcmp parameters must be
                    // null-terminated. 
 
                    if (lstrcmp(szItem, "Regular") == 0) 
                        uItemPos = 0; 
                    else if (lstrcmp(szItem, "Bold") == 0) 
                        uItemPos = 2; 
                    else if (lstrcmp(szItem, "Italic") == 0) 
                        uItemPos = 3; 
                    else if (lstrcmp(szItem, "Underline") == 0) 
                        uItemPos = 4; 
 
                    // Get the string that corresponds to the 
                    // selected item. 
 
                    GetMenuString(hmenu, uItemPos, szItem, 
                        sizeof(szItem)/sizeof(TCHAR), MF_BYPOSITION); 
 
                    // Append the new accelerator text to the 
                    // menu-item text. 
 
                    for (pch = szItem; *pch != '\t'; pch++); 
                        ++pch; 
 
                    for (pch2 = szAccelText; *pch2 != '\0'; pch2++) 
                        *pch++ = *pch2; 
                    *pch = '\0'; 
 
                    // Modify the menu item to reflect the new 
                    // accelerator text. 
 
                    idItem = GetMenuItemID(hmenu, uItemPos); 
                    ModifyMenu(hmenu, idItem, MF_BYCOMMAND | 
                        MF_STRING, idItem, szItem); 
 
                    // Reset the selection flags. 
 
                    fItemSelected = FALSE; 
                    fKeySelected = FALSE; 
 
                    // Save the current accelerator table. 
 
                    haccelOld = haccel; 
 
                    // Count the number of entries in the current 
                    // table, allocate a buffer for the table, and 
                    // then copy the table into the buffer. 
 
                    cAccelerators = CopyAcceleratorTable( 
                        haccelOld, NULL, 0); 
                    lpaccelNew = (LPACCEL) LocalAlloc(LPTR, 
                        cAccelerators * sizeof(ACCEL)); 
 
                    if (lpaccelNew != NULL) 
                    {
                        CopyAcceleratorTable(haccel, lpaccelNew, 
                            cAccelerators); 
                    }
 
                    // Find the accelerator that the user modified 
                    // and change its flags and virtual-key code 
                    // as appropriate. 
 
                    for (i = 0; i < (UINT) cAccelerators; i++) 
                    { 
                           if (lpaccelNew[i].cmd == (WORD) idItem)
                        {
                            lpaccelNew[i].fVirt = fAccelFlags; 
                            lpaccelNew[i].key = wVKCode; 
                        }
                    } 
 
                    // Create the new accelerator table, and 
                    // destroy the old one. 
 
                    DestroyAcceleratorTable(haccelOld); 
                    haccel = CreateAcceleratorTable(lpaccelNew, 
                        cAccelerators); 
 
                    // Destroy the dialog box. 
 
                    EndDialog(hwndDlg, TRUE); 
                    return 0; 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    break; 
            } 
        default: 
            break; 
    } 
    return FALSE; 
}
```



 

 