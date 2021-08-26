---
title: Descrizione comando
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli descrizione comando.
ms.assetid: vs|controls|~\controls\tooltip\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30ebe66569ede133c311168d3f3f2870dc3aeabe8eaeaa3e15d6584be2d6873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046041"
---
# <a name="tooltip"></a>Descrizione comando

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli descrizione comando.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                              | Contenuto                                                                                                                          |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sui controlli descrizione comando](tooltip-controls.md)     | Le descrizioni comando vengono visualizzate automaticamente o popup quando l'utente posiziona il puntatore del mouse su uno strumento o su un altro elemento dell'interfaccia utente.<br/> |
| [Uso dei controlli descrizione comando](using-tooltip-contro.md) | Questa sezione contiene esempi che illustrano come creare tipi diversi di descrizioni comando.<br/>                             |



 

### <a name="messages"></a>Messaggi



| Argomento                                               | Contenuto                                                                                                                                                                                                          |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ATTIVAZIONE \_ TTM**](ttm-activate.md)               | Attiva o disattiva un controllo descrizione comando. <br/>                                                                                                                                                           |
| [**TTM \_ ADDTOOL**](ttm-addtool.md)                 | Registra uno strumento con un controllo descrizione comando. <br/>                                                                                                                                                              |
| [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md)           | Calcola il rettangolo di visualizzazione del testo di un controllo descrizione comando dal rettangolo della finestra o il rettangolo della finestra della descrizione comando necessario per visualizzare un rettangolo di visualizzazione del testo specificato. <br/>                                |
| [**TTM \_ DELTOOL**](ttm-deltool.md)                 | Rimuove uno strumento da un controllo descrizione comando. <br/>                                                                                                                                                                |
| [**TTM \_ ENUMTOOLS**](ttm-enumtools.md)             | Recupera le informazioni mantenute da un controllo descrizione comando sullo strumento corrente, ovvero lo strumento per cui la descrizione comando visualizza attualmente testo. <br/>                                               |
| [**TTM \_ GETBUBBLESIZE**](ttm-getbubblesize.md)     | Restituisce la larghezza e l'altezza di un controllo descrizione comando.<br/>                                                                                                                                                     |
| [**TTM \_ GETCURRENTTOOL**](ttm-getcurrenttool.md)   | Recupera le informazioni per lo strumento corrente in un controllo descrizione comando. <br/>                                                                                                                                  |
| [**TTM \_ GETDELAYTIME**](ttm-getdelaytime.md)       | Recupera le durate iniziali, popup e di nuova visualizzazione attualmente impostate per un controllo descrizione comando.<br/>                                                                                                               |
| [**TTM \_ GETMARGIN**](ttm-getmargin.md)             | Recupera i margini superiore, sinistro, inferiore e destro impostati per una finestra della descrizione comando. Un margine è la distanza, in pixel, tra il bordo della finestra della descrizione comando e il testo contenuto all'interno della finestra della descrizione comando. <br/> |
| [**TTM \_ GETMAXTIPWIDTH**](ttm-getmaxtipwidth.md)   | Recupera la larghezza massima per una finestra della descrizione comando. <br/>                                                                                                                                                     |
| [**TTM \_ GETTEXT**](ttm-gettext.md)                 | Recupera le informazioni mantenute da un controllo descrizione comando su uno strumento. <br/>                                                                                                                                   |
| [**TTM \_ GETTIPBKCOLOR**](ttm-gettipbkcolor.md)     | Recupera il colore di sfondo in una finestra della descrizione comando. <br/>                                                                                                                                                   |
| [**TTM \_ GETTIPTEXTCOLOR**](ttm-gettiptextcolor.md) | Recupera il colore del testo in una finestra della descrizione comando. <br/>                                                                                                                                                         |
| [**TTM \_ GETTITLE**](ttm-gettitle.md)               | Recuperare informazioni relative al titolo di un controllo descrizione comando.<br/>                                                                                                                                        |
| [**TTM \_ GETTOOLCOUNT**](ttm-gettoolcount.md)       | Recupera un conteggio degli strumenti gestiti da un controllo descrizione comando. <br/>                                                                                                                                       |
| [**TTM \_ GETTOOLINFO**](ttm-gettoolinfo.md)         | Recupera le informazioni mantenute da un controllo descrizione comando su uno strumento. <br/>                                                                                                                              |
| [**TTM \_ HITTEST**](ttm-hittest.md)                 | Verifica un punto per determinare se si trova all'interno del rettangolo di delimitazione dello strumento specificato e, in caso contrario, recupera informazioni sullo strumento. <br/>                                                     |
| [**TTM \_ NEWTOOLRECT**](ttm-newtoolrect.md)         | Imposta un nuovo rettangolo di delimitazione per uno strumento. <br/>                                                                                                                                                             |
| [**TTM \_ POP**](ttm-pop.md)                         | Rimuove una finestra della descrizione comando visualizzata dalla visualizzazione. <br/>                                                                                                                                                         |
| [**TTM \_ POPUP**](ttm-popup.md)                     | Determina la visualizzazione della descrizione comando in corrispondenza delle coordinate dell'ultimo messaggio del mouse.<br/>                                                                                                                            |
| [**TTM \_ RELAYEVENT**](ttm-relayevent.md)           | Passa un messaggio del mouse a un controllo descrizione comando per l'elaborazione. <br/>                                                                                                                                           |
| [**TTM \_ SETDELAYTIME**](ttm-setdelaytime.md)       | Imposta le durate iniziali, popup e di nuova visualizzazione per un controllo descrizione comando.<br/>                                                                                                                                  |
| [**TTM \_ SETMARGIN**](ttm-setmargin.md)             | Imposta i margini superiore, sinistro, inferiore e destro per una finestra della descrizione comando. Un margine è la distanza, in pixel, tra il bordo della finestra della descrizione comando e il testo contenuto all'interno della finestra della descrizione comando. <br/>          |
| [**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md)   | Imposta la larghezza massima per una finestra della descrizione comando. <br/>                                                                                                                                                          |
| [**TTM \_ SETTIPBKCOLOR**](ttm-settipbkcolor.md)     | Imposta il colore di sfondo in una finestra della descrizione comando. <br/>                                                                                                                                                        |
| [**TTM \_ SETTIPTEXTCOLOR**](ttm-settiptextcolor.md) | Imposta il colore del testo in una finestra della descrizione comando. <br/>                                                                                                                                                              |
| [**TTM \_ SETTITLE**](ttm-settitle.md)               | Aggiunge un'icona standard e una stringa del titolo a una descrizione comando.<br/>                                                                                                                                                    |
| [**TTM \_ SETTOOLINFO**](ttm-settoolinfo.md)         | Imposta le informazioni mantenute da un controllo descrizione comando per uno strumento. <br/>                                                                                                                                     |
| [**TTM \_ SETWINDOWTHEME**](ttm-setwindowtheme.md)   | Imposta lo stile di visualizzazione di un controllo descrizione comando.<br/>                                                                                                                                                            |
| [**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md)     | Attiva o disattiva una descrizione comando di rilevamento.<br/>                                                                                                                                                           |
| [**TTM \_ TRACKPOSITION**](ttm-trackposition.md)     | Imposta la posizione di una descrizione comando di rilevamento.<br/>                                                                                                                                                               |
| [**AGGIORNAMENTO \_ TTM**](ttm-update.md)                   | Forza il ridisegno della descrizione comando corrente. <br/>                                                                                                                                                             |
| [**TTM \_ UPDATETIPTEXT**](ttm-updatetiptext.md)     | Imposta il testo della descrizione comando per uno strumento. <br/>                                                                                                                                                                     |
| [**FINESTRA \_ TTMFROMPOINT**](ttm-windowfrompoint.md) | Consente a una routine di sottoclasse di visualizzare il testo di una descrizione comando per una finestra diversa da quella sotto il cursore del mouse. <br/>                                                                              |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                 | Contenuto                                                                                                                                                                                                                                                              |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (descrizione comando)](nm-customdraw-tooltip.md) | Inviato da un controllo descrizione comando per notificare alle finestre padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                 |
| [TTN \_ GETDISPINFO](ttn-getdispinfo.md)               | Inviato da un controllo descrizione comando per recuperare le informazioni necessarie per visualizzare una finestra della descrizione comando. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                            |
| [COLLEGAMENTO \_ TTNCLICK](ttn-linkclick.md)                   | Inviato quando si fa clic su un collegamento di testo all'interno di una descrizione comando del fumetto. <br/>                                                                                                                                                                                                |
| [TTN \_ NEEDTEXT](ttn-needtext.md)                     | Inviato da un controllo descrizione comando per recuperare le informazioni necessarie per visualizzare una finestra della descrizione comando. Questa notifica è identica a [TTN \_ GETDISPINFO](ttn-getdispinfo.md). Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md) <br/> |
| [TTN \_ POP](ttn-pop.md)                               | Notifica alla finestra proprietaria che una descrizione comando sta per essere nascosta. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                  |
| [TTN \_ SHOW](ttn-show.md)                             | Notifica alla finestra proprietaria che sta per essere visualizzato un controllo descrizione comando. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                       |



 

