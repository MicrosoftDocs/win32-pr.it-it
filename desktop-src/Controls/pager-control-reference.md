---
title: Cercapersone
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli pager.
ms.assetid: vs|controls|~\controls\pager\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bf9860c9e1dd1d565b24c7bbfc02e46480198f5bdea03717288abc83591a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914771"
---
# <a name="pager"></a>Cercapersone

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli pager.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                | Contenuto                                                                                                                                         |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Controlli pager](pager-controls.md) | Un *controllo pager* è un contenitore finestra usato con una finestra che non dispone di un'area di visualizzazione sufficiente per visualizzare tutto il contenuto.<br/> |



 

### <a name="macros"></a>Macro



| Argomento                                                 | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Pager \_ ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse)     | Abilita o disabilita l'inoltro del mouse per il controllo pager. Quando l'inoltro del mouse è abilitato, il controllo pager inoltra [**i messaggi WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) alla finestra contenuta. È possibile usare questa macro o inviare il [**messaggio \_ FORWARDMOUSE PGM**](pgm-forwardmouse.md) in modo esplicito. <br/>                                                                                                                     |
| [**\_GetBkColor del pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor)         | Recupera il colore di sfondo corrente per il controllo pager. È possibile usare questa macro o inviare il [**messaggio \_ PGM GETBKCOLOR**](pgm-getbkcolor.md) in modo esplicito. <br/>                                                                                                                                                                                                                                                                 |
| [**\_GetBorder del pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder)           | Recupera le dimensioni correnti del bordo per il controllo pager. È possibile usare questa macro o inviare il [**messaggio \_ PGM GETBORDER**](pgm-getborder.md) in modo esplicito. <br/>                                                                                                                                                                                                                                                                        |
| [**\_GetButtonSize del pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize)   | Recupera le dimensioni correnti del pulsante per il controllo pager. È possibile usare questa macro o inviare il [**messaggio \_ PGM GETBUTTONSIZE in**](pgm-getbuttonsize.md) modo esplicito. <br/>                                                                                                                                                                                                                                                                |
| [**Pager \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) | Recupera lo stato del pulsante specificato in un controllo pager. È possibile usare questa macro o inviare il [**messaggio \_ PGM GETBUTTONSTATE**](pgm-getbuttonstate.md) in modo esplicito. <br/>                                                                                                                                                                                                                                                       |
| [**\_GetDropTarget del pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget)   | Recupera il puntatore a interfaccia [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) di un controllo pager. È possibile usare questa macro o inviare il [**messaggio \_ PGM GETDROPTARGET**](pgm-getdroptarget.md) in modo esplicito. <br/>                                                                                                                                                                                                                                       |
| [**GetPos del \_ pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos)                 | Recupera la posizione di scorrimento corrente del controllo pager. È possibile usare questa macro o inviare il [**messaggio \_ GETPOS PGM in**](pgm-getpos.md) modo esplicito. <br/>                                                                                                                                                                                                                                                                           |
| [**Pager \_ RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize)         | Forza il ricalcolo delle dimensioni della finestra contenuta nel controllo pager. L'uso di questa macro comporta l'invio di una notifica [ \_ PGN CALCSIZE.](pgn-calcsize.md) È possibile usare questa macro o inviare il [**messaggio PGM \_ RECALCSIZE in**](pgm-recalcsize.md) modo esplicito. <br/>                                                                                                                                                        |
| [**\_SetBkColor del pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor)         | Imposta il colore di sfondo corrente per il controllo pager. È possibile usare questa macro o inviare il [**messaggio PGM \_ SETBKCOLOR**](pgm-setbkcolor.md) in modo esplicito. <br/>                                                                                                                                                                                                                                                                      |
| [**\_SetBorder del pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder)           | Imposta le dimensioni correnti del bordo per il controllo pager. È possibile usare questa macro o inviare il [**messaggio PGM \_ SETBORDER**](pgm-setborder.md) in modo esplicito. <br/>                                                                                                                                                                                                                                                                             |
| [**\_SetButtonSize del pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize)   | Imposta le dimensioni correnti del pulsante per il controllo pager. È possibile usare questa macro o inviare il [**messaggio PGM \_ SETBUTTONSIZE in**](pgm-setbuttonsize.md) modo esplicito. <br/>                                                                                                                                                                                                                                                                     |
| [**SetChild del \_ pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild)             | Imposta la finestra contenuta per il controllo pager. Questa macro non modificherà l'elemento padre della finestra contenuta. assegna solo un handle di finestra al controllo pager per lo scorrimento. Nella maggior parte dei casi, la finestra contenuta sarà una finestra figlio. In questo caso, la finestra contenuta deve essere un elemento figlio del controllo pager. È possibile usare questa macro o inviare il [**messaggio PGM \_ SETCHILD in**](pgm-setchild.md) modo esplicito. <br/> |
| [**SetPos \_ del pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos)                 | Imposta la posizione di scorrimento per il controllo pager. È possibile usare questa macro o inviare il [**messaggio \_ PGM SETPOS in**](pgm-setpos.md) modo esplicito. <br/>                                                                                                                                                                                                                                                                                       |
| [**\_SetScrollInfo del pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)   | **Destinato all'uso interno; non consigliato per l'uso nelle applicazioni.**<br/> Imposta i parametri di scorrimento del controllo pager, inclusi il valore di timeout, le righe per timeout e i pixel per riga. È possibile usare questa macro o inviare il [**messaggio PGM \_ SETSETSCROLLINFO in**](pgm-setscrollinfo.md) modo esplicito. <br/>                                                                                                  |



 

### <a name="messages"></a>Messaggi



