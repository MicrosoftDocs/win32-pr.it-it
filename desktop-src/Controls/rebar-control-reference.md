---
title: Rebar
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli Rebar.
ms.assetid: vs|controls|~\controls\rebar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ac71ea71b5e0b0bd1e222d46c070a62512f0f5ff3b885fe13b19fad10f7bf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434841"
---
# <a name="rebar"></a>Rebar

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli Rebar.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                            | Contenuto                                                                               |
|--------------------------------------------------|----------------------------------------------------------------------------------------|
| [Controlli Rebar](rebar-controls.md)             | *I controlli Rebar* fungono da contenitori per le finestre figlio.<br/>                       |
| [Uso dei controlli Rebar](using-rebar-controls.md) | Questa sezione contiene codice di esempio che illustra come implementare i controlli Rebar.<br/> |



 

### <a name="messages"></a>Messaggi



| Argomento                                               | Contenuto                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RB \_ BEGINDRAG**](rb-begindrag.md)               | Attiva la modalità di trascinamento della selezione per il controllo Rebar. Questo messaggio non determina l'invio di una notifica [RBN \_ BEGINDRAG.](rbn-begindrag.md) <br/>                                                 |
| [**RB \_ DELETEBAND**](rb-deleteband.md)             | Elimina una banda da un controllo Rebar. <br/>                                                                                                                                                     |
| [**RB \_ DRAGMOVE**](rb-dragmove.md)                 | Aggiorna la posizione di trascinamento nel controllo Rebar dopo un messaggio [**RB \_ BEGINDRAG**](rb-begindrag.md) precedente. <br/>                                                                           |
| [**RB \_ ENDDRAG**](rb-enddrag.md)                   | Termina l'operazione di trascinamento della selezione del controllo Rebar. Questo messaggio non determina l'invio di una notifica [ \_ RBN ENDDRAG.](rbn-enddrag.md) <br/>                                          |
| [**RB \_ GETBANDBORDERS**](rb-getbandborders.md)     | Recupera i bordi di una banda. Il risultato di questo messaggio può essere utilizzato per calcolare l'area utilizzabile in una banda. <br/>                                                                          |
| [**RB \_ GETBANDCOUNT**](rb-getbandcount.md)         | Recupera il conteggio delle bande attualmente presenti nel controllo Rebar. <br/>                                                                                                                             |
| [**RB \_ GETBANDINFO**](rb-getbandinfo.md)           | Recupera informazioni su una banda specificata in un controllo Rebar. <br/>                                                                                                                         |
| [**RB \_ GETBANDMARGINS**](rb-getbandmargins.md)     | Recupera i margini di una banda.<br/>                                                                                                                                                          |
| [**RB \_ GETBARHEIGHT**](rb-getbarheight.md)         | Recupera l'altezza del controllo Rebar. <br/>                                                                                                                                               |
| [**RB \_ GETBARINFO**](rb-getbarinfo.md)             | Recupera informazioni sul controllo Rebar e sull'elenco di immagini che usa. <br/>                                                                                                                |
| [**RB \_ GETBKCOLOR**](rb-getbkcolor.md)             | Recupera il colore di sfondo predefinito di un controllo Rebar. <br/>                                                                                                                                    |
| [**RB \_ GETCOLORSCHEME**](rb-getcolorscheme.md)     | Recupera le informazioni sulla combinazione di colori dal controllo Rebar. <br/>                                                                                                                           |
| [**RB \_ GETDROPTARGET**](rb-getdroptarget.md)       | Recupera il puntatore all'interfaccia [**IDropTarget di**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) un controllo Rebar. <br/>                                                                                                        |
| [**RB \_ GETEXTENDEDSTYLE**](rb-getextendedstyle.md) | Ottiene lo stile esteso. <br/>                                                                                                                                                                 |
| [**RB \_ GETPALETTE**](rb-getpalette.md)             | Recupera la tavolozza corrente del controllo Rebar. <br/>                                                                                                                                           |
| [**RB \_ GETRECT**](rb-getrect.md)                   | Recupera il rettangolo di delimitazione per una determinata banda in un controllo Rebar. <br/>                                                                                                                    |
| [**RB \_ GETROWCOUNT**](rb-getrowcount.md)           | Recupera il numero di righe di bande in un controllo Rebar. <br/>                                                                                                                                |
| [**RB \_ GETROWHEIGHT**](rb-getrowheight.md)         | Recupera l'altezza di una riga specificata in un controllo Rebar. <br/>                                                                                                                              |
| [**RB \_ GETTEXTCOLOR**](rb-gettextcolor.md)         | Recupera il colore del testo predefinito di un controllo Rebar. <br/>                                                                                                                                          |
| [**RB \_ GETTOOLTIPS**](rb-gettooltips.md)           | Recupera l'handle per qualsiasi controllo descrizione comando associato al controllo Rebar. <br/>                                                                                                           |
| [**RB \_ GETUNICODEFORMAT**](rb-getunicodeformat.md) | Recupera il flag di formato carattere Unicode per il controllo . <br/>                                                                                                                             |
| [**RB \_ HITTEST**](rb-hittest.md)                   | Determina quale parte di una banda rebar si trova in un determinato punto dello schermo, se esiste una banda rebar in quel punto. <br/>                                                                        |
| [**RB \_ IDTOINDEX**](rb-idtoindex.md)               | Converte un identificatore di banda in un indice di banda in un controllo Rebar. <br/>                                                                                                                           |
| [**RB \_ INSERTBAND**](rb-insertband.md)             | Inserisce una nuova banda in un controllo Rebar. <br/>                                                                                                                                                   |
| [**RB \_ MAXIMIZEBAND**](rb-maximizeband.md)         | Ridimensiona una banda in un controllo Rebar in base alle dimensioni ideali o massime. <br/>                                                                                                                   |
| [**RB \_ MINIMIZEBAND**](rb-minimizeband.md)         | Ridimensiona una banda in un controllo Rebar alle dimensioni più piccole. <br/>                                                                                                                                  |
| [**RB \_ MOVEBAND**](rb-moveband.md)                 | Sposta una banda da un indice a un altro. <br/>                                                                                                                                                  |
| [**RB \_ PUSHCHEVRON**](rb-pushchevron.md)           | Inviato a un controllo Rebar per eseguire il push a livello di codice di una chevron.<br/>                                                                                                                               |
| [**RB \_ SETBANDINFO**](rb-setbandinfo.md)           | Imposta le caratteristiche di una banda esistente in un controllo Rebar. <br/>                                                                                                                             |
| [**RB \_ SETBANDWIDTH**](rb-setbandwidth.md)         | Imposta la larghezza per una banda ancorata.<br/>                                                                                                                                                         |
| [**RB \_ SETBARINFO**](rb-setbarinfo.md)             | Imposta le caratteristiche di un controllo Rebar. <br/>                                                                                                                                             |
| [**RB \_ SETBKCOLOR**](rb-setbkcolor.md)             | Imposta il colore di sfondo predefinito di un controllo Rebar. <br/>                                                                                                                                         |
| [**RB \_ SETCOLORSCHEME**](rb-setcolorscheme.md)     | Imposta le informazioni sulla combinazione colori per il controllo Rebar. <br/>                                                                                                                                 |
| [**RB \_ SETEXTENDEDSTYLE**](rb-setextendedstyle.md) | Imposta lo stile esteso. Questo messaggio non è implementato.<br/>                                                                                                                                 |
| [**RB \_ SETPALETTE**](rb-setpalette.md)             | Imposta la tavolozza corrente del controllo Rebar. <br/>                                                                                                                                                |
| [**RB \_ SETPARENT**](rb-setparent.md)               | Imposta la finestra padre di un controllo Rebar. <br/>                                                                                                                                                    |
| [**RB \_ SETTEXTCOLOR**](rb-settextcolor.md)         | Imposta il colore del testo predefinito di un controllo Rebar. <br/>                                                                                                                                               |
| [**RB \_ SETTOOLTIPS**](rb-settooltips.md)           | Associa un controllo descrizione comando al controllo Rebar. <br/>                                                                                                                                     |
| [**RB \_ SETUNICODEFORMAT**](rb-setunicodeformat.md) | Imposta il flag di formato carattere Unicode per il controllo . Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo. <br/> |
| [**RB \_ SETWINDOWTHEME**](rb-setwindowtheme.md)     | Imposta lo stile di visualizzazione di un controllo Rebar.<br/>                                                                                                                                                 |
| [**RB \_ SHOWBAND**](rb-showband.md)                 | Mostra o nasconde una determinata banda in un controllo Rebar. <br/>                                                                                                                                          |
| [**RB \_ SIZETORECT**](rb-sizetorect.md)             | Tenta di trovare il layout migliore delle bande per il rettangolo specificato. <br/>                                                                                                                   |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                        | Contenuto                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (rebar)](nm-customdraw-rebar.md)            | Inviato dal controllo Rebar per notificare alla finestra padre le operazioni di disegno. Questa notifica viene inviata sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                                               |
| [NM \_ NCHITTEST (rebar)](nm-nchittest-rebar.md)              | Inviato da un controllo Rebar quando il controllo riceve un [**messaggio \_ WM NCHITTEST.**](/windows/desktop/inputdev/wm-nchittest) Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                 |
| [NM \_ RELEASEDCAPTURE (rebar)](nm-releasedcapture-rebar-.md) | Notifica alla finestra padre di un controllo Rebar che il controllo sta rilasciando mouse capture. Questa notifica viene inviata sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                        |
| [RBN \_ AUTOBREAK](rbn-autobreak.md)                          | Notifica [all'elemento padre di un controllo Rebar](rebar-controls.md) che verrà visualizzata un'interruzione nella barra. L'elemento padre determina se eseguire l'interruzione. <br/>                                                                                                                            |
| [RBN \_ AUTOSIZE](rbn-autosize.md)                            | Inviato da un controllo Rebar creato con lo [**stile \_ AUTOSIZE di RBS**](rebar-control-styles.md) quando l'elemento Rebar viene ridimensionato automaticamente. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                  |
| [RBN \_ BEGINDRAG](rbn-begindrag.md)                          | Inviato da un controllo Rebar quando l'utente inizia a trascinare una banda. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                           |
| [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md)                  | Inviato da un controllo Rebar quando viene premuto un elemento chevron. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                                                                        |
| [RBN \_ CHILDSIZE](rbn-childsize.md)                          | Inviato da un controllo Rebar quando viene ridimensionata la finestra figlio di una banda. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                          |
| [RBN \_ DELETEDBAND](rbn-deletedband.md)                      | Inviato da un controllo Rebar dopo l'eliminazione di una banda. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                  |
| [RBN \_ DELETINGBAND](rbn-deletingband.md)                    | Inviato da un controllo Rebar quando una banda sta per essere eliminata. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                             |
| [RBN \_ ENDDRAG](rbn-enddrag.md)                              | Inviato da un controllo Rebar quando l'utente smette di trascinare una banda. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                            |
| [RBN \_ GETOBJECT](rbn-getobject.md)                          | Inviato da un controllo Rebar creato con lo [**stile \_ RBS REGISTERDROP**](rebar-control-styles.md) quando un oggetto viene trascinato su una banda nel controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/> |
| [RBN \_ HEIGHTCHANGE](rbn-heightchange.md)                    | Inviato da un controllo Rebar quando viene modificata l'altezza. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                    |
| [LAYOUT RBN \_ MODIFICATO](rbn-layoutchanged.md)                  | Inviato da un controllo Rebar quando l'utente modifica il layout delle bande del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                        |
| [RBN \_ MINMAX](rbn-minmax.md)                                | Inviato da un controllo Rebar prima di ingrandire o ridurre al minimo una banda. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                       |
| [RBN \_ SPLITTERDRAG](rbn-splitterdrag.md)                    | Inviato da un controllo Rebar quando l'utente trascina una barra di divisione. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                 |



 

### <a name="structures"></a>Strutture



| Argomento                                        | Contenuto                                                                                                                                      |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize)         | Contiene informazioni utilizzate nella gestione dei codici di notifica [RBN \_ AUTOSIZE.](rbn-autosize.md) <br/>                                   |
| [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar)                   | Contiene informazioni utilizzate nella gestione di vari codici di notifica rebar. <br/>                                                           |
| [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) | Contiene informazioni usate con la [notifica RBN \_ AUTOBREAK.](rbn-autobreak.md)<br/>                                               |
| [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron)     | Contiene informazioni usate nella gestione del codice di notifica [ \_ RBN CHEVRONPUSHED.](rbn-chevronpushed.md) <br/>                          |
| [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) | Contiene informazioni utilizzate nella gestione del codice di notifica [ \_ CHILDSIZE RBN.](rbn-childsize.md) <br/>                                  |
| [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter)   | Contiene informazioni utilizzate per gestire un codice di notifica [RBN \_ SPLITTERDRAG.](rbn-splitterdrag.md)<br/>                                |
| [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo)       | Contiene informazioni specifiche di un'operazione di hit test. Questa struttura viene usata con il [**messaggio RB \_ HITTEST.**](rb-hittest.md) <br/> |
| [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)       | Contiene informazioni che definiscono una banda in un controllo Rebar. <br/>                                                                      |
| [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo)               | Contiene informazioni che descrivono le caratteristiche del controllo Rebar. <br/>                                                                |



 

### <a name="constants"></a>Costanti



| Argomento                                            | Contenuto                                                                                              |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Stili del controllo Rebar](rebar-control-styles.md) | I controlli Rebar supportano un'ampia gamma di stili di controllo oltre agli stili di finestra standard. <br/> |



 

 

