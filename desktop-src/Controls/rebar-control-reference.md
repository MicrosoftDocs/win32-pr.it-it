---
title: Rebar
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli Rebar.
ms.assetid: vs|controls|~\controls\rebar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef14343d33fb5ae45a2d93df74a9b915aca6d7b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474454"
---
# <a name="rebar"></a>Rebar

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli Rebar.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                            | Contenuto                                                                               |
|--------------------------------------------------|----------------------------------------------------------------------------------------|
| [Controlli Rebar](rebar-controls.md)             | I *controlli Rebar* fungono da contenitori per le finestre figlio.<br/>                       |
| [Uso di controlli Rebar](using-rebar-controls.md) | Questa sezione contiene il codice di esempio che illustra come implementare i controlli Rebar.<br/> |



 

### <a name="messages"></a>Messaggi



| Argomento                                               | Contenuto                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RB \_ BEGINDRAG**](rb-begindrag.md)               | Inserisce il controllo Rebar in modalità di trascinamento della selezione. Questo messaggio non comporta l'invio di una notifica [RBN \_ BEGINDRAG](rbn-begindrag.md) . <br/>                                                 |
| [**RB \_ DELETEBAND**](rb-deleteband.md)             | Elimina una banda da un controllo Rebar. <br/>                                                                                                                                                     |
| [**RB \_ DRAGMOVE**](rb-dragmove.md)                 | Aggiorna la posizione del trascinamento nel controllo Rebar dopo un messaggio [**RB \_ BEGINDRAG**](rb-begindrag.md) precedente. <br/>                                                                           |
| [**RB \_ ENDDRAG**](rb-enddrag.md)                   | Termina l'operazione di trascinamento e rilascio del controllo Rebar. Questo messaggio non comporta l'invio di una notifica [RBN \_ ENDDRAG](rbn-enddrag.md) . <br/>                                          |
| [**RB \_ GETBANDBORDERS**](rb-getbandborders.md)     | Recupera i bordi di una banda. Il risultato di questo messaggio può essere utilizzato per calcolare l'area utilizzabile di una banda. <br/>                                                                          |
| [**RB \_ GETBANDCOUNT**](rb-getbandcount.md)         | Recupera il conteggio delle bande attualmente presenti nel controllo Rebar. <br/>                                                                                                                             |
| [**RB \_ GETBANDINFO**](rb-getbandinfo.md)           | Recupera le informazioni su una banda specificata in un controllo Rebar. <br/>                                                                                                                         |
| [**RB \_ GETBANDMARGINS**](rb-getbandmargins.md)     | Recupera i margini di una banda.<br/>                                                                                                                                                          |
| [**RB \_ GETBARHEIGHT**](rb-getbarheight.md)         | Recupera l'altezza del controllo Rebar. <br/>                                                                                                                                               |
| [**RB \_ GETBARINFO**](rb-getbarinfo.md)             | Recupera le informazioni sul controllo Rebar e sull'elenco di immagini utilizzate. <br/>                                                                                                                |
| [**RB \_ GETBKCOLOR**](rb-getbkcolor.md)             | Recupera il colore di sfondo predefinito di un controllo Rebar. <br/>                                                                                                                                    |
| [**RB \_ GETCOLORSCHEME**](rb-getcolorscheme.md)     | Recupera le informazioni sulla combinazione di colori dal controllo Rebar. <br/>                                                                                                                           |
| [**RB \_ GETDROPTARGET**](rb-getdroptarget.md)       | Recupera un puntatore all'interfaccia [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) del controllo Rebar. <br/>                                                                                                        |
| [**RB \_ GETEXTENDEDSTYLE**](rb-getextendedstyle.md) | Ottiene lo stile esteso. <br/>                                                                                                                                                                 |
| [**\_tavolozza RB**](rb-getpalette.md)             | Recupera la tavolozza corrente del controllo Rebar. <br/>                                                                                                                                           |
| [**RB \_ GETrect**](rb-getrect.md)                   | Recupera il rettangolo di delimitazione per una determinata banda in un controllo Rebar. <br/>                                                                                                                    |
| [**RB \_ GETrowcount**](rb-getrowcount.md)           | Recupera il numero di righe di bande in un controllo Rebar. <br/>                                                                                                                                |
| [**RB \_ GETROWHEIGHT**](rb-getrowheight.md)         | Recupera l'altezza di una riga specificata in un controllo Rebar. <br/>                                                                                                                              |
| [**RB \_ GETTEXTCOLOR**](rb-gettextcolor.md)         | Recupera il colore del testo predefinito di un controllo Rebar. <br/>                                                                                                                                          |
| [**RB \_ GETtooltips**](rb-gettooltips.md)           | Recupera l'handle per qualsiasi controllo ToolTip associato al controllo Rebar. <br/>                                                                                                           |
| [**RB \_ GETUNICODEFORMAT**](rb-getunicodeformat.md) | Recupera il flag del formato carattere Unicode per il controllo. <br/>                                                                                                                             |
| [**stato RB \_ HITTEST**](rb-hittest.md)                   | Determina quale parte di una banda Rebar si trova in un determinato punto sullo schermo, se in quel punto esiste una banda del controllo Rebar. <br/>                                                                        |
| [**RB \_ IDTOINDEX**](rb-idtoindex.md)               | Converte un identificatore di banda in un indice di banda in un controllo Rebar. <br/>                                                                                                                           |
| [**RB \_ INSERTBAND**](rb-insertband.md)             | Inserisce una nuova banda in un controllo Rebar. <br/>                                                                                                                                                   |
| [**RB \_ MAXIMIZEBAND**](rb-maximizeband.md)         | Ridimensiona una banda in un controllo Rebar alla dimensione ideale o più grande. <br/>                                                                                                                   |
| [**RB \_ MINIMIZEBAND**](rb-minimizeband.md)         | Ridimensiona una banda in un controllo Rebar alla dimensione minima. <br/>                                                                                                                                  |
| [**RB \_ MOVEBAND**](rb-moveband.md)                 | Sposta una banda da un indice a un altro. <br/>                                                                                                                                                  |
| [**RB \_ PUSHCHEVRON**](rb-pushchevron.md)           | Inviato a un controllo Rebar per eseguire il push a livello di codice di una freccia di espansione.<br/>                                                                                                                               |
| [**RB \_ SETBANDINFO**](rb-setbandinfo.md)           | Imposta le caratteristiche di una banda esistente in un controllo Rebar. <br/>                                                                                                                             |
| [**sebandwidth RB \_**](rb-setbandwidth.md)         | Imposta la larghezza di una banda ancorata.<br/>                                                                                                                                                         |
| [**RB \_ SETBARINFO**](rb-setbarinfo.md)             | Imposta le caratteristiche di un controllo Rebar. <br/>                                                                                                                                             |
| [**RB \_ SETBKCOLOR**](rb-setbkcolor.md)             | Imposta il colore di sfondo predefinito del controllo Rebar. <br/>                                                                                                                                         |
| [**RB \_ SETCOLORSCHEME**](rb-setcolorscheme.md)     | Imposta le informazioni sulla combinazione di colori per il controllo Rebar. <br/>                                                                                                                                 |
| [**RB \_ SETEXTENDEDSTYLE**](rb-setextendedstyle.md) | Imposta lo stile esteso. Questo messaggio non è implementato.<br/>                                                                                                                                 |
| [**\_tavolozza RB**](rb-setpalette.md)             | Imposta la tavolozza corrente del controllo Rebar. <br/>                                                                                                                                                |
| [**PADRE di RB \_**](rb-setparent.md)               | Imposta la finestra padre di un controllo Rebar. <br/>                                                                                                                                                    |
| [**RB \_ SETTEXTCOLOR**](rb-settextcolor.md)         | Imposta il colore del testo predefinito del controllo Rebar. <br/>                                                                                                                                               |
| [**\_descrizioni comandi RB**](rb-settooltips.md)           | Associa un controllo ToolTip al controllo Rebar. <br/>                                                                                                                                     |
| [**RB \_ SETUNICODEFORMAT**](rb-setunicodeformat.md) | Imposta il flag di formato carattere Unicode per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo. <br/> |
| [**RB \_ SETWINDOWTHEME**](rb-setwindowtheme.md)     | Imposta lo stile di visualizzazione di un controllo Rebar.<br/>                                                                                                                                                 |
| [**RB \_ SHOWBAND**](rb-showband.md)                 | Mostra o nasconde una determinata banda in un controllo Rebar. <br/>                                                                                                                                          |
| [**RB \_ SIZETORECT**](rb-sizetorect.md)             | Tenta di trovare il layout migliore delle bande per il rettangolo specificato. <br/>                                                                                                                   |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                        | Contenuto                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (Rebar)](nm-customdraw-rebar.md)            | Inviato dal controllo Rebar per notificare alla finestra padre le operazioni di disegno. Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .<br/>                                                                                               |
| [NM \_ NCHITTEST (Rebar)](nm-nchittest-rebar.md)              | Inviato da un controllo Rebar quando il controllo riceve un messaggio [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) . Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                 |
| [NM \_ RELEASEDCAPTURE (Rebar)](nm-releasedcapture-rebar-.md) | Notifica alla finestra padre di un controllo Rebar che il controllo sta rilasciando l'acquisizione del mouse. Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) . <br/>                                                                                        |
| [RBN \_ automatici](rbn-autobreak.md)                          | Notifica all'elemento padre di un controllo [Rebar](rebar-controls.md) che verrà visualizzata un'interruzioni nella barra. L'elemento padre determina se eseguire l'interruzioni. <br/>                                                                                                                            |
| [\_ridimensionamento automatico RBN](rbn-autosize.md)                            | Inviato da un controllo Rebar creato con lo [**stile \_ AUTOSIZE di RBS**](rebar-control-styles.md) quando il Rebar viene ridimensionato automaticamente. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                  |
| [\_BEGINDRAG RBN](rbn-begindrag.md)                          | Inviato da un controllo Rebar quando l'utente inizia a trascinare un gruppo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                           |
| [\_CHEVRONPUSHED RBN](rbn-chevronpushed.md)                  | Inviato da un controllo Rebar quando viene eseguito il push di una freccia di espansione. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                                        |
| [\_CHILDSIZE RBN](rbn-childsize.md)                          | Inviato da un controllo Rebar quando la finestra figlio di una banda viene ridimensionata. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                          |
| [\_DELETEDBAND RBN](rbn-deletedband.md)                      | Inviato da un controllo Rebar dopo l'eliminazione di una banda. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                  |
| [\_DELETINGBAND RBN](rbn-deletingband.md)                    | Inviato da un controllo Rebar quando un gruppo sta per essere eliminato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                             |
| [\_ENDDRAG RBN](rbn-enddrag.md)                              | Inviato da un controllo Rebar quando l'utente smette di trascinare un gruppo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                            |
| [RBN \_ GETobject](rbn-getobject.md)                          | Inviato da un controllo Rebar creato con lo [**stile \_ REGISTERDROP di RBS**](rebar-control-styles.md) quando un oggetto viene trascinato su una banda nel controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/> |
| [\_HEIGHTCHANGE RBN](rbn-heightchange.md)                    | Inviato da un controllo Rebar quando l'altezza è cambiata. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                    |
| [\_LAYOUTCHANGED RBN](rbn-layoutchanged.md)                  | Inviato da un controllo Rebar quando l'utente modifica il layout delle bande del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                        |
| [\_MinMax RBN](rbn-minmax.md)                                | Inviato da un controllo Rebar prima di massimizzare o ridurre al minimo un gruppo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                       |
| [\_SPLITTERDRAG RBN](rbn-splitterdrag.md)                    | Inviato da un controllo Rebar quando l'utente trascina una barra di divisione. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                 |



 

