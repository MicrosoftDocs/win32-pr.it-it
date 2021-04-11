---
title: Come creare una barra degli strumenti Explorer-Style Internet
description: Una delle principali funzionalità dell'interfaccia utente di Windows Internet Explorer è la barra degli strumenti. Non solo fornisce agli utenti l'accesso a un'ampia gamma di funzionalità, ma consente agli utenti di personalizzare il layout in base alle preferenze personali.
ms.assetid: d24969ec-4dea-44c6-b045-5611de8f1cce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32228f941a7c7e1253884ab5d72368f66f25c7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118538"
---
# <a name="how-to-create-an-internet-explorer-style-toolbar"></a>Come creare una barra degli strumenti Explorer-Style Internet

Una delle principali funzionalità dell'interfaccia utente di Windows Internet Explorer è la barra degli strumenti. Non solo fornisce agli utenti l'accesso a un'ampia gamma di funzionalità, ma consente agli utenti di personalizzare il layout in base alle preferenze personali.

Lo screenshot seguente mostra la barra degli strumenti di Internet Explorer ed evidenzia alcune delle funzionalità principali.

![screenshot della barra degli strumenti di Windows Internet Explorer, con etichette per otto funzionalità](images/howto1a.jpg)

Questa barra degli strumenti è costituita essenzialmente da un controllo Rebar con quattro bande: tre barre degli strumenti e una barra dei menu. Poiché viene implementato con l'API dei controlli comuni, gli sviluppatori possono creare barre degli strumenti con una o tutte le funzionalità. In questo argomento vengono illustrate le funzionalità essenziali della barra degli strumenti di Internet Explorer e viene illustrato come implementarle nell'applicazione.

