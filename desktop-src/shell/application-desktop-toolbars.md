---
description: Una barra degli strumenti del desktop dell'applicazione (denominata anche barra delle applicazioni) è una finestra simile alla barra Windows barra delle applicazioni.
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: Uso delle barre degli strumenti del desktop dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c8604136040f5f3a1b4c1e9fcecb3b0c26b087724f477e592857ca4046d3a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351451"
---
# <a name="using-application-desktop-toolbars"></a>Uso delle barre degli strumenti del desktop dell'applicazione

Una *barra degli strumenti del desktop* dell'applicazione (denominata anche barra delle applicazioni) è una finestra simile alla barra Windows barra delle applicazioni. È ancorato a un bordo dello schermo e in genere contiene pulsanti che consentono all'utente di accedere rapidamente ad altre applicazioni e finestre. Il sistema impedisce ad altre applicazioni di usare l'area del desktop usata da una barra delle app. Sul desktop può esistere un numero qualsiasi di barre delle app in qualsiasi momento.

In questo argomento sono contenute le sezioni seguenti.

-   [Informazioni sulle barre degli strumenti di Application Desktop](#about-application-desktop-toolbars)
    -   [sending messages](#sending-messages)
    -   [Registrazione](#registration)
    -   [Dimensioni e posizione della barra delle app](#appbar-size-and-position)
    -   [Nascondi automaticamente le barre degli strumenti del desktop dell'applicazione](#autohide-application-desktop-toolbars)
    -   [Messaggi di notifica di Appbar](#appbar-notification-messages)
-   [Registrazione di una barra degli strumenti desktop dell'applicazione](#registering-an-application-desktop-toolbar)
-   [Impostazione delle dimensioni e della posizione di Appbar](#setting-the-appbar-size-and-position)
-   [Elaborazione dei messaggi di notifica di Appbar](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a>Informazioni sulle barre degli strumenti di Application Desktop

Windows un'API che consente di sfruttare i servizi appbar forniti dal sistema. I servizi consentono di garantire che le barre delle app definite dall'applicazione funzionino senza problemi tra loro e con la barra delle applicazioni. Il sistema gestisce le informazioni su ogni barra delle app e invia i messaggi di appbars per notificare gli eventi che possono influire su dimensioni, posizione e aspetto.

### <a name="sending-messages"></a>sending messages

Un'applicazione usa un set speciale di messaggi, denominati messaggi della barra delle applicazioni, per aggiungere o rimuovere una barra delle app, impostare le dimensioni e la posizione di una barra delle applicazioni e recuperare informazioni su dimensioni, posizione e stato della barra delle applicazioni. Per inviare un messaggio di appbar, un'applicazione deve usare la [**funzione SHAppBarMessage.**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) I parametri della funzione includono un identificatore di messaggio, ad esempio [**ABM \_ NEW,**](abm-new.md)e l'indirizzo di una [**struttura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) I membri della struttura contengono informazioni necessarie al sistema per elaborare il messaggio specificato.

Per qualsiasi messaggio appbar specificato, il sistema usa alcuni membri della [**struttura APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) e ignora gli altri. Tuttavia, il sistema usa sempre i **membri cbSize** e **hWnd,** quindi un'applicazione deve riempire questi membri per ogni messaggio della barra delle app. Il **membro cbSize** specifica le dimensioni della struttura e il membro **hWnd** è l'handle per la finestra della barra dell'app.

Alcuni messaggi della barra delle app richiedono informazioni dal sistema. Durante l'elaborazione di questi messaggi, il sistema copia le informazioni richieste nella [**struttura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)

### <a name="registration"></a>Registrazione

Il sistema mantiene un elenco interno di barre delle app e mantiene le informazioni su ogni barra nell'elenco. Il sistema usa le informazioni per gestire le barre delle app, eseguire i relativi servizi e inviare loro messaggi di notifica.

Un'applicazione deve registrare un'appbar, ovvero aggiungerla all'elenco interno, prima di poter ricevere i servizi appbar dal sistema. Per registrare un'appbar, un'applicazione invia il [**messaggio ABM \_ NEW.**](abm-new.md) La struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) corrispondente include l'handle per la finestra della barra dell'app e un identificatore di messaggio definito dall'applicazione. Il sistema usa l'identificatore del messaggio per inviare messaggi di notifica alla procedura della finestra della barra delle app. Per altre informazioni, vedere Messaggi di notifica di Appbar.

Un'applicazione annulla la registrazione di una barra delle app inviando il [**messaggio ABM \_ REMOVE.**](abm-remove.md) L'annullamento della registrazione di una barra delle app la rimuove dall'elenco interno delle barre delle app del sistema. Il sistema non invia più messaggi di notifica alla barra delle app o impedisce ad altre applicazioni di usare l'area dello schermo usata dalla barra delle app. Un'applicazione deve sempre inviare **ABM \_ REMOVE** prima di eliminare un'appbar.

### <a name="appbar-size-and-position"></a>Dimensioni e posizione della barra delle app

Un'applicazione deve impostare le dimensioni e la posizione di una barra delle applicazioni in modo che non interferisca con altre barre delle applicazioni o con la barra delle applicazioni. Ogni barra delle app deve essere ancorata a un bordo specifico dello schermo e più barre delle app possono essere ancorate a un bordo. Tuttavia, se una barra delle applicazioni è ancorata allo stesso bordo della barra delle applicazioni, il sistema garantisce che la barra delle applicazioni sia sempre sul bordo più esterno.

Per impostare le dimensioni e la posizione di una barra delle app, un'applicazione propone innanzitutto un bordo dello schermo e un rettangolo di delimitazione per la barra dell'app inviando il [**messaggio \_ QUERYPOS ABM.**](abm-querypos.md) Il sistema determina se qualsiasi parte dell'area dello schermo all'interno del rettangolo proposto viene usata dalla barra delle applicazioni o da un'altra barra delle applicazioni, regola il rettangolo (se necessario) e restituisce il rettangolo regolato all'applicazione.

Successivamente, l'applicazione invia il [**messaggio ABM \_ SETPOS**](abm-setpos.md) per impostare il nuovo rettangolo di delimitazione per la barra dell'app. Anche in questo caso, il sistema può regolare il rettangolo prima di restituirlo all'applicazione. Per questo motivo, l'applicazione deve usare il rettangolo regolato restituito da **ABM \_ SETPOS** per impostare le dimensioni e la posizione finali. L'applicazione può usare la [**funzione MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) per spostare la barra dell'app in posizione.

Usando un processo in due passaggi per impostare le dimensioni e la posizione, il sistema consente all'applicazione di fornire un feedback intermedio all'utente durante l'operazione di spostamento. Ad esempio, se l'utente trascina una barra dell'app, l'applicazione potrebbe visualizzare un rettangolo ombreggiato che indica la nuova posizione prima che la barra dell'app venga effettivamente spostata.

Un'applicazione deve impostare le dimensioni e la posizione della relativa barra delle app dopo la registrazione e ogni volta che la barra dell'app riceve il messaggio di notifica [**ABN \_ POSCHANGED.**](abn-poschanged.md) Una barra delle app riceve questo messaggio di notifica ogni volta che si verifica una modifica nello stato di visibilità, posizione o dimensione della barra delle applicazioni e ogni volta che un'altra barra delle app sullo stesso lato dello schermo viene ridimensionata, aggiunta o rimossa.

Ogni volta che un appbar riceve il messaggio WM \_ ACTIVATE, deve inviare il [**messaggio ABM \_ ACTIVATE.**](abm-activate.md) Analogamente, quando un'appbar riceve un messaggio WM \_ WINDOWPOSCHANGED, deve chiamare [**ABM \_ WINDOWPOSCHANGED**](abm-windowposchanged.md). L'invio di questi messaggi garantisce che il sistema imposta correttamente l'ordine z di tutte le barre delle app con rilevamento automatico sullo stesso bordo.

### <a name="autohide-application-desktop-toolbars"></a>Nascondi automaticamente le barre degli strumenti del desktop dell'applicazione

Una barra dell'app con nascondimento automatico è normalmente nascosta, ma diventa visibile quando l'utente sposta il cursore del mouse sul bordo dello schermo a cui è associata la barra dell'app. La barra dell'app si nasconde di nuovo quando l'utente sposta il cursore del mouse fuori dal rettangolo di delimitazione della barra.

Anche se il sistema consente una serie di appbar diverse in un determinato momento, consente una sola barra dell'app con rilevamento automatico alla volta per ogni bordo dello schermo in base al primo utilizzo. Il sistema mantiene automaticamente l'ordine z di una barra dell'app con nascondimento automatico (solo all'interno del relativo gruppo di ordine z).

Un'applicazione usa il [**messaggio ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) per registrare o annullare la registrazione di una barra delle app con rilevamento automatico. Il messaggio specifica il bordo per la barra delle app e un flag che specifica se la barra dell'app deve essere registrata o annullata. Il messaggio ha esito negativo se è in corso la registrazione di una barra dell'app con rilevamento automatico, ma ne è già associata una al bordo specificato. Un'applicazione può recuperare l'handle alla barra dell'app di rilevamento automatico associata a un bordo inviando il [**messaggio ABM \_ GETAUTOHIDEBAR.**](abm-getautohidebar.md)

Non è necessario registrare una barra delle app con rilevamento automatico come normale barra dell'app. ciò significa che non è necessario registrarlo inviando il [**messaggio ABM \_ NEW.**](abm-new.md) Una barra delle app non registrata da **ABM \_ NEW** si sovrappone alle barre delle app ancorate sullo stesso bordo dello schermo.

### <a name="appbar-notification-messages"></a>Messaggi di notifica di Appbar

Il sistema invia messaggi per notificare a una barra delle app gli eventi che possono influire sulla posizione e sull'aspetto. I messaggi vengono inviati nel contesto di un messaggio definito dall'applicazione. L'applicazione specifica l'identificatore del messaggio quando invia il messaggio [**ABM \_ NEW**](abm-new.md) per registrare l'appbar. Il codice di notifica si trova nel *parametro wParam* del messaggio definito dall'applicazione.

Una barra delle app riceve il messaggio di notifica [**ABN \_ POSCHANGED**](abn-poschanged.md) quando le dimensioni, la posizione o lo stato di visibilità della barra delle applicazioni cambiano, quando un'altra barra delle app viene aggiunta allo stesso bordo dello schermo o quando un'altra barra delle app sullo stesso bordo dello schermo viene ridimensionata o rimossa. Un'appbar deve rispondere a questo messaggio di notifica inviando messaggi [**ABM \_ QUERYPOS**](abm-querypos.md) e [**ABM \_ SETPOS.**](abm-setpos.md) Se la posizione di una barra delle app è cambiata, deve chiamare la [**funzione MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) per spostarsi nella nuova posizione.

Il sistema invia il messaggio di notifica [**ABN \_ STATECHANGE**](abn-statechange.md) ogni volta che viene modificato lo stato di rilevamento automatico  o sempre  attivo della barra delle applicazioni, ovvero quando l'utente seleziona o deseleziona la casella di controllo Sempre in alto o Nascondi automaticamente nella finestra delle proprietà della barra delle applicazioni. Una barra delle applicazioni può usare questo messaggio di notifica per impostarne lo stato in modo che sia conforme a quello della barra delle applicazioni, se necessario.

Quando un'applicazione a schermo intero viene avviata o quando viene chiusa l'ultima applicazione a schermo intero, una barra delle app riceve il messaggio di notifica [**ABN \_ FULLSCREENAPP.**](abn-fullscreenapp.md) Il *parametro lParam* indica se l'applicazione a schermo intero si sta aprendo o chiudendo. Se si apre, la barra dell'app deve essere in fondo all'ordine z. La barra delle app deve ripristinare la posizione nell'ordine z quando l'ultima applicazione a schermo intero è stata chiusa.

Una barra delle app riceve il messaggio di notifica [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) quando l'utente seleziona il comando Cascade, Tile Horizontally o Tile Vertically dal menu di scelta rapida della barra delle applicazioni. Il sistema invia il messaggio due volte, prima di riorganizzare le finestre (*lParam* è **TRUE**) e dopo aver organizzato le finestre (*lParam* è **FALSE**).

Una barra delle app può usare [**i messaggi ABN \_ WINDOWARRANGE**](abn-windowarrange.md) per escludersi dall'operazione a catena o riquadro. Per escludersi, la barra dell'app deve nascondersi quando *lParam* è **TRUE** e mostrarsi quando *lParam* è **FALSE.** Se una barra delle app si nasconde in risposta a questo messaggio, non è necessario inviare i messaggi [**ABM \_ QUERYPOS**](abm-querypos.md) e [**ABM \_ SETPOS**](abm-setpos.md) in risposta all'operazione a catena o al riquadro.

## <a name="registering-an-application-desktop-toolbar"></a>Registrazione di una barra degli strumenti desktop dell'applicazione

Un'applicazione deve registrare un'appbar inviando il [**messaggio ABM \_ NEW.**](abm-new.md) La registrazione di un'appbar la aggiunge all'elenco interno del sistema e fornisce al sistema un identificatore di messaggio da usare per inviare messaggi di notifica alla barra delle app. Prima di uscire, un'applicazione deve annullare la registrazione della barra delle app inviando il [**messaggio ABM \_ REMOVE.**](abm-remove.md) L'annullamento della registrazione rimuove la barra delle app dall'elenco interno del sistema e impedisce alla barra di ricevere messaggi di notifica della barra delle app.

La funzione nell'esempio seguente registra o annulla la registrazione di una barra dell'app, a seconda del valore di un parametro flag booleano.


```C++
// RegisterAccessBar - registers or unregisters an appbar. 
// Returns TRUE if successful, or FALSE otherwise. 

// hwndAccessBar - handle to the appbar 
// fRegister - register and unregister flag 

// Global variables 
//     g_uSide - screen edge (defaults to ABE_TOP) 
//     g_fAppRegistered - flag indicating whether the bar is registered 

BOOL RegisterAccessBar(HWND hwndAccessBar, BOOL fRegister) 
{ 
    APPBARDATA abd; 
    
    // An application-defined message identifier
    APPBAR_CALLBACK = (WM_USER + 0x01);
    
    // Specify the structure size and handle to the appbar. 
    abd.cbSize = sizeof(APPBARDATA); 
    abd.hWnd = hwndAccessBar; 

    if (fRegister) 
    { 
        // Provide an identifier for notification messages. 
        abd.uCallbackMessage = APPBAR_CALLBACK; 

        // Register the appbar. 
        if (!SHAppBarMessage(ABM_NEW, &abd)) 
            return FALSE; 

        g_uSide = ABE_TOP;       // default edge 
        g_fAppRegistered = TRUE; 

    } 
    else 
    { 
        // Unregister the appbar. 
        SHAppBarMessage(ABM_REMOVE, &abd); 
        g_fAppRegistered = FALSE; 
    } 

    return TRUE; 
}
```



## <a name="setting-the-appbar-size-and-position"></a>Impostazione delle dimensioni e della posizione di Appbar

Un'applicazione deve impostare le dimensioni e la posizione di una barra delle app dopo la registrazione della barra dell'app, dopo che l'utente ha spostato o ridimensionato la barra dell'app e ogni volta che la barra dell'app riceve il messaggio di notifica [**ABN \_ POSCHANGED.**](abn-poschanged.md) Prima di impostare le dimensioni e la posizione della barra dell'app, l'applicazione esegue una query sul sistema per cercare un rettangolo di delimitazione approvato inviando il [**messaggio \_ QUERYPOS ABM.**](abm-querypos.md) Il sistema restituisce un rettangolo di delimitazione che non interferisce con la barra delle applicazioni o con qualsiasi altra barra delle applicazioni. Il sistema regola il rettangolo esclusivamente in base alla sottrazione di rettangoli; non fa alcuno sforzo per mantenere le dimensioni iniziali del rettangolo. Per questo motivo, la barra dell'app deve regolare il rettangolo, se necessario, dopo l'invio **di \_ QUERYPOS ABM.**

Successivamente, l'applicazione passa di nuovo il rettangolo di delimitazione al sistema usando il [**messaggio \_ SETPOS ABM.**](abm-setpos.md) Chiama quindi la funzione [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) per spostare la barra dell'app nella posizione .

L'esempio seguente mostra come impostare le dimensioni e la posizione di una barra dell'app.


```C++
// AppBarQuerySetPos - sets the size and position of an appbar. 

// uEdge - screen edge to which the appbar is to be anchored 
// lprc - current bounding rectangle of the appbar 
// pabd - address of the APPBARDATA structure with the hWnd and cbSize members filled

void PASCAL AppBarQuerySetPos(UINT uEdge, LPRECT lprc, PAPPBARDATA pabd) 
{ 
    int iHeight = 0; 
    int iWidth = 0; 

    pabd->rc = *lprc; 
    pabd->uEdge = uEdge; 

    // Copy the screen coordinates of the appbar's bounding 
    // rectangle into the APPBARDATA structure. 
    if ((uEdge == ABE_LEFT) || (uEdge == ABE_RIGHT)) 
    { 
        iWidth = pabd->rc.right - pabd->rc.left; 
        pabd->rc.top = 0; 
        pabd->rc.bottom = GetSystemMetrics(SM_CYSCREEN); 
    } 
    else 
    { 
        iHeight = pabd->rc.bottom - pabd->rc.top; 
        pabd->rc.left = 0; 
        pabd->rc.right = GetSystemMetrics(SM_CXSCREEN); 
    } 

    // Query the system for an approved size and position. 
    SHAppBarMessage(ABM_QUERYPOS, pabd); 

    // Adjust the rectangle, depending on the edge to which the appbar is anchored.
    switch (uEdge) 
    { 
        case ABE_LEFT: 
            pabd->rc.right = pabd->rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            pabd->rc.left = pabd->rc.right - iWidth; 
            break; 

        case ABE_TOP: 
            pabd->rc.bottom = pabd->rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            pabd->rc.top = pabd->rc.bottom - iHeight; 
            break; 
    } 

    // Pass the final bounding rectangle to the system. 
    SHAppBarMessage(ABM_SETPOS, pabd); 

    // Move and size the appbar so that it conforms to the 
    // bounding rectangle passed to the system. 
    MoveWindow(pabd->hWnd, 
               pabd->rc.left, 
               pabd->rc.top, 
               pabd->rc.right - pabd->rc.left, 
               pabd->rc.bottom - pabd->rc.top, 
               TRUE); 

}
```



## <a name="processing-appbar-notification-messages"></a>Elaborazione dei messaggi di notifica di Appbar

Una barra delle app riceve un messaggio di notifica quando lo stato della barra delle applicazioni cambia, quando un'applicazione a schermo intero viene avviata (o l'ultima si chiude) o quando si verifica un evento che può influire sulle dimensioni e sulla posizione della barra delle applicazioni. Nell'esempio seguente viene illustrato come elaborare i vari messaggi di notifica.


```C++
// AppBarCallback - processes notification messages sent by the system. 

// hwndAccessBar - handle to the appbar 
// uNotifyMsg - identifier of the notification message 
// lParam - message parameter 

void AppBarCallback(HWND hwndAccessBar, UINT uNotifyMsg, 
    LPARAM lParam) 
{ 
    APPBARDATA abd; 
    UINT uState; 

    abd.cbSize = sizeof(abd); 
    abd.hWnd = hwndAccessBar; 

    switch (uNotifyMsg) 
    { 
        case ABN_STATECHANGE: 

            // Check to see if the taskbar's always-on-top state has changed
            // and, if it has, change the appbar's state accordingly.
            uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

            SetWindowPos(hwndAccessBar, 
                         (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                         0, 0, 0, 0, 
                         SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 

            break; 

        case ABN_FULLSCREENAPP: 

            // A full-screen application has started, or the last full-screen
            // application has closed. Set the appbar's z-order appropriately.
            if (lParam) 
            { 
                SetWindowPos(hwndAccessBar, 
                             (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                             0, 0, 0, 0, 
                             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 
            else 
            { 
                uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

                if (uState & ABS_ALWAYSONTOP) 
                    SetWindowPos(hwndAccessBar, 
                                 HWND_TOPMOST, 
                                 0, 0, 0, 0, 
                                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 

        case ABN_POSCHANGED: 

            // The taskbar or another appbar has changed its size or position.
            AppBarPosChanged(&abd); 
            break; 
    } 
}
```



La funzione seguente regola il rettangolo di delimitazione di una barra dell'app e quindi chiama la funzione AppBarQuerySetPos definita dall'applicazione (inclusa nella sezione precedente) per impostare le dimensioni e la posizione della barra di conseguenza.


```C++
// AppBarPosChanged - adjusts the appbar's size and position. 

// pabd - address of an APPBARDATA structure that contains information 
//        used to adjust the size and position. 

void PASCAL AppBarPosChanged(PAPPBARDATA pabd) 
{ 
    RECT rc; 
    RECT rcWindow; 
    int iHeight; 
    int iWidth; 

    rc.top = 0; 
    rc.left = 0; 
    rc.right = GetSystemMetrics(SM_CXSCREEN); 
    rc.bottom = GetSystemMetrics(SM_CYSCREEN); 

    GetWindowRect(pabd->hWnd, &rcWindow); 

    iHeight = rcWindow.bottom - rcWindow.top; 
    iWidth = rcWindow.right - rcWindow.left; 

    switch (g_uSide) 
    { 
        case ABE_TOP: 
            rc.bottom = rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            rc.top = rc.bottom - iHeight; 
            break; 

        case ABE_LEFT: 
            rc.right = rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            rc.left = rc.right - iWidth; 
            break; 
    } 

    AppBarQuerySetPos(g_uSide, &rc, pabd); 
}
```



 

 
