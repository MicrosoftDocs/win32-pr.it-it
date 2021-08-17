---
title: Uso di menu
description: In questa sezione vengono forniti esempi di codice per le attività correlate ai menu.
ms.assetid: b1391e37-a146-46ec-a329-aa57cfcfd351
keywords:
- risorse, menu
- menu, creazione
- risorse del modello di menu
- risorse, menu-modello
- formato del modello di menu esteso
- formato del modello di menu precedente
- caricamento di risorse del modello di menu
- menu, classe
- menu, scelta rapida
- creazione di menu
- menu di classe
- menu di scelta rapida
- bitmap delle voci di menu
- menu, proprietario disegnato
- menu disegnati dal proprietario
- bitmap con segno di spunta personalizzate
- menu, caselle di controllo
- menu, tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f3a71a580a323fa2058613f8c9a14d9c2782bd3ba139e5d182750e5047fe74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971930"
---
# <a name="using-menus"></a>Uso di menu

In questa sezione vengono descritte le attività seguenti:

-   [Uso di una Menu-Template risorsa](#using-a-menu-template-resource)
    -   [Formato Menu-Template esteso](#extended-menu-template-format)
    -   [Formato Menu-Template precedente](#old-menu-template-format)
    -   [Caricamento di una Menu-Template risorsa](#loading-a-menu-template-resource)
    -   [Creazione di un menu classe](#creating-a-class-menu)
-   [Creazione di un menu di scelta rapida](#creating-a-shortcut-menu)
    -   [Elaborazione del messaggio \_ CONTEXTMENU WM](/windows)
    -   [Creazione di un menu di scelta Font-Attributes collegamento](#creating-a-shortcut-font-attributes-menu)
    -   [Visualizzazione di un menu di scelta rapida](#displaying-a-shortcut-menu)
-   [Uso Menu-Item bitmap](#using-menu-item-bitmaps)
    -   [Impostazione del flag del tipo di bitmap](#setting-the-bitmap-type-flag)
    -   [Creazione della bitmap](#creating-the-bitmap)
    -   [Aggiunta di linee e grafici a un menu](#adding-lines-and-graphs-to-a-menu)
    -   [Esempio di Menu-Item bitmap](#example-of-menu-item-bitmaps)
-   [Creazione Owner-Drawn voci di menu](#creating-owner-drawn-menu-items)
    -   [Impostazione del flag Owner-Drawn](#setting-the-owner-drawn-flag)
    -   [Menu disegnati dal proprietario e messaggio \_ MEASUREITEM WM](/windows)
    -   [Menu disegnati dal proprietario e messaggio \_ DRAWITEM WM](/windows)
    -   [Menu disegnati dal proprietario e messaggio \_ MENUCHAR WM](/windows)
    -   [Impostazione dei tipi di carattere per Menu-Item di testo](#setting-fonts-for-menu-item-text-strings)
    -   [Esempio di voci Owner-Drawn menu](#example-of-owner-drawn-menu-items)
-   [Uso di bitmap con segni di spunta personalizzati](#using-custom-check-mark-bitmaps)
    -   [Creazione di bitmap del segno di spunta personalizzate](#creating-custom-check-mark-bitmaps)
    -   [Associazione di bitmap a una voce di menu](#associating-bitmaps-with-a-menu-item)
    -   [Impostazione dell'attributo di segno di spunta](#setting-the-check-mark-attribute)
    -   [Simulazione di caselle di controllo in un menu](#simulating-check-boxes-in-a-menu)
    -   [Esempio di utilizzo di bitmap con segno di spunta personalizzate](#example-of-using-custom-check-mark-bitmaps)

## <a name="using-a-menu-template-resource"></a>Uso di una Menu-Template risorse

In genere si include un menu in un'applicazione creando una risorsa modello di menu e quindi caricando il menu in fase di esecuzione. Questa sezione descrive il formato di un modello di menu e illustra come caricare una risorsa modello di menu e usarla nell'applicazione. Per informazioni sulla creazione di una risorsa modello di menu, vedere la documentazione inclusa con gli strumenti di sviluppo.

-   [Formato Menu-Template esteso](#extended-menu-template-format)
-   [Formato Menu-Template precedente](#old-menu-template-format)
-   [Caricamento di una Menu-Template risorsa](#loading-a-menu-template-resource)
-   [Creazione di un menu classe](#creating-a-class-menu)

### <a name="extended-menu-template-format"></a>Formato Menu-Template esteso

Il formato del modello di menu esteso supporta funzionalità di menu aggiuntive. Analogamente alle risorse standard del modello di menu, le risorse del modello di menu esteso hanno il tipo di risorsa **\_ MENU RT.** Il sistema distingue i due formati di risorsa in base al numero di versione, che è il primo membro dell'intestazione della risorsa.

Un modello di menu esteso è costituito da [**una struttura MENUEX \_ TEMPLATE \_ HEADER**](menuex-template-header.md) seguita da un'altra [**struttura di definizione dell'elemento MENUEX TEMPLATE \_ \_ ITEM.**](menuex-template-item.md)

### <a name="old-menu-template-format"></a>Formato Menu-Template precedente

Un modello di menu precedente (Microsoft Windows NT 3.51 e versioni precedenti) definisce un menu, ma non supporta la nuova funzionalità di menu. Una risorsa modello di menu precedente ha il **tipo di risorsa \_ MENU RT.**

Un modello di menu precedente è costituito da [**una struttura MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) seguita da una o più [**strutture MENUITEMTEMPLATE.**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)

### <a name="loading-a-menu-template-resource"></a>Caricamento di una Menu-Template risorsa

Per caricare una risorsa modello di menu, usare la funzione [**LoadMenu,**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) specificando un handle per il modulo che contiene la risorsa e l'identificatore del modello di menu. La **funzione LoadMenu** restituisce un handle di menu che è possibile usare per assegnare il menu a una finestra. Questa finestra diventa la finestra proprietaria del menu, ricevendo tutti i messaggi generati dal menu.

Per creare un menu da un modello di menu già in memoria, usare la [**funzione LoadMenuIndirect.**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) Ciò è utile se l'applicazione genera modelli di menu in modo dinamico.

Per assegnare un menu a una finestra, usa la funzione [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) o specifica l'handle del menu nel parametro *hMenu* della [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) durante la creazione di una finestra. Un altro modo per assegnare un menu a una finestra è specificare un modello di menu quando si registra una classe di finestra. il modello identifica il menu specificato come menu della classe per la classe della finestra.

Per fare in modo che il sistema assegni automaticamente un menu specifico a una finestra, specificare il modello del menu quando si registra la classe della finestra. Il modello identifica il menu specificato come menu della classe per la classe della finestra. Quindi, quando si crea una finestra della classe specificata, il sistema assegna automaticamente il menu specificato alla finestra.

Non è possibile assegnare un menu a una finestra che è una finestra figlio.

Per creare un menu di classe, includere l'identificatore della risorsa modello di menu come membro **lpszMenuName** di una struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) e quindi passare un puntatore alla struttura alla funzione [**RegisterClass.**](/windows/desktop/api/winuser/nf-winuser-registerclassa)

### <a name="creating-a-class-menu"></a>Creazione di un menu classe

Nell'esempio seguente viene illustrato come creare un menu di classe per un'applicazione, creare una finestra che usa il menu della classe ed elaborare i comandi di menu nella routine della finestra.

Di seguito è riportata la parte rilevante del file di intestazione dell'applicazione:


```
// Menu-template resource identifier 
 
#define IDM_MYMENURESOURCE   3
```



Di seguito sono riportate le parti rilevanti dell'applicazione stessa:


```
HINSTANCE hinst; 
 
int APIENTRY WinMain(HINSTANCE hinstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg = { };  // message 
    WNDCLASS wc;    // windowclass data 
    HWND hwnd;      // handle to the main window 
 
    // Create the window class for the main window. Specify 
    // the identifier of the menu-template resource as the 
    // lpszMenuName member of the WNDCLASS structure to create 
    // the class menu. 
 
    wc.style = 0; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  MAKEINTRESOURCE(IDM_MYMENURESOURCE); 
    wc.lpszClassName = "MainWClass"; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    hinst = hinstance; 
 
    // Create the main window. Set the hmenu parameter to NULL so 
    // that the system uses the class menu for the window. 
 
    hwnd = CreateWindow("MainWClass", "Sample Application", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, hinstance, 
        NULL); 
 
    if (hwnd == NULL) 
        return FALSE; 
 
    // Make the window visible and send a WM_PAINT message to the 
    // window procedure. 
 
    ShowWindow(hwnd, nCmdShow); 
    UpdateWindow(hwnd); 
 
    // Start the main message loop. 
 
    while (GetMessage(&msg, NULL, 0, 0)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
    return msg.wParam; 
        UNREFERENCED_PARAMETER(hPrevInstance); 
} 
 
 
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    switch (uMsg) 
    { 
        // Process other window messages. 
 
        case WM_COMMAND: 
 
            // Test for the identifier of a command item. 
 
            switch(LOWORD(wParam)) 
            { 
                case IDM_FI_OPEN: 
                    DoFileOpen();   // application-defined 
                    break; 
 
                case IDM_FI_CLOSE: 
                    DoFileClose();  // application-defined 
                    break; 
                // Process other menu commands. 
 
                default: 
                    break; 
 
            } 
            return 0; 
 
        // Process other window messages. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="creating-a-shortcut-menu"></a>Creazione di un menu di scelta rapida

Per usare un menu di scelta rapida in un'applicazione, passarne l'handle alla [**funzione TrackPopupMenuEx.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) Un'applicazione chiama in **genere TrackPopupMenuEx** in una routine della finestra in risposta a un messaggio generato dall'utente, ad esempio [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) o [**WM \_ KEYDOWN.**](/windows/desktop/inputdev/wm-keydown)

Oltre all'handle del menu a comparsa, [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) richiede di specificare un handle per la finestra proprietaria, la posizione del menu di scelta rapida (nelle coordinate dello schermo) e il pulsante del mouse che l'utente può usare per scegliere un elemento.

La funzione [**TrackPopupMenu precedente**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) è ancora supportata, ma le nuove applicazioni devono usare la [**funzione TrackPopupMenuEx.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) La **funzione TrackPopupMenuEx** richiede gli stessi parametri di **TrackPopupMenu,** ma consente anche di specificare una parte della schermata che il menu non deve nascondere. Un'applicazione chiama in genere queste funzioni in una routine della finestra durante l'elaborazione [**del messaggio WM \_ CONTEXTMENU.**](wm-contextmenu.md)

È possibile specificare la posizione di un menu di scelta rapida fornendo le coordinate x e y insieme al flag **TPM \_ CENTERALIGN,** **TPM \_ LEFTALIGN** o **TPM \_ RIGHTALIGN.** Il flag specifica la posizione del menu di scelta rapida rispetto alle coordinate x e y.

È consigliabile consentire all'utente di scegliere una voce da un menu di scelta rapida usando lo stesso pulsante del mouse usato per visualizzare il menu. A tale scopo, specificare il flag **TPM \_ LEFTBUTTON** o **TPM \_ RIGHTBUTTON** per indicare quale pulsante del mouse può essere utilizzato dall'utente per scegliere una voce di menu.

-   [Elaborazione del messaggio \_ CONTEXTMENU WM](/windows)
-   [Creazione di un menu di scelta Font-Attributes collegamento](#creating-a-shortcut-font-attributes-menu)
-   [Visualizzazione di un menu di scelta rapida](#displaying-a-shortcut-menu)

### <a name="processing-the-wm_contextmenu-message"></a>Elaborazione del messaggio \_ CONTEXTMENU WM

Il [**messaggio WM \_ CONTEXTMENU**](wm-contextmenu.md) viene generato quando la routine della finestra di un'applicazione passa il messaggio [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) o [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) alla [**funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) L'applicazione può elaborare questo messaggio per visualizzare un menu di scelta rapida appropriato per una parte specifica della schermata. Se l'applicazione non visualizza un menu di scelta rapida, deve passare il messaggio a **DefWindowProc per** la gestione predefinita.

Di seguito è riportato un esempio di elaborazione del messaggio [**WM \_ CONTEXTMENU**](wm-contextmenu.md) come potrebbe essere visualizzato nella routine della finestra di un'applicazione. Le parole di ordine basso e alto del parametro *lParam* specificano le coordinate dello schermo del mouse quando viene rilasciato il pulsante destro del mouse (si noti che queste coordinate possono assumere valori negativi nei sistemi con più monitor). La funzione **OnContextMenu** definita dall'applicazione restituisce **TRUE** se viene visualizzato un menu di scelta rapida oppure **FALSE** in caso contrario.


```
case WM_CONTEXTMENU: 
    if (!OnContextMenu(hwnd, GET_X_LPARAM(lParam),
              GET_Y_LPARAM(lParam))) 
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    break; 
```



La funzione OnContextMenu definita dall'applicazione seguente visualizza un menu di scelta rapida se la posizione del mouse specificata si trova all'interno dell'area client della finestra. Una funzione più sofisticata potrebbe visualizzare uno dei diversi menu, a seconda della parte dell'area client specificata. Per visualizzare effettivamente il menu di scelta rapida, questo esempio chiama una funzione definita dall'applicazione denominata DisplayContextMenu. Per una descrizione di questa funzione, vedere [Visualizzazione di un menu di scelta rapida.](#displaying-a-shortcut-menu)


```
BOOL WINAPI OnContextMenu(HWND hwnd, int x, int y) 
{ 
    RECT rc;                    // client area of window 
    POINT pt = { x, y };        // location of mouse click 
 
    // Get the bounding rectangle of the client area. 
 
    GetClientRect(hwnd, &rc); 
 
    // Convert the mouse position to client coordinates. 
 
    ScreenToClient(hwnd, &pt); 
 
    // If the position is in the client area, display a  
    // shortcut menu. 
 
    if (PtInRect(&rc, pt)) 
    { 
        ClientToScreen(hwnd, &pt); 
        DisplayContextMenu(hwnd, pt); 
        return TRUE; 
    } 
 
    // Return FALSE if no menu is displayed. 
 
    return FALSE; 
} 
```



### <a name="creating-a-shortcut-font-attributes-menu"></a>Creazione di un menu Font-Attributes collegamento

L'esempio in questa sezione contiene parti di codice di un'applicazione che crea e visualizza un menu di scelta rapida che consente all'utente di impostare tipi di carattere e attributi del tipo di carattere. L'applicazione visualizza il menu nell'area client della finestra principale ogni volta che l'utente fa clic sul pulsante sinistro del mouse.

Ecco il modello di menu per il menu di scelta rapida fornito nel file di definizione delle risorse dell'applicazione.


```
PopupMenu MENU 
BEGIN 
  POPUP "Dummy Popup" 
    BEGIN 
      POPUP "Fonts" 
        BEGIN 
          MENUITEM "Courier",     IDM_FONT_COURIER 
          MENUITEM "Times Roman", IDM_FONT_TMSRMN 
          MENUITEM "Swiss",       IDM_FONT_SWISS 
          MENUITEM "Helvetica",   IDM_FONT_HELV 
          MENUITEM "Old English", IDM_FONT_OLDENG 
        END 
      POPUP "Sizes" 
        BEGIN 
          MENUITEM "7",  IDM_SIZE_7 
          MENUITEM "8",  IDM_SIZE_8 
          MENUITEM "9",  IDM_SIZE_9 
          MENUITEM "10", IDM_SIZE_10 
          MENUITEM "11", IDM_SIZE_11 
          MENUITEM "12", IDM_SIZE_12 
          MENUITEM "14", IDM_SIZE_14 
        END 
      POPUP "Styles" 
        BEGIN 
          MENUITEM "Bold",        IDM_STYLE_BOLD 
          MENUITEM "Italic",      IDM_STYLE_ITALIC 
          MENUITEM "Strike Out",  IDM_STYLE_SO 
          MENUITEM "Superscript", IDM_STYLE_SUPER 
          MENUITEM "Subscript",   IDM_STYLE_SUB 
        END 
    END 
 
END 
```



Nell'esempio seguente vengono fornite la routine della finestra e le funzioni di supporto usate per creare e visualizzare il menu di scelta rapida.


```
LRESULT APIENTRY MenuWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rc;    // client area             
    POINT pt;   // location of mouse click  
 
    switch (uMsg) 
    { 
        case WM_LBUTTONDOWN: 
 
            // Get the bounding rectangle of the client area. 
 
            GetClientRect(hwnd, (LPRECT) &rc); 
 
            // Get the client coordinates for the mouse click.  
 
            pt.x = GET_X_LPARAM(lParam); 
            pt.y = GET_Y_LPARAM(lParam); 
 
            // If the mouse click took place inside the client 
            // area, execute the application-defined function 
            // that displays the shortcut menu. 
 
            if (PtInRect((LPRECT) &rc, pt)) 
                HandlePopupMenu(hwnd, pt); 
            break; 
        // Process other window messages.  
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
 
VOID APIENTRY HandlePopupMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // menu template          
    HMENU hmenuTrackPopup;  // shortcut menu   
 
    //  Load the menu template containing the shortcut menu from the 
    //  application's resources. 
 
    hmenu = LoadMenu(hinst, "PopupMenu"); 
    if (hmenu == NULL) 
        return; 
 
    // Get the first shortcut menu in the menu template. This is the 
    // menu that TrackPopupMenu displays. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // TrackPopup uses screen coordinates, so convert the 
    // coordinates of the mouse click to screen coordinates. 
 
    ClientToScreen(hwnd, (LPPOINT) &pt); 
 
    // Draw and track the shortcut menu.  
 
    TrackPopupMenu(hmenuTrackPopup, TPM_LEFTALIGN | TPM_LEFTBUTTON, 
        pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



### <a name="displaying-a-shortcut-menu"></a>Visualizzazione di un menu di scelta rapida

La funzione illustrata nell'esempio seguente visualizza un menu di scelta rapida.

L'applicazione include una risorsa di menu identificata dalla stringa "ShortcutExample". La barra dei menu contiene semplicemente un nome di menu. L'applicazione usa [**la funzione TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) per visualizzare il menu associato a questa voce di menu. La barra dei menu non viene visualizzata perché **TrackPopupMenu** richiede un handle per un menu, un sottomenu o un menu di scelta rapida.


```
VOID APIENTRY DisplayContextMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // top-level menu 
    HMENU hmenuTrackPopup;  // shortcut menu 
 
    // Load the menu resource. 
 
    if ((hmenu = LoadMenu(hinst, "ShortcutExample")) == NULL) 
        return; 
 
    // TrackPopupMenu cannot display the menu bar so get 
    // a handle to the first shortcut menu. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // Display the shortcut menu. Track the right mouse 
    // button. 
 
    TrackPopupMenu(hmenuTrackPopup, 
            TPM_LEFTALIGN | TPM_RIGHTBUTTON, 
            pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



## <a name="using-menu-item-bitmaps"></a>Uso Menu-Item bitmap

Il sistema può usare una bitmap anziché una stringa di testo per visualizzare una voce di menu. Per usare una bitmap, è necessario impostare il flag **MIIM \_ BITMAP** per la voce di menu e specificare un handle per la bitmap che il sistema deve visualizzare per la voce di menu nel membro **hbmpItem** della struttura [**MENUITEMINFO.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) Questa sezione descrive come usare bitmap per le voci di menu.

-   [Impostazione del flag del tipo di bitmap](#setting-the-bitmap-type-flag)
-   [Creazione della bitmap](#creating-the-bitmap)
-   [Aggiunta di linee e grafici a un menu](#adding-lines-and-graphs-to-a-menu)
-   [Esempio di Menu-Item bitmap](#example-of-menu-item-bitmaps)

### <a name="setting-the-bitmap-type-flag"></a>Impostazione del flag del tipo di bitmap

Il flag **MIIM \_ BITMAP** o **MF \_ BITMAP** indica al sistema di usare una bitmap anziché una stringa di testo per visualizzare una voce di menu. Il flag **MIIM \_ BITMAP** o **MF \_ BITMAP** di una voce di menu deve essere impostato in fase di esecuzione. Non è possibile impostarlo nel file di definizione delle risorse.

Per le nuove applicazioni, è possibile usare la [**funzione SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) o [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) per impostare il flag di tipo **\_ MIIM BITMAP.** Per modificare una voce di menu da una voce di testo a una voce bitmap, usare **SetMenuItemInfo**. Per aggiungere una nuova voce bitmap a un menu, usare la **funzione InsertMenuItem.**

Le applicazioni scritte per le versioni precedenti del sistema possono continuare a usare le funzioni [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)o [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) per impostare il flag **\_ BITMAP MF.** Per modificare una voce di menu da una voce di stringa di testo a una voce bitmap, usare **ModifyMenu**. Per aggiungere una nuova voce bitmap a un menu, usare il flag **\_ BITMAP MF** con la **funzione InsertMenu** **o AppendMenu.**

### <a name="creating-the-bitmap"></a>Creazione della bitmap

Quando si imposta il flag di tipo **MIIM \_ BITMAP** o **MF \_ BITMAP** per una voce di menu, è necessario specificare anche un handle per la bitmap che il sistema deve visualizzare per la voce di menu. È possibile fornire la bitmap come risorsa bitmap o crearne una in fase di esecuzione. Se si usa una risorsa bitmap, è possibile usare la [**funzione LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) per caricare la bitmap e ottenerne l'handle.

Per creare la bitmap in fase di esecuzione, usare Windows Graphics Device Interface (GDI). GDI offre diversi modi per creare una bitmap in fase di esecuzione, ma gli sviluppatori usano in genere il metodo seguente:

1.  Usare la [**funzione CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) per creare un contesto di dispositivo compatibile con il contesto di dispositivo usato dalla finestra principale dell'applicazione.
2.  Usare la [**funzione CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) per creare una bitmap compatibile con la finestra principale dell'applicazione o usare la funzione [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) per creare una bitmap monocromatica.
3.  Usare la [**funzione SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) per selezionare la bitmap nel contesto di dispositivo compatibile.
4.  Usare le funzioni di disegno GDI, ad esempio [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) e [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), per disegnare un'immagine nella bitmap.

Per altre informazioni, vedere [Bitmap .](/windows/desktop/gdi/bitmaps)

### <a name="adding-lines-and-graphs-to-a-menu"></a>Aggiunta di linee e grafici a un menu

L'esempio di codice seguente illustra come creare un menu contenente bitmap di voci di menu. Crea due menu. Il primo è un menu Grafico che contiene tre bitmap di voci di menu: un grafico a torta, un grafico a linee e un grafico a barre. L'esempio illustra come caricare queste bitmap dal file di risorse dell'applicazione e quindi usare le funzioni [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) e [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) per creare le voci di menu e di menu.

Il secondo menu è un menu Righe. Contiene bitmap che mostrano gli stili di linea forniti dalla penna predefinita nel sistema. Le bitmap di tipo linea vengono create in fase di esecuzione usando le funzioni GDI.

Ecco le definizioni delle risorse bitmap nel file di definizione delle risorse dell'applicazione.


```
PIE BITMAP pie.bmp 
LINE BITMAP line.bmp 
BAR BITMAP bar.bmp 
 
```



Ecco le parti rilevanti del file di intestazione dell'applicazione.


```
// Menu-item identifiers 
 
#define IDM_SOLID       PS_SOLID 
#define IDM_DASH        PS_DASH 
#define IDM_DASHDOT     PS_DASHDOT 
#define IDM_DASHDOTDOT  PS_DASHDOTDOT 
 
#define IDM_PIE  1 
#define IDM_LINE 2 
#define IDM_BAR  3 
 
// Line-type flags  
 
#define SOLID       0 
#define DOT         1 
#define DASH        2 
#define DASHDOT     3 
#define DASHDOTDOT  4 
 
// Count of pens  
 
#define CPENS 5 
 
// Chart-type flags  
 
#define PIE  1 
#define LINE 2 
#define BAR  3 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
VOID MakeChartMenu(HWND); 
VOID MakeLineMenu(HWND, HPEN, HBITMAP); 
```



L'esempio seguente illustra come vengono creati i menu e le bitmap delle voci di menu in un'applicazione.


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HPEN hpen[CPENS]; 
    static HBITMAP hbmp[CPENS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Create the Chart and Line menus.  
 
            MakeChartMenu(hwnd); 
            MakeLineMenu(hwnd, hpen, hbmp); 
            return 0; 
 
        // Process other window messages. 
 
        case WM_DESTROY: 
 
            for (i = 0; i < CPENS; i++) 
            { 
                DeleteObject(hbmp[i]); 
                DeleteObject(hpen[i]); 
            } 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
VOID MakeChartMenu(HWND hwnd) 
{ 
    HBITMAP hbmpPie;    // handle to pie chart bitmap   
    HBITMAP hbmpLine;   // handle to line chart bitmap  
    HBITMAP hbmpBar;    // handle to bar chart bitmap   
    HMENU hmenuMain;    // handle to main menu          
    HMENU hmenuChart;   // handle to Chart menu  
 
    // Load the pie, line, and bar chart bitmaps from the 
    // resource-definition file. 
 
    hbmpPie = LoadBitmap(hinst, MAKEINTRESOURCE(PIE)); 
    hbmpLine = LoadBitmap(hinst, MAKEINTRESOURCE(LINE)); 
    hbmpBar = LoadBitmap(hinst, MAKEINTRESOURCE(BAR)); 
 
    // Create the Chart menu and add it to the menu bar. 
    // Append the Pie, Line, and Bar menu items to the Chart 
    // menu. 
 
    hmenuMain = GetMenu(hwnd); 
    hmenuChart = CreatePopupMenu(); 
    AppendMenu(hmenuMain, MF_STRING | MF_POPUP, (UINT) hmenuChart, 
        "Chart"); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_PIE, (LPCTSTR) hbmpPie); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_LINE, 
        (LPCTSTR) hbmpLine); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_BAR, (LPCTSTR) hbmpBar); 
 
    return; 
} 
 
VOID MakeLineMenu(HWND hwnd, HPEN phpen, HBITMAP phbmp) 
{ 
    HMENU hmenuLines;       // handle to Lines menu      
    HMENU hmenu;            // handle to main menu              
    COLORREF crMenuClr;     // menu-item background color       
    HBRUSH hbrBackground;   // handle to background brush       
    HBRUSH hbrOld;          // handle to previous brush         
    WORD wLineX;            // width of line bitmaps            
    WORD wLineY;            // height of line bitmaps           
    HDC hdcMain;            // handle to main window's DC       
    HDC hdcLines;           // handle to compatible DC          
    HBITMAP hbmpOld;        // handle to previous bitmap        
    int i;                  // loop counter                     
 
    // Create the Lines menu. Add it to the menu bar.  
 
    hmenu = GetMenu(hwnd); 
    hmenuLines = CreatePopupMenu(); 
    AppendMenu(hmenu, MF_STRING | MF_POPUP, 
        (UINT) hmenuLines, "&Lines"); 
 
    // Create a brush for the menu-item background color.  
 
    crMenuClr = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crMenuClr); 
 
    // Create a compatible device context for the line bitmaps, 
    // and then select the background brush into it. 
 
    hdcMain = GetDC(hwnd); 
    hdcLines = CreateCompatibleDC(hdcMain); 
    hbrOld = SelectObject(hdcLines, hbrBackground); 
 
    // Get the dimensions of the check-mark bitmap. The width of 
    // the line bitmaps will be five times the width of the 
    // check-mark bitmap. 
 
    wLineX = GetSystemMetrics(SM_CXMENUCHECK) * (WORD) 5; 
    wLineY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    // Create the bitmaps and select them, one at a time, into the 
    // compatible device context. Initialize each bitmap by 
    // filling it with the menu-item background color. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        phbmp[i] = CreateCompatibleBitmap(hdcMain, wLineX, wLineY); 
        if (i == 0) 
            hbmpOld = SelectObject(hdcLines, phbmp[i]); 
        else 
            SelectObject(hdcLines, phbmp[i]); 
        ExtFloodFill(hdcLines, 0, 0, crMenuClr, FLOODFILLBORDER); 
    } 
 
    // Create the pens.  
 
    phpen[0] = CreatePen(PS_SOLID, 1, RGB(0, 0, 0)); 
    phpen[1] = CreatePen(PS_DOT, 1, RGB(0, 0, 0)); 
    phpen[2] = CreatePen(PS_DASH, 1, RGB(0, 0, 0)); 
    phpen[3] = CreatePen(PS_DASHDOT, 1, RGB(0, 0, 0)); 
    phpen[4] = CreatePen(PS_DASHDOTDOT, 1, RGB(0, 0, 0)); 
 
    // Select a pen and a bitmap into the compatible device 
    // context, draw a line into the bitmap, and then append 
    // the bitmap as an item in the Lines menu. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        SelectObject(hdcLines, phbmp[i]); 
        SelectObject(hdcLines, phpen[i]); 
        MoveToEx(hdcLines, 0, wLineY / 2, NULL); 
        LineTo(hdcLines, wLineX, wLineY / 2); 
        AppendMenu(hmenuLines, MF_BITMAP, i + 1, 
            (LPCTSTR) phbmp[i]); 
    } 
 
    // Release the main window's device context and destroy the 
    // compatible device context. Also, destroy the background 
    // brush. 
 
    ReleaseDC(hwnd, hdcMain); 
    SelectObject(hdcLines, hbrOld); 
    DeleteObject(hbrBackground); 
    SelectObject(hdcLines, hbmpOld); 
    DeleteDC(hdcLines); 
 
    return; 
} 
```



### <a name="example-of-menu-item-bitmaps"></a>Esempio di Menu-Item bitmap

L'esempio in questo argomento crea due menu, ognuno dei quali contiene diverse voci di menu bitmap. Per ogni menu, l'applicazione aggiunge un nome di menu corrispondente alla barra dei menu della finestra principale.

Il primo menu contiene voci di menu che mostrano ognuno dei tre tipi di grafico: torta, linea e barra. Le bitmap per queste voci di menu sono definite come risorse e vengono caricate usando la [**funzione LoadBitmap.**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) Associato a questo menu è un nome di menu "Grafico" sulla barra dei menu.

Il secondo menu contiene voci di menu che mostrano ognuno dei cinque stili di riga usati con la funzione [**CreatePen:**](/windows/desktop/api/wingdi/nf-wingdi-createpen) **PS \_ SOLID,** **PS \_ DASH,** **PS \_ DOT,** **PS \_ DASHDOT** e **PS \_ DASHDOTDOT.** L'applicazione crea le bitmap per queste voci di menu in fase di esecuzione usando le funzioni di disegno GDI. Associato a questo menu è un nome di menu **Righe** sulla barra dei menu.

Nella routine della finestra dell'applicazione sono definite due matrici statiche di handle bitmap. Una matrice contiene gli handle delle tre bitmap usate per **il** menu Grafico. L'altra contiene gli handle delle cinque bitmap usate per il menu **Righe.** Quando si elabora [**il messaggio WM \_ CREATE,**](/windows/desktop/winmsg/wm-create) la routine della finestra carica le bitmap del grafico, crea le bitmap delle linee e quindi aggiunge le voci di menu corrispondenti. Quando si elabora [**il messaggio WM \_ DESTROY,**](/windows/desktop/winmsg/wm-destroy) la routine della finestra elimina tutte le bitmap.

Di seguito sono riportate le parti rilevanti del file di intestazione dell'applicazione.


```
// Menu-item identifiers 
 
#define IDM_PIE         1 
#define IDM_LINE        2 
#define IDM_BAR         3 
 
#define IDM_SOLID       4 
#define IDM_DASH        5 
#define IDM_DASHDOT     6 
#define IDM_DASHDOTDOT  7 
 
// Number of items on the Chart and Lines menus 
 
#define C_LINES         5 
#define C_CHARTS        3 
 
// Bitmap resource identifiers 
 
#define IDB_PIE         1 
#define IDB_LINE        2 
#define IDB_BAR         3 
 
// Dimensions of the line bitmaps 
 
#define CX_LINEBMP      40 
#define CY_LINEBMP      10 
```



Di seguito sono riportate le parti rilevanti della procedura della finestra. La routine della finestra esegue la maggior parte dell'inizializzazione chiamando le funzioni LoadChartBitmaps, CreateLineBitmaps e AddBitmapMenu definite dall'applicazione, descritte più avanti in questo argomento.


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    static HBITMAP aHbmLines[C_LINES]; 
    static HBITMAP aHbmChart[C_CHARTS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
             // Call application-defined functions to load the 
             // bitmaps for the Chart menu and create those for 
             // the Lines menu. 
 
            LoadChartBitmaps(aHbmChart); 
            CreateLineBitmaps(aHbmLines); 
 
             // Call an application-defined function to create 
             // menus containing the bitmap menu items. The function 
             // also adds a menu name to the window's menu bar. 
 
            AddBitmapMenu( 
                    hwnd,      // menu bar's owner window 
                    "&Chart",  // text of menu name on menu bar 
                    IDM_PIE,   // ID of first item on menu 
                    aHbmChart, // array of bitmap handles 
                    C_CHARTS   // number of items on menu 
                    ); 
            AddBitmapMenu(hwnd, "&Lines", IDM_SOLID, 
                    aHbmLines, C_LINES); 
            break; 
 
        case WM_DESTROY: 
            for (i = 0; i < C_LINES; i++) 
                DeleteObject(aHbmLines[i]); 
            for (i = 0; i < C_CHARTS; i++) 
                DeleteObject(aHbmChart[i]); 
            PostQuitMessage(0); 
            break; 
 
        // Process additional messages here. 
 
        default: 
            return (DefWindowProc(hwnd, uMsg, wParam, lParam)); 
    } 
    return 0; 
} 
```



La funzione LoadChartBitmaps definita dall'applicazione carica le risorse bitmap per il menu grafico chiamando la [**funzione LoadBitmap,**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) come indicato di seguito.


```
VOID WINAPI LoadChartBitmaps(HBITMAP *paHbm) 
{ 
    paHbm[0] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_PIE)); 
    paHbm[1] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_LINE)); 
    paHbm[2] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_BAR)); 
} 
```



La funzione CreateLineBitmaps definita dall'applicazione crea le bitmap per il menu Linee usando le funzioni di disegno GDI. La funzione crea un contesto di dispositivo di memoria con le stesse proprietà del controller di dominio della finestra del desktop. Per ogni stile di linea, la funzione crea una bitmap, la seleziona nel controller di dominio di memoria e disegna al suo interno.


```
VOID WINAPI CreateLineBitmaps(HBITMAP *paHbm) 
{ 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
    COLORREF clrMenu = GetSysColor(COLOR_MENU); 
    HBRUSH hbrOld; 
    HPEN hpenOld; 
    HBITMAP hbmOld; 
    int fnDrawMode; 
    int i; 
 
     // Create a brush using the menu background color, 
     // and select it into the memory DC. 
 
    hbrOld = SelectObject(hdcMem, CreateSolidBrush(clrMenu)); 
 
     // Create the bitmaps. Select each one into the memory 
     // DC that was created and draw in it. 
 
    for (i = 0; i < C_LINES; i++) 
    { 
        // Create the bitmap and select it into the DC. 
 
        paHbm[i] = CreateCompatibleBitmap(hdcDesktop, 
                CX_LINEBMP, CY_LINEBMP); 
        hbmOld = SelectObject(hdcMem, paHbm[i]); 
 
        // Fill the background using the brush. 
 
        PatBlt(hdcMem, 0, 0, CX_LINEBMP, CY_LINEBMP, PATCOPY); 
 
        // Create the pen and select it into the DC. 
 
        hpenOld = SelectObject(hdcMem, 
                CreatePen(PS_SOLID + i, 1, RGB(0, 0, 0))); 
 
         // Draw the line. To preserve the background color where 
         // the pen is white, use the R2_MASKPEN drawing mode. 
 
        fnDrawMode = SetROP2(hdcMem, R2_MASKPEN); 
        MoveToEx(hdcMem, 0, CY_LINEBMP / 2, NULL); 
        LineTo(hdcMem, CX_LINEBMP, CY_LINEBMP / 2); 
        SetROP2(hdcMem, fnDrawMode); 
 
        // Delete the pen, and select the old pen and bitmap. 
 
        DeleteObject(SelectObject(hdcMem, hpenOld)); 
        SelectObject(hdcMem, hbmOld); 
    } 
 
    // Delete the brush and select the original brush. 
 
    DeleteObject(SelectObject(hdcMem, hbrOld)); 
 
    // Delete the memory DC and release the desktop DC. 
 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
} 
```



La funzione AddBitmapMenu definita dall'applicazione crea un menu e aggiunge il numero specificato di voci di menu bitmap. Aggiunge quindi un nome di menu corrispondente alla barra dei menu della finestra specificata.


```
VOID WINAPI AddBitmapMenu( 
        HWND hwnd,          // window that owned the menu bar 
        LPSTR lpszText,     // text of menu name on menu bar 
        UINT uID,           // ID of first bitmap menu item 
        HBITMAP *paHbm,     // bitmaps for the menu items 
        int cItems)         // number bitmap menu items 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup = CreatePopupMenu(); 
    MENUITEMINFO mii; 
    int i; 
 
    // Add the bitmap menu items to the menu. 
 
    for (i = 0; i < cItems; i++) 
    { 
        mii.fMask = MIIM_ID | MIIM_BITMAP | MIIM_DATA; 
        mii.wID = uID + i; 
        mii.hbmpItem = &paHbm[i]; 
        InsertMenuItem(hmenuPopup, i, TRUE, &mii); 
    } 
 
    // Add a menu name to the menu bar. 
 
    mii.fMask = MIIM_STRING | MIIM_DATA | MIIM_SUBMENU; 
    mii.fType = MFT_STRING; 
    mii.hSubMenu = hmenuPopup; 
    mii.dwTypeData = lpszText; 
    InsertMenuItem(hmenuBar, 
        GetMenuItemCount(hmenuBar), TRUE, &mii); 
} 
```



## <a name="creating-owner-drawn-menu-items"></a>Creazione di Owner-Drawn di menu

Se è necessario un controllo completo sull'aspetto di una voce di menu, è possibile usare una voce di menu disegnata dal proprietario nell'applicazione. Questa sezione descrive i passaggi necessari per creare e usare una voce di menu disegnata dal proprietario.

-   [Impostazione del flag Owner-Drawn](#setting-the-owner-drawn-flag)
-   [Menu disegnati dal proprietario e messaggio WM \_ MEASUREITEM](/windows)
-   [Menu disegnati dal proprietario e messaggio WM \_ DRAWITEM](/windows)
-   [Menu disegnati dal proprietario e messaggio WM \_ MENUCHAR](/windows)
-   [Impostazione dei tipi di carattere Menu-Item stringhe di testo](#setting-fonts-for-menu-item-text-strings)
-   [Esempio di Owner-Drawn menu](#example-of-owner-drawn-menu-items)

### <a name="setting-the-owner-drawn-flag"></a>Impostazione del flag Owner-Drawn

Non è possibile definire una voce di menu disegnata dal proprietario nel file di definizione delle risorse dell'applicazione. È invece necessario creare una nuova voce di menu o modificarne una esistente usando il flag di menu **MFT \_ OWNERDRAW.**

È possibile usare la [**funzione InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) o [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) per specificare una voce di menu disegnata dal proprietario. Usare **InsertMenuItem** per inserire una nuova voce di menu nella posizione specificata in una barra dei menu o in un menu. Usare **SetMenuItemInfo** per modificare il contenuto di un menu.

Quando si chiamano queste due funzioni, è necessario specificare un puntatore a una struttura [**MENUITEMINFO,**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) che specifica le proprietà della nuova voce di menu o le proprietà da modificare per una voce di menu esistente. Per impostare un elemento come elemento disegnato dal proprietario, specificare il valore **\_ FTYPE MIIM** per il membro **fMask** e il valore **MFT \_ OWNERDRAW** per il **membro fType.**

Impostando i membri appropriati della struttura [**MENUITEMINFO,**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) è possibile associare un valore definito dall'applicazione, denominato **dati elemento**, a ogni voce di menu. A tale scopo, specificare il **valore MIIM \_ DATA** per il membro **fMask** e il valore definito dall'applicazione per **il membro dwItemData.**

È possibile usare i dati degli elementi con qualsiasi tipo di voce di menu, ma è particolarmente utile per le voci disegnate dal proprietario. Si supponga, ad esempio, che una struttura contenga informazioni usate per disegnare una voce di menu. Un'applicazione potrebbe usare i dati dell'elemento per una voce di menu per archiviare un puntatore alla struttura . I dati dell'elemento vengono inviati alla finestra proprietaria del menu con i [**messaggi WM \_ MEASUREITEM**](../controls/wm-measureitem.md) [**e WM \_ DRAWITEM.**](../controls/wm-drawitem.md) Per recuperare i dati dell'elemento per un menu in qualsiasi momento, usare la [**funzione GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)

Le applicazioni scritte per le versioni precedenti del sistema possono continuare a chiamare [**AppendMenu,**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)o [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) per assegnare il flag **MF \_ OWNERDRAW** a una voce di menu disegnata dal proprietario.

Quando si chiama una di queste tre funzioni, è possibile passare un valore come *parametro lpNewItem.* Questo valore può rappresentare qualsiasi informazione significativa per l'applicazione e che sarà disponibile per l'applicazione quando l'elemento deve essere visualizzato. Ad esempio, il valore può contenere un puntatore a una struttura . la struttura , a sua volta, potrebbe contenere una stringa di testo e un handle per il tipo di carattere logico che verrà utilizzato dall'applicazione per disegnare la stringa.

### <a name="owner-drawn-menus-and-the-wm_measureitem-message"></a>Owner-Drawn menu e il messaggio WM \_ MEASUREITEM

Prima che il sistema visualizzi una voce di menu disegnata dal proprietario per la prima volta, invia il messaggio [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) alla routine della finestra proprietaria del menu dell'elemento. Questo messaggio contiene un puntatore a [**una struttura MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) che identifica l'elemento e contiene i dati dell'elemento assegnati da un'applicazione. La routine della finestra deve riempire i **membri itemWidth** e **itemHeight** della struttura prima di restituire dall'elaborazione del messaggio. Il sistema usa le informazioni in questi membri durante la creazione del rettangolo di delimitazione in cui un'applicazione disegna la voce di menu. Usa anche le informazioni per rilevare quando l'utente sceglie l'elemento.

### <a name="owner-drawn-menus-and-the-wm_drawitem-message"></a>Owner-Drawn menu e il messaggio WM \_ DRAWITEM

Ogni volta che l'elemento deve essere disegnato, ad esempio quando viene visualizzato per la prima volta o quando l'utente lo seleziona, il sistema invia il messaggio [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) alla routine della finestra della finestra proprietaria del menu. Questo messaggio contiene un puntatore a una [**struttura DRAWITEMSTRUCT,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) che contiene informazioni sull'elemento, inclusi i dati dell'elemento che un'applicazione potrebbe aver assegnato. **INOLTRE, DRAWITEMSTRUCT** contiene flag che indicano lo stato dell'elemento ,ad esempio se è in grigio o selezionato, nonché un rettangolo di delimitazione e un contesto di dispositivo che l'applicazione usa per disegnare l'elemento.

Un'applicazione deve eseguire le operazioni seguenti durante l'elaborazione [**del messaggio WM \_ DRAWITEM:**](../controls/wm-drawitem.md)

-   Determinare il tipo di disegno necessario. A tale scopo, controllare il **membro itemAction** della [**struttura DRAWITEMSTRUCT.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
-   Disegnare la voce di menu in modo appropriato, usando il rettangolo di delimitazione e il contesto di dispositivo ottenuti dalla [**struttura DRAWITEMSTRUCT.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) L'applicazione deve disegnare solo all'interno del rettangolo di delimitazione. Per motivi di prestazioni, il sistema non ritaglia parti dell'immagine disegnate all'esterno del rettangolo.
-   Ripristinare tutti gli oggetti GDI selezionati per il contesto di dispositivo della voce di menu.

Se l'utente seleziona la voce di menu, il sistema imposta il membro **itemAction** della [**struttura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) sul valore **ODA \_ SELECT** e imposta il **valore ODS \_ SELECTED** nel **membro itemState.** Questo è il segnale di un'applicazione per ridisegnare la voce di menu per indicare che è selezionata.

### <a name="owner-drawn-menus-and-the-wm_menuchar-message"></a>Owner-Drawn menu e il messaggio WM \_ MENUCHAR

I menu diversi dai menu disegnati dal proprietario possono specificare un menu mnemotico inserendo un carattere di sottolineatura accanto a un carattere nella stringa di menu. In questo modo l'utente può selezionare il menu premendo ALT e premendo il carattere mnemoico del menu. Nei menu disegnati dal proprietario, tuttavia, non è possibile specificare un menu mnemoico in questo modo. Al contrario, l'applicazione deve elaborare il [**messaggio WM \_ MENUCHAR**](wm-menuchar.md) per fornire menu disegnati dal proprietario con menu mnemonici.

Il [**messaggio WM \_ MENUCHAR**](wm-menuchar.md) viene inviato quando l'utente tipizza un menu mnemotico che non corrisponde a nessuno dei caratteri mnemoici predefiniti del menu corrente. Il valore contenuto in *wParam* specifica il carattere ASCII corrispondente al tasto premuto dall'utente con il tasto ALT. La parola di ordine basso *di wParam* specifica il tipo di menu selezionato e può essere uno dei valori seguenti:

-   **MF \_ POPUP** se il menu corrente è un sottomenu.
-   **MF \_ SYSMENU se** il menu è il menu di sistema.

La parola più alta di *wParam* contiene l'handle di menu per il menu corrente. La finestra con i menu disegnati dal proprietario può elaborare [**WM \_ MENUCHAR**](wm-menuchar.md) come segue:


```
   case WM_MENUCHAR:
      nIndex = Determine index of menu item to be selected from
               character that was typed and handle to the current
               menu.
      return MAKELRESULT(nIndex, 2);
```



I due valori nella parola più alta del valore restituito informano il sistema che la parola di ordine più basso del valore restituito contiene l'indice in base zero della voce di menu da selezionare.

Le costanti seguenti corrispondono ai possibili valori restituiti dal [**messaggio WM \_ MENUCHAR.**](wm-menuchar.md)



| Costante         | Valore | Significato                                                                                                                                                       |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MNC \_ IGNORE**  | 0     | Il sistema deve rimuovere il carattere che l'utente ha premuto e creare un breve segnale acustico sull'altoparlante del sistema.                                                       |
| **MNC \_ CLOSE**   | 1     | Il sistema deve chiudere il menu attivo.                                                                                                                      |
| **MNC \_ EXECUTE** | 2     | Il sistema deve scegliere l'elemento specificato nella parola di ordine basso del valore restituito. La finestra proprietaria riceve un [**messaggio WM \_ COMMAND.**](wm-command.md) |
| **MNC \_ SELECT**  | 3     | Il sistema deve selezionare l'elemento specificato nella parola di ordine basso del valore restituito.                                                                        |



 

### <a name="setting-fonts-for-menu-item-text-strings"></a>Impostazione dei tipi di carattere Menu-Item stringhe di testo

Questo argomento contiene un esempio di un'applicazione che usa voci di menu disegnate dal proprietario in un menu. Il menu contiene voci che impostano gli attributi del tipo di carattere corrente e gli elementi vengono visualizzati usando l'attributo del tipo di carattere appropriato.

Ecco come viene definito il menu nel file di definizione delle risorse. Si noti che le stringhe per le voci di menu Regular, Bold, Italic e Underline vengono assegnate in fase di esecuzione, quindi le relative stringhe sono vuote nel file di definizione delle risorse.


```
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "",    IDM_REGULAR 
        MENUITEM SEPARATOR 
        MENUITEM    "",    IDM_BOLD 
        MENUITEM    "",    IDM_ITALIC 
        MENUITEM    "",    IDM_ULINE 
    END 
END 
```



La procedura della finestra dell'applicazione elabora i messaggi coinvolti nell'uso di voci di menu disegnate dal proprietario. L'applicazione usa [**il messaggio WM \_ CREATE**](/windows/desktop/winmsg/wm-create) per eseguire le operazioni seguenti:

-   Impostare il flag **MF \_ OWNERDRAW** per le voci di menu.
-   Impostare le stringhe di testo per le voci di menu.
-   Ottenere gli handle dei tipi di carattere usati per disegnare gli elementi.
-   Ottenere i valori di colore di testo e sfondo per le voci di menu selezionate.

Le stringhe di testo e gli handle del tipo di carattere vengono archiviati in una matrice di strutture MYITEM definite dall'applicazione. La funzione GetAFont definita dall'applicazione crea un tipo di carattere che corrisponde all'attributo del tipo di carattere specificato e restituisce un handle per il tipo di carattere. Gli handle vengono distrutti durante l'elaborazione del [**messaggio WM \_ DESTROY.**](/windows/desktop/winmsg/wm-destroy)

Durante l'elaborazione del [**messaggio WM \_ MEASUREITEM,**](../controls/wm-measureitem.md) l'esempio ottiene la larghezza e l'altezza di una stringa di voce di menu e copia questi valori nella [**struttura MEASUREITEMSTRUCT.**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) Il sistema usa i valori di larghezza e altezza per calcolare le dimensioni del menu.

Durante l'elaborazione del [**messaggio WM \_ DRAWITEM,**](../controls/wm-drawitem.md) la stringa della voce di menu viene disegnata con spazio accanto alla stringa per la bitmap del segno di spunta. Se l'utente seleziona l'elemento, per disegnare l'elemento vengono usati il testo e i colori di sfondo selezionati.


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    typedef struct _MYITEM 
    { 
        HFONT hfont; 
        LPSTR psz; 
    } MYITEM;             // structure for item font and string  
 
    MYITEM *pmyitem;      // pointer to item's font and string        
    static MYITEM myitem[CITEMS];   // array of MYITEMS               
    static HMENU hmenu;             // handle to main menu            
    static COLORREF crSelText;  // text color of selected item        
    static COLORREF crSelBkgnd; // background color of selected item  
    COLORREF crText;            // text color of unselected item      
    COLORREF crBkgnd;           // background color unselected item   
    LPMEASUREITEMSTRUCT lpmis;  // pointer to item of data             
    LPDRAWITEMSTRUCT lpdis;     // pointer to item drawing data        
    HDC hdc;                    // handle to screen DC                
    SIZE size;                  // menu-item text extents             
    WORD wCheckX;               // check-mark width                   
    int nTextX;                 // width of menu item                 
    int nTextY;                 // height of menu item                
    int i;                      // loop counter                       
    HFONT hfontOld;             // handle to old font                 
    BOOL fSelected = FALSE;     // menu-item selection flag
    size_t * pcch;
    HRESULT hResult;           
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Modify the Regular, Bold, Italic, and Underline 
            // menu items to make them owner-drawn items. Associate 
            // a MYITEM structure with each item to contain the 
            // string for and font handle to each item. 
 
            hmenu = GetMenu(hwnd); 
            ModifyMenu(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED | MF_OWNERDRAW, IDM_REGULAR, 
                (LPTSTR) &myitem[REGULAR]); 
            ModifyMenu(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_BOLD, (LPTSTR) &myitem[BOLD]); 
            ModifyMenu(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ITALIC, 
                (LPTSTR) &myitem[ITALIC]); 
            ModifyMenu(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ULINE, (LPTSTR) &myitem[ULINE]); 
 
            // Retrieve each item's font handle and copy it into 
            // the hfont member of each item's MYITEM structure. 
            // Also, copy each item's string into the structures. 
 
            myitem[REGULAR].hfont = GetAFont(REGULAR); 
            myitem[REGULAR].psz = "Regular"; 
            myitem[BOLD].hfont = GetAFont(BOLD); 
            myitem[BOLD].psz = "Bold"; 
            myitem[ITALIC].hfont = GetAFont(ITALIC); 
            myitem[ITALIC].psz = "Italic"; 
            myitem[ULINE].hfont = GetAFont(ULINE); 
            myitem[ULINE].psz = "Underline"; 
 
            // Retrieve the text and background colors of the 
            // selected menu text. 
 
            crSelText = GetSysColor(COLOR_HIGHLIGHTTEXT); 
            crSelBkgnd = GetSysColor(COLOR_HIGHLIGHT); 
 
            return 0; 
 
        case WM_MEASUREITEM: 
 
            // Retrieve a device context for the main window.  
 
            hdc = GetDC(hwnd); 
 
            // Retrieve pointers to the menu item's 
            // MEASUREITEMSTRUCT structure and MYITEM structure. 
 
            lpmis = (LPMEASUREITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpmis->itemData; 
 
            // Select the font associated with the item into 
            // the main window's device context. 
 
            hfontOld = SelectObject(hdc, pmyitem->hfont); 
 
            // Retrieve the width and height of the item's string, 
            // and then copy the width and height into the 
            // MEASUREITEMSTRUCT structure's itemWidth and 
            // itemHeight members.
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            GetTextExtentPoint32(hdc, pmyitem->psz, 
                *pcch, &size); 
            lpmis->itemWidth = size.cx; 
            lpmis->itemHeight = size.cy; 
 
            // Select the old font back into the device context, 
            // and then release the device context. 
 
            SelectObject(hdc, hfontOld); 
            ReleaseDC(hwnd, hdc); 
 
            return TRUE; 
 
            break; 
 
        case WM_DRAWITEM: 
 
            // Get pointers to the menu item's DRAWITEMSTRUCT 
            // structure and MYITEM structure. 
 
            lpdis = (LPDRAWITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpdis->itemData; 
 
            // If the user has selected the item, use the selected 
            // text and background colors to display the item. 
 
            if (lpdis->itemState & ODS_SELECTED) 
            { 
                crText = SetTextColor(lpdis->hDC, crSelText); 
                crBkgnd = SetBkColor(lpdis->hDC, crSelBkgnd); 
                fSelected = TRUE; 
            } 
 
            // Remember to leave space in the menu item for the 
            // check-mark bitmap. Retrieve the width of the bitmap 
            // and add it to the width of the menu item. 
 
            wCheckX = GetSystemMetrics(SM_CXMENUCHECK); 
            nTextX = wCheckX + lpdis->rcItem.left; 
            nTextY = lpdis->rcItem.top; 
 
            // Select the font associated with the item into the 
            // item's device context, and then draw the string. 
 
            hfontOld = SelectObject(lpdis->hDC, pmyitem->hfont);
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            ExtTextOut(lpdis->hDC, nTextX, nTextY, ETO_OPAQUE, 
                &lpdis->rcItem, pmyitem->psz, 
                *pcch, NULL); 
 
            // Select the previous font back into the device 
            // context. 
 
            SelectObject(lpdis->hDC, hfontOld); 
 
            // Return the text and background colors to their 
            // normal state (not selected). 
 
            if (fSelected) 
            { 
                SetTextColor(lpdis->hDC, crText); 
                SetBkColor(lpdis->hDC, crBkgnd); 
            } 
 
            return TRUE; 
 
        // Process other messages.  
 
        case WM_DESTROY: 
 
            // Destroy the menu items' font handles.  
 
            for (i = 0; i < CITEMS; i++) 
                DeleteObject(myitem[i].hfont); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HFONT GetAFont(int fnFont) 
{ 
    static LOGFONT lf;  // structure for font information  
 
    // Get a handle to the ANSI fixed-pitch font, and copy 
    // information about the font to a LOGFONT structure. 
 
    GetObject(GetStockObject(ANSI_FIXED_FONT), sizeof(LOGFONT), 
        &lf); 
 
    // Set the font attributes, as appropriate.  
 
    if (fnFont == BOLD) 
        lf.lfWeight = FW_BOLD; 
    else 
        lf.lfWeight = FW_NORMAL; 
 
    lf.lfItalic = (fnFont == ITALIC); 
    lf.lfItalic = (fnFont == ULINE); 
 
    // Create the font, and then return its handle.  
 
    return CreateFont(lf.lfHeight, lf.lfWidth, 
        lf.lfEscapement, lf.lfOrientation, lf.lfWeight, 
        lf.lfItalic, lf.lfUnderline, lf.lfStrikeOut, lf.lfCharSet, 
        lf.lfOutPrecision, lf.lfClipPrecision, lf.lfQuality, 
        lf.lfPitchAndFamily, lf.lfFaceName); 
} 
```



### <a name="example-of-owner-drawn-menu-items"></a>Esempio di Owner-Drawn menu

L'esempio in questo argomento usa voci di menu disegnate dal proprietario in un menu. Le voci di menu selezionano attributi di carattere specifici e l'applicazione visualizza ogni voce di menu usando un tipo di carattere con l'attributo corrispondente. Ad esempio, la voce di menu **Corsivo** viene visualizzata in corsivo. Il **nome** del menu Carattere sulla barra dei menu apre il menu.

La barra dei menu e il menu a discesa sono definiti inizialmente da una risorsa modello di menu estesa. Poiché un modello di menu non può specificare voci disegnate dal proprietario, inizialmente il menu contiene quattro voci di menu di testo con le stringhe seguenti: "Regular", "Bold", "Italic" e "Underline". La procedura della finestra dell'applicazione le modifica in elementi creati dal proprietario quando elabora il [**messaggio WM \_ CREATE.**](/windows/desktop/winmsg/wm-create) Quando riceve il messaggio **WM \_ CREATE,** la routine della finestra chiama la funzione OnCreate definita dall'applicazione, che esegue i passaggi seguenti per ogni voce di menu:

-   Alloca una struttura MYITEM definita dall'applicazione.
-   Ottiene il testo della voce di menu e lo salva nella struttura MYITEM definita dall'applicazione.
-   Crea il tipo di carattere utilizzato per visualizzare la voce di menu e salva il relativo handle nella struttura MYITEM definita dall'applicazione.
-   Modifica il tipo di voce di menu **in MFT \_ OWNERDRAW** e salva un puntatore alla struttura MYITEM definita dall'applicazione come dati dell'elemento.

Poiché un puntatore a ogni struttura MYITEM definita dall'applicazione viene salvato come dati dell'elemento, viene passato alla routine della finestra insieme ai messaggi [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) e [**WM \_ DRAWITEM**](../controls/wm-drawitem.md) per la voce di menu corrispondente. Il puntatore è contenuto nel **membro itemData** delle strutture [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) e [**DRAWITEMSTRUCT.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)

Alla prima visualizzazione, viene inviato un messaggio [**WM \_ MEASUREITEM**](../controls/wm-measureitem.md) per ogni voce di menu disegnata dal proprietario. L'applicazione elabora questo messaggio selezionando il tipo di carattere per la voce di menu in un contesto di dispositivo e quindi determinando lo spazio necessario per visualizzare il testo della voce di menu in tale tipo di carattere. Il tipo di carattere e il testo della voce di menu sono entrambi specificati dalla struttura della voce di menu `MYITEM` (la struttura definita dall'applicazione). L'applicazione determina le dimensioni del testo usando la [**funzione GetTextExtentPoint32.**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a)

La routine della finestra elabora il [**messaggio WM \_ DRAWITEM**](../controls/wm-drawitem.md) visualizzando il testo della voce di menu nel tipo di carattere appropriato. Il tipo di carattere e il testo della voce di menu sono entrambi specificati dalla struttura della voce di `MYITEM` menu. L'applicazione seleziona i colori del testo e dello sfondo appropriati allo stato della voce di menu.

La procedura della finestra elabora il messaggio [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy) per eliminare i tipi di carattere e liberare memoria. L'applicazione elimina il tipo di carattere e libera la struttura MYITEM definita dall'applicazione per ogni voce di menu.

Di seguito sono riportate le parti rilevanti del file di intestazione dell'applicazione.


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_REGULAR   11 
#define IDM_BOLD      12 
#define IDM_ITALIC    13 
#define IDM_UNDERLINE 14 
 
// Structure associated with menu items 
 
typedef struct tagMYITEM 
{ 
    HFONT hfont; 
    int   cchItemText; 
    char  szItemText[1]; 
} MYITEM; 
 
#define CCH_MAXITEMTEXT 256 
 
```



Di seguito sono riportate le parti rilevanti della routine della finestra dell'applicazione e delle funzioni associate.


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_MEASUREITEM: 
            OnMeasureItem(hwnd, (LPMEASUREITEMSTRUCT) lParam); 
            return TRUE; 
 
        case WM_DRAWITEM: 
            OnDrawItem(hwnd, (LPDRAWITEMSTRUCT) lParam); 
            return TRUE; 
 
        // Additional message processing goes here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Modify each menu item. Assume that the IDs IDM_REGULAR 
    // through IDM_UNDERLINE are consecutive numbers. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
         // Allocate an item structure, leaving space for a 
         // string of up to CCH_MAXITEMTEXT characters. 
 
        pMyItem = (MYITEM *) LocalAlloc(LMEM_FIXED, 
                sizeof(MYITEM) + CCH_MAXITEMTEXT); 
 
        // Save the item text in the item structure. 
 
        mii.fMask = MIIM_STRING; 
        mii.dwTypeData = pMyItem->szItemText; 
        mii.cch = CCH_MAXITEMTEXT; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem->cchItemText = mii.cch; 
 
        // Reallocate the structure to the minimum required size. 
 
        pMyItem = (MYITEM *) LocalReAlloc(pMyItem, 
                sizeof(MYITEM) + mii.cch, LMEM_MOVEABLE); 
 
        // Create the font used to draw the item. 
 
        pMyItem->hfont = CreateMenuItemFont(uID); 
 
        // Change the item to an owner-drawn item, and save 
        // the address of the item structure as item data. 
 
        mii.fMask = MIIM_FTYPE | MIIM_DATA; 
        mii.fType = MFT_OWNERDRAW; 
        mii.dwItemData = (ULONG_PTR) pMyItem; 
        SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
    } 
    return TRUE; 
} 
 
HFONT CreateMenuItemFont(UINT uID) 
{ 
    LOGFONT lf;
    HRESULT hr; 
 
    ZeroMemory(&lf, sizeof(lf)); 
    lf.lfHeight = 20; 
    hr = StringCchCopy(lf.lfFaceName, 32, "Times New Roman");
    if (FAILED(hr))
    {
    // TODO: writer error handler
    } 
 
    switch (uID) 
    { 
        case IDM_BOLD: 
            lf.lfWeight = FW_HEAVY; 
            break; 
 
        case IDM_ITALIC: 
            lf.lfItalic = TRUE; 
            break; 
 
        case IDM_UNDERLINE: 
            lf.lfUnderline = TRUE; 
            break; 
    } 
    return CreateFontIndirect(&lf); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get  
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Free resources associated with each menu item. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
        // Get the item data. 
 
        mii.fMask = MIIM_DATA; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem = (MYITEM *) mii.dwItemData; 
 
        // Destroy the font and free the item structure. 
 
        DeleteObject(pMyItem->hfont); 
        LocalFree(pMyItem); 
    } 
} 
 
VOID WINAPI OnMeasureItem(HWND hwnd, LPMEASUREITEMSTRUCT lpmis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpmis->itemData; 
    HDC hdc = GetDC(hwnd); 
    HFONT hfntOld = (HFONT)SelectObject(hdc, pMyItem->hfont); 
    SIZE size; 
 
    GetTextExtentPoint32(hdc, pMyItem->szItemText, 
            pMyItem->cchItemText, &size); 
 
    lpmis->itemWidth = size.cx; 
    lpmis->itemHeight = size.cy; 
 
    SelectObject(hdc, hfntOld); 
    ReleaseDC(hwnd, hdc); 
} 
 
VOID WINAPI OnDrawItem(HWND hwnd, LPDRAWITEMSTRUCT lpdis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpdis->itemData; 
    COLORREF clrPrevText, clrPrevBkgnd; 
    HFONT hfntPrev; 
    int x, y; 
 
    // Set the appropriate foreground and background colors. 
 
    if (lpdis->itemState & ODS_SELECTED) 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHTTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHT)); 
    } 
    else 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_MENUTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_MENU)); 
    } 
 
    // Determine where to draw and leave space for a check mark. 
 
    x = lpdis->rcItem.left; 
    y = lpdis->rcItem.top; 
    x += GetSystemMetrics(SM_CXMENUCHECK); 
 
    // Select the font and draw the text. 
 
    hfntPrev = (HFONT)SelectObject(lpdis->hDC, pMyItem->hfont); 
    ExtTextOut(lpdis->hDC, x, y, ETO_OPAQUE, 
            &lpdis->rcItem, pMyItem->szItemText, 
            pMyItem->cchItemText, NULL); 
 
    // Restore the original font and colors. 
 
    SelectObject(lpdis->hDC, hfntPrev); 
    SetTextColor(lpdis->hDC, clrPrevText); 
    SetBkColor(lpdis->hDC, clrPrevBkgnd); 
} 
```



## <a name="using-custom-check-mark-bitmaps"></a>Uso di bitmap con segno di spunta personalizzato

Il sistema fornisce una bitmap di segno di spunta predefinita per la visualizzazione accanto a una voce di menu selezionata. È possibile personalizzare una singola voce di menu fornendo una coppia di bitmap per sostituire la bitmap del segno di spunta predefinita. Il sistema visualizza una bitmap quando l'elemento è selezionato e l'altro quando è chiaro. In questa sezione vengono descritti i passaggi necessari per la creazione e l'uso di bitmap con segno di spunta personalizzato.

-   [Creazione di bitmap con segno di spunta personalizzato](#creating-custom-check-mark-bitmaps)
-   [Associazione di bitmap a una voce di menu](#associating-bitmaps-with-a-menu-item)
-   [Impostazione dell'attributo di segno di spunta](#setting-the-check-mark-attribute)
-   [Simulazione di caselle di controllo in un menu](#simulating-check-boxes-in-a-menu)
-   [Esempio di uso di bitmap con segno di spunta personalizzato](#example-of-using-custom-check-mark-bitmaps)

### <a name="creating-custom-check-mark-bitmaps"></a>Creazione di bitmap con segno di spunta personalizzato

Una bitmap del segno di spunta personalizzata deve avere le stesse dimensioni della bitmap del segno di spunta predefinita. È possibile recuperare le dimensioni predefinite del segno di spunta della bitmap chiamando la [**funzione GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) La parola in ordine basso del valore restituito di questa funzione specifica la larghezza. la parola di ordine alto specifica l'altezza.

È possibile usare le risorse bitmap per fornire bitmap con segno di spunta. Tuttavia, poiché le dimensioni della bitmap richieste variano a seconda del tipo di visualizzazione, potrebbe essere necessario ridimensionare la bitmap in fase di esecuzione usando la [**funzione StretchBlt.**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) A seconda della bitmap, la distorsione causata dal ridimensionamento potrebbe produrre risultati inaccettabili.

Anziché usare una risorsa bitmap, è possibile creare una bitmap in fase di esecuzione usando le funzioni GDI.

**Per creare una bitmap in fase di esecuzione**

1.  Usare la [**funzione CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) per creare un contesto di dispositivo compatibile con quello usato dalla finestra principale dell'applicazione.

    Il parametro *hdc della* funzione può specificare **NULL** o il valore restituito dalla funzione. [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) restituisce un handle al contesto di dispositivo compatibile.

2.  Usare la [**funzione CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) per creare una bitmap compatibile con la finestra principale dell'applicazione.

    I parametri *nWidth* e *nHeight* di questa funzione impostano le dimensioni della bitmap. devono specificare le informazioni su larghezza e altezza restituite dalla [**funzione GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)

    > [!Note]  
    > È anche possibile usare la [**funzione CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) per creare una bitmap monocromatica.

     

3.  Usare la [**funzione SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) per selezionare la bitmap nel contesto di dispositivo compatibile.
4.  Usare le funzioni di disegno GDI, ad esempio [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) e [**LineTo,**](/windows/desktop/api/wingdi/nf-wingdi-lineto)per disegnare un'immagine nella bitmap o usare funzioni come [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) e [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) per copiare un'immagine nella bitmap.

Per altre informazioni, vedere [Bitmap .](/windows/desktop/gdi/bitmaps)

### <a name="associating-bitmaps-with-a-menu-item"></a>Associazione di bitmap a una voce di menu

È possibile associare una coppia di bitmap con segno di spunta a una voce di menu passando gli handle delle bitmap alla [**funzione SetMenuItemBitmaps.**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) Il *parametro hBitmapUnchecked* identifica la bitmap non crittografata e il parametro *hBitmapChecked* identifica la bitmap selezionata. Se si desidera rimuovere uno o entrambi i segni di spunta da una voce di menu, è possibile impostare il parametro *hBitmapUnchecked* o *hBitmapChecked* o entrambi su **NULL.**

### <a name="setting-the-check-mark-attribute"></a>Impostazione dell'attributo di segno di spunta

La [**funzione CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) imposta l'attributo di segno di spunta di una voce di menu su selezionato o deselezionato. È possibile specificare il **valore MF \_ CHECKED** per impostare l'attributo del segno di spunta su selected e il valore **MF \_ UNCHECKED** per impostarlo su clear.

È anche possibile impostare lo stato di controllo di una voce di menu usando la [**funzione SetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa)

A volte un gruppo di voci di menu rappresenta un set di opzioni che si escludono a vicenda. Usando la [**funzione CheckMenuRadioItem,**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) è possibile controllare una voce di menu rimuovendo contemporaneamente il segno di spunta da tutte le altre voci di menu nel gruppo.

### <a name="simulating-check-boxes-in-a-menu"></a>Simulazione di caselle di controllo in un menu

Questo argomento contiene un esempio che illustra come simulare le caselle di controllo in un menu. L'esempio contiene un menu Carattere le cui voci consentono all'utente di impostare gli attributi grassetto, corsivo e sottolineatura del tipo di carattere corrente. Quando un attributo del tipo di carattere è attivo, nella casella di controllo accanto alla voce di menu corrispondente viene visualizzato un segno di spunta. In caso contrario, accanto all'elemento viene visualizzata una casella di controllo vuota.

L'esempio sostituisce la bitmap con segno di spunta predefinita con due bitmap: una bitmap con una casella di controllo selezionata e la bitmap con una casella vuota. La bitmap della casella di controllo selezionata viene visualizzata accanto alla voce di menu Grassetto, Corsivo o Sottolineatura quando l'attributo di segno di spunta dell'elemento è impostato su **MF \_ CHECKED**. La bitmap della casella di controllo vuota o deselezionata viene visualizzata quando l'attributo del segno di spunta è impostato su **MF \_ UNCHECKED**.

Il sistema fornisce una bitmap predefinita che contiene le immagini usate per le caselle di controllo e i pulsanti di opzione. L'esempio isola le caselle di controllo selezionate e vuote, le copia in due bitmap separate e quindi le usa come bitmap selezionate e cancellate per gli elementi del **menu** Carattere.

Per recuperare un handle per la bitmap della casella di controllo definita dal sistema, nell'esempio viene chiamata la funzione [**LoadBitmap,**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) specificando **NULL** come parametro *hInstance* e **OBM \_ CHECKBOXES** come parametro *lpBitmapName.* Poiché le immagini nella bitmap hanno tutte le stesse dimensioni, l'esempio può isolarle dividendo la larghezza e l'altezza della bitmap per il numero di immagini nelle righe e nelle colonne.

La parte seguente di un file di definizione delle risorse mostra come vengono definite le voci di **menu** nel menu Carattere. Si noti che inizialmente non sono presenti attributi del tipo di carattere, quindi l'attributo del segno di spunta per l'elemento **Regular** è impostato su selected e, per impostazione predefinita, l'attributo check-mark degli elementi rimanenti è impostato su clear.


```
#include "men3.h" 
 
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "&Regular",     IDM_REGULAR, CHECKED 
        MENUITEM SEPARATOR 
        MENUITEM    "&Bold",        IDM_BOLD 
        MENUITEM    "&Italic",      IDM_ITALIC 
        MENUITEM    "&Underline",   IDM_ULINE 
    END 
END
```



Ecco il contenuto pertinente del file di intestazione dell'applicazione.


```
// Menu-item identifiers  
 
#define IDM_REGULAR 0x1 
#define IDM_BOLD    0x2 
#define IDM_ITALIC  0x4 
#define IDM_ULINE   0x8 
 
// Check-mark flags  
 
#define CHECK   1 
#define UNCHECK 2 
 
// Font-attribute mask  
 
#define ATTRIBMASK 0xe 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
HBITMAP GetMyCheckBitmaps(UINT); 
BYTE CheckOrUncheckMenuItem(BYTE, HMENU); 
```



Nell'esempio seguente vengono illustrate le parti della routine della finestra che creano le bitmap con segno di spunta. impostare l'attributo di segno di spunta delle voci di menu **Grassetto,** **Corsivo** **e Sottolineatura;** ed eliminano le bitmap con segno di spunta.


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HBITMAP hbmpCheck;   // handle to checked bitmap    
    static HBITMAP hbmpUncheck; // handle to unchecked bitmap  
    static HMENU hmenu;         // handle to main menu         
    BYTE fbFontAttrib;          // font-attribute flags        
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Call the application-defined GetMyCheckBitmaps 
            // function to get the predefined checked and 
            // unchecked check box bitmaps. 
 
            hbmpCheck = GetMyCheckBitmaps(CHECK); 
            hbmpUncheck = GetMyCheckBitmaps(UNCHECK); 
 
            // Set the checked and unchecked bitmaps for the menu 
            // items. 
 
            hmenu = GetMenu(hwndMain); 
            SetMenuItemBitmaps(hmenu, IDM_BOLD, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ITALIC, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ULINE, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the menu commands.  
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // CheckOrUncheckMenuItem is an application- 
                    // defined function that sets the menu item 
                    // checkmarks and returns the user-selected 
                    // font attributes. 
 
                    fbFontAttrib = CheckOrUncheckMenuItem( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // Set the font attributes.  
 
                    return 0; 
 
                // Process other command messages.  
 
                default: 
                    break; 
            } 
 
            break; 
 
        // Process other window messages.  
 
        case WM_DESTROY: 
 
            // Destroy the checked and unchecked bitmaps.  
 
            DeleteObject(hbmpCheck); 
            DeleteObject(hbmpUncheck); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HBITMAP GetMyCheckBitmaps(UINT fuCheck) 
{ 
    COLORREF crBackground;  // background color                  
    HBRUSH hbrBackground;   // background brush                  
    HBRUSH hbrTargetOld;    // original background brush         
    HDC hdcSource;          // source device context             
    HDC hdcTarget;          // target device context             
    HBITMAP hbmpCheckboxes; // handle to check-box bitmap        
    BITMAP bmCheckbox;      // structure for bitmap data         
    HBITMAP hbmpSourceOld;  // handle to original source bitmap  
    HBITMAP hbmpTargetOld;  // handle to original target bitmap  
    HBITMAP hbmpCheck;      // handle to check-mark bitmap       
    RECT rc;                // rectangle for check-box bitmap    
    WORD wBitmapX;          // width of check-mark bitmap        
    WORD wBitmapY;          // height of check-mark bitmap       
 
    // Get the menu background color and create a solid brush 
    // with that color. 
 
    crBackground = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crBackground); 
 
    // Create memory device contexts for the source and 
    // destination bitmaps. 
 
    hdcSource = CreateCompatibleDC((HDC) NULL); 
    hdcTarget = CreateCompatibleDC(hdcSource); 
 
    // Get the size of the system default check-mark bitmap and 
    // create a compatible bitmap of the same size. 
 
    wBitmapX = GetSystemMetrics(SM_CXMENUCHECK); 
    wBitmapY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    hbmpCheck = CreateCompatibleBitmap(hdcSource, wBitmapX, 
        wBitmapY); 
 
    // Select the background brush and bitmap into the target DC. 
 
    hbrTargetOld = SelectObject(hdcTarget, hbrBackground); 
    hbmpTargetOld = SelectObject(hdcTarget, hbmpCheck); 
 
    // Use the selected brush to initialize the background color 
    // of the bitmap in the target device context. 
 
    PatBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, PATCOPY); 
 
    // Load the predefined check box bitmaps and select it 
    // into the source DC. 
 
    hbmpCheckboxes = LoadBitmap((HINSTANCE) NULL, 
        (LPTSTR) OBM_CHECKBOXES); 
 
    hbmpSourceOld = SelectObject(hdcSource, hbmpCheckboxes); 
 
    // Fill a BITMAP structure with information about the 
    // check box bitmaps, and then find the upper-left corner of 
    // the unchecked check box or the checked check box. 
 
    GetObject(hbmpCheckboxes, sizeof(BITMAP), &bmCheckbox); 
 
    if (fuCheck == UNCHECK) 
    { 
        rc.left = 0; 
        rc.right = (bmCheckbox.bmWidth / 4); 
    } 
    else 
    { 
        rc.left = (bmCheckbox.bmWidth / 4); 
        rc.right = (bmCheckbox.bmWidth / 4) * 2; 
    } 
 
    rc.top = 0; 
    rc.bottom = (bmCheckbox.bmHeight / 3); 
 
    // Copy the appropriate bitmap into the target DC. If the 
    // check-box bitmap is larger than the default check-mark 
    // bitmap, use StretchBlt to make it fit; otherwise, just 
    // copy it. 
 
    if (((rc.right - rc.left) > (int) wBitmapX) || 
            ((rc.bottom - rc.top) > (int) wBitmapY)) 
    {
        StretchBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, 
            hdcSource, rc.left, rc.top, rc.right - rc.left, 
            rc.bottom - rc.top, SRCCOPY); 
    }
 
    else 
    {
        BitBlt(hdcTarget, 0, 0, rc.right - rc.left, 
            rc.bottom - rc.top, 
            hdcSource, rc.left, rc.top, SRCCOPY); 
    }
 
    // Select the old source and destination bitmaps into the 
    // source and destination DCs, and then delete the DCs and 
    // the background brush. 
 
    SelectObject(hdcSource, hbmpSourceOld); 
    SelectObject(hdcTarget, hbrTargetOld); 
    hbmpCheck = SelectObject(hdcTarget, hbmpTargetOld); 
 
    DeleteObject(hbrBackground); 
    DeleteObject(hdcSource); 
    DeleteObject(hdcTarget); 
 
    // Return a handle to the new check-mark bitmap.  
 
    return hbmpCheck; 
} 
 
 
BYTE CheckOrUncheckMenuItem(BYTE bMenuItemID, HMENU hmenu) 
{ 
    DWORD fdwMenu; 
    static BYTE fbAttributes; 
 
    switch (bMenuItemID) 
    { 
        case IDM_REGULAR: 
 
            // Whenever the Regular menu item is selected, add a 
            // check mark to it and then remove checkmarks from 
            // any font-attribute menu items. 
 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
            } 
            fbAttributes = IDM_REGULAR; 
            return fbAttributes; 
 
        case IDM_BOLD: 
        case IDM_ITALIC: 
        case IDM_ULINE: 
 
            // Toggle the check mark for the selected menu item and 
            // set the font attribute flags appropriately. 
 
            fdwMenu = GetMenuState(hmenu, (UINT) bMenuItemID, 
                MF_BYCOMMAND); 
            if (!(fdwMenu & MF_CHECKED)) 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes |= bMenuItemID; 
            }
            else 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes ^= bMenuItemID; 
            } 
 
            // If any font attributes are currently selected, 
            // remove the check mark from the Regular menu item; 
            // if no attributes are selected, add a check mark 
            // to the Regular menu item. 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes &= (BYTE) ~IDM_REGULAR; 
            }
            else 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes = IDM_REGULAR; 
            } 
 
            return fbAttributes; 
    } 
} 
```



### <a name="example-of-using-custom-check-mark-bitmaps"></a>Esempio di uso di bitmap con segno di spunta personalizzato

L'esempio in questo argomento assegna bitmap con segno di spunta personalizzate alle voci di menu in due menu. Le voci di menu nel primo menu specificano gli attributi dei caratteri: grassetto, corsivo e sottolineatura. Ogni voce di menu può essere selezionata o deselezionata. Per queste voci di menu, nell'esempio vengono utilizzate bitmap con segno di spunta simili agli stati selezionato e deselezionato di un controllo casella di controllo.

Le voci di menu nel secondo menu specificano le impostazioni di allineamento dei paragrafi: a sinistra, al centro e a destra. Viene selezionata solo una di queste voci di menu in qualsiasi momento. Per queste voci di menu, nell'esempio vengono utilizzate bitmap con segno di spunta simili agli stati selezionati e non crittografati di un controllo pulsante di opzione.

La routine della finestra elabora il [**messaggio WM \_ CREATE**](/windows/desktop/winmsg/wm-create) chiamando la funzione OnCreate definita dall'applicazione. `OnCreate`crea le quattro bitmap con segno di spunta e le assegna alle voci di menu appropriate usando la [**funzione SetMenuItemBitmaps.**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps)

Per creare ogni bitmap, OnCreate chiama la funzione CreateMenuBitmaps definita dall'applicazione, specificando un puntatore a una funzione di disegno specifica della bitmap. CreateMenuBitmaps crea una bitmap monocromatica delle dimensioni richieste, la seleziona in un contesto di dispositivo di memoria e cancella lo sfondo. Chiama quindi la funzione di disegno specificata per riempire in primo piano.

Le quattro funzioni di disegno definite dall'applicazione sono DrawCheck, DrawUncheck, **DrawRadioCheck** e DrawRadioUncheck. Disegnano un rettangolo con una X, un rettangolo vuoto, un'ellisse contenente un'ellisse riempita più piccola e un'ellisse vuota, rispettivamente.

La procedura della finestra elabora il [**messaggio WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy) eliminando le bitmap con segno di spunta. Recupera ogni handle bitmap usando la [**funzione GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) e quindi passa un handle alla funzione.

Quando l'utente sceglie una voce di menu, viene inviato [**un messaggio WM \_ COMMAND**](wm-command.md) alla finestra del proprietario. Per le voci di menu del menu **Carattere,** la routine della finestra chiama la funzione CheckCharacterItem definita dall'applicazione. Per le voci del menu **Paragrafo,** la routine della finestra chiama la funzione CheckParagraphItem definita dall'applicazione.

Ogni voce del menu **Carattere** può essere selezionata e cancellata in modo indipendente. Pertanto, CheckCharacterItem cambia semplicemente lo stato di controllo della voce di menu specificata. In primo luogo, la funzione chiama la [**funzione GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) per ottenere lo stato corrente della voce di menu. Passa quindi il flag **di stato MFS \_ CHECKED** e imposta il nuovo stato chiamando la [**funzione SetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa)

A differenza degli attributi di carattere, è possibile selezionare un solo allineamento di paragrafo alla volta. CheckParagraphItem controlla quindi la voce di menu specificata e rimuove il segno di spunta da tutte le altre voci del menu. A tale scopo, chiama la [**funzione CheckMenuRadioItem.**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem)

Di seguito sono riportate le parti rilevanti del file di intestazione dell'applicazione.


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_BOLD      11 
#define IDM_ITALIC    12 
#define IDM_UNDERLINE 13 
 
// Menu-item identifiers for the Paragraph menu 
 
#define IDM_PARAGRAPH 20 
#define IDM_LEFT      21 
#define IDM_CENTER    22 
#define IDM_RIGHT     23 
 
// Function-pointer type for drawing functions 
 
typedef VOID (WINAPI * DRAWFUNC)(HDC hdc, SIZE size); 
 
```



Di seguito sono riportate le parti rilevanti della routine della finestra dell'applicazione e le funzioni correlate.


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_UNDERLINE: 
                    CheckCharacterItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                case IDM_LEFT: 
                case IDM_CENTER: 
                case IDM_RIGHT: 
                    CheckParagraphItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                // Process other commands here. 
 
            } 
            break; 
 
        // Process other messages here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
VOID WINAPI CheckCharacterItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the state of the specified menu item. 
 
    mii.fMask = MIIM_STATE;    // information to get 
    GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
 
    // Toggle the checked state. 
 
    mii.fState ^= MFS_CHECKED; 
    SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
} 
 
VOID WINAPI CheckParagraphItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Check the specified item and uncheck all the others. 
 
    CheckMenuRadioItem( 
            hmenuPopup,         // handle to menu 
            IDM_LEFT,           // first item in range 
            IDM_RIGHT,          // last item in range 
            uID,                // item to check 
            MF_BYCOMMAND        // IDs, not positions 
            ); 
} 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    HBITMAP hbmChecked; 
    HBITMAP hbmUnchecked; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_BOLD; uID <= IDM_UNDERLINE; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Get a handle to the Paragraph pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawRadioCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawRadioUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_LEFT; uID <= IDM_RIGHT; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Initially check the IDM_LEFT paragraph item. 
 
    CheckMenuRadioItem(hmenuPopup, IDM_LEFT, IDM_RIGHT, 
            IDM_LEFT, MF_BYCOMMAND); 
    return TRUE; 
} 
 
HBITMAP WINAPI CreateMenuBitmap(DRAWFUNC lpfnDraw) 
{ 
    // Create a DC compatible with the desktop window's DC. 
 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
 
    // Determine the required bitmap size. 
 
    SIZE size = { GetSystemMetrics(SM_CXMENUCHECK), 
                  GetSystemMetrics(SM_CYMENUCHECK) }; 
 
    // Create a monochrome bitmap and select it. 
 
    HBITMAP hbm = CreateBitmap(size.cx, size.cy, 1, 1, NULL); 
    HBITMAP hbmOld = SelectObject(hdcMem, hbm); 
 
    // Erase the background and call the drawing function. 
 
    PatBlt(hdcMem, 0, 0, size.cx, size.cy, WHITENESS); 
    (*lpfnDraw)(hdcMem, size); 
 
    // Clean up. 
 
    SelectObject(hdcMem, hbmOld); 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
    return hbm; 
} 
 
VOID WINAPI DrawCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    MoveToEx(hdc, 0, 0, NULL); 
    LineTo(hdc, size.cx, size.cy); 
    MoveToEx(hdc, 0, size.cy - 1, NULL); 
    LineTo(hdc, size.cx - 1, 0); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, GetStockObject(BLACK_BRUSH)); 
    Ellipse(hdc, 2, 2, size.cx - 2, size.cy - 2); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_BOLD, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_LEFT, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
} 
```



 

 