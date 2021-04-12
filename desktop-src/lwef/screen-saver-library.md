---
title: Gestione degli screen saver
description: L'API Microsoft Win32 supporta applicazioni speciali denominate screen saver.
ms.assetid: cda5e690-71fe-4df7-b8a2-3a2ad65b1bfb
keywords:
- screen saver
- Pannello di controllo, screen saver
- ScreenSaverConfigureDialog
- file di definizione moduli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b7e0d0c177af2798b041fa12b4cc5793bf9be0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473019"
---
# <a name="handling-screen-savers"></a>Gestione degli screen saver

L'API Microsoft Win32 supporta applicazioni speciali denominate *screen saver*. Gli screen saver iniziano quando il mouse e la tastiera sono rimasti inattivi per un periodo di tempo specificato. Vengono usati per i due motivi seguenti:

-   Per proteggere una schermata dall'ustione fosforo causata da immagini statiche.
-   Per nascondere le informazioni riservate rimaste su una schermata.

Questo argomento è suddiviso nelle sezioni seguenti.

-   [Informazioni sugli screen saver](#about-screen-savers)
-   [Uso delle funzioni screen saver](#using-the-screen-saver-functions)
    -   [Creazione di uno screen saver](#creating-a-screen-saver)
    -   [Installazione di nuovi screen saver](#installing-new-screen-savers)
    -   [Aggiunta della Guida alla finestra di dialogo configurazione screen saver](#adding-help-to-the-screen-saver-configuration-dialog-box)

## <a name="about-screen-savers"></a>Informazioni sugli screen saver

L'applicazione desktop nel pannello di controllo di Windows consente agli utenti di eseguire una selezione da un elenco di screen saver, specificare la quantità di tempo che deve trascorrere prima che l'screen saver venga avviata, configurare gli screen saver e visualizzare i salvaschermi. Gli screen saver vengono caricati automaticamente all'avvio di Windows o quando un utente attiva il screen saver tramite il pannello di controllo.

Una volta scelto un screen saver, Windows monitora le sequenze di tasti e i movimenti del mouse, quindi avvia il screen saver dopo un periodo di inattività. Tuttavia, Windows non avvia il screen saver se sussistono le condizioni seguenti:

-   L'applicazione attiva non è un'applicazione basata su Windows.
-   È presente una finestra di training basata su computer (CBT).
-   L'applicazione attiva riceve il messaggio [WM \_ SYSCOMMAND](../menurc/wm-syscommand.md) con il parametro *wParam* impostato sul valore SC \_ SCREENSAVE, ma non passa il messaggio alla funzione [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) .

**Contesto di sicurezza dello screen saver**

Il contesto di sicurezza del screen saver dipende dal fatto che un utente sia connesso in modo interattivo. Se un utente è connesso in modo interattivo quando viene richiamato il screen saver, il screen saver viene eseguito nel contesto di sicurezza dell'utente interattivo. Se nessun utente è connesso, il contesto di sicurezza del screen saver dipende dalla versione di Windows in uso.

-   Windows XP e Windows 2000-screen saver vengono eseguiti nel contesto di LocalSystem con account con restrizioni.
-   Windows 2003-screen saver viene eseguito nel contesto di LocalService con tutti i privilegi rimossi e il gruppo Administrators è disabilitato.
-   Non si applica a Windows NT4.

Il contesto di sicurezza determina il livello delle operazioni con privilegi che possono essere eseguite da un screen saver.

**Windows Vista e versioni successive:** Se la protezione con password è abilitata dal criterio, l'screen saver viene avviata indipendentemente dall'operazione eseguita da un'applicazione con la \_ notifica SC SCREENSAVE.

Gli screen saver contengono funzioni esportate, definizioni di risorse e dichiarazioni di variabili specifiche. La libreria screen saver contiene la funzione **principale** e un altro codice di avvio necessario per un screen saver. All'avvio di un screen saver, il codice di avvio nella libreria screen saver crea una finestra a schermo intero. La classe della finestra per questa finestra è dichiarata come segue:


```
WNDCLASS cls; 
cls.hCursor        = NULL; 
cls.hIcon          = LoadIcon(hInst, MAKEINTATOM(ID_APP)); 
cls.lpszMenuName   = NULL; 
cls.lpszClassName  = "WindowsScreenSaverClass"; 
cls.hbrBackground  = GetStockObject(BLACK_BRUSH); 
cls.hInstance      = hInst; 
cls.style          = CS_VREDRAW  | CS_HREDRAW | CS_SAVEBITS | CS_DBLCLKS; 
cls.lpfnWndProc    = (WNDPROC) ScreenSaverProc; 
cls.cbWndExtra     = 0; 
cls.cbClsExtra     = 0;
```



Per creare una screen saver, la maggior parte degli sviluppatori crea un modulo di codice sorgente contenente tre funzioni obbligatorie e le collega alla libreria di screen saver. Un modulo screen saver è responsabile solo per la configurazione e per fornire effetti visivi.

Una delle tre funzioni obbligatorie in un modulo screen saver è [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc). Questa funzione elabora messaggi specifici e passa di nuovo i messaggi non elaborati alla libreria screen saver. Di seguito sono riportati alcuni dei messaggi tipici elaborati da **ScreenSaverProc**.



| Messaggio        | Significato                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| creazione di WM \_     | Recuperare tutti i dati di inizializzazione dal file di Regedit.ini. Impostare un timer di finestra per la finestra di screen saver. Eseguire qualsiasi altra inizializzazione richiesta.                                     |
| \_ERASEBKGND WM | Cancellare la finestra screen saver e prepararsi per le operazioni di disegno successive.                                                                                                               |
| \_timer WM      | Eseguire operazioni di disegno.                                                                                                                                                                |
| eliminazione di WM \_    | Elimina i timer creati quando l'applicazione ha elaborato il messaggio [WM \_ create](../winmsg/wm-create.md) . Eseguire eventuali operazioni di pulizia necessarie aggiuntive. |



 

[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) passa messaggi non elaborati alla libreria screen saver chiamando la funzione [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) . Nella tabella seguente viene descritto il modo in cui questa funzione elabora vari messaggi.



| Message         | Azione                                                                    |
|-----------------|---------------------------------------------------------------------------|
| \_cursore WM   | Impostare il cursore sul cursore null, rimuovendo il cursore dalla schermata.           |
| \_disegno WM       | Disegnare lo sfondo dello schermo.                                              |
| \_LBUTTONDOWN WM | Terminare il screen saver.                                               |
| \_MBUTTONDOWN WM | Terminare il screen saver.                                               |
| \_RBUTTONDOWN WM | Terminare il screen saver.                                               |
| KeyDown di WM \_     | Terminare il screen saver.                                               |
| MOUSEMOVE di WM \_   | Terminare il screen saver.                                               |
| \_attivazione WM    | Terminare il screen saver se il parametro *wParam* è impostato su **false**. |



 

La seconda funzione obbligatoria in un modulo screen saver è [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog). Questa funzione Visualizza una finestra di dialogo che consente all'utente di configurare il screen saver (un'applicazione deve fornire un modello di finestra di dialogo corrispondente). Windows consente di visualizzare la finestra di dialogo configurazione quando l'utente seleziona il pulsante di **installazione** nella finestra di dialogo screen saver del pannello di controllo.

La terza funzione obbligatoria in un modulo screen saver è [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses). Questa funzione deve essere chiamata da tutte le applicazioni screen saver. Tuttavia, le applicazioni che non necessitano di speciali finestre o controlli personalizzati nella finestra di dialogo di configurazione possono semplicemente restituire **true**. Per la registrazione delle classi di finestra corrispondenti, le applicazioni che richiedono controlli Windows o personalizzati speciali devono usare questa funzione.

Oltre alla creazione di un modulo che supporta le tre funzioni appena descritte, un screen saver deve fornire un'icona. Questa icona è visibile solo quando il screen saver viene eseguito come applicazione autonoma. (Per essere eseguito dal pannello di controllo, una screen saver deve avere l'estensione di file SCR; per essere eseguita come applicazione autonoma, è necessario che l'estensione del nome file sia exe). L'icona deve essere identificata nel file di risorse del screen saver dall'app Constant ID \_ , definita nel file di intestazione scrnsave. h.

Un requisito finale è una stringa di descrizione screen saver. Il file di risorse per un screen saver deve contenere una stringa visualizzata dal pannello di controllo come nome del screen saver. La stringa di descrizione deve essere la prima stringa nella tabella di stringhe del file di risorse (identificato con il valore ordinale 1). Tuttavia, la stringa di descrizione viene ignorata dal pannello di controllo se il screen saver ha un nome di file lungo. In tal caso, il nome del file verrà usato come stringa di descrizione.

## <a name="using-the-screen-saver-functions"></a>Uso delle funzioni screen saver

In questa sezione viene usato il codice di esempio tratto da un'applicazione screen saver per illustrare le attività seguenti:

-   [Creazione di uno screen saver](#creating-a-screen-saver)
-   [Installazione di nuovi screen saver](#installing-new-screen-savers)
-   [Aggiunta della Guida alla finestra di dialogo configurazione screen saver](#adding-help-to-the-screen-saver-configuration-dialog-box)

### <a name="creating-a-screen-saver"></a>Creazione di uno screen saver

A intervalli compresi tra 1 e 10 secondi, l'applicazione in questo esempio disegna la schermata con uno dei quattro colori seguenti: bianco, grigio chiaro, grigio scuro e nero. L'applicazione disegna la schermata ogni volta che riceve un messaggio [del \_ timer WM](../winmsg/wm-timer.md) . L'utente può regolare l'intervallo in corrispondenza del quale viene inviato il messaggio selezionando la finestra di dialogo di configurazione dell'applicazione e modificando una singola barra di scorrimento orizzontale.

### <a name="screen-saver-library"></a>Libreria screen saver

Le funzioni di screen saver statiche sono contenute nella libreria di screen saver. Sono disponibili due versioni della libreria, scrnsave. lib e Scrnsavw. lib. È necessario collegare il progetto a uno di questi. Scrnsave. lib viene usato per gli screen saver che usano caratteri ANSI e Scrnsavw. lib viene usato per gli screen saver che usano caratteri Unicode. Un screen saver collegato a Scrnsavw. lib verrà eseguito solo su piattaforme Windows che supportano Unicode, mentre una screen saver collegata a scrnsave. lib verrà eseguita su qualsiasi piattaforma Windows.

### <a name="supporting-the-configuration-dialog-box"></a>Supporto della finestra di dialogo di configurazione

La maggior parte degli screen saver fornisce una finestra di dialogo di configurazione che consente all'utente di specificare i dati di personalizzazione, ad esempio colori univoci, velocità di disegno, spessore linea, caratteri e così via. Per supportare la finestra di dialogo configurazione, l'applicazione deve fornire un modello di finestra di dialogo e deve supportare anche la funzione [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) . Di seguito è riportato il modello della finestra di dialogo per l'applicazione di esempio.


```
DLG_SCRNSAVECONFIGURE DIALOG 6, 18, 160, 63
LANGUAGE LANG_NEUTRAL, SUBLANG_NEUTRAL
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION | WS_SYSMENU
CAPTION "Sample Screen-Saver Setup"
FONT 8, "MS Shell Dlg"
BEGIN
    GROUPBOX      "Redraw Speed", 101, 0, 6, 98, 40
    SCROLLBAR     ID_SPEED, 5, 31, 89, 10
    LTEXT         "Fast", 103, 6, 21, 20, 8
    LTEXT         "Slow", 104, 75, 21, 20, 8
    PUSHBUTTON    "OK", ID_OK, 117, 10, 40, 14
    PUSHBUTTON    "Cancel", ID_CANCEL, 117, 32, 40, 14
END
```



È necessario definire la costante utilizzata per identificare il modello della finestra di dialogo usando il valore decimale 2003, come nell'esempio seguente:


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



Nell'esempio seguente viene illustrata la funzione [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) trovata nell'applicazione di esempio.


```
#define MINVEL  1                 // minimum redraw speed value     
#define MAXVEL  10                // maximum redraw speed value    
#define DEFVEL  5                 // default redraw speed value    
 
LONG    lSpeed = DEFVEL;          // redraw speed variable         
  
extern HINSTANCE hMainInstance;   // screen saver instance handle  
 
CHAR   szAppName[80];             // .ini section name             
CHAR   szTemp[20];                // temporary array of characters  
CHAR   szRedrawSpeed[ ] = "Redraw Speed";   // .ini speed entry 
CHAR   szIniFile[MAXFILELEN];     // .ini or registry file name  
 
BOOL WINAPI ScreenSaverConfigureDialog(hDlg, message, wParam, lParam) 
HWND     hDlg; 
UINT     message; 
DWORD    wParam; 
LONG     lParam; 
HRESULT  hr;
{ 
    static HWND hSpeed;   // handle to speed scroll bar 
    static HWND hOK;      // handle to OK push button  
 
    switch(message) 
    { 
        case WM_INITDIALOG: 
 
            // Retrieve the application name from the .rc file.  
            LoadString(hMainInstance, idsAppName, szAppName, 
                       80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, 
                       MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry. 
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // If the initialization file does not contain an entry 
            // for this screen saver, use the default value. 
            if(lSpeed > MAXVEL || lSpeed < MINVEL) 
                lSpeed = DEFVEL; 
 
            // Initialize the redraw speed scroll bar control.
            hSpeed = GetDlgItem(hDlg, ID_SPEED); 
            SetScrollRange(hSpeed, SB_CTL, MINVEL, MAXVEL, FALSE); 
            SetScrollPos(hSpeed, SB_CTL, lSpeed, TRUE); 
 
            // Retrieve a handle to the OK push button control.  
            hOK = GetDlgItem(hDlg, ID_OK); 
 
            return TRUE; 
 
        case WM_HSCROLL: 

            // Process scroll bar input, adjusting the lSpeed 
            // value as appropriate. 
            switch (LOWORD(wParam)) 
                { 
                    case SB_PAGEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_LINEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_PAGEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_LINEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_THUMBPOSITION: 
                        lSpeed = HIWORD(wParam); 
                    break; 
 
                    case SB_BOTTOM: 
                        lSpeed = MINVEL; 
                    break; 
 
                    case SB_TOP: 
                        lSpeed = MAXVEL; 
                    break; 
 
                    case SB_THUMBTRACK: 
                    case SB_ENDSCROLL: 
                        return TRUE; 
                    break; 
                } 

                if ((int) lSpeed <= MINVEL) 
                    lSpeed = MINVEL; 
                if ((int) lSpeed >= MAXVEL) 
                    lSpeed = MAXVEL; 
 
                SetScrollPos((HWND) lParam, SB_CTL, lSpeed, TRUE); 
            break; 
 
        case WM_COMMAND: 
            switch(LOWORD(wParam)) 
            { 
                case ID_OK: 
 
                    // Write the current redraw speed variable to
                    // the .ini file. 
                    hr = StringCchPrintf(szTemp, 20, "%ld", lSpeed);
                    if (SUCCEEDED(hr))
                        WritePrivateProfileString(szAppName, szRedrawSpeed, 
                                                  szTemp, szIniFile); 
 
                case ID_CANCEL: 
                    EndDialog(hDlg, LOWORD(wParam) == ID_OK); 

                return TRUE; 
            } 
    } 
    return FALSE; 
}
```



Oltre a fornire il modello della finestra di dialogo e a supportare la funzione [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) , un'applicazione deve supportare anche la funzione [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) . Questa funzione registra le classi di finestra non standard richieste dal screen saver. Poiché nell'applicazione di esempio sono state utilizzate solo classi di finestra standard nella relativa routine della finestra di dialogo, questa funzione restituisce semplicemente **true**, come nell'esempio seguente:


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a>Supporto della procedura screen saver finestra

Ogni screen saver deve supportare una routine della finestra denominata [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc). Analogamente alla maggior parte delle routine della finestra, **ScreenSaverProc** elabora un set di messaggi specifici e passa tutti i messaggi non elaborati a una procedura predefinita. Tuttavia, anziché passarli alla funzione [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) , **ScreenSaverProc** passa i messaggi non elaborati alla funzione [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) . Un'altra differenza tra **ScreenSaverProc** e una normale routine della finestra è che l'handle passato a **ScreenSaverProc** identifica l'intero desktop anziché una finestra client. Nell'esempio seguente viene illustrata la procedura della finestra **ScreenSaverProc** per l'screen saver di esempio.


```
LONG WINAPI ScreenSaverProc(hwnd, message, wParam, lParam) 
HWND  hwnd; 
UINT  message; 
DWORD wParam; 
LONG  lParam; 
{ 
    static HDC          hdc;      // device-context handle  
    static RECT         rc;       // RECT structure  
    static UINT         uTimer;   // timer identifier  
 
    switch(message) 
    { 
        case WM_CREATE: 
 
            // Retrieve the application name from the .rc file. 
            LoadString(hMainInstance, idsAppName, szAppName, 80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry.  
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // Set a timer for the screen saver window using the 
            // redraw rate stored in Regedit.ini. 
            uTimer = SetTimer(hwnd, 1, lSpeed * 1000, NULL); 
            break; 
 
        case WM_ERASEBKGND: 
 
            // The WM_ERASEBKGND message is issued before the 
            // WM_TIMER message, allowing the screen saver to 
            // paint the background as appropriate. 

            hdc = GetDC(hwnd); 
            GetClientRect (hwnd, &rc); 
            FillRect (hdc, &rc, GetStockObject(BLACK_BRUSH)); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_TIMER: 
 
            // The WM_TIMER message is issued at (lSpeed * 1000) 
            // intervals, where lSpeed == .001 seconds. This 
            // code repaints the entire desktop with a white, 
            // light gray, dark gray, or black brush each 
            // time a WM_TIMER message is issued. 

            hdc = GetDC(hwnd); 
            GetClientRect(hwnd, &rc); 
            if (i++ <= 4) 
                FillRect(hdc, &rc, GetStockObject(i)); 
            else 
                (i = 0); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_DESTROY: 
 
            // When the WM_DESTROY message is issued, the screen saver 
            // must destroy any of the timers that were set at WM_CREATE 
            // time. 

            if (uTimer) 
                KillTimer(hwnd, uTimer); 
            break; 
    } 
 
    // DefScreenSaverProc processes any messages ignored by ScreenSaverProc. 
    return DefScreenSaverProc(hwnd, message, wParam, lParam); 
}
```



### <a name="creating-a-module-definition-file"></a>Creazione di un file di definizione del modulo

Le funzioni [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) e [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) devono essere esportate nel file di definizione del modulo dell'applicazione. Tuttavia, [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) non deve essere esportato. Nell'esempio seguente viene illustrato il file di definizione del modulo per l'applicazione di esempio.


```
NAME    SSTEST.SCR 

DESCRIPTION 'SCRNSAVE : Test' 
 
STUB    'WINSTUB.EXE' 
EXETYPE WINDOWS 
 
CODE    MOVEABLE 
DATA    MOVEABLE MULTIPLE 
 
HEAPSIZE  1024 
STACKSIZE 4096 
 
EXPORTS 
        ScreenSaverProc 
        ScreenSaverConfigureDialog
```



### <a name="installing-new-screen-savers"></a>Installazione di nuovi screen saver

Quando si compila l'elenco di screen saver disponibili, il pannello di controllo Cerca i file con estensione SCR nella directory di avvio di Windows. Poiché gli screen saver sono file eseguibili di Windows standard con estensioni exe, è necessario rinominarli in modo che dispongano di estensioni SCR e copiarli nella directory corretta.

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a>Aggiunta della Guida alla finestra di dialogo configurazione screen saver

La finestra di dialogo di configurazione per un screen saver include in genere **un pulsante?** . Le applicazioni screen saver possono verificare l'identificatore del pulsante della guida e chiamare la funzione [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) nello stesso modo in cui vengono fornite informazioni in altre applicazioni basate su Windows.

 

 