-   [Controllo Rebar](#the-rebar-control)
    -   [Implementazione del controllo Rebar](#implementing-the-rebar-control)
-   [Barre degli strumenti](#how-to-create-an-internet-explorer-style-toolbar)
    -   [Pulsanti a discesa](#drop-down-buttons)
    -   [Pulsanti di tipo elenco](#list-style-buttons)
    -   [Virgolette acute](#handling-chevrons)
    -   [Rilevamento a caldo](#hot-tracking)
-   [Argomenti correlati](#related-topics)

## <a name="the-rebar-control"></a>Controllo Rebar

La struttura sottostante della barra degli strumenti di Internet Explorer viene fornita da un [controllo Rebar](rebar-controls.md). Questo controllo consente agli utenti di personalizzare la disposizione di una raccolta di strumenti. Ogni controllo Rebar contiene una o più *bande*, che in genere sono rettangoli stretti o lunghi che contengono una finestra figlio, in genere un controllo barra degli strumenti.

Il controllo Rebar Visualizza le bande in un'area rettangolare, in genere nella parte superiore della finestra. Questo rettangolo è suddiviso in una o più strisce che corrispondono all'altezza di una banda. Ogni banda può trovarsi su uno strip separato oppure più bande possono essere posizionate nella stessa striscia.

Un controllo Rebar fornisce agli utenti due modi per disporre gli strumenti:

-   Ogni banda ha in genere una *pinza* sul bordo sinistro. I pinze vengono usati quando due o più bande in una singola striscia superano la larghezza della finestra. Trascinando il pulsante a sinistra o a destra, gli utenti possono controllare la quantità di spazio allocata a ogni banda.
-   Gli utenti possono spostare le bande all'interno del rettangolo di visualizzazione del rebar trascinando e rilasciando. Il controllo Rebar modifica quindi la visualizzazione in modo da adattarsi alla nuova disposizione delle bande. Se tutte le bande vengono rimosse da una striscia, l'altezza del controllo Rebar verrà ridotta, ampliando l'area di visualizzazione.

Un'applicazione può aggiungere o rimuovere bande in base alle esigenze. In genere, le applicazioni consentono agli utenti di selezionare le bande che desiderano visualizzare tramite il menu Visualizza o un menu di scelta rapida.

Se la larghezza combinata delle bande in una striscia supera la larghezza della finestra, il controllo Rebar modificherà le larghezze in base alle esigenze. Alcuni degli strumenti potrebbero essere coperti dalla banda adiacente.

La [versione 5,80](common-control-versions.md) dei controlli comuni fornisce un modo per rendere gli strumenti che sono stati coperti da un'altra banda accessibile all'utente. Se si imposta il \_ flag RBBS USECHEVRON nel membro **fStyle** della struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) della banda, viene visualizzata una freccia di *espansione* per le barre degli strumenti che sono state analizzate. Quando un utente fa clic sulla freccia di espansione, viene visualizzato un menu che consente di usare gli strumenti nascosti. La schermata seguente di Microsoft Internet Explorer 6 Mostra il menu visualizzato quando viene analizzata una parte della barra degli strumenti standard.

![screenshot che mostra il menu visualizzato facendo clic sulla freccia di espansione](images/howto2.jpg)

Poiché ogni banda contiene un controllo, è possibile fornire flessibilità aggiuntiva tramite l'API del controllo. Ad esempio, è possibile implementare la personalizzazione della barra degli strumenti per consentire all'utente di aggiungere, spostare o eliminare pulsanti su una barra degli strumenti.

### <a name="implementing-the-rebar-control"></a>Implementazione del controllo Rebar

La maggior parte delle funzionalità della barra degli strumenti di Internet Explorer è effettivamente implementata nelle singole bande. L'implementazione del controllo Rebar è semplice ed è riportata di seguito.

1.  Creare il controllo Rebar con [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Impostare *dwExStyle* su [**WS \_ ex \_ TOOLWINDOW**](/windows/desktop/winmsg/extended-window-styles) e *lpClassName* su [**REBARCLASSNAME**](common-control-window-classes.md). Internet Explorer utilizza gli stili della finestra seguenti:

    -   [**\_BANDBORDERS RBS**](rebar-control-styles.md)
    -   [**\_DBLCLKTOGGLE RBS**](rebar-control-styles.md)
    -   [**\_REGISTERDROP RBS**](rebar-control-styles.md)
    -   [**\_VARHEIGHT RBS**](rebar-control-styles.md)
    -   [**\_NOdivider CCS**](common-control-styles.md)
    -   [**\_NOPARENTALIGN CCS**](common-control-styles.md)
    -   [**\_bordo WS**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ figlio**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ CLIPCHILDREN**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ CLIPSIBLINGS**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ visibile**](/windows/desktop/winmsg/window-styles)

    Impostare gli altri parametri appropriati per l'applicazione.

2.  Creare un controllo con [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o una funzione di creazione di controlli specializzata, ad esempio [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex).
3.  Inizializzare una banda per il controllo compilando i membri di [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa). Includere lo \_ stile RBBS USECHEVRON con il membro **fStyle** per abilitare le frecce.
4.  Aggiungere la banda al controllo Rebar con un messaggio [**RB \_ INSERTBAND**](rb-insertband.md) .
5.  Ripetere i passaggi 2-4 per le bande rimanenti.
6.  Implementare i gestori per le notifiche Rebar. In particolare, sarà necessario gestire [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) per visualizzare un menu a discesa quando si fa clic su una freccia di espansione. Per ulteriori informazioni, vedere [gestione delle frecce](#handling-chevrons).

I pinze sono inclusi per impostazione predefinita. Per omettere la pinza per una banda, impostare il \_ flag RBBS nopinze nel membro **fStyle** della struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) della banda. Per ulteriori informazioni sull'implementazione di controlli Rebar, vedere [informazioni sui controlli Rebar](rebar-controls.md).

### <a name="handling-chevrons"></a>Gestione delle frecce

Quando un utente fa clic su una freccia di espansione, il controllo Rebar invia all'applicazione una notifica di [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) . La struttura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) passata con la notifica contiene l'identificatore della banda e una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) con il rettangolo occupato dalla freccia di espansione. Il gestore deve determinare quali pulsanti sono nascosti e visualizzare i comandi associati in un menu a comparsa.

La procedura seguente illustra come gestire una notifica [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) :

1.  Recuperare il rettangolo di delimitazione corrente per la banda selezionata inviando al controllo Rebar un messaggio [**RB \_ GetRect**](rb-getrect.md) .
2.  Recuperare il numero totale di pulsanti inviando il controllo barra degli strumenti della banda a [**TB \_ BUTTONCOUNT**](tb-buttoncount.md) messaggio.
3.  A partire dal pulsante più a sinistra, recuperare il rettangolo di delimitazione del pulsante inviando la barra degli strumenti per il controllo di un messaggio [**\_ GETITEMRECT TB**](tb-getitemrect.md) .
4.  Passare i rettangoli della banda e del pulsante alla funzione [**IntersectRect**](/windows/desktop/api/winuser/nf-winuser-intersectrect) . Questa funzione restituirà una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che corrisponde alla parte visibile del pulsante.
5.  Passare il rettangolo del pulsante e il rettangolo per la parte visibile del pulsante alla funzione [**EqualRect**](/windows/desktop/api/winuser/nf-winuser-equalrect) .
6.  Se [**EqualRect**](/windows/desktop/api/winuser/nf-winuser-equalrect) restituisce **true**, l'intero pulsante è visibile. Ripetere i passaggi 3-5 per il pulsante avanti sulla barra degli strumenti. Se **EqualRect** restituisce **false**, il pulsante è almeno parzialmente nascosto e tutti i pulsanti rimanenti saranno completamente nascosti. Continuare con il passaggio successivo.
7.  Creare un menu a comparsa con gli elementi per ognuno dei pulsanti nascosti.
8.  Consente di visualizzare il menu di scelta rapida tramite la funzione [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) . Usare il rettangolo della freccia di espansione passato con la notifica [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) per posizionare il menu. Il menu deve trovarsi immediatamente sotto la freccia di espansione, con i bordi sinistro allineati.
9.  Gestire i comandi di menu.

## <a name="the-toolbars"></a>Barre degli strumenti

La maggior parte della complessità della barra degli strumenti di Internet Explorer risiede nell'implementazione di controlli che compongono le bande Rebar. Internet Explorer visualizza generalmente quattro bande:

-   Barra dei menu
-   Barra degli strumenti standard
-   Barra degli strumenti dei collegamenti
-   Barra degli strumenti dell'indirizzo

Tutte queste bande, inclusa la barra dei menu, contengono effettivamente i controlli della barra degli strumenti. In questa sezione viene illustrata l'implementazione delle barre degli strumenti standard e collegamenti. La barra dei menu è leggermente più complessa e viene discussa separatamente in [come creare una barra dei menu Explorer-Style Internet](cc-faq-iemenubar.md).

Le procedure di base per l'implementazione dei controlli della barra degli strumenti sono descritte in [informazioni sui controlli Toolbar](toolbar-controls-overview.md). Questa sezione è incentrata su alcune delle funzionalità più recenti della barra degli strumenti utilizzate da Internet Explorer per aumentare l'usabilità del controllo.

-   [Pulsanti a discesa](#drop-down-buttons)
-   [Pulsanti di tipo elenco](#list-style-buttons)
-   [Virgolette acute](#handling-chevrons)
-   [Rilevamento a caldo](#hot-tracking)

### <a name="drop-down-buttons"></a>Pulsanti a discesa

I pulsanti a discesa supportano più comandi. Quando l'utente fa clic su un pulsante a discesa, il pulsante Visualizza un menu a comparsa anziché avviare un comando. L'utente avvia un comando selezionandola dal menu. Lo screenshot seguente mostra un pulsante a discesa e un menu sulla barra degli strumenti standard di Internet Explorer.

![screenshot che mostra il menu a discesa posta](images/howto3.jpg)

La funzionalità a discesa può essere aggiunta a qualsiasi stile di pulsante aggiungendo un flag di stile al membro **fStyle** della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) del pulsante. Sono disponibili tre stili di pulsante a discesa, tutti usati da Internet Explorer:

-   I pulsanti a discesa semplici hanno lo stile a [**\_ discesa BTNS**](toolbar-control-and-button-styles.md) . Sembrano pulsanti normali, ma visualizzano un menu quando si fa clic anziché avviare un comando.
-   I pulsanti freccia a discesa semplici hanno lo [**stile \_ WHOLEDROPDOWN BTNS**](toolbar-control-and-button-styles.md) . Hanno una freccia visualizzata accanto all'immagine del pulsante o al testo. Oltre alla differenza nell'aspetto, sono identici ai pulsanti a discesa semplici. Il pulsante posta utilizzato come esempio nell'illustrazione precedente è un pulsante a discesa.
-   I pulsanti freccia a discesa che aggiungono lo stile esteso [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) all' [**elenco a \_ discesa BTNS**](toolbar-control-and-button-styles.md) hanno una freccia separata dal testo o dall'immagine. Questo stile di pulsante combina le funzionalità dell'elenco a discesa e i pulsanti standard. Se l'utente fa clic sulla freccia, viene visualizzato un menu e l'utente può scegliere tra diversi comandi. Se l'utente fa clic sul pulsante adiacente, viene avviato un comando predefinito. Lo screenshot seguente mostra il pulsante **indietro** di Internet Explorer, che usa una freccia separata.

    ![screenshot che mostra il menu del pulsante di suddivisione indietro](images/howto4.jpg)

Quando l'utente fa clic su un pulsante a discesa con lo stile della freccia semplice o semplice, il controllo Toolbar invia all'applicazione una notifica a [ \_ discesa TBN](tbn-dropdown.md) . Quando l'applicazione riceve questo messaggio, è responsabile della creazione e della visualizzazione del menu e della gestione del comando selezionato.

Quando l'utente fa clic su una freccia separata, il controllo Toolbar invia all'applicazione una notifica a [ \_ discesa TBN](tbn-dropdown.md) . L'applicazione deve gestirla nello stesso modo in cui gestisce gli altri due tipi di pulsanti a discesa. Se l'utente fa clic sul pulsante principale, l'applicazione riceve un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) con l'ID comando del pulsante, come se si trattasse di un pulsante standard. Le applicazioni in genere rispondono avviando il comando superiore nel menu a discesa, ma è possibile rispondere in modo appropriato.

### <a name="list-style-buttons"></a>Pulsanti List-Style

Se si aggiunge un testo, i pulsanti standard vengono visualizzati sotto la bitmap. La schermata seguente mostra i pulsanti **Cerca** e **Preferiti** di Internet Explorer con testo del pulsante standard.

![screenshot che mostra la barra degli strumenti ricerca e preferiti con i pulsanti standard](images/howto6.jpg)

Microsoft Internet Explorer 5 e versioni successive utilizzano lo stile di [**\_ elenco TBSTYLE**](toolbar-control-and-button-styles.md) . Il testo è a destra della bitmap, riducendo l'altezza del pulsante e ampliando l'area di visualizzazione. Nella figura seguente sono illustrati i pulsanti **Cerca** e **Preferiti** di Internet Explorer 6 con lo stile di **\_ elenco TBSTYLE** .

![screenshot che mostra la barra degli strumenti ricerca e preferiti con i pulsanti di tipo elenco](images/howto5.jpg)

### <a name="chevrons"></a>Virgolette acute

Quando l'utente riorganizza le bande nel controllo Rebar, è possibile che venga analizzata una parte di una barra degli strumenti. Se la banda è stata creata con lo \_ stile RBBS USECHEVRON, il controllo Rebar visualizzerà una freccia di espansione sul bordo destro della barra degli strumenti. L'utente fa clic sulla freccia di espansione per visualizzare un menu con gli strumenti nascosti.

### <a name="hot-tracking"></a>Hot-Tracking

Quando è abilitata la funzionalità di rilevamento a caldo, un pulsante diventa *attivo* quando il cursore è posizionato su di esso. Il pulsante attivo è generalmente distinto dagli altri pulsanti della barra degli strumenti da un'immagine distinta. Per impostazione predefinita, viene generato un pulsante attivo sopra il resto della barra degli strumenti. Quando un nuovo pulsante diventa attivo, l'applicazione riceve una notifica [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md) . Nella figura seguente sono illustrati i pulsanti **Cerca** e **Preferiti** di Internet Explorer 5 con un pulsante **ricerca** a caldo. Oltre a avere un aspetto elevato, la bitmap grigia del pulsante è stata sostituita da una mappa colorata.

![cattura di schermata che mostra i pulsanti Cerca e preferiti con un pulsante ricerca a caldo](images/howto7.jpg)

Per abilitare il rilevamento a caldo, creare un controllo Toolbar con lo stile [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) o [**TBSTYLE \_ List**](toolbar-control-and-button-styles.md) . Queste sono denominate barre degli strumenti *Flat* perché i singoli pulsanti non vengono in genere evidenziati in alcun modo. Le bitmap vengono semplicemente visualizzate una accanto all'altra. Hanno un aspetto simile a un pulsante solo quando sono a caldo. Questi due stili sono anche trasparenti, il che significa che lo sfondo delle icone sarà il colore della finestra client sottostante.

Per visualizzare una bitmap diversa quando il pulsante è attivo, creare un secondo [elenco](image-lists.md) di immagini che contiene le immagini sensibili per tutti i pulsanti sulla barra degli strumenti. Le dimensioni e l'ordine di queste immagini devono corrispondere a quelle dell'elenco di immagini predefinite. Inviare la barra degli strumenti per controllare un messaggio [**TB \_ SETHOTIMAGELIST**](tb-sethotimagelist.md) per impostare l'elenco di immagini a caldo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come creare una barra dei menu Explorer-Style Internet](cc-faq-iemenubar.md)
</dt> </dl>

 

 