### <a name="structures"></a>Strutture



| Argomento                                    | Contenuto                                                                                                                                                                                                                           |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) | Contiene informazioni specifiche di un codice [di notifica NM \_ CUSTOMDRAW](nm-customdraw-tooltip.md) inviato da un controllo descrizione comando. <br/>                                                                                           |
| [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa)     | Contiene informazioni utilizzate nella gestione del codice [di notifica \_ GETDISPINFO TTN.](ttn-getdispinfo.md) Questa struttura sostituisce la struttura **TOOLTIPTEXT.** <br/>                                                          |
| [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)             | La [**struttura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) contiene informazioni su uno strumento in un controllo descrizione comando.<br/>                                                                                                                      |
| [**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle)         | Fornisce informazioni sul titolo di un controllo descrizione comando. <br/>                                                                                                                                                             |
| [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa)   | Contiene informazioni utilizzate da un controllo descrizione comando per determinare se un punto si trova nel rettangolo di delimitazione dello strumento specificato. Se il punto si trova nel rettangolo, la struttura riceve informazioni sullo strumento. <br/> |



 

### <a name="constants"></a>Costanti



| Argomento                                | Contenuto                                                                     |
|--------------------------------------|------------------------------------------------------------------------------|
| [Stili della descrizione comando](tooltip-styles.md) | Questa sezione elenca gli stili dei controlli usati con i controlli descrizione comando.<br/> |



 

 

 





