---
title: Cercapersone
description: In questa sezione sono contenute informazioni sugli elementi di programmazione utilizzati con i controlli cercapersone.
ms.assetid: vs|controls|~\controls\pager\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df98100ed649e4237c51bfcabf41420c49d004
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300532"
---
# <a name="pager"></a>Cercapersone

In questa sezione sono contenute informazioni sugli elementi di programmazione utilizzati con i controlli cercapersone.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                | Contenuto                                                                                                                                         |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Controlli cercapersone](pager-controls.md) | Un *controllo pager* è un contenitore di finestre utilizzato con una finestra che non dispone di un'area di visualizzazione sufficiente per visualizzare tutto il contenuto.<br/> |



 

### <a name="macros"></a>Macro



| Argomento                                                 | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cercapersone \_ ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse)     | Abilita o Disabilita l'avanzamento del mouse per il controllo pager. Quando l'avanzamento del mouse è abilitato, il controllo pager trasmette i messaggi di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) alla finestra contenuta. È possibile utilizzare questa macro o inviare il [**messaggio \_ FORWARDMOUSE PGM**](pgm-forwardmouse.md) in modo esplicito. <br/>                                                                                                                     |
| [**Cercapersone \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor)         | Recupera il colore di sfondo corrente per il controllo pager. È possibile utilizzare questa macro o inviare il [**messaggio \_ GETBKCOLOR PGM**](pgm-getbkcolor.md) in modo esplicito. <br/>                                                                                                                                                                                                                                                                 |
| [**Pager \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder)           | Recupera le dimensioni correnti del bordo per il controllo pager. È possibile usare questa macro o inviare il messaggio [**PGM \_ GetBorder**](pgm-getborder.md) in modo esplicito. <br/>                                                                                                                                                                                                                                                                        |
| [**Cercapersone \_ GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize)   | Recupera le dimensioni correnti del pulsante per il controllo pager. È possibile utilizzare questa macro o inviare il [**messaggio \_ GETBUTTONSIZE PGM**](pgm-getbuttonsize.md) in modo esplicito. <br/>                                                                                                                                                                                                                                                                |
| [**Cercapersone \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) | Recupera lo stato del pulsante specificato in un controllo pager. È possibile utilizzare questa macro o inviare il [**messaggio \_ GETBUTTONSTATE PGM**](pgm-getbuttonstate.md) in modo esplicito. <br/>                                                                                                                                                                                                                                                       |
| [**Cercapersone \_ GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget)   | Recupera un puntatore all'interfaccia [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) del controllo pager. È possibile utilizzare questa macro o inviare il [**messaggio \_ GETDROPTARGET PGM**](pgm-getdroptarget.md) in modo esplicito. <br/>                                                                                                                                                                                                                                       |
| [**Cercapersone \_ GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos)                 | Recupera la posizione di scorrimento corrente del controllo cercapersone. È possibile utilizzare questa macro o inviare il [**messaggio \_ GETPOS PGM**](pgm-getpos.md) in modo esplicito. <br/>                                                                                                                                                                                                                                                                           |
| [**Cercapersone \_ RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize)         | Impone al controllo pager di ricalcolare la dimensione della finestra contenuta. L'uso di questa macro comporterà l'invio di una notifica [PGN \_ CALCSIZE](pgn-calcsize.md) . È possibile utilizzare questa macro o inviare il [**messaggio \_ RECALCSIZE PGM**](pgm-recalcsize.md) in modo esplicito. <br/>                                                                                                                                                        |
| [**Cercapersone \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor)         | Imposta il colore di sfondo corrente per il controllo pager. È possibile utilizzare questa macro o inviare il [**messaggio \_ SETBKCOLOR PGM**](pgm-setbkcolor.md) in modo esplicito. <br/>                                                                                                                                                                                                                                                                      |
| [**\_Bordo cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder)           | Imposta la dimensione corrente del bordo per il controllo pager. È possibile utilizzare questa macro o inviare in modo esplicito il messaggio [**PGM di \_ Border**](pgm-setborder.md) . <br/>                                                                                                                                                                                                                                                                             |
| [**Cercapersone \_ SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize)   | Imposta la dimensione corrente del pulsante per il controllo pager. È possibile utilizzare questa macro o inviare il [**messaggio \_ SETBUTTONSIZE PGM**](pgm-setbuttonsize.md) in modo esplicito. <br/>                                                                                                                                                                                                                                                                     |
| [**\_Figlio cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild)             | Imposta la finestra contenuta per il controllo pager. Questa macro non modificherà l'elemento padre della finestra contenuta; assegna un handle di finestra al controllo pager per lo scorrimento. Nella maggior parte dei casi, la finestra contenuta sarà una finestra figlio. In tal caso, la finestra contenuta deve essere un elemento figlio del controllo pager. È possibile utilizzare questa macro o inviare in modo esplicito il messaggio [**PGM \_ figlio**](pgm-setchild.md) . <br/> |
| [**Cercapersone \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos)                 | Imposta la posizione di scorrimento per il controllo pager. È possibile utilizzare questa macro o inviare il [**messaggio \_ SETPOS PGM**](pgm-setpos.md) in modo esplicito. <br/>                                                                                                                                                                                                                                                                                       |
| [**Cercapersone \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)   | **Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.**<br/> Imposta i parametri di scorrimento del controllo pager, inclusi il valore di timeout, le righe per ogni timeout e i pixel per riga. È possibile utilizzare questa macro o inviare il [**messaggio \_ SETSETSCROLLINFO PGM**](pgm-setscrollinfo.md) in modo esplicito. <br/>                                                                                                  |



 

### <a name="messages"></a>Messaggi



