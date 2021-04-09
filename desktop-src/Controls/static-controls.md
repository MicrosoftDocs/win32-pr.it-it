---
title: Controllo statico
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli statici. Un controllo statico è un controllo che consente a un'applicazione di fornire all'utente testo informativo e grafici che in genere non richiedono alcuna risposta.
ms.assetid: vs|controls|~\controls\staticcontrols\staticcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62c8c5b554dad8c6f3c18d0c1ceb9300dde57b20
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047446"
---
# <a name="static-control"></a>Controllo statico

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli statici. Un *controllo statico* è un controllo che consente a un'applicazione di fornire all'utente testo informativo e grafici che in genere non richiedono alcuna risposta.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                              | Contenuto                                                              |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [Informazioni sui controlli statici](about-static-controls.md) | In questo argomento viene illustrato il modo in cui vengono utilizzati i controlli statici.<br/>         |
| [Stili del controllo statico](static-control-styles.md) |                                                                       |
| [Uso di controlli statici](using-static-controls.md) | In questo argomento viene fornito un esempio in cui viene utilizzato un controllo statico.<br/> |



 

### <a name="messages"></a>Messaggi



| Argomento                                 | Contenuto                                                                                                                                                                        |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_icona GetIcon STM**](stm-geticon.md)   | Un'applicazione invia il messaggio [**STM \_ GetIcon**](stm-geticon.md) per recuperare un handle per l'icona associata a un controllo statico con \_ stile icona SS. <br/> |
| [**GetImage STM \_**](stm-getimage.md) | Un'applicazione invia un messaggio [**STM \_ GetImage**](stm-getimage.md) per recuperare un handle per l'immagine (icona o bitmap) associata a un controllo statico. <br/>          |
| [**ICONA di STM \_**](stm-seticon.md)   | Un'applicazione invia il messaggio dell' [**\_ icona STM**](stm-seticon.md) per associare un'icona a un controllo icona. <br/>                                                     |
| [**\_Immagine STM**](stm-setimage.md) | Un'applicazione invia un messaggio di [**\_ Immagine STM**](stm-setimage.md) per associare una nuova immagine a un controllo statico.<br/>                                                |



 

### <a name="notifications"></a>Notifiche



| Argomento                                           | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [STN \_ selezionato](stn-clicked.md)                 | Quando l'utente fa clic su un controllo statico con stile di [**\_ notifica SS**](static-control-styles.md) , viene inviato il codice di notifica [ \_ con clic su STN](stn-clicked.md) . La finestra padre del controllo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                                                  |
| [\_DBLCLK STN](stn-dblclk.md)                   | Il codice di notifica di [STN \_ DBLCLK](stn-dblclk.md) viene inviato quando l'utente fa doppio clic su un controllo statico con stile di **\_ notifica SS** . La finestra padre del controllo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                                                                          |
| [STN \_ disabilitato](stn-disable.md)                 | Il codice di notifica di [ \_ disabilitazione di STN](stn-disable.md) viene inviato quando un controllo statico è disabilitato. Il controllo statico deve avere lo stile di **\_ notifica SS** per ricevere il codice di notifica. La finestra padre del controllo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                            |
| [\_Abilitazione di STN](stn-enable.md)                   | L' [ \_ Abilitazione](stn-enable.md) del codice di notifica di STN viene inviata quando un controllo statico è abilitato. Il controllo statico deve avere lo stile di **\_ notifica SS** per ricevere il codice di notifica. La finestra padre del controllo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                               |
| [**\_CTLCOLORSTATIC WM**](wm-ctlcolorstatic.md) | Un controllo statico o un controllo di modifica che è di sola lettura o disabilitato invia il [**messaggio \_ CTLCOLORSTATIC WM**](wm-ctlcolorstatic.md) alla relativa finestra padre quando il controllo sta per essere disegnato. Rispondendo a questo messaggio, la finestra padre può usare l'handle del contesto di dispositivo specificato per impostare il testo e i colori di sfondo del controllo statico. <br/> Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/> |



 

 

