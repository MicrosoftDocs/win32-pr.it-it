---
title: Trackbar
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli trackbar.
ms.assetid: vs|controls|~\controls\trackbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f56c5a483340a8e77ef0df6503481d3cbc50e51a85bd07258cdf283dd563c6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060541"
---
# <a name="trackbar"></a>Trackbar

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli trackbar.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                                  | Contenuto                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sui controlli Trackbar](trackbar-controls.md)       | Un trackbar è una finestra che contiene un dispositivo di scorrimento (talvolta denominato pollice) in un canale e segni di graduazione facoltativi. Quando l'utente sposta il dispositivo di scorrimento usando il mouse o i tasti di direzione, il trackbar invia messaggi di notifica per indicare la modifica.<br/> |
| [Uso dei controlli Trackbar](using-trackbar-controls.md) | In questa sezione vengono forniti dettagli di implementazione ed esempi per i controlli trackbar.<br/>                                                                                                                                                                               |



 

### <a name="messages"></a>Messaggi



| Argomento                                                 | Contenuto                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TBM \_ CLEARSEL**](tbm-clearsel.md)                 | Cancella l'intervallo di selezione corrente in un trackbar. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ CLEARTICS**](tbm-cleartics.md)               | Rimuove i segni di graduazione correnti da un trackbar. Questo messaggio non rimuove il primo e l'ultimo segno di graduazione, che vengono creati automaticamente dal trackbar. <br/>                                                                                                                                           |
| [**TBM \_ GETBUDDY**](tbm-getbuddy.md)                 | Recupera l'handle per una finestra del controllo trackbar in una determinata posizione. La posizione specificata è relativa all'orientamento del controllo (orizzontale o verticale). <br/>                                                                                                                                 |
| [**TBM \_ GETCHANNELRECT**](tbm-getchannelrect.md)     | Recupera le dimensioni e la posizione del rettangolo di delimitazione per il canale di un trackbar. Il canale è l'area su cui si sposta il dispositivo di scorrimento. Contiene l'evidenziazione quando viene selezionato un intervallo. <br/>                                                                                                         |
| [**TBM \_ GETLINESIZE**](tbm-getlinesize.md)           | Recupera il numero di posizioni logiche che il dispositivo di scorrimento del trackbar sposta in risposta all'input della tastiera dai tasti di direzione, ad esempio i tasti o . Le posizioni logiche sono gli incrementi interi nell'intervallo di posizioni del dispositivo di scorrimento minimo/massimo del trackbar. <br/>                                         |
| [**TBM \_ GETNUMTICS**](tbm-getnumtics.md)             | Recupera il numero di segni di graduazione in un trackbar. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETPAGESIZE**](tbm-getpagesize.md)           | Recupera il numero di posizioni logiche che il dispositivo di scorrimento del trackbar sposta in risposta all'input da tastiera, ad esempio i tasti o o l'input del mouse, ad esempio i clic nel canale del trackbar. Le posizioni logiche sono gli incrementi interi nell'intervallo di posizioni del dispositivo di scorrimento minimo/massimo del trackbar. <br/>   |
| [**TBM \_ GETPOS**](tbm-getpos.md)                     | Recupera la posizione logica corrente del dispositivo di scorrimento in un trackbar. Le posizioni logiche sono i valori interi nell'intervallo tra le posizioni minime e massime del dispositivo di scorrimento del trackbar. <br/>                                                                                                                       |
| [**TBM \_ GETPTICS**](tbm-getptics.md)                 | Recupera l'indirizzo di una matrice che contiene le posizioni dei segni di graduazione per un trackbar. <br/>                                                                                                                                                                                                        |
| [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md)           | Recupera la posizione massima del dispositivo di scorrimento in un trackbar. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md)           | Recupera la posizione minima per il dispositivo di scorrimento in un trackbar. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETSELEND**](tbm-getselend.md)               | Recupera la posizione finale dell'intervallo di selezione corrente in un trackbar. <br/>                                                                                                                                                                                                                            |
| [**TBM \_ GETSELSTART**](tbm-getselstart.md)           | Recupera la posizione iniziale dell'intervallo di selezione corrente in un trackbar. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md)     | Recupera la lunghezza del dispositivo di scorrimento in un trackbar. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETTHUMBRECT**](tbm-getthumbrect.md)         | Recupera le dimensioni e la posizione del rettangolo di delimitazione per il dispositivo di scorrimento in un trackbar. <br/>                                                                                                                                                                                                                |
| [**TBM \_ GETTIC**](tbm-gettic.md)                     | Recupera la posizione logica di un segno di graduazione in un trackbar. La posizione logica può essere uno qualsiasi dei valori interi nell'intervallo tra le posizioni minime e massime del dispositivo di scorrimento del trackbar. <br/>                                                                                                                     |
| [**TBM \_ GETTICPOS**](tbm-getticpos.md)               | Recupera la posizione fisica corrente di un segno di graduazione in un trackbar.<br/>                                                                                                                                                                                                                                   |
| [**TBM \_ GETTOOLTIPS**](tbm-gettooltips.md)           | Recupera l'handle per il controllo descrizione comando assegnato al trackbar, se presente. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETUNICODEFORMAT**](tbm-getunicodeformat.md) | Recupera il flag di formato carattere Unicode per il controllo. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ SETBUDDY**](tbm-setbuddy.md)                 | Assegna una finestra come finestra degli amici per un controllo trackbar. Le finestre di controllo trackbar vengono visualizzate automaticamente in una posizione relativa all'orientamento del controllo (orizzontale o verticale). <br/>                                                                                                          |
| [**TBM \_ SETLINESIZE**](tbm-setlinesize.md)           | Imposta il numero di posizioni logiche che il dispositivo di scorrimento del trackbar sposta in risposta all'input da tastiera dei tasti di direzione, ad esempio i tasti o . Le posizioni logiche sono gli incrementi interi nell'intervallo di posizioni del dispositivo di scorrimento minimo/massimo del trackbar. <br/>                                              |
| [**TBM \_ SETPAGESIZE**](tbm-setpagesize.md)           | Imposta il numero di posizioni logiche che il dispositivo di scorrimento del trackbar sposta in risposta all'input da tastiera, ad esempio i tasti o o l'input del mouse, ad esempio i clic nel canale del trackbar. Le posizioni logiche sono gli incrementi interi nell'intervallo di posizioni del dispositivo di scorrimento minimo/massimo del trackbar. <br/>        |
| [**TBM \_ SETPOS**](tbm-setpos.md)                     | Imposta la posizione logica corrente del dispositivo di scorrimento in un trackbar. <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SETPOSNOTIFY**](tbm-setposnotify.md)         | Imposta la posizione logica corrente del dispositivo di scorrimento in un trackbar. <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SETRANGE**](tbm-setrange.md)                 | Imposta l'intervallo di posizioni logiche minime e massime per il dispositivo di scorrimento in un trackbar. <br/>                                                                                                                                                                                                                  |
| [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)           | Imposta la posizione logica massima per il dispositivo di scorrimento in un trackbar. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)           | Imposta la posizione logica minima per il dispositivo di scorrimento in un trackbar. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETSEL**](tbm-setsel.md)                     | Imposta le posizioni iniziale e finale per l'intervallo di selezione disponibile in un trackbar. <br/>                                                                                                                                                                                                                |
| [**TBM \_ SETSELEND**](tbm-setselend.md)               | Imposta la posizione logica finale dell'intervallo di selezione corrente in un trackbar. Questo messaggio viene ignorato se il trackbar non ha lo [**stile \_ TBS ENABLESELRANGE.**](trackbar-control-styles.md) <br/>                                                                              |
| [**TBM \_ SETSELSTART**](tbm-setselstart.md)           | Imposta la posizione logica iniziale dell'intervallo di selezione corrente in un trackbar. Questo messaggio viene ignorato se il trackbar non ha lo [**stile \_ TBS ENABLESELRANGE.**](trackbar-control-styles.md) <br/>                                                                            |
| [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md)     | Imposta la lunghezza del dispositivo di scorrimento in un trackbar. Questo messaggio viene ignorato se il trackbar non ha lo [**stile TBS \_ FIXEDLENGTH.**](trackbar-control-styles.md) <br/>                                                                                                                      |
| [**TBM \_ SETTIC**](tbm-settic.md)                     | Imposta un segno di graduazione in un trackbar nella posizione logica specificata. <br/>                                                                                                                                                                                                                                      |
| [**TBM \_ SETTICFREQ**](tbm-setticfreq.md)             | Imposta la frequenza di intervallo per i segni di graduazione in un trackbar. Ad esempio, se la frequenza è impostata su due, viene visualizzato un segno di graduazione per ogni altro incremento nell'intervallo del trackbar. L'impostazione predefinita per la frequenza è una; ciò significa che ogni incremento nell'intervallo è associato a un segno di graduazione. <br/> |
| [**TBM \_ SETTIPSIDE**](tbm-settipside.md)             | Posiziona un controllo descrizione comando utilizzato da un controllo trackbar. Controlli Trackbar che usano le descrizioni comando di visualizzazione dello stile [**\_ TBS TOOLTIPS.**](trackbar-control-styles.md) <br/>                                                                                                                           |
| [**TBM \_ SETTOOLTIPS**](tbm-settooltips.md)           | Assegna un controllo descrizione comando a un controllo trackbar. <br/>                                                                                                                                                                                                                                                       |
| [**TBM \_ SETUNICODEFORMAT**](tbm-setunicodeformat.md) | Imposta il flag di formato carattere Unicode per il controllo . Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo. <br/>                                                                                                               |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                              | Contenuto                                                                                                                                                                                      |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (trackbar)](nm-customdraw-trackbar.md)            | Inviato da un controllo trackbar per notificare alle finestre padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>        |
| [NM \_ RELEASEDCAPTURE (trackbar)](nm-releasedcapture-trackbar-.md) | Notifica alla finestra padre di un controllo TrackBar che il controllo sta rilasciando mouse capture. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/> |
| [TRBN \_ THUMBPOSCHANGING](trbn-thumbposchanging.md)                | Notifica che la posizione del cursore su un trackbar sta cambiando. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>                               |



 

### <a name="constants"></a>Costanti



| Argomento                                                  | Contenuto                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Valori di disegno personalizzati](custom-draw-values.md)           | Questa sezione elenca i valori usati per identificare le parti di un controllo TrackBar. <br/>      |
| [Stili del controllo Trackbar](trackbar-control-styles.md) | Questa sezione contiene informazioni sugli stili usati con i controlli trackbar. <br/> |



 

 

 