### <a name="structures"></a>Strutture



| Argomento                                        | Contenuto                                                                                                                                      |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize)         | Contiene informazioni utilizzate per la gestione dei codici di notifica [ \_ AUTOSIZE RBN](rbn-autosize.md) . <br/>                                   |
| [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar)                   | Contiene informazioni utilizzate per la gestione di diversi codici di notifica del controllo Rebar. <br/>                                                           |
| [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) | Contiene informazioni utilizzate con la notifica di [ \_ autobreak RBN](rbn-autobreak.md) .<br/>                                               |
| [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron)     | Contiene informazioni utilizzate per la gestione del codice di notifica [ \_ CHEVRONPUSHED di RBN](rbn-chevronpushed.md) . <br/>                          |
| [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) | Contiene informazioni utilizzate per la gestione del codice di notifica [ \_ CHILDSIZE di RBN](rbn-childsize.md) . <br/>                                  |
| [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter)   | Contiene informazioni utilizzate per gestire un codice di notifica [ \_ SPLITTERDRAG RBN](rbn-splitterdrag.md) .<br/>                                |
| [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo)       | Contiene informazioni specifiche per un'operazione di hit test. Questa struttura viene utilizzata con il messaggio di [**RB \_ HITTEST**](rb-hittest.md) . <br/> |
| [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)       | Contiene informazioni che definiscono una banda in un controllo Rebar. <br/>                                                                      |
| [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo)               | Contiene informazioni che descrivono le caratteristiche del controllo Rebar. <br/>                                                                |



 

### <a name="constants"></a>Costanti



| Argomento                                            | Contenuto                                                                                              |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Stili del controllo Rebar](rebar-control-styles.md) | I controlli Rebar supportano un'ampia gamma di stili di controllo oltre agli stili di finestra standard. <br/> |



 

 