| Argomento                                              | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_FORWARDMOUSE PGM**](pgm-forwardmouse.md)      | Abilita o Disabilita l'avanzamento del mouse per il controllo pager. Quando l'avanzamento del mouse è abilitato, il controllo pager trasmette i messaggi di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) alla finestra contenuta. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ ForwardMouse del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) . <br/>                                                                                                                       |
| [**\_GETBKCOLOR PGM**](pgm-getbkcolor.md)          | Recupera il colore di sfondo corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ GetBkColor del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) . <br/>                                                                                                                                                                                                                                                                   |
| [**PGM \_ GETborder**](pgm-getborder.md)            | Recupera le dimensioni correnti del bordo per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**pager \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) . <br/>                                                                                                                                                                                                                                                                          |
| [**\_GETBUTTONSIZE PGM**](pgm-getbuttonsize.md)    | Recupera le dimensioni correnti del pulsante per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ GetButtonSize del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) . <br/>                                                                                                                                                                                                                                                                  |
| [**\_GETBUTTONSTATE PGM**](pgm-getbuttonstate.md)  | Recupera lo stato del pulsante specificato in un controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ GetButtonState del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) . <br/>                                                                                                                                                                                                                                                         |
| [**\_GETDROPTARGET PGM**](pgm-getdroptarget.md)    | Recupera un puntatore all'interfaccia [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) del controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ GetDropTarget del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) . <br/>                                                                                                                                                                                                                                         |
| [**\_GETPOS PGM**](pgm-getpos.md)                  | Recupera la posizione di scorrimento corrente del controllo cercapersone. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ GetPos del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) . <br/>                                                                                                                                                                                                                                                                             |
| [**\_RECALCSIZE PGM**](pgm-recalcsize.md)          | Impone al controllo pager di ricalcolare la dimensione della finestra contenuta. L'invio di questo messaggio comporterà l'invio di una notifica [PGN \_ CALCSIZE](pgn-calcsize.md) . È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ RecalcSize del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) . <br/>                                                                                                                                                      |
| [**\_SETBKCOLOR PGM**](pgm-setbkcolor.md)          | Imposta il colore di sfondo corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ SetBkColor del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) . <br/>                                                                                                                                                                                                                                                                        |
| [**PGM ( \_ bordo)**](pgm-setborder.md)            | Imposta la dimensione corrente del bordo per il controllo pager. È possibile inviare questo messaggio in modo esplicito o [**usare \_ la macro pager di pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) . <br/>                                                                                                                                                                                                                                                                               |
| [**\_SETBUTTONSIZE PGM**](pgm-setbuttonsize.md)    | Imposta la dimensione corrente del pulsante per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ SetButtonSize del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) . <br/>                                                                                                                                                                                                                                                                       |
| [**\_figlio PGM**](pgm-setchild.md)              | Imposta la finestra contenuta per il controllo pager. Questo messaggio non modificherà l'elemento padre della finestra contenuta; assegna un handle di finestra al controllo pager per lo scorrimento. Nella maggior parte dei casi, la finestra contenuta sarà una finestra figlio. In tal caso, la finestra contenuta deve essere un elemento figlio del controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**pager \_ figlio**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) . <br/> |
| [**\_SETPOS PGM**](pgm-setpos.md)                  | Imposta la posizione di scorrimento corrente per il controllo cercapersone. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ SetPos del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) . <br/>                                                                                                                                                                                                                                                                                 |
| [**\_SETSETSCROLLINFO PGM**](pgm-setscrollinfo.md) | **Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.**<br/> Imposta i parametri di scorrimento del controllo pager, inclusi il valore di timeout, le righe per ogni timeout e i pixel per riga. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ SetScrollInfo di cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) . <br/>                                                                                                  |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                        | Contenuto                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ RELEASEDCAPTURE (cercapersone)](nm-releasedcapture-pager-.md) | Notifica alla finestra padre di un controllo pager che il controllo ha rilasciato l'acquisizione del mouse. NM \_ RELEASEDCAPTURE viene inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) . <br/>                                                                                                                |
| [\_CALCSIZE PGN](pgn-calcsize.md)                            | Notifica inviata da un controllo cercapersone per ottenere le dimensioni di scorrimento della finestra contenuta. Queste dimensioni vengono utilizzate dal controllo pager per determinare la dimensione scorrevole della finestra contenuta. Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) . <br/> |
| [\_HOTITEMCHANGE PGN](pgn-hotitemchange.md)                  | Inviato da un controllo cercapersone quando cambia l'elemento attivo (evidenziato). <br/>                                                                                                                                                                                                                               |
| [\_scorrimento PGN](pgn-scroll.md)                                | Notifica inviata da un controllo pager prima della finestra contenuta a scorrimento. Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) . <br/>                                                                                                                         |



 

### <a name="structures"></a>Strutture



| Argomento                                | Contenuto                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) | Contiene e riceve le informazioni utilizzate dal controllo pager per calcolare l'area di scorrimento della finestra contenuta. Viene usato con la notifica [ \_ CALCSIZE PGN](pgn-calcsize.md) . <br/> |
| [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem)   | Contiene informazioni utilizzate con la [notifica \_ HOTITEMCHANGE PGN](pgn-hotitemchange.md) . <br/>                                                                                                |
| [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll)     | Contiene e riceve le informazioni utilizzate dal controllo pager per lo scorrimento della finestra contenuta. Viene usato con la notifica [di \_ scorrimento PGN](pgn-scroll.md) . <br/>                          |



 

### <a name="constants"></a>Costanti



| Argomento                                            | Contenuto                                                                            |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [Stili del controllo pager](pager-control-styles.md) | In questa sezione vengono elencati gli stili della finestra utilizzati durante la creazione di controlli cercapersone. <br/> |



 

 

