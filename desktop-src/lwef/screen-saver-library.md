---
title: Gestione degli screen saver
description: L'API Microsoft Win32 supporta applicazioni speciali denominate screen saver.
ms.assetid: cda5e690-71fe-4df7-b8a2-3a2ad65b1bfb
keywords:
- screen saver
- Pannello di controllo,screen saver
- ScreenSaverConfigureDialog
- file di definizione del modulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61343cd586ed022c334b797a77320ee25eccdf48653b4732adc597f4aedde26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975721"
---
# <a name="handling-screen-savers"></a>Gestione degli screen saver

L'API Microsoft Win32 supporta applicazioni speciali denominate *screen saver.* Gli screen saver vengono avviati quando il mouse e la tastiera sono inattivi per un periodo di tempo specificato. Vengono usati per i due motivi seguenti:

-   Per proteggere uno schermo dalla masterizzazione di phosphor causata da immagini statiche.
-   Per nascondere le informazioni riservate a sinistra in una schermata.

Questo argomento è suddiviso nelle sezioni seguenti.

-   [Informazioni sugli screen saver](#about-screen-savers)
-   [Uso delle funzioni screen saver](#using-the-screen-saver-functions)
    -   [Creazione di uno screen saver](#creating-a-screen-saver)
    -   [Installazione di nuovi screen saver](#installing-new-screen-savers)
    -   [Aggiunta della Guida alla finestra di dialogo di configurazione dello screen saver](#adding-help-to-the-screen-saver-configuration-dialog-box)

## <a name="about-screen-savers"></a>Informazioni sugli screen saver

L'applicazione desktop nel Windows Pannello di controllo consente agli utenti di selezionare da un elenco di screen saver, specificare quanto tempo deve trascorrere prima dell'avvio del screen saver, configurare gli screen saver e gli screen saver di anteprima. Gli screen saver vengono caricati automaticamente all'avvio Windows o quando un utente attiva il screen saver tramite il Pannello di controllo.

Dopo aver scelto screen saver, Windows monitora le sequenze di tasti e i movimenti del mouse e quindi avvia il screen saver dopo un periodo di inattività. Tuttavia, Windows avvia il screen saver se si verifica una delle condizioni seguenti:

-   L'applicazione attiva non è Windows basata su criteri.
-   È presente una finestra CBT (Computer-Based Training).
-   L'applicazione attiva riceve il messaggio [ \_ WM SYSCOMMAND](../menurc/wm-syscommand.md) con il parametro *wParam* impostato sul valore SC SCREENSAVE, ma non passa il messaggio alla \_ funzione [DefWindowProc.](/windows/win32/api/winuser/nf-winuser-defwindowproca)

**Contesto di sicurezza dello screen saver**

Il contesto di sicurezza del screen saver dipende dal fatto che un utente sia connesso in modo interattivo. Se un utente è connesso in modo interattivo quando viene screen saver, il screen saver viene eseguito nel contesto di sicurezza dell'utente interattivo. Se nessun utente è connesso, il contesto di sicurezza del screen saver dipende dalla versione di Windows in uso.

-   Windows XP e Windows 2000: screen saver viene eseguito nel contesto di LocalSystem con account limitati.
-   Windows 2003- screen saver viene eseguito nel contesto di LocalService con tutti i privilegi rimossi e il gruppo administrators disabilitato.
-   Non si applica a Windows NT4.

Il contesto di sicurezza determina il livello di operazioni con privilegi che possono essere eseguite da un screen saver.

**Windows Vista e versioni successive:** Se la protezione tramite password è abilitata dai criteri, il screen saver viene avviato indipendentemente dalle attività che un'applicazione esegue con la notifica SC \_ SCREENSAVE.

Gli screen saver contengono funzioni esportate, definizioni di risorse e dichiarazioni di variabili specifiche. La screen saver contiene la **funzione main** e altro codice di avvio necessario per un screen saver. Quando viene screen saver, il codice di avvio nella libreria screen saver crea una finestra a schermo intero. La classe della finestra per questa finestra viene dichiarata come segue:


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



Per creare un screen saver, la maggior parte degli sviluppatori crea un modulo di codice sorgente contenente tre funzioni necessarie e le collega alla libreria screen saver. Un screen saver modulo è responsabile solo della configurazione di se stesso e della fornitura di effetti visivi.

Una delle tre funzioni necessarie in un modulo screen saver è [**ScreenSaverProc.**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) Questa funzione elabora messaggi specifici e passa di nuovo tutti i messaggi non elaborato alla screen saver libreria. Di seguito sono riportati alcuni dei messaggi tipici elaborati **da ScreenSaverProc.**



| Messaggio        | Significato                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WM \_ CREATE     | Recuperare i dati di inizializzazione dal file Regedit.ini. Impostare un timer di finestra per la screen saver finestra. Eseguire qualsiasi altra inizializzazione richiesta.                                     |
| WM \_ ERASEBKGND | Cancellare la finestra screen saver e prepararsi per le successive operazioni di disegno.                                                                                                               |
| WM \_ TIMER      | Eseguire operazioni di disegno.                                                                                                                                                                |
| WM \_ DESTROY    | Eliminare i timer creati quando l'applicazione ha elaborato il [messaggio WM \_ CREATE.](../winmsg/wm-create.md) Eseguire eventuali operazioni di pulizia aggiuntive necessarie. |



 

[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) passa i messaggi non elaborati alla libreria screen saver chiamando la [**funzione DefScreenSaverProc.**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) Nella tabella seguente viene descritto il modo in cui questa funzione elabora i vari messaggi.



| Message         | Azione                                                                    |
|-----------------|---------------------------------------------------------------------------|
| WM \_ SETCURSOR   | Impostare il cursore sul cursore Null, rimuovendo il cursore dallo schermo.           |
| WM \_ PAINT       | Paint lo sfondo dello schermo.                                              |
| WM \_ LBUTTONDOWN | Terminare il screen saver.                                               |
| WM \_ MBUTTONDOWN | Terminare il screen saver.                                               |
| WM \_ RBUTTONDOWN | Terminare il screen saver.                                               |
| WM \_ KEYDOWN     | Terminare il screen saver.                                               |
| WM \_ MOUSEMOVE   | Terminare il screen saver.                                               |
| WM \_ ACTIVATE    | Terminare screen saver se il *parametro wParam* è impostato su **FALSE.** |



 

La seconda funzione richiesta in un modulo screen saver è [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog). Questa funzione visualizza una finestra di dialogo che consente all'utente di configurare il screen saver (un'applicazione deve fornire un modello di finestra di dialogo corrispondente). Windows visualizza la finestra di dialogo di configurazione  quando l'utente seleziona il pulsante Setup (Configurazione) nella finestra Pannello di controllo screen saver del programma di installazione.

La terza funzione richiesta in un modulo screen saver è [**RegisterDialogClasses.**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) Questa funzione deve essere chiamata da tutte le screen saver applicazioni. Tuttavia, le applicazioni che non richiedono finestre speciali o controlli personalizzati nella finestra di dialogo di configurazione possono semplicemente restituire **TRUE.** Le applicazioni che richiedono finestre speciali o controlli personalizzati devono usare questa funzione per registrare le classi di finestre corrispondenti.

Oltre a creare un modulo che supporta le tre funzioni appena descritte, un screen saver deve fornire un'icona. Questa icona è visibile solo quando il screen saver viene eseguito come applicazione autonoma. Per essere eseguito dal Pannello di controllo, un screen saver deve avere l'estensione scr. Per essere eseguito come applicazione autonoma, deve avere l'estensione .exe file. L'icona deve essere identificata nel file di risorse del screen saver dall'ID costante APP, definito nel file di intestazione \_ Scrnsave.h.

Un requisito finale è una screen saver di descrizione. Il file di risorse per screen saver deve contenere una stringa che il Pannello di controllo visualizza come nome screen saver. La stringa di descrizione deve essere la prima stringa nella tabella di stringhe del file di risorse (identificata con il valore ordinale 1). Tuttavia, la stringa di descrizione viene ignorata dal Pannello di controllo se il screen saver ha un nome file lungo. In questo caso, il nome file verrà usato come stringa di descrizione.

## <a name="using-the-screen-saver-functions"></a>Uso delle funzioni screen saver

Questa sezione usa codice di esempio tratto da un'screen saver per illustrare le attività seguenti:

-   [Creazione di uno screen saver](#creating-a-screen-saver)
-   [Installazione di nuovi screen saver](#installing-new-screen-savers)
-   [Aggiunta della Guida alla finestra di dialogo di configurazione dello screen saver](#adding-help-to-the-screen-saver-configuration-dialog-box)

### <a name="creating-a-screen-saver"></a>Creazione di uno screen saver

A intervalli compresi tra 1 e 10 secondi, l'applicazione in questo esempio ridisegna lo schermo con uno dei quattro colori seguenti: bianco, grigio chiaro, grigio scuro e nero. L'applicazione disegna lo schermo ogni volta che riceve un [messaggio WM \_ TIMER.](../winmsg/wm-timer.md) L'utente può modificare l'intervallo di invio del messaggio selezionando la finestra di dialogo di configurazione dell'applicazione e modificando una singola barra di scorrimento orizzontale.

### <a name="screen-saver-library"></a>Libreria dello screen saver

Le funzioni screen saver sono contenute nella libreria screen saver statica. Sono disponibili due versioni della libreria, Scrnsave.lib e Scrnsavw.lib. È necessario collegare il progetto a uno di questi. Scrnsave.lib viene usato per gli screen saver che usano caratteri ANSI e Scrnsavw.lib viene usato per gli screen saver che usano caratteri Unicode. Un screen saver collegato a Scrnsavw.lib verrà eseguito solo su piattaforme Windows che supportano Unicode, mentre un screen saver collegato a Scrnsave.lib verrà eseguito in qualsiasi piattaforma Windows.

### <a name="supporting-the-configuration-dialog-box"></a>Supporto della finestra di dialogo di configurazione

La maggior parte degli screen saver fornisce una finestra di dialogo di configurazione per consentire all'utente di specificare dati di personalizzazione, ad esempio colori univoci, velocità di disegno, spessore della linea, tipi di carattere e così via. Per supportare la finestra di dialogo di configurazione, l'applicazione deve fornire un modello di finestra di dialogo e deve supportare anche la [**funzione ScreenSaverConfigureDialog.**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) Di seguito è riportato il modello di finestra di dialogo per l'applicazione di esempio.


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



È necessario definire la costante utilizzata per identificare il modello di finestra di dialogo usando il valore decimale 2003, come nell'esempio seguente:


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



L'esempio seguente illustra [**la funzione ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) disponibile nell'applicazione di esempio.


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



Oltre a fornire il modello di finestra di dialogo e a supportare la [**funzione ScreenSaverConfigureDialog,**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) un'applicazione deve supportare anche la [**funzione RegisterDialogClasses.**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) Questa funzione registra tutte le classi di finestra non standard richieste dal screen saver. Poiché l'applicazione di esempio usava solo classi finestra standard nella routine della finestra di dialogo, questa funzione restituisce **semplicemente TRUE**, come nell'esempio seguente:


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a>Supporto della procedura screen saver finestra

Ogni screen saver deve supportare una routine finestra denominata [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc). Come la maggior parte delle procedure di finestra, **ScreenSaverProc** elabora un set di messaggi specifici e passa tutti i messaggi non elaborati a una procedura predefinita. Tuttavia, invece di passarli alla funzione [DefWindowProc,](/windows/win32/api/winuser/nf-winuser-defwindowproca) **ScreenSaverProc** passa messaggi non elaborati alla [**funzione DefScreenSaverProc.**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) Un'altra differenza **tra ScreenSaverProc** e una normale routine della finestra è che l'handle passato a **ScreenSaverProc** identifica l'intero desktop anziché una finestra client. L'esempio seguente illustra la **procedura della finestra ScreenSaverProc** per l'esempio screen saver.


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

Le [**funzioni ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) e [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) devono essere esportate nel file di definizione del modulo dell'applicazione. Non è tuttavia consigliabile esportare [**RegisterDialogClasses.**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) Nell'esempio seguente viene illustrato il file di definizione del modulo per l'applicazione di esempio.


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

Quando si compila l'elenco degli screen saver disponibili, il Pannello di controllo cerca nella directory di avvio Windows file con estensione scr. Poiché gli screen saver sono Windows file eseguibili con .exe, è necessario rinominarli in modo che abbia estensioni scr e copiarli nella directory corretta.

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a>Aggiunta della Guida alla finestra di dialogo Configurazione dello screen saver

La finestra di dialogo di configurazione per un screen saver in genere include un **pulsante ?** . Le applicazioni screen saver possono cercare l'identificatore del pulsante Guida e chiamare la funzione [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) nello stesso modo in cui viene fornita la Guida in altre applicazioni Windows basate su file.

 

 