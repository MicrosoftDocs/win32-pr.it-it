---
description: Una barra degli strumenti del desktop dell'applicazione (detta anche AppBar) è una finestra simile alla barra delle applicazioni di Windows.
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: Uso delle barre degli strumenti del desktop applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140ef94c1daeb571cd0d766dfbd4dc28b7991efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128470"
---
# <a name="using-application-desktop-toolbars"></a>Uso delle barre degli strumenti del desktop applicazione

Una *barra degli strumenti del desktop dell'applicazione* (detta anche AppBar) è una finestra simile alla barra delle applicazioni di Windows. È ancorato a un bordo dello schermo e contiene in genere pulsanti che consentono all'utente di accedere rapidamente ad altre applicazioni e finestre. Il sistema impedisce ad altre applicazioni di utilizzare l'area desktop utilizzata da un AppBar. Sul desktop può esistere un numero qualsiasi di AppBar in un determinato momento.

In questo argomento sono contenute le sezioni seguenti.

-   [Informazioni sulle barre degli strumenti del desktop applicazione](#about-application-desktop-toolbars)
    -   [sending messages](#sending-messages)
    -   [Registrazione](#registration)
    -   [Dimensioni e posizione AppBar](#appbar-size-and-position)
    -   [Nascondi automaticamente le barre degli strumenti del desktop dell'applicazione](#autohide-application-desktop-toolbars)
    -   [Messaggi di notifica AppBar](#appbar-notification-messages)
-   [Registrazione di una barra degli strumenti del desktop dell'applicazione](#registering-an-application-desktop-toolbar)
-   [Impostazione delle dimensioni e della posizione del AppBar](#setting-the-appbar-size-and-position)
-   [Elaborazione dei messaggi di notifica AppBar](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a>Informazioni sulle barre degli strumenti del desktop applicazione

Windows fornisce un'API che consente di sfruttare i vantaggi offerti dai servizi AppBar forniti dal sistema. I servizi consentono di garantire che i AppBar definiti dall'applicazione funzionino senza problemi tra loro e con la barra delle applicazioni. Il sistema mantiene le informazioni su ogni AppBar e invia i messaggi AppBar per notificare gli eventi che possono influire sulle dimensioni, sulla posizione e sull'aspetto.

### <a name="sending-messages"></a>sending messages

Un'applicazione usa uno speciale set di messaggi, denominati messaggi AppBar, per aggiungere o rimuovere un AppBar, impostare le dimensioni e la posizione di AppBar e recuperare le informazioni sulle dimensioni, sulla posizione e sullo stato della barra delle applicazioni. Per inviare un messaggio AppBar, un'applicazione deve usare la funzione [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) . I parametri della funzione includono un identificatore del messaggio, ad esempio [**ABM \_ New**](abm-new.md), e l'indirizzo di una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . I membri della struttura contengono informazioni necessarie al sistema per elaborare il messaggio specificato.

Per ogni messaggio AppBar, il sistema usa alcuni membri della struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) e ignora gli altri. Tuttavia, il sistema usa sempre i membri **cbSize** e **HWND** , quindi un'applicazione deve compilare tali membri per ogni messaggio di AppBar. Il membro **cbSize** specifica le dimensioni della struttura e il membro **HWND** è l'handle per la finestra di AppBar.

Alcuni messaggi AppBar richiedono informazioni dal sistema. Durante l'elaborazione di questi messaggi, il sistema copia le informazioni richieste nella struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .

### <a name="registration"></a>Registrazione

Il sistema mantiene un elenco interno di AppBar e gestisce le informazioni su ogni barra dell'elenco. Il sistema utilizza le informazioni per gestire AppBar, per eseguirne i servizi e per inviare messaggi di notifica.

Un'applicazione deve registrare un AppBar (ovvero aggiungerlo all'elenco interno) prima di poter ricevere i servizi AppBar dal sistema. Per registrare un AppBar, un'applicazione invia il [**\_ nuovo messaggio ABM**](abm-new.md) . La struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) associata include l'handle per la finestra di AppBar e un identificatore di messaggio definito dall'applicazione. Il sistema utilizza l'identificatore del messaggio per inviare messaggi di notifica alla routine della finestra AppBar. Per ulteriori informazioni, vedere AppBar Notification messages.

Un'applicazione annulla la registrazione di un AppBar inviando il messaggio di [**\_ rimozione di ABM**](abm-remove.md) . L'annullamento della registrazione di un AppBar lo rimuove dall'elenco interno del sistema di AppBar. Il sistema non invia più messaggi di notifica a AppBar o impedisce ad altre applicazioni di utilizzare l'area dello schermo utilizzata dal AppBar. Un'applicazione deve sempre inviare **la \_ rimozione di ABM** prima di eliminare un AppBar.

### <a name="appbar-size-and-position"></a>Dimensioni e posizione AppBar

Un'applicazione deve impostare le dimensioni e la posizione di un AppBar in modo che non interferisca con altri AppBar o la barra delle applicazioni. Ogni AppBar deve essere ancorato a un bordo particolare dello schermo e più AppBar possono essere ancorati a un bordo. Tuttavia, se un AppBar è ancorato allo stesso bordo della barra delle applicazioni, il sistema garantisce che la barra delle applicazioni si trovi sempre sul bordo più esterno.

Per impostare le dimensioni e la posizione di un AppBar, un'applicazione propone prima di tutto un bordo dello schermo e un rettangolo di delimitazione per il AppBar inviando il messaggio di [**\_ QUERYPOS ABM**](abm-querypos.md) . Il sistema determina se una parte dell'area dello schermo all'interno del rettangolo proposto viene utilizzata dalla barra delle applicazioni o da un altro AppBar, regola il rettangolo (se necessario) e restituisce il rettangolo modificato per l'applicazione.

Successivamente, l'applicazione invia il [**messaggio \_ SETPOS di ABM**](abm-setpos.md) per impostare il nuovo rettangolo di delimitazione per il AppBar. Anche in questo caso, il sistema può regolare il rettangolo prima di restituirlo all'applicazione. Per questo motivo, l'applicazione deve usare il rettangolo modificato restituito da **ABM \_ SETPOS** per impostare le dimensioni e la posizione finali. L'applicazione può usare la funzione [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) per spostare il AppBar in posizione.

Utilizzando un processo in due passaggi per impostare le dimensioni e la posizione, il sistema consente all'applicazione di fornire feedback intermedio all'utente durante l'operazione di spostamento. Se, ad esempio, l'utente trascina un AppBar, l'applicazione potrebbe visualizzare un rettangolo ombreggiato che indica la nuova posizione prima che il AppBar venga effettivamente spostato.

Un'applicazione deve impostare la dimensione e la posizione del relativo AppBar dopo la registrazione e ogni volta che il AppBar riceve il messaggio di notifica [**\_ POSCHANGED di ABN**](abn-poschanged.md) . Un AppBar riceve questo messaggio di notifica ogni volta che si verifica una modifica nella dimensione, nella posizione o nello stato di visibilità della barra delle applicazioni e ogni volta che un altro AppBar sullo stesso lato dello schermo viene ridimensionato, aggiunto o rimosso.

Ogni volta che un AppBar riceve il \_ messaggio di attivazione WM, deve inviare il messaggio di [**\_ attivazione di ABM**](abm-activate.md) . Analogamente, quando un AppBar riceve un \_ messaggio WM WINDOWPOSCHANGED, deve chiamare [**ABM \_ WINDOWPOSCHANGED**](abm-windowposchanged.md). L'invio di questi messaggi garantisce che il sistema imposti correttamente lo z-order di qualsiasi AppBar di Nascondi automaticamente sullo stesso perimetro.

### <a name="autohide-application-desktop-toolbars"></a>Nascondi automaticamente le barre degli strumenti del desktop dell'applicazione

Un AppBar di Nascondi automaticamente è uno che in genere è nascosto ma diventa visibile quando l'utente sposta il cursore del mouse sul bordo dello schermo a cui è associato il AppBar. Il AppBar si nasconde nuovamente quando l'utente sposta il cursore del mouse fuori dal rettangolo di delimitazione della barra.

Sebbene il sistema consenta un numero di AppBar diversi in un determinato momento, consente solo un AppBar di Nascondi alla volta per ogni bordo dello schermo in base alla prima, prima di tutto. Il sistema mantiene automaticamente l'ordine z di un AppBar di Nascondi automaticamente (solo all'interno del gruppo z order).

Un'applicazione usa il [**messaggio \_ SETAUTOHIDEBAR di ABM**](abm-setautohidebar.md) per registrare o annullare la registrazione di un AppBar di Nascondi automaticamente. Il messaggio specifica il bordo per AppBar e un flag che specifica se il AppBar deve essere registrato o annullato. Il messaggio ha esito negativo se un AppBar di Nascondi automaticamente viene registrato, ma ne è già associato uno al bordo specificato. Un'applicazione può recuperare l'handle per il AppBar di Nascondi automaticamente associato a un bordo inviando il messaggio di [**\_ GETAUTOHIDEBAR ABM**](abm-getautohidebar.md) .

Non è necessario che un AppBar di Nascondi automaticamente si registri come AppBar normali; Ciò significa che non è necessario registrarlo inviando il nuovo messaggio [**ABM \_**](abm-new.md) . Un AppBar non registrato da **ABM \_ New** si sovrappone a qualsiasi AppBar ancorato sullo stesso bordo dello schermo.

### <a name="appbar-notification-messages"></a>Messaggi di notifica AppBar

Il sistema invia messaggi per notificare a un AppBar gli eventi che possono influire sulla posizione e sull'aspetto. I messaggi vengono inviati nel contesto di un messaggio definito dall'applicazione. L'applicazione specifica l'identificatore del messaggio quando invia il nuovo messaggio [**ABM \_**](abm-new.md) per registrare il AppBar. Il codice di notifica si trova nel parametro *wParam* del messaggio definito dall'applicazione.

Un AppBar riceve il messaggio di notifica [**\_ POSCHANGED di ABN**](abn-poschanged.md) quando cambia la dimensione, la posizione o lo stato di visibilità della barra delle applicazioni, quando un altro AppBar viene aggiunto allo stesso bordo dello schermo o quando un altro AppBar sullo stesso bordo dello schermo viene ridimensionato o rimosso. Un AppBar deve rispondere a questo messaggio di notifica inviando i messaggi [**ABM \_ QUERYPOS**](abm-querypos.md) e [**ABM \_ SETPOS**](abm-setpos.md) . Se la posizione di un AppBar è cambiata, deve chiamare la funzione [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) per spostarsi alla nuova posizione.

Il sistema invia il messaggio di notifica [**\_ STATECHANGE di ABN**](abn-statechange.md) ogni volta che lo stato di Nascondi automaticamente o sempre in primo piano della barra delle applicazioni è cambiato, ovvero quando l'utente seleziona o deseleziona la casella di controllo **Always on top** o **Nascondi automaticamente** nella finestra delle proprietà della barra delle applicazioni. Un AppBar può utilizzare questo messaggio di notifica per impostare lo stato di conformità a quello della barra delle applicazioni, se lo si desidera.

Quando viene avviata un'applicazione a schermo intero o quando viene chiusa l'ultima applicazione a schermo intero, un AppBar riceve il messaggio di notifica [**\_ FULLSCREENAPP di ABN**](abn-fullscreenapp.md) . Il parametro *lParam* indica se l'applicazione a schermo intero è in apertura o in chiusura. Se si apre, il AppBar deve essere rilasciato nella parte inferiore dello z-order. Il AppBar deve ripristinare la posizione dell'ordine z quando l'ultima applicazione a schermo intero è stata chiusa.

Un AppBar riceve il messaggio di notifica [**\_ WINDOWARRANGE di ABN**](abn-windowarrange.md) quando l'utente seleziona il comando Cascade, affianca orizzontalmente o Affianca verticalmente dal menu di scelta rapida della barra delle applicazioni. Il sistema invia il messaggio due volte, prima di ridisporre le finestre (*lParam* è **true**) e dopo la disposizione di Windows (*lParam* è **false**).

Un AppBar può usare i messaggi [**\_ WINDOWARRANGE di ABN**](abn-windowarrange.md) per escludere se stesso dall'operazione Cascade o Tile. Per escludere se stesso, AppBar deve nascondersi quando *lParam* è **true** e mostrarsi quando *lParam* è **false**. Se un AppBar si nasconde in risposta a questo messaggio, non è necessario inviare i messaggi [**ABM \_ QUERYPOS**](abm-querypos.md) e [**ABM \_ SETPOS**](abm-setpos.md) in risposta all'operazione Cascade o Tile.

## <a name="registering-an-application-desktop-toolbar"></a>Registrazione di una barra degli strumenti del desktop dell'applicazione

Un'applicazione deve registrare un AppBar inviando il [**\_ nuovo messaggio ABM**](abm-new.md) . La registrazione di un AppBar lo aggiunge all'elenco interno del sistema e fornisce al sistema un identificatore di messaggio da usare per inviare messaggi di notifica al AppBar. Prima di uscire, un'applicazione deve annullare la registrazione del AppBar inviando il messaggio di [**\_ rimozione di ABM**](abm-remove.md) . L'annullamento della registrazione rimuove il AppBar dall'elenco interno del sistema e impedisce alla barra di ricevere messaggi di notifica AppBar.

La funzione nell'esempio seguente registra o Annulla la registrazione di un AppBar, a seconda del valore di un parametro del flag booleano.


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



## <a name="setting-the-appbar-size-and-position"></a>Impostazione delle dimensioni e della posizione del AppBar

Un'applicazione deve impostare le dimensioni e la posizione di un AppBar dopo la registrazione del AppBar, dopo che l'utente ha spostato o ridimensionato il AppBar e ogni volta che il AppBar riceve il messaggio di notifica [**\_ POSCHANGED di ABN**](abn-poschanged.md) . Prima di impostare le dimensioni e la posizione del AppBar, l'applicazione esegue una query sul sistema per un rettangolo di delimitazione approvato inviando il messaggio di [**\_ QUERYPOS ABM**](abm-querypos.md) . Il sistema restituisce un rettangolo di delimitazione che non interferisce con la barra delle applicazioni o con altri AppBar. Il sistema regola il rettangolo esclusivamente in base alla sottrazione del rettangolo. non è possibile mantenere le dimensioni iniziali del rettangolo. Per questo motivo, il AppBar deve modificare il rettangolo, se necessario, dopo l'invio **di \_ QUERYPOS ABM**.

Successivamente, l'applicazione passa di nuovo il rettangolo di delimitazione al sistema tramite il [**messaggio \_ SETPOS di ABM**](abm-setpos.md) . Chiama quindi la funzione [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) per spostare il AppBar in posizione.

Nell'esempio seguente viene illustrato come impostare le dimensioni e la posizione di un AppBar.


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



## <a name="processing-appbar-notification-messages"></a>Elaborazione dei messaggi di notifica AppBar

Un AppBar riceve un messaggio di notifica quando viene modificato lo stato della barra delle applicazioni, quando viene avviata un'applicazione a schermo intero (o l'ultimo si chiude) o quando si verifica un evento che può influire sulle dimensioni e la posizione di AppBar. Nell'esempio seguente viene illustrato come elaborare i vari messaggi di notifica.


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



La funzione seguente regola il rettangolo di delimitazione di un AppBar e quindi chiama la funzione AppBarQuerySetPos definita dall'applicazione (inclusa nella sezione precedente) per impostare di conseguenza le dimensioni e la posizione della barra.


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



 

 
