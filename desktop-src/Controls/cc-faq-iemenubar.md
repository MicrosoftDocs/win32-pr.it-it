---
title: Come creare una barra dei menu Explorer-Style Internet
description: A prima vista, la barra dei menu in Microsoft Internet Explorer 5 e versioni successive ha un aspetto simile a quello di un menu standard. Tuttavia, l'aspetto è molto diverso quando si inizia a usarlo.
ms.assetid: e0fe25f2-3d49-4c5a-a3f9-2f468f2cfef2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b262bc55407d263c97d4bd7e3938a9794d3a58f5
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103873001"
---
# <a name="how-to-create-an-internet-explorer-style-menu-bar"></a>Come creare una barra dei menu Explorer-Style Internet

A prima vista, la barra dei menu in Microsoft Internet Explorer 5 e versioni successive ha un aspetto simile a quello di un menu standard. Tuttavia, l'aspetto è molto diverso quando si inizia a usarlo.

Lo screenshot seguente mostra la barra dei menu di Windows Internet Explorer con il menu strumenti selezionato.

![screenshot che mostra la barra dei menu di Windows Internet Explorer con il menu strumenti selezionato](images/howto8.jpg)

La barra dei menu è in realtà un controllo Toolbar simile a un menu standard. Anziché le voci di menu di primo livello, una barra dei menu include una serie di pulsanti di solo testo che visualizzano un menu a discesa quando si fa clic su di esso. Tuttavia, come tipo specializzato di barra degli strumenti, una barra dei menu presenta alcune funzionalità non disponibili nei menu standard:

-   Può essere personalizzato utilizzando le tecniche standard della barra degli strumenti, consentendo all'utente di spostare, eliminare o aggiungere elementi.
-   È possibile eseguire il monitoraggio a caldo, in modo che gli utenti sappiano quando si trovano su un elemento di livello superiore senza prima fare clic su di esso.

Una barra dei menu può essere incorporata in un controllo Rebar, fornendo le funzionalità seguenti:

-   Può avere un grip, che consente all'utente di spostare o ridimensionare la banda.
-   Può condividere una striscia nel controllo Rebar con altre bande, ad esempio la barra degli strumenti standard nella figura precedente.
-   Può visualizzare una freccia di espansione quando è coperta da una banda adiacente, concedendo all'utente l'accesso agli elementi nascosti.
-   Può avere una bitmap di sfondo definita dall'applicazione.

In questo argomento viene illustrato come implementare una barra dei menu. Poiché una barra dei menu è un'implementazione specializzata di un controllo Toolbar, lo stato attivo si troverà negli argomenti specifici delle barre dei menu. Per informazioni su come incorporare una barra degli strumenti in un controllo Rebar, vedere [come creare una barra degli strumenti Explorer-Style Internet](cc-faq-ietoolbar.md) e [informazioni sui controlli Rebar](rebar-controls.md).