| Argomento                                              | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PGM \_ FORWARDMOUSE**](pgm-forwardmouse.md)      | Abilita o disabilita l'inoltro del mouse per il controllo pager. Quando l'inoltro del mouse è abilitato, il controllo pager inoltra [**i messaggi WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) alla finestra contenuta. È possibile inviare questo messaggio in modo esplicito o usare la macro [**Pager \_ ForwardMouse.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) <br/>                                                                                                                       |
| [**PGM \_ GETBKCOLOR**](pgm-getbkcolor.md)          | Recupera il colore di sfondo corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Pager GetBkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) <br/>                                                                                                                                                                                                                                                                   |
| [**PGM \_ GETBORDER**](pgm-getborder.md)            | Recupera le dimensioni correnti del bordo per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetBorder del pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) <br/>                                                                                                                                                                                                                                                                          |
| [**PGM \_ GETBUTTONSIZE**](pgm-getbuttonsize.md)    | Recupera le dimensioni correnti del pulsante per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Pager GetButtonSize.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) <br/>                                                                                                                                                                                                                                                                  |
| [**PGM \_ GETBUTTONSTATE**](pgm-getbuttonstate.md)  | Recupera lo stato del pulsante specificato in un controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Pager GetButtonState.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) <br/>                                                                                                                                                                                                                                                         |
| [**PGM \_ GETDROPTARGET**](pgm-getdroptarget.md)    | Recupera il puntatore a interfaccia [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) di un controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetDropTarget del pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) <br/>                                                                                                                                                                                                                                         |
| [**PGM \_ GETPOS**](pgm-getpos.md)                  | Recupera la posizione di scorrimento corrente del controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetPos del pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) <br/>                                                                                                                                                                                                                                                                             |
| [**PGM \_ RECALCSIZE**](pgm-recalcsize.md)          | Forza il ricalcolo delle dimensioni della finestra contenuta nel controllo pager. L'invio di questo messaggio comporta l'invio di una notifica [ \_ PGN CALCSIZE.](pgn-calcsize.md) È possibile inviare questo messaggio in modo esplicito o usare la macro [**Pager \_ RecalcSize.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) <br/>                                                                                                                                                      |
| [**PGM \_ SETBKCOLOR**](pgm-setbkcolor.md)          | Imposta il colore di sfondo corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Pager SetBkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) <br/>                                                                                                                                                                                                                                                                        |
| [**PGM \_ SETBORDER**](pgm-setborder.md)            | Imposta le dimensioni correnti del bordo per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Pager SetBorder.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) <br/>                                                                                                                                                                                                                                                                               |
| [**PGM \_ SETBUTTONSIZE**](pgm-setbuttonsize.md)    | Imposta le dimensioni correnti del pulsante per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetButtonSize del pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) <br/>                                                                                                                                                                                                                                                                       |
| [**PGM \_ SETCHILD**](pgm-setchild.md)              | Imposta la finestra contenuta per il controllo pager. Questo messaggio non modificherà l'elemento padre della finestra contenuta. assegna solo un handle di finestra al controllo pager per lo scorrimento. Nella maggior parte dei casi, la finestra contenuta sarà una finestra figlio. In questo caso, la finestra contenuta deve essere un elemento figlio del controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Pager SetChild.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) <br/> |
| [**PGM \_ SETPOS**](pgm-setpos.md)                  | Imposta la posizione di scorrimento corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Pager SetPos.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) <br/>                                                                                                                                                                                                                                                                                 |
| [**PGM \_ SETSETSCROLLINFO**](pgm-setscrollinfo.md) | **Destinato all'uso interno; non consigliato per l'uso nelle applicazioni.**<br/> Imposta i parametri di scorrimento del controllo pager, inclusi il valore di timeout, le righe per timeout e i pixel per riga. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ Pager SetScrollInfo.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) <br/>                                                                                                  |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                        | Contenuto                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ RELEASEDCAPTURE (pager)](nm-releasedcapture-pager-.md) | Notifica alla finestra padre di un controllo pager che il controllo ha rilasciato il mouse capture. NM \_ RELEASEDCAPTURE viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                |
| [PGN \_ CALCSIZE](pgn-calcsize.md)                            | Notifica inviata da un controllo pager per ottenere le dimensioni scorrevoli della finestra contenuta. Queste dimensioni vengono utilizzate dal controllo pager per determinare le dimensioni scorrevoli della finestra contenuta. Questa notifica viene inviata sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/> |
| [PGN \_ HOTITEMCHANGE](pgn-hotitemchange.md)                  | Inviato da un controllo pager quando l'elemento con stato di accesso (evidenziato) viene modificato. <br/>                                                                                                                                                                                                                               |
| [SCORRIMENTO \_ PGN](pgn-scroll.md)                                | Notifica inviata da un controllo pager prima dello scorrimento della finestra contenuta. Questa notifica viene inviata sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                         |



 

### <a name="structures"></a>Strutture



| Argomento                                | Contenuto                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) | Contiene e riceve informazioni utilizzate dal controllo pager per calcolare l'area scorrevole della finestra contenuta. Viene usato con la [notifica \_ CALCSIZE PGN.](pgn-calcsize.md) <br/> |
| [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem)   | Contiene le informazioni usate con la [notifica \_ HOTITEMCHANGE PGN.](pgn-hotitemchange.md) <br/>                                                                                                |
| [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll)     | Contiene e riceve informazioni utilizzate dal controllo pager durante lo scorrimento della finestra contenuta. Viene usato con la notifica [SCROLL PGN. \_ ](pgn-scroll.md) <br/>                          |



 

### <a name="constants"></a>Costanti



| Argomento                                            | Contenuto                                                                            |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [Stili del controllo Pager](pager-control-styles.md) | In questa sezione vengono elencati gli stili della finestra usati durante la creazione di controlli pager. <br/> |



 

 

