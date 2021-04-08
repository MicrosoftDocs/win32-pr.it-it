---
title: Uso di tasti di scelta rapida
description: In questa sezione vengono illustrate le attività associate agli acceleratori tastiera.
ms.assetid: 11c42d69-7454-43e6-9f44-c14a283814ce
keywords:
- input utente, tasti di scelta rapida
- acquisizione dell'input dell'utente, tasti di scelta rapida
- tasti di scelta rapida
- acceleratori
- tabelle dei tasti di scelta rapida
- risorse tabella di tasti di scelta rapida
- translate Accelerator (funzione)
- Messaggio WM_COMMAND
- WM_SYS messaggio di comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2241ba828ea9e6be5e4bb0b7471adcc3130940ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046731"
---
# <a name="using-keyboard-accelerators"></a>Uso di tasti di scelta rapida

In questa sezione vengono illustrate le attività associate agli acceleratori tastiera.

-   [Uso di una risorsa della tabella dei tasti di scelta rapida](#using-an-accelerator-table-resource)
    -   [Creazione della risorsa della tabella dei tasti di scelta rapida](#creating-the-accelerator-table-resource)
    -   [Caricamento della risorsa della tabella dei tasti di scelta rapida](#loading-the-accelerator-table-resource)
    -   [Chiamata della funzione di accelerazione translate](#calling-the-translate-accelerator-function)
    -   [Elaborazione \_ dei messaggi di comando WM](/windows)
    -   [Eliminazione definitiva della risorsa della tabella dei tasti di scelta rapida](#destroying-the-accelerator-table-resource)
    -   [Creazione di acceleratori per gli attributi del tipo di carattere](#creating-accelerators-for-font-attributes)
-   [Uso di una tabella di tasti di scelta rapida creata in fase di esecuzione](#using-an-accelerator-table-created-at-run-time)
    -   [Creazione di una tabella Run-Time Accelerator](#creating-a-run-time-accelerator-table)
    -   [Elaborazione di acceleratori](#processing-accelerators)
    -   [Eliminazione di una tabella di tasti di scelta rapida Run-Time](#destroying-a-run-time-accelerator-table)
    -   [Creazione di acceleratori modificabili dall'utente](#creating-user-editable-accelerators)

## <a name="using-an-accelerator-table-resource"></a>Uso di una risorsa della tabella dei tasti di scelta rapida

Il modo più comune per aggiungere il supporto acceleratore a un'applicazione consiste nell'includere una risorsa della tabella dei tasti di scelta rapida con il file eseguibile dell'applicazione e quindi caricare la risorsa in fase di esecuzione.

In questa sezione vengono trattati gli argomenti seguenti.

-   [Creazione della risorsa della tabella dei tasti di scelta rapida](#creating-the-accelerator-table-resource)
-   [Caricamento della risorsa della tabella dei tasti di scelta rapida](#loading-the-accelerator-table-resource)
-   [Chiamata della funzione di accelerazione translate](#calling-the-translate-accelerator-function)
-   [Elaborazione \_ dei messaggi di comando WM](/windows)
-   [Eliminazione definitiva della risorsa della tabella dei tasti di scelta rapida](#destroying-the-accelerator-table-resource)
-   [Creazione di acceleratori per gli attributi del tipo di carattere](#creating-accelerators-for-font-attributes)

### <a name="creating-the-accelerator-table-resource"></a>Creazione della risorsa della tabella dei tasti di scelta rapida

Si crea una risorsa della tabella di tasti di scelta rapida [usando l'istruzione ACCELERATORS](./accelerators-resource.md) nel file di definizione delle risorse dell'applicazione. È necessario assegnare un nome o un identificatore di risorsa alla tabella dei tasti di scelta rapida, preferibilmente a differenza di quanto avviene per qualsiasi altra risorsa. Il sistema usa questo identificatore per caricare la risorsa in fase di esecuzione.

Ogni acceleratore definito richiede una voce separata nella tabella dei tasti di scelta rapida. In ogni voce si definisce la sequenza di tasti (codice carattere ASCII o codice chiave virtuale) che genera l'acceleratore e l'identificatore dell'acceleratore. È inoltre necessario specificare se la sequenza di tasti deve essere utilizzata in combinazione con i tasti ALT, MAIUSC o CTRL. Per ulteriori informazioni sulle chiavi virtuali, vedere [input da tastiera](/windows/desktop/inputdev/keyboard-input).

Una sequenza di tasti ASCII viene specificata racchiudendo il carattere ASCII tra virgolette doppie o usando il valore intero del carattere in combinazione con il flag ASCII. Gli esempi seguenti illustrano come definire gli acceleratori ASCII.

``` syntax
"A", ID_ACCEL1         ; SHIFT+A 
65,  ID_ACCEL2, ASCII  ; SHIFT+A 
```

Una sequenza di tasti del codice a chiave virtuale viene specificata in modo diverso a seconda che la sequenza di tasti sia una chiave alfanumerica o una chiave non alfanumerica. Per una chiave alfanumerica, la lettera o il numero della chiave, racchiuso tra virgolette doppie, viene combinato con il flag **VIRTKEY** . Per una chiave non alfanumerica, il codice della chiave virtuale per la chiave specifica viene combinato con il flag **VIRTKEY** . Negli esempi seguenti viene illustrato come definire gli acceleratori del codice a chiave virtuale.

``` syntax
"a",       ID_ACCEL3, VIRTKEY   ; A (caps-lock on) or a 
VK_INSERT, ID_ACCEL4, VIRTKEY   ; INSERT key 
```

Nell'esempio seguente viene illustrata una risorsa della tabella dei tasti di scelta rapida che definisce acceleratori per le operazioni sui file. Il nome della risorsa è *FileAccel*.

``` syntax
FileAccel ACCELERATORS 
BEGIN 
    VK_F12, IDM_OPEN, CONTROL, VIRTKEY  ; CTRL+F12 
    VK_F4,  IDM_CLOSE, ALT, VIRTKEY     ; ALT+F4 
    VK_F12, IDM_SAVE, SHIFT, VIRTKEY    ; SHIFT+F12 
    VK_F12, IDM_SAVEAS, VIRTKEY         ; F12 
END 
```

Se si desidera che l'utente prema ALT, MAIUSC o CTRL in una combinazione con la sequenza di tasti di scelta rapida, specificare i flag ALT, MAIUSC e CONTROL nella definizione dell'acceleratore. Di seguito sono riportati alcuni esempi.

``` syntax
"B",   ID_ACCEL5, ALT                   ; ALT_SHIFT+B 
"I",   ID_ACCEL6, CONTROL, VIRTKEY      ; CTRL+I 
VK_F5, ID_ACCEL7, CONTROL, ALT, VIRTKEY ; CTRL+ALT+F5 
```

Per impostazione predefinita, quando un tasto di scelta rapida corrisponde a una voce di menu, il sistema evidenzia la voce di menu. È possibile usare il flag **noinverte** per impedire l'evidenziazione per un singolo acceleratore. Nell'esempio seguente viene illustrato come utilizzare il flag **noinverte** :

``` syntax
VK_DELETE, ID_ACCEL8, VIRTKEY, SHIFT, NOINVERT  ; SHIFT+DELETE 
```

Per definire acceleratori che corrispondono alle voci di menu nell'applicazione, includere gli acceleratori nel testo delle voci di menu. Nell'esempio seguente viene illustrato come includere acceleratori nel testo di una voce di menu in un file di definizione delle risorse.

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

### <a name="loading-the-accelerator-table-resource"></a>Caricamento della risorsa della tabella dei tasti di scelta rapida

Un'applicazione carica una risorsa della tabella dei tasti di scelta rapida chiamando la funzione [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) e specificando l'handle dell'istanza per l'applicazione il cui file eseguibile contiene la risorsa e il nome o l'identificatore della risorsa. **LoadAccelerators** carica la tabella dei tasti di scelta rapida specificata in memoria e restituisce l'handle alla tabella dei tasti di scelta rapida.

Un'applicazione può caricare una risorsa della tabella dei tasti di scelta rapida in qualsiasi momento. In genere, un'applicazione a thread singolo carica la tabella dei tasti di scelta rapida prima di immettere il ciclo di messaggi principale. Un'applicazione che usa più thread in genere carica la risorsa della tabella di tasti di scelta rapida per un thread prima di immettere il ciclo di messaggi per il thread. Un'applicazione o un thread potrebbe inoltre utilizzare più tabelle di tasti di scelta rapida, ciascuna associata a una particolare finestra dell'applicazione. Tale applicazione caricherà la tabella dei tasti di scelta rapida per la finestra ogni volta che l'utente ha attivato la finestra. Per ulteriori informazioni sui thread, vedere [processi e thread](/windows/desktop/ProcThread/processes-and-threads).

### <a name="calling-the-translate-accelerator-function"></a>Chiamata della funzione di accelerazione translate

Per elaborare gli acceleratori, il ciclo di messaggi di un'applicazione (o di un thread) deve contenere una chiamata alla funzione [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) . **TranslateAccelerator** Confronta le sequenze di tasti con una tabella dei tasti di scelta rapida e, se trova una corrispondenza, traduce le sequenze di tasti in un messaggio [**WM \_**](wm-command.md) (o [**WM \_ SYSCOMMAND**](wm-syscommand.md)). La funzione Invia quindi il messaggio a una routine della finestra. I parametri della funzione **TranslateAccelerator** includono l'handle per la finestra che deve ricevere i messaggi di **\_ comando WM** , l'handle alla tabella dei tasti di scelta rapida utilizzata per convertire gli acceleratori e un puntatore a [**una struttura di messaggi contenente**](/windows/win32/api/winuser/ns-winuser-msg) un messaggio dalla coda. Nell'esempio seguente viene illustrato come chiamare **TranslateAccelerator** dall'interno di un ciclo di messaggi.


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



### <a name="processing-wm_command-messages"></a>Elaborazione \_ dei messaggi di comando WM

Quando si usa un tasto di scelta rapida, la finestra specificata nella funzione [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) riceve un [**\_ comando WM**](wm-command.md) o un messaggio [**WM \_ SYSCOMMAND**](wm-syscommand.md) . La parola inferiore del parametro *wParam* contiene l'identificatore del tasto di scelta rapida. La routine della finestra esamina l'identificatore per determinare l'origine del messaggio **del \_ comando WM** ed elabora il messaggio di conseguenza.

In genere, se un tasto di scelta rapida corrisponde a una voce di menu nell'applicazione, all'acceleratore e alla voce di menu viene assegnato lo stesso identificatore. Se è necessario sapere se un messaggio [**di \_ comando WM**](wm-command.md) è stato generato da un acceleratore o da una voce di menu, è possibile esaminare la parola più ordinata del parametro *wParam* . Se un tasto di scelta rapida ha generato il messaggio, la parola più ordinata è 1; Se una voce di menu ha generato il messaggio, la parola più ordinata è 0.

### <a name="destroying-the-accelerator-table-resource"></a>Eliminazione definitiva della risorsa della tabella dei tasti di scelta rapida

Il sistema elimina automaticamente le risorse della tabella dei tasti di scelta rapida caricate dalla funzione [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) , rimuovendo la risorsa dalla memoria dopo la chiusura dell'applicazione.

### <a name="creating-accelerators-for-font-attributes"></a>Creazione di acceleratori per gli attributi del tipo di carattere

Nell'esempio riportato in questa sezione viene illustrato come eseguire le attività seguenti:

-   Creare una risorsa della tabella dei tasti di scelta rapida.
-   Caricare la tabella dei tasti di scelta rapida in fase di esecuzione.
-   Tradurre gli acceleratori in un ciclo di messaggi.
-   Elabora i messaggi di [**\_ comando WM**](wm-command.md) generati dagli acceleratori.

Queste attività vengono illustrate nel contesto di un'applicazione che include un menu di **caratteri** e gli acceleratori corrispondenti che consentono all'utente di selezionare gli attributi del tipo di carattere corrente.

La parte seguente di un file di definizione delle risorse definisce il menu dei **caratteri** e la tabella dei tasti di scelta rapida associata. Si noti che le voci di menu mostrano le sequenze di tasti di scelta rapida e che ogni acceleratore ha lo stesso identificatore della voce di menu associata.


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



Le sezioni seguenti del file di origine dell'applicazione mostrano come implementare gli acceleratori.


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



## <a name="using-an-accelerator-table-created-at-run-time"></a>Uso di una tabella di tasti di scelta rapida creata in fase di esecuzione

In questo argomento viene illustrato come utilizzare le tabelle di tasti di scelta rapida create in fase di esecuzione.

-   [Creazione di una tabella Run-Time Accelerator](#creating-a-run-time-accelerator-table)
-   [Elaborazione di acceleratori](#processing-accelerators)
-   [Eliminazione di una tabella di tasti di scelta rapida Run-Time](#destroying-a-run-time-accelerator-table)
-   [Creazione di acceleratori modificabili dall'utente](#creating-user-editable-accelerators)

### <a name="creating-a-run-time-accelerator-table"></a>Creazione di una tabella Run-Time Accelerator

Il primo passaggio per la creazione di una tabella di tasti di scelta rapida in fase di esecuzione consiste nel compilare una matrice di strutture [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) . Ogni struttura della matrice definisce un tasto di scelta rapida nella tabella. La definizione di un acceleratore include i relativi flag, la relativa chiave e il relativo identificatore. La struttura **Accel** ha il formato seguente.

``` syntax
typedef struct tagACCEL { // accl 
    BYTE   fVirt; 
    WORD   key; 
    WORD   cmd; 
} ACCEL;
```

Si definisce la sequenza di tasti di un acceleratore specificando un codice carattere ASCII o un codice di chiave virtuale nel membro **chiave** della struttura di [**accelerazione**](/windows/win32/api/winuser/ns-winuser-accel) . Se si specifica un codice a chiave virtuale, è necessario prima includere il flag **FVIRTKEY** nel membro **fVirt** . in caso contrario, il sistema interpreta il codice come un codice carattere ASCII. È possibile includere il flag **FCONTROL**, **Falt** o **FSHIFT** , o tutti e tre, per combinare il tasto CTRL, ALT o MAIUSC con la sequenza di tasti.

Per creare la tabella dei tasti di scelta rapida, passare un puntatore alla matrice di strutture [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) alla funzione [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) . **CreateAcceleratorTable** crea la tabella dei tasti di scelta rapida e restituisce l'handle alla tabella.

### <a name="processing-accelerators"></a>Elaborazione di acceleratori

Il processo di caricamento e chiamata di acceleratori forniti da una tabella di tasti di scelta rapida creata in fase di esecuzione è identico all'elaborazione di quelli forniti da una risorsa della tabella dei tasti di scelta rapida. Per altre informazioni, vedere [caricamento della risorsa della tabella dei tasti di scelta rapida tramite l'](#loading-the-accelerator-table-resource) [elaborazione \_ dei messaggi di comando WM](/windows).

### <a name="destroying-a-run-time-accelerator-table"></a>Eliminazione di una tabella di tasti di scelta rapida Run-Time

Il sistema elimina automaticamente le tabelle dei tasti di scelta rapida create in fase di esecuzione, rimuovendo le risorse dalla memoria dopo la chiusura dell'applicazione. È possibile eliminare una tabella di tasti di scelta rapida e rimuoverla dalla memoria prima passando l'handle della tabella alla funzione [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) .

### <a name="creating-user-editable-accelerators"></a>Creazione di acceleratori modificabili dall'utente

Questo esempio illustra come creare una finestra di dialogo che consente all'utente di modificare il tasto di scelta rapida associato a una voce di menu. La finestra di dialogo è costituita da una casella combinata che contiene voci di menu, una casella combinata contenente i nomi delle chiavi e caselle di controllo per la selezione dei tasti CTRL, ALT e MAIUSC. Nella figura seguente viene illustrata la finestra di dialogo.

![finestra di dialogo con caselle combinate e caselle di controllo](images/useredit.gif)

Nell'esempio seguente viene illustrato il modo in cui la finestra di dialogo viene definita nel file di definizione delle risorse.

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

La barra dei menu dell'applicazione contiene un sottomenu **carattere** i cui elementi sono associati ad acceleratori.

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

Nella finestra di dialogo viene utilizzata una matrice di strutture VKEY definite dall'applicazione, ciascuna contenente una stringa di testo della sequenza di tasti e una stringa di testo del tasto di scelta rapida. Quando viene creata, la finestra di dialogo analizza la matrice e aggiunge ogni stringa di testo della sequenza di tasti alla casella combinata **Seleziona sequenza di tasti** . Quando l'utente fa clic sul pulsante **OK** , la finestra di dialogo Cerca la stringa di testo della sequenza di tasti selezionata e recupera la stringa di testo dell'acceleratore corrispondente. La finestra di dialogo aggiunge la stringa di testo acceleratore al testo della voce di menu selezionata dall'utente. Nell'esempio seguente viene illustrata la matrice di strutture VKEY:


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



La procedura di inizializzazione della finestra di dialogo Compila l' **elemento SELECT** e seleziona le caselle combinate della **sequenza di tasti** . Dopo che l'utente ha selezionato una voce di menu e un tasto di scelta rapida associato, nella finestra di dialogo vengono esaminati i controlli della finestra di dialogo per ottenere la selezione dell'utente, viene aggiornato il testo della voce di menu e quindi viene creata una nuova tabella dei tasti di scelta rapida che contiene il nuovo acceleratore definito dall'utente. Nell'esempio seguente viene illustrata la routine della finestra di dialogo. Si noti che è necessario inizializzare nella routine della finestra.


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



 

 