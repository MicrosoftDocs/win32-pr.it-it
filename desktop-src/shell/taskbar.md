---
description: L'interfaccia di Windows include una barra degli strumenti del desktop applicazione speciale denominata barra delle applicazioni. È possibile utilizzare la barra delle applicazioni per attività come il cambio tra le finestre aperte e l'avvio di nuove applicazioni.
ms.assetid: 14d520e7-7c15-441d-9662-24b972d208ac
title: Barra delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce37991c6265f02ab92ece62dbae341031d272a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994968"
---
# <a name="the-taskbar"></a>Barra delle applicazioni

L'interfaccia di Windows include una [barra degli strumenti del desktop applicazione](application-desktop-toolbars.md) speciale denominata *barra delle applicazioni*. È possibile utilizzare la barra delle applicazioni per attività come il cambio tra le finestre aperte e l'avvio di nuove applicazioni.

> [!Note]  
> Per informazioni sulle modifiche apportate alla barra delle applicazioni a partire da Windows 7, vedere [estensioni della barra delle applicazioni](taskbar-extensions.md).

 

In questo argomento sono contenute le sezioni seguenti.

-   [Informazioni sulla barra delle applicazioni](#about-the-taskbar)
    -   [Opzioni di visualizzazione della barra delle applicazioni](#taskbar-display-options)
    -   [Aggiunta di collegamenti al menu Start](#adding-shortcuts-to-the-start-menu)
    -   [Gestione dei pulsanti della barra delle applicazioni](#managing-taskbar-buttons)
    -   [Aggiunta, modifica ed eliminazione di icone nell'area di notifica](#adding-modifying-and-deleting-icons-in-the-notification-area)
    -   [Notifica di creazione della barra delle applicazioni](#taskbar-creation-notification)
-   [Uso della barra delle applicazioni](#using-the-taskbar)
    -   [Aggiunta ed eliminazione delle icone delle barre degli strumenti nell'area di notifica](#adding-and-deleting-taskbar-icons-in-the-notification-area)
    -   [Ricezione di eventi del mouse](#receiving-mouse-events)

## <a name="about-the-taskbar"></a>Informazioni sulla barra delle applicazioni

La barra delle applicazioni include quanto segue:

-   Menu **Start**
-   Barra avvio veloce (solo Windows Vista e versioni precedenti)
-   Pulsanti della barra delle applicazioni
-   Barre degli strumenti (facoltativo)
-   Area delle notifiche

Il menu **Start** contiene i comandi che consentono di accedere a programmi, documenti e impostazioni. Questi comandi includono **tutti i programmi, i** **documenti**, il **Pannello di controllo**, i **giochi**, la **Guida e il supporto tecnico**, l' **arresto** e la **ricerca di programmi e file**.

L' **avvio** nelle versioni precedenti di Windows conteneva elementi quali **trova** ed **Esegui**, la cui funzionalità era inclusa nei **programmi e nei file di ricerca** in Windows Vista e versioni successive.

La barra avvio veloce, disponibile nelle versioni di Windows precedenti a Windows 7, contiene collegamenti alle applicazioni. Windows fornisce voci predefinite, ad esempio Windows Internet Explorer, e l'utente può aggiungere eventuali altri collegamenti scelti. Le icone in quest'area rispondono a un solo clic. In Windows 7 e versioni successive questa funzionalità è inclusa nei pulsanti della barra delle applicazioni.

La shell posiziona un pulsante sulla barra delle applicazioni ogni volta che un'applicazione crea una finestra senza proprietario, ovvero una finestra che non dispone di un elemento padre e con i bit di stile estesi appropriati. vedere la sezione relativa alla [gestione dei pulsanti della barra delle applicazioni](#managing-taskbar-buttons). Per passare a una finestra, l'utente fa clic sul pulsante della finestra. Questa funzionalità è stata notevolmente espansa a partire da Windows 7. Per ulteriori informazioni, vedere [estensioni della barra delle applicazioni](taskbar-extensions.md).

Le applicazioni possono inserire icone nell'area di notifica per indicare lo stato di un'operazione o per notificare all'utente un evento. Un'applicazione potrebbe ad esempio inserire un'icona della stampante nell'area di notifica per indicare che un processo di stampa è in corso. Tuttavia, in Windows 7 e versioni successive, alcune delle informazioni fornite in precedenza dall'area di notifica devono essere fornite tramite il pulsante della barra delle applicazioni di un'applicazione. L'area di notifica si trova sul bordo destro della barra delle applicazioni (se la barra delle applicazioni è orizzontale) o nella parte inferiore (se la barra delle applicazioni è verticale). Per ulteriori informazioni, vedere [notifiche e l'area di notifica](notification-area.md).

L'area di notifica Visualizza anche l'ora corrente se è selezionata questa opzione. L'opzione è disponibile come:

-   **Windows 7 e versioni successive**: l'elenco a discesa **Clock** nella pagina **attiva o disattiva icone di sistema** dell'applicazione del pannello di controllo delle icone dell' **area di notifica** , accessibile anche tramite le proprietà dell'area di notifica.
-   **Windows Vista**: la casella di controllo **Clock** nella pagina **area di notifica** della finestra delle proprietà della **barra delle applicazioni e del menu Start** .
-   **Windows XP**: la casella di controllo **Mostra Clock** nella finestra **delle proprietà della barra delle applicazioni e del menu Start** .

È possibile fare clic con il pulsante destro del mouse sulla barra delle applicazioni per visualizzare il menu di scelta rapida. Nel menu di scelta rapida sono inclusi i comandi per le finestre a cascata, le finestre dello stack, le finestre affiancate, il desktop, avviare Gestione attività e impostare le proprietà della barra delle applicazioni. Nel menu di scelta rapida è inoltre disponibile l'opzione per aggiungere o rimuovere un set di barre degli strumenti dalla barra delle applicazioni. È possibile aggiungere nuove barre degli strumenti a questo menu eseguendone la registrazione nella categoria CATId \_ deskband. Per altre informazioni, vedere [implementazione di oggetti banda](band-objects.md). Si noti che, a partire da Windows 7, la barra delle applicazioni e l'area di notifica dispongono di menu di scelta rapida distinti. Questi menu di scelta rapida condividono alcune opzioni, ad esempio la disposizione della finestra, e ne aggiungono altre.

### <a name="taskbar-display-options"></a>Opzioni di visualizzazione della barra delle applicazioni

La barra delle applicazioni supporta due opzioni di visualizzazione: Nascondi automaticamente e, solo in Windows Vista e versioni precedenti, Always On Top (la barra delle applicazioni è sempre in questa modalità in Windows 7 e versioni successive). Per impostare queste opzioni, l'utente deve aprire il menu di scelta rapida della barra delle applicazioni, fare clic su **Proprietà** e selezionare o deselezionare la casella di controllo **Nascondi automaticamente la barra delle applicazioni** o **Mantieni la barra delle applicazioni su altre finestre** . Per recuperare lo stato di queste opzioni di visualizzazione, utilizzare il messaggio [**ABM \_ GetState**](abm-getstate.md) . Se si desidera ricevere una notifica quando lo stato di queste opzioni di visualizzazione cambia, elaborare il messaggio di notifica [**\_ STATECHANGE di ABN**](abn-statechange.md) nella routine della finestra. Per modificare lo stato di queste opzioni di visualizzazione, utilizzare il messaggio di [**\_ stato ABM**](abm-setstate.md) .

L' *area di lavoro* è la parte dello schermo non nascosta dalla barra delle applicazioni. Per recuperare le dimensioni dell'area di lavoro, chiamare la funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con il valore **SPI \_ GETWORKAREA** impostato. Per recuperare le coordinate del rettangolo che descrivono la posizione della barra delle applicazioni, utilizzare il messaggio [**\_ GETTASKBARPOS di ABM**](abm-gettaskbarpos.md) .

È possibile coprire la barra delle applicazioni impostando in modo esplicito le dimensioni del rettangolo della finestra uguale alla dimensione dello schermo con [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos). Per i sistemi Windows 2000 o versioni successive, la finestra non deve avere [**WS \_ Caption**](../winmsg/window-styles.md) o [**WS \_ THICKFRAME**](../winmsg/window-styles.md). in caso contrario, la finestra deve essere ridimensionata in modo che l'area client copra l'intero schermo. Inoltre, in particolare, se la barra delle applicazioni è impostata su Always On Top, rimarrà nascosta solo mentre l'applicazione è l'applicazione in primo piano.

### <a name="adding-shortcuts-to-the-start-menu"></a>Aggiunta di collegamenti al menu Start

Per aggiungere un elemento al sottomenu **programmi** in Microsoft windows NT 4,0, Windows 2000 e versioni successive o Windows 95 o versione successiva, attenersi alla seguente procedura.

1.  Creare un [collegamento della shell](./links.md) usando l'interfaccia [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .
2.  Ottenere il PIDL della cartella programmi usando [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation), passando i [**\_ programmi CSIDL**](csidl.md).
3.  Aggiungere il collegamento della shell alla cartella programmi. È anche possibile creare una cartella nella cartella programmi e aggiungere il collegamento a tale cartella.

### <a name="managing-taskbar-buttons"></a>Gestione dei pulsanti della barra delle applicazioni

La shell crea un pulsante sulla barra delle applicazioni ogni volta che un'applicazione crea una finestra che non è di proprietà. Per assicurarsi che il pulsante finestra venga inserito sulla barra delle applicazioni, creare una finestra senza proprietario con lo stile esteso [**WS \_ \_ AppWindow**](../winmsg/extended-window-styles.md) . Per evitare che il pulsante della finestra venga inserito sulla barra delle applicazioni, creare la finestra senza proprietario con lo stile esteso [**WS \_ \_ TOOLWINDOW**](../winmsg/extended-window-styles.md) . In alternativa, è possibile creare una finestra nascosta e rendere questa finestra nascosta il proprietario della finestra visibile.

La shell rimuoverà il pulsante di una finestra dalla barra delle applicazioni solo se lo stile della finestra supporta i pulsanti della barra delle applicazioni visibile. Per modificare in modo dinamico lo stile di una finestra che non supporta i pulsanti della barra delle applicazioni visibili, è necessario nascondere prima la finestra (chiamando [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) con il **pulsante \_ Nascondi di SW**), modificare lo stile della finestra e quindi visualizzare la finestra.

Il pulsante finestra contiene in genere l'icona e il titolo dell'applicazione. Tuttavia, se l'applicazione non contiene un menu di sistema, il pulsante della finestra viene creato senza l'icona.

Se si desidera che l'applicazione ottenga l'attenzione dell'utente quando la finestra non è attiva, utilizzare la funzione [**FlashWindow**](/windows/win32/api/winuser/nf-winuser-flashwindow) per indicare all'utente che un messaggio è in attesa. Questa funzione lampeggia il pulsante della finestra. Quando l'utente fa clic sul pulsante della finestra per attivare la finestra, l'applicazione può visualizzare il messaggio.

### <a name="modifying-the-contents-of-the-taskbar"></a>Modifica del contenuto della barra delle applicazioni

La [versione 4,71 e successive](versions.md) di Shell32.dll aggiunge la funzionalità per modificare il contenuto della barra delle applicazioni. Da un'applicazione, ora è possibile aggiungere, rimuovere e attivare i pulsanti della barra delle applicazioni. L'attivazione dell'elemento non attiva la finestra; Mostra l'elemento premuto sulla barra delle applicazioni.

Le funzionalità di modifica della barra delle applicazioni sono implementate in un oggetto Component Object Model (COM) (la \_ barra delle applicazioni CLSID) che espone l'interfaccia [**ITASKBARLIST**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) (IID \_ ITaskbarList). È necessario chiamare il metodo [**ITaskbarList:: HrInit**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist-hrinit) per inizializzare l'oggetto. È quindi possibile usare i metodi dell'interfaccia [**ITaskbarList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) per modificare il contenuto della barra delle applicazioni.

### <a name="adding-modifying-and-deleting-icons-in-the-notification-area"></a>Aggiunta, modifica ed eliminazione di icone nell'area di notifica

Utilizzare la [**funzione \_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) per aggiungere, modificare o eliminare icone dall'area di notifica. Il parametro *dwMessage* della **Shell \_ NotifyIcon** è un messaggio alla barra delle applicazioni che specifica l'azione da intraprendere. Il parametro *PNid* è un puntatore a una struttura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) utilizzata per identificare l'icona e passare eventuali informazioni aggiuntive necessarie per l'elaborazione del messaggio da parte del sistema.

Con le icone dell'area di notifica è possibile eseguire le azioni seguenti.

-   Per aggiungere un'icona all'area di notifica della barra delle applicazioni, chiamare la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con il parametro *dwMessage* impostato su NIM \_ Add. La struttura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) viene utilizzata per specificare l'handle e l'identificatore dell'icona e qualsiasi testo della descrizione comando. Se l'utente ha selezionato la casella di controllo **Mostra Clock** nelle proprietà della barra delle applicazioni, il sistema posiziona l'icona sulla sinistra del clock. In caso contrario, l'icona viene visualizzata sul lato destro o nella parte inferiore della barra delle applicazioni. Qualsiasi icona esistente viene spostata a sinistra per fare spazio per la nuova icona.
-   Per modificare le informazioni di un'icona, inclusi il relativo handle di icona, il testo della descrizione comando e l'identificatore del messaggio di callback, chiamare la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con *dwMessage* impostata su NIM \_ Modify.
-   Per eliminare un'icona dall'area di notifica, chiamare la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con il parametro *dwMessage* impostato su NIM \_ Delete.

Al termine di un'operazione dell'interfaccia utente, restituire lo stato attivo all'area di notifica chiamando la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con *DWMESSAGE* impostato su NIM \_ SetFocus. Ad esempio, è possibile eseguire questa operazione quando un'icona della barra delle applicazioni Visualizza un menu di scelta rapida, ma l'utente lo annulla premendo il tasto ESC.

### <a name="receiving-notification-area-callback-messages"></a>Ricezione di messaggi di callback dell'area di notifica

Le applicazioni in genere inseriscono icone nell'area di notifica della barra delle applicazioni per fungere da indicatori di stato. È possibile fornire informazioni aggiuntive quando l'utente esegue le azioni del mouse, ad esempio lo spostamento del puntatore del mouse sull'icona o il clic sull'icona.

Il sistema invia notifiche agli eventi del mouse e della tastiera inviando un messaggio di callback definito dall'applicazione associato a una particolare icona. In questo modo, il sistema può notificare a un'applicazione quando l'utente, ad esempio, fa clic sull'icona o la seleziona premendo un tasto.

Si definisce il messaggio di callback di un'icona quando si aggiunge l'icona alla barra delle applicazioni. L'identificatore del messaggio di callback viene specificato nel membro **uCallbackMessage** della struttura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) passata con Nim \_ Add. Quando si verifica un evento, il sistema invia il messaggio di callback alla routine della finestra specificata dal membro **HWND** . Il parametro *wParam* del messaggio contiene l'identificatore dell'icona della barra delle applicazioni in cui si è verificato l'evento. Il parametro *lParam* include il mouse o il messaggio della tastiera associato all'evento. Ad esempio, quando il puntatore del mouse si sposta su un'icona della barra delle applicazioni, *lParam* contiene [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md).

I risultati di diversi eventi del mouse possono essere riepilogati come segue:

-   Quando l'utente sposta il puntatore del mouse sull'icona, il sistema Visualizza il testo della descrizione comando specificato in [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa).
-   Quando l'utente fa clic sull'icona, l'applicazione riceve una notifica [**\_ LBUTTONDOWN WM**](../inputdev/wm-lbuttondown.md) .
-   Quando l'utente fa clic con il pulsante destro del mouse sull'icona, l'applicazione riceve una notifica [**\_ RBUTTONDOWN WM**](../inputdev/wm-rbuttondown.md) .
-   Quando l'utente fa doppio clic sull'icona, l'applicazione riceve una [**notifica \_ LBUTTONDBLCLK WM**](../inputdev/wm-lbuttondblclk.md) .

In genere, facendo clic sull'icona si fa in modo che l'applicazione visualizzi una finestra con ulteriori informazioni, facendo clic con il pulsante destro del mouse sul menu di scelta rapida e scegliendo Esegui il comando di menu di scelta rapida predefinito.

Per un esempio di come modificare il testo della descrizione comando associato a un'icona dell'area di notifica, vedere le [descrizioni comandi dei fumetti per le icone della barra di stato](../controls/tooltip-controls.md).

Le versioni 5,0 e successive della shell gestiscono gli eventi del mouse e della tastiera [**\_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) della shell in modi diversi rispetto alle versioni precedenti della shell presenti in Windows NT 4,0, Windows 95 e Windows 98. Le differenze sono le seguenti:

-   Se un utente richiede il menu di scelta rapida di un'icona di notifica con la tastiera, la shell versione 5,0 invia all'applicazione associata un messaggio [**WM \_ ContextMenu**](../menurc/wm-contextmenu.md) . Le versioni precedenti inviano messaggi [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) e [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md) .
-   Se un utente seleziona un'icona di notifica con la tastiera e la attiva con la barra spaziatrice o il tasto invio, la shell della versione 5,0 invia all'applicazione associata una notifica di **\_ selezione** della chiave Nin. Le versioni precedenti inviano messaggi [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) e [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md) .
-   Se un utente seleziona un'icona di notifica con il mouse e la attiva con il tasto invio, la shell della versione 5,0 invia all'applicazione associata una notifica **\_ Select Nin** . Le versioni precedenti inviano messaggi [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) e [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md) .
-   Se un utente passa il puntatore del mouse su un'icona a cui è associata una descrizione comandi a fumetto, la versione 6,0 della shell (Windows XP) Invia i messaggi seguenti.
    -   -   **Nin \_ BALLOONSHOW** : inviato quando viene visualizzato il fumetto (i palloni vengono accodati).
        -   **Nin \_ BALLOONHIDE** : inviato quando il fumetto scompare, ad esempio quando l'icona viene eliminata. Questo messaggio non viene inviato se il fumetto viene eliminato a causa di un timeout o di un clic del mouse.
        -   **Nin \_ BALLOONTIMEOUT** : inviato quando il fumetto viene eliminato a causa di un timeout.
        -   **Nin \_ BALLOONUSERCLICK** : inviato quando il fumetto viene eliminato a causa di un clic del mouse.

È possibile selezionare il modo in cui la shell deve comportarsi chiamando la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con *dwMessage* impostato su **NIM \_ seversion**. Impostare il membro **uVersion** della struttura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) per indicare se si desidera la versione 5,0 o il comportamento precedente alla versione 5,0.

### <a name="taskbar-creation-notification"></a>Notifica di creazione della barra delle applicazioni

Con Microsoft Internet Explorer 4,0 e versioni successive, la shell notifica alle applicazioni che la barra delle applicazioni è stata creata. Quando viene creata la barra delle applicazioni, viene registrato un messaggio con la stringa TaskbarCreated e il messaggio viene trasmesso a tutte le finestre di primo livello. Quando l'applicazione della barra delle applicazioni riceve questo messaggio, è necessario presupporre che tutte le icone della barra delle applicazioni aggiunte siano state rimosse e aggiungerle nuovamente. Questa funzionalità viene in genere applicata solo ai servizi già in esecuzione all'avvio della shell. Nell'esempio seguente viene illustrato un metodo molto semplificato per la gestione di questo caso.

In Windows 10 la barra delle applicazioni trasmette anche questo messaggio quando viene modificato il valore DPI dello schermo principale.

```
LRESULT CALLBACK WndProc(HWND hWnd, 
                         UINT uMessage, 
                         WPARAM wParam, 
                         LPARAM lParam)
{
    static UINT s_uTaskbarRestart;

    switch(uMessage)
    {
        case WM_CREATE:
            s_uTaskbarRestart = RegisterWindowMessage(TEXT("TaskbarCreated"));
            break;
        
        default:
            if(uMessage == s_uTaskbarRestart)
                AddTaskbarIcons();
            break;
    }

    return DefWindowProc(hWnd, uMessage, wParam, lParam);
}
```



## <a name="using-the-taskbar"></a>Uso della barra delle applicazioni

Questa sezione include esempi che illustrano come aggiungere icone all'area di notifica della barra delle applicazioni e come elaborare i messaggi di callback per le icone della barra delle applicazioni.

### <a name="adding-and-deleting-taskbar-icons-in-the-notification-area"></a>Aggiunta ed eliminazione delle icone delle barre degli strumenti nell'area di notifica

Per aggiungere un'icona all'area di notifica della barra delle applicazioni, compilare una struttura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) e quindi passare la struttura a [**\_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con *dwMessage* impostato su **NIM \_ Add**. I membri della struttura devono specificare l'handle per la finestra che aggiunge l'icona, nonché l'identificatore dell'icona e l'handle dell'icona. È anche possibile specificare il testo della descrizione comando per l'icona. Se è necessario ricevere i messaggi del mouse per l'icona, specificare l'identificatore del messaggio di callback che il sistema deve usare per inviare il messaggio alla routine della finestra.

La funzione nell'esempio seguente illustra come aggiungere un'icona alla barra delle applicazioni.


```
// MyTaskBarAddIcon - adds an icon to the notification area. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window to receive callback messages 
// uID - identifier of the icon 
// hicon - handle to the icon to add 
// lpszTip - tooltip text 

BOOL MyTaskBarAddIcon(HWND hwnd, UINT uID, HICON hicon, LPSTR lpszTip) 
{ 
    BOOL res; 
    NOTIFYICONDATA tnid; 
 
    tnid.cbSize = sizeof(NOTIFYICONDATA); 
    tnid.hWnd = hwnd; 
    tnid.uID = uID; 
    tnid.uFlags = NIF_MESSAGE | NIF_ICON | NIF_TIP; 
    tnid.uCallbackMessage = MYWM_NOTIFYICON; 
    tnid.hIcon = hicon; 
    if (lpszTip) 
        hr = StringCbCopyN(tnid.szTip, sizeof(tnid.szTip), lpszTip, 
                           sizeof(tnid.szTip));
        // TODO: Add error handling for the HRESULT.
    else 
        tnid.szTip[0] = (TCHAR)'\0'; 
 
    res = Shell_NotifyIcon(NIM_ADD, &tnid); 
 
    if (hicon) 
        DestroyIcon(hicon); 
 
    return res; 
}
```



Per eliminare un'icona dall'area di notifica della barra delle applicazioni, compilare una struttura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) e chiamare la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) con *dwMessage* impostato su **NIM \_ Delete**. Quando si elimina un'icona della barra delle applicazioni, specificare solo i membri **cbSize**, **HWND** e **uID** della struttura. Ad esempio:


```
// MyTaskBarDeleteIcon - deletes an icon from the notification area. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window that added the icon. 
// uID - identifier of the icon to delete. 

BOOL MyTaskBarDeleteIcon(HWND hwnd, UINT uID) 
{ 
    BOOL res; 
    NOTIFYICONDATA tnid; 
 
    tnid.cbSize = sizeof(NOTIFYICONDATA); 
    tnid.hWnd = hwnd; 
    tnid.uID = uID; 
         
    res = Shell_NotifyIcon(NIM_DELETE, &tnid); 
    return res; 
}
```



### <a name="receiving-mouse-events"></a>Ricezione di eventi del mouse

Se si specifica un messaggio di callback per un'icona della barra delle applicazioni, il sistema invia il messaggio all'applicazione ogni volta che si verifica un evento del mouse nel rettangolo di delimitazione dell'icona. Il parametro *wParam* del messaggio specifica l'identificatore dell'icona della barra delle applicazioni e il parametro *lParam* del messaggio specifica il messaggio generato dal sistema come risultato dell'evento del mouse.

La funzione nell'esempio seguente è di un'applicazione che aggiunge le icone della batteria e della stampante alla barra delle applicazioni. L'applicazione chiama la funzione quando riceve un messaggio di callback. La funzione determina se l'utente ha fatto clic su una delle icone e, se si è verificato un clic, chiama una funzione definita dall'applicazione per visualizzare le informazioni sullo stato.


```
// On_MYWM_NOTIFYICON - processes callback messages for taskbar icons. 
// wParam - first message parameter of the callback message. 
// lParam - second message parameter of the callback message. 

void On_MYWM_NOTIFYICON(WPARAM wParam, LPARAM lParam) 
{ 
    UINT uID; 
    UINT uMouseMsg; 
 
    uID = (UINT) wParam; 
    uMouseMsg = (UINT) lParam; 
 
    if (uMouseMsg == WM_LBUTTONDOWN) 
    { 
        switch (uID) 
        { 
            case IDI_MYBATTERYICON: 
 
                // The user clicked the battery icon. Display the 
                // battery status. 
                ShowBatteryStatus(); 
                break; 
 
            case IDI_MYPRINTERICON: 
 
                // The user clicked the printer icon. Display the 
                // status of the print job. 
                ShowJobStatus(); 
                break; 
 
            default: 
                break; 
        } 
     } 

     return; 
 }
```



 

 