-   [Creazione di una barra degli strumenti in una barra dei menu](#making-a-toolbar-into-a-menu-bar)
-   [Gestione della navigazione con il menu Hot-Tracking disabilitato](#handling-navigation-with-menu-hot-tracking-disabled)
    -   [Navigazione del mouse](#mouse-navigation)
    -   [Navigazione da tastiera](#keyboard-navigation)
    -   [Navigazione mista](#mixed-navigation)
-   [Gestione della navigazione con il menu Hot-Tracking abilitato](#handling-navigation-with-menu-hot-tracking-enabled)
    -   [Elaborazione dei messaggi per il rilevamento a caldo del menu](#message-processing-for-menu-hot-tracking)
    -   [Navigazione del mouse](#mouse-navigation)
    -   [Navigazione da tastiera](#keyboard-navigation)

## <a name="making-a-toolbar-into-a-menu-bar"></a>Creazione di una barra degli strumenti in una barra dei menu

Per creare una barra degli strumenti in una barra dei menu:

-   Creare una barra degli strumenti Flat includendo [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) con gli altri flag di stile della finestra. Lo **stile \_ Flat TBSTYLE** Abilita anche il rilevamento a caldo. Con questo stile, la barra dei menu è simile a un menu standard fino a quando l'utente non attiva un pulsante. Quindi, il pulsante sembra uscire dalla barra degli strumenti e premere quando si fa clic su di esso, proprio come un pulsante standard. Poiché il rilevamento a caldo è abilitato, per attivare un pulsante è sufficiente passare il puntatore del mouse su di esso. Se il cursore si sposta su un altro pulsante, viene attivato e il pulsante precedente viene disattivato.
-   Creare pulsanti di tipo elenco includendo [**l' \_ elenco TBSTYLE**](toolbar-control-and-button-styles.md) con gli altri flag di stile della finestra. Questo stile crea un pulsante più sottile che sembra più simile a una voce di menu di primo livello standard.
-   Impostare i pulsanti solo per il testo impostando il membro **iBitmap** della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) del pulsante su i \_ IMAGENONE e il  membro di di base al testo del pulsante.
-   Assegnare a ogni pulsante lo stile a [**\_ discesa BTNS**](toolbar-control-and-button-styles.md) . Quando si fa clic sul pulsante, il controllo Toolbar invia all'applicazione una notifica a [ \_ discesa TBN](tbn-dropdown.md) per chiedere di visualizzare il menu del pulsante.
-   Incorporare la barra dei menu in una banda del controllo Rebar. Abilitare sia i grip che le frecce, come illustrato in [come creare una barra degli strumenti Explorer-Style Internet](cc-faq-ietoolbar.md).
-   Implementare un gestore a [ \_ discesa TBN](tbn-dropdown.md) per visualizzare il *menu a discesa* del pulsante quando viene selezionato. Il menu a discesa è un tipo di menu di scelta rapida. Viene creato tramite la funzione [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) , con l'angolo superiore sinistro allineato all'angolo inferiore sinistro del pulsante.
-   Implementare la navigazione tramite tastiera, in modo che la barra dei menu sia completamente accessibile senza mouse.
-   Implementare il monitoraggio a caldo del menu. Con i menu standard, dopo che è stato visualizzato il menu di una voce di menu di primo livello, lo stato del cursore su un altro elemento di primo livello Visualizza automaticamente il menu e comprime il menu dell'elemento precedente. Il controllo Toolbar rileverà il cursore e modificherà l'immagine del pulsante, ma visualizzerà automaticamente il nuovo menu. L'applicazione deve eseguire questa operazione in modo esplicito.

La maggior parte di questi elementi è semplice da implementare e viene discussa altrove. Per informazioni generali su come usare le barre degli strumenti e i controlli Rebar, vedere [come creare una barra degli strumenti Explorer-Style Internet](cc-faq-ietoolbar.md), [informazioni sui controlli della barra degli strumenti](toolbar-controls-overview.md)o [sui controlli Rebar](rebar-controls.md) . Per informazioni su come gestire i menu popup, vedere i [menu](/windows/desktop/menurc/menus) . Nella parte restante di questo argomento vengono illustrati i due elementi finali, la navigazione da tastiera e il monitoraggio a caldo del menu.

## <a name="handling-navigation-with-menu-hot-tracking-disabled"></a>Gestione della navigazione con il menu Hot-Tracking disabilitato

Gli utenti possono scegliere di spostarsi sulla barra dei menu con il mouse, la tastiera o una combinazione di entrambi. Per implementare la navigazione della barra dei menu, l'applicazione deve gestire le notifiche della barra degli strumenti e monitorare il mouse e la tastiera. Questa attività può essere suddivisa in due parti distinte: con e senza rilevamento a caldo dei menu. In questa sezione viene illustrato come gestire la navigazione quando non viene visualizzato alcun menu e il menu di scelta rapida non è abilitato.

### <a name="mouse-navigation"></a>Navigazione del mouse

Se la registrazione a caldo del menu è disabilitata, è possibile trattare una barra dei menu come barra degli strumenti normale. Se l'utente si sposta con un mouse, è necessario che tutte le applicazioni eseguano la gestione della notifica a [ \_ discesa TBN](tbn-dropdown.md) . Quando viene ricevuta questa notifica, Visualizza il menu a discesa appropriato e Abilita il rilevamento a caldo del menu. Da quel punto in poi, si sta usando il menu di scelta rapida per la [gestione della navigazione con il menu Hot-Tracking abilitata](#handling-navigation-with-menu-hot-tracking-enabled).

Come descritto in [navigazione mista](#mixed-navigation), è anche necessario gestire la notifica [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) per tenere traccia del pulsante attivo. Questa notifica non è rilevante se l'utente si sposta solo con il mouse, ma è necessario quando lo spostamento del mouse e della tastiera è misto.

### <a name="keyboard-navigation"></a>Navigazione tramite tastiera

Come indicato nella sezione precedente, l'utente può eseguire una serie di operazioni di spostamento con la tastiera quando il menu di rilevamento a caldo è disabilitato. I controlli Toolbar supportano la navigazione tramite tastiera solo se hanno lo stato attivo. Non gestiscono inoltre tutte le pressioni dei tasti necessarie per le barre dei menu. La soluzione più semplice per gestire la navigazione da tastiera consiste nell'elaborare in modo esplicito gli eventi di pressione del tasto pertinenti.

Se il rilevamento a caldo del menu è disabilitato, l'applicazione deve gestire questi eventi di pressione del tasto nel modo seguente:

-   Tasto F10. Attivare il primo pulsante con [**TB \_ SETHOTITEM**](tb-sethotitem.md).
-   Tasti freccia sinistra e freccia destra. Attivare il pulsante adiacente con [**TB \_ SETHOTITEM**](tb-sethotitem.md). Se l'utente tenta di spostarsi in una delle estremità della barra dei menu, attivare il primo pulsante all'estremità opposta.
-   Tasto ESCAPE. Disattiva il pulsante attivo con [**TB \_ SETHOTITEM**](tb-sethotitem.md). La barra dei menu deve essere restituita allo stato precedente all'attivazione del primo pulsante.
-   Tasto di scelta rapida del *tasto* Alt. Usare il messaggio [**TB \_ MAPACCELERATOR**](tb-mapaccelerator.md) per determinare il pulsante a cui corrisponde il carattere *chiave* . Consente di visualizzare il menu a discesa del pulsante e di abilitare il menu di scelta rapida.
-   Tasto freccia GIÙ. Se un pulsante è attivo ma non è stato visualizzato alcun menu, visualizzare il menu del pulsante e abilitare il monitoraggio a caldo del menu.
-   Tasto INVIO. Disattiva il pulsante attivo con [**TB \_ SETHOTITEM**](tb-sethotitem.md). La barra dei menu deve essere restituita allo stato precedente all'attivazione del primo pulsante.

### <a name="mixed-navigation"></a>Navigazione mista

I gestori di navigazione da tastiera descritti nella sezione precedente eseguono essenzialmente due attività: tenere traccia del pulsante attivo e visualizzare il menu appropriato quando si seleziona un pulsante. Questi gestori sono sufficienti fino a quando l'utente si sposta solo con la tastiera. Tuttavia, gli utenti spesso combinano la navigazione da tastiera e mouse. Ad esempio, potrebbe attivare il primo pulsante con la chiave F10, utilizzare il mouse per attivare un pulsante diverso e quindi aprire il relativo menu con il tasto freccia giù. Se si esegue il monitoraggio solo delle pressioni dei tasti per tenere traccia del tasto attivo, verrà visualizzato il menu errato. È anche necessario gestire la notifica [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) per tenere traccia in modo accurato del pulsante attivo.

## <a name="handling-navigation-with-menu-hot-tracking-enabled"></a>Gestione della navigazione con il menu Hot-Tracking abilitato

Quando è abilitata la funzionalità di rilevamento a caldo del menu, l'applicazione deve modificare il modo in cui risponde alla navigazione dell'utente. Per replicare il comportamento dei menu standard, è necessario implementare in modo esplicito le funzionalità seguenti.

Con la navigazione del mouse:

-   Se l'utente sposta il cursore su un altro pulsante, il menu viene visualizzato immediatamente e il menu precedente scompare.
-   Il rilevamento a caldo del menu rimane attivo fino a quando l'utente non seleziona un comando o fa clic su un punto che non fa parte dell'area dei menu. L'azione disattiva il rilevamento a caldo del menu fino a quando non si fa clic su un altro pulsante.
-   Se il cursore si sposta dal menu, il menu a discesa corrente rimane fino a quando il cursore non viene spostato di nuovo o quando l'utente fa clic su un punto esterno all'area coperta dal menu. Se il cursore torna a un pulsante diverso da quello attualmente visualizzato, il menu precedente viene compresso e viene visualizzato il nuovo menu.

Con navigazione da tastiera:

-   Il tasto freccia destra sposta lo stato attivo a destra. Se l'elemento dispone di un sottomenu, visualizzare il sottomenu. Se l'elemento non dispone di un sottomenu, comprimere il menu e i sottomenu, attivare il pulsante avanti con [**TB \_ SETHOTITEM**](tb-sethotitem.md)e visualizzare il menu per il pulsante adiacente. Se l'ultimo pulsante è attivo quando viene ricevuto questo messaggio, visualizzare il menu per il primo pulsante.
-   Il tasto freccia sinistra sposta lo stato attivo a sinistra. Se l'elemento è un sottomenu, comprimerlo e spostare lo stato attivo sul menu padre. Se l'elemento non è un sottomenu, comprimere il menu, attivare il pulsante avanti con [**TB \_ SETHOTITEM**](tb-sethotitem.md)e visualizzare il menu per tale pulsante.

<!-- -->

-   Il tasto ESCAPE esegue il backup della visualizzazione di un passaggio.
    -   Se viene visualizzato un sottomenu, questo viene compresso e lo stato attivo passa al menu padre.
    -   Se il menu di un pulsante viene visualizzato, viene compresso e il menu di scelta rapida del menu è disabilitato. Il pulsante dell'elemento rimane attivo.
    -   Se non vengono visualizzati menu ma un pulsante è attivo, il pulsante viene disattivato e il menu di scelta rapida del menu è disabilitato.
-   I tasti freccia su e freccia giù vengono usati solo per spostarsi all'interno di un menu specifico.
-   Il tasto invio avvia il comando associato a una voce di menu. Se la voce di menu dispone di un sottomenu, il tasto invio lo Visualizza.

Come nel caso di disabilitato rilevamento a caldo del menu, l'applicazione deve essere in grado di gestire il mouse, la tastiera e la navigazione mista. Tuttavia, il fatto che venga visualizzato un menu significa che la messaggistica dovrà essere gestita in modo diverso.

### <a name="message-processing-for-menu-hot-tracking"></a>Elaborazione dei messaggi per il menu Hot-Tracking

Per il controllo attivo del menu è necessario che venga visualizzato un menu in qualsiasi momento, a parte il breve intervallo necessario per passare a un nuovo menu. Tuttavia, il menu a discesa visualizzato da [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) è modale. L'applicazione continuerà a ricevere direttamente alcuni messaggi, inclusi [**i \_ comandi WM**](/windows/desktop/menurc/wm-command), [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md)e i normali messaggi correlati ai menu, ad esempio [**WM \_ MENUSELECT**](/windows/desktop/menurc/wm-menuselect). Tuttavia, non riceverà direttamente i messaggi della tastiera o del mouse di basso livello. Per gestire i messaggi, ad esempio [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove), è necessario impostare un hook del messaggio per intercettare i messaggi indirizzati al menu.

Quando viene visualizzato un menu a discesa, impostare l'hook del messaggio chiamando la funzione [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa) con il parametro *IDHOOK* impostato su WH \_ msgfilter. Tutti i messaggi destinati al menu verranno passati alla [routine hook](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)). Il frammento di codice seguente, ad esempio, imposta un hook di messaggio che consente di intercettare i messaggi che passano a un menu a discesa. `MsgHook` è il nome della routine hook e `hhookMsg` è l'handle per la routine.


```
hhookMsg = SetWindowsHookEx(WH_MSGFILTER, MsgHook, HINST_THISDLL, 0);
```



I messaggi di menu vengono identificati impostando il parametro *nCode* della routine hook sul \_ menu MSGF. Il parametro *lParam* punterà a una struttura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) con il messaggio. I dettagli dei messaggi che devono essere gestiti e il modo in cui vengono descritti nella parte restante di questo argomento.

L'applicazione deve passare tutti i messaggi al hook del messaggio successivo chiamando la funzione [**CallNextHookEx**](/windows/desktop/api/winuser/nf-winuser-callnexthookex) . È inoltre necessario inviare i messaggi del mouse direttamente al controllo Toolbar, assicurandosi di convertire le coordinate dei punti nello spazio delle coordinate del client della barra degli strumenti. L'invio diretto dei messaggi garantisce che il controllo Toolbar riceva i messaggi del mouse appropriati. Ad esempio, la barra degli strumenti deve ricevere messaggi di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) per tenere traccia dei pulsanti.

Quando viene attivato un nuovo pulsante, l'applicazione deve comprimere il vecchio menu a discesa con un messaggio [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) e visualizzare un nuovo menu. Deve inoltre comprimere il menu a discesa quando lo stato attivo viene ricavato dalla barra dei menu con navigazione da tastiera oppure facendo clic all'esterno dell'area dei menu. Quando si comprime un menu, è necessario liberarne l'hook del messaggio usando la funzione [**UnhookWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-unhookwindowshookex) . Se è necessario visualizzare un altro menu a discesa, creare un nuovo hook del messaggio. Quando viene avviato un comando, il menu viene compresso automaticamente, ma è necessario liberare in modo esplicito l'hook del messaggio.

Nell'esempio di codice seguente viene liberato l'hook del messaggio impostato nell'esempio precedente.


```
UnhookWindowsHookEx(hhookMsg);
```



### <a name="mouse-navigation"></a>Navigazione del mouse

Quando una barra degli strumenti normale controlla i pulsanti sensibili, evidenzia il pulsante attivo e invia all'applicazione una notifica [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) ogni volta che viene attivato un nuovo pulsante. L'applicazione è responsabile della visualizzazione del menu a discesa appropriato. Deve:

-   Gestire la notifica [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) per tenere traccia del pulsante attivo. Quando si modifica il pulsante attivo, comprimere il vecchio menu e crearne uno nuovo.
-   Gestire la notifica a [ \_ discesa TBN](tbn-dropdown.md) inviata quando si fa clic su un pulsante. Dovrebbe quindi comprimere il menu e disabilitare il rilevamento a caldo del menu. Il pulsante rimane attivo.
-   Gestire i messaggi [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)e [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) nella routine hook del messaggio, per tenere traccia della posizione del mouse. Se si fa clic con il mouse all'esterno dell'area dei menu, comprimere il menu a discesa corrente, disattivare il monitoraggio a caldo del menu e tornare alla barra dei menu sullo stato di preattivazione.
-   Quando viene avviato un comando di menu, Disabilita il rilevamento a caldo del menu. Il menu verrà compresso automaticamente, ma è necessario liberare in modo esplicito l'hook del messaggio.

È inoltre necessario gestire la messaggistica relativa ai menu, ad esempio il messaggio [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) inviato quando una voce di menu deve visualizzare un sottomenu. Per informazioni su come gestire tali messaggi, vedere [menu](/windows/desktop/menurc/menus).

### <a name="keyboard-navigation"></a>Navigazione tramite tastiera

L'applicazione deve elaborare i messaggi della tastiera nella procedura di hook del messaggio e agire su quelli che influiscono sul rilevamento a caldo del menu. È necessario gestire le pressioni di tasto seguenti:

-   Tasto ESCAPE. Il tasto ESCAPE supporta la visualizzazione di un livello verso l'alto. Se un sottomenu viene visualizzato, deve essere compresso. Se viene visualizzato il menu primario di un pulsante, comprimerlo e disabilitare il rilevamento a caldo del menu. Il pulsante rimane attivo.
-   Tasto freccia DESTRA. Se l'elemento contiene un sottomenu, visualizzarlo. Se l'elemento non dispone di un sottomenu, comprimere il menu e i sottomenu, attivare il pulsante avanti con [**TB \_ SETHOTITEM**](tb-sethotitem.md)e visualizzare il relativo menu. Se l'ultimo pulsante era attivo al momento della ricezione della notifica, visualizzare il menu per il primo pulsante.
-   Tasto freccia SINISTRA. Se l'elemento si trova in un sottomenu, comprimerlo e spostare lo stato attivo sul menu padre. Se l'elemento non è un sottomenu, comprimere il menu, attivare il pulsante adiacente con [**TB \_ SETHOTITEM**](tb-sethotitem.md)e visualizzare il relativo menu. Se il primo pulsante era attivo al momento della ricezione della notifica, visualizzare il menu per l'ultimo pulsante.
-   Tasti freccia su e freccia giù. Queste chiavi vengono usate per spostarsi all'interno di un menu, ma non influiscono direttamente sul rilevamento a caldo del menu.
-   Tasto di scelta rapida del *tasto* Alt. Usare il messaggio [**TB \_ MAPACCELERATOR**](tb-mapaccelerator.md) per determinare il pulsante a cui corrisponde il carattere *chiave* . Se corrisponde a un pulsante diverso da quello attualmente attivo, comprimere il menu a discesa corrente, attivare il pulsante nuovo con [**TB \_ SETHOTITEM**](tb-sethotitem.md)e visualizzare il menu per il pulsante adiacente. Se il *carattere chiave* corrisponde al pulsante attualmente visualizzato, comprimere il menu a discesa e disabilitare il rilevamento a caldo del menu. Il pulsante deve rimanere attivo.

 

 