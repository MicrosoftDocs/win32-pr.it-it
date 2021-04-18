---
title: TrackBar
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli TrackBar.
ms.assetid: vs|controls|~\controls\trackbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe8e58cd8db9c2811f31cac92ee3d1d31c2c02d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298131"
---
# <a name="trackbar"></a>TrackBar

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli TrackBar.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                                  | Contenuto                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sui controlli TrackBar](trackbar-controls.md)       | Un TrackBar è una finestra che contiene un dispositivo di scorrimento (talvolta denominato Thumb) in un canale e segni di graduazione facoltativi. Quando l'utente sposta il dispositivo di scorrimento usando il mouse o i tasti di direzione, il TrackBar invia messaggi di notifica per indicare la modifica.<br/> |
| [Uso di controlli TrackBar](using-trackbar-controls.md) | In questa sezione vengono forniti dettagli ed esempi di implementazione per i controlli TrackBar.<br/>                                                                                                                                                                               |



 

### <a name="messages"></a>Messaggi



| Argomento                                                 | Contenuto                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TBM \_ CLEARSEL**](tbm-clearsel.md)                 | Cancella l'intervallo di selezione corrente in un TrackBar. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ CLEARTICS**](tbm-cleartics.md)               | Rimuove i segni di graduazione correnti da un TrackBar. Questo messaggio non rimuove il primo e l'ultimo segno di graduazione, che vengono creati automaticamente dal TrackBar. <br/>                                                                                                                                           |
| [**TBM \_ GETbuddy**](tbm-getbuddy.md)                 | Recupera l'handle a una finestra buddy del controllo TrackBar in una posizione specificata. La posizione specificata è relativa all'orientamento del controllo (orizzontale o verticale). <br/>                                                                                                                                 |
| [**TBM \_ GETCHANNELRECT**](tbm-getchannelrect.md)     | Recupera le dimensioni e la posizione del rettangolo di delimitazione per il canale di un TrackBar. (Il canale è l'area in cui viene spostato il dispositivo di scorrimento. Contiene l'evidenziazione quando viene selezionato un intervallo. <br/>                                                                                                         |
| [**TBM \_ GETLINESIZE**](tbm-getlinesize.md)           | Recupera il numero di posizioni logiche spostate dal dispositivo di scorrimento del TrackBar in risposta all'input da tastiera dei tasti di direzione, ad esempio i tasti o. Le posizioni logiche sono gli incrementi interi nell'intervallo compreso tra minimo e massimo per le posizioni del dispositivo di scorrimento. <br/>                                         |
| [**TBM \_ GETNUMTICS**](tbm-getnumtics.md)             | Recupera il numero di segni di graduazione in un TrackBar. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETpagesize**](tbm-getpagesize.md)           | Recupera il numero di posizioni logiche spostate dal dispositivo di scorrimento di TrackBar in risposta all'input da tastiera, ad esempio le chiavi o o l'input del mouse, ad esempio i clic nel canale del TrackBar. Le posizioni logiche sono gli incrementi interi nell'intervallo compreso tra minimo e massimo per le posizioni del dispositivo di scorrimento. <br/>   |
| [**TBM \_ GETPOS**](tbm-getpos.md)                     | Recupera la posizione logica corrente del dispositivo di scorrimento in un TrackBar. Le posizioni logiche sono i valori integer nell'intervallo tra le posizioni minime e massime del dispositivo di scorrimento. <br/>                                                                                                                       |
| [**TBM \_ GETPTICS**](tbm-getptics.md)                 | Recupera l'indirizzo di una matrice che contiene le posizioni dei segni di graduazione per un TrackBar. <br/>                                                                                                                                                                                                        |
| [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md)           | Recupera la posizione massima per il dispositivo di scorrimento in un TrackBar. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md)           | Recupera la posizione minima del dispositivo di scorrimento in un TrackBar. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETselend**](tbm-getselend.md)               | Recupera la posizione finale dell'intervallo di selezione corrente in un TrackBar. <br/>                                                                                                                                                                                                                            |
| [**TBM \_ GETSELSTART**](tbm-getselstart.md)           | Recupera la posizione iniziale dell'intervallo di selezione corrente in un TrackBar. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md)     | Recupera la lunghezza del dispositivo di scorrimento in un TrackBar. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETTHUMBRECT**](tbm-getthumbrect.md)         | Recupera le dimensioni e la posizione del rettangolo di delimitazione per il dispositivo di scorrimento in un TrackBar. <br/>                                                                                                                                                                                                                |
| [**\_Getter TBM**](tbm-gettic.md)                     | Recupera la posizione logica di un segno di graduazione in un TrackBar. La posizione logica può essere uno qualsiasi dei valori integer nell'intervallo compreso tra le posizioni minime e massime del dispositivo di scorrimento. <br/>                                                                                                                     |
| [**TBM \_ GETTICPOS**](tbm-getticpos.md)               | Recupera la posizione fisica corrente di un segno di graduazione in un TrackBar.<br/>                                                                                                                                                                                                                                   |
| [**\_GETtooltips TBM**](tbm-gettooltips.md)           | Recupera l'handle per il controllo ToolTip assegnato a TrackBar, se presente. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETUNICODEFORMAT**](tbm-getunicodeformat.md) | Recupera il flag del formato carattere Unicode per il controllo. <br/>                                                                                                                                                                                                                                           |
| [**seBuddy TBM \_**](tbm-setbuddy.md)                 | Assegna una finestra come finestra di Buddy per un controllo TrackBar. Le finestre del contatto TrackBar vengono visualizzate automaticamente in un percorso relativo all'orientamento del controllo (orizzontale o verticale). <br/>                                                                                                          |
| [**TBM \_ SETLINESIZE**](tbm-setlinesize.md)           | Imposta il numero di posizioni logiche spostate dal dispositivo di scorrimento di TrackBar in risposta all'input da tastiera dei tasti di direzione, ad esempio i tasti o. Le posizioni logiche sono gli incrementi interi nell'intervallo compreso tra minimo e massimo per le posizioni del dispositivo di scorrimento. <br/>                                              |
| [**sepagesize TBM \_**](tbm-setpagesize.md)           | Imposta il numero di posizioni logiche spostate dal dispositivo di scorrimento di TrackBar in risposta all'input da tastiera, ad esempio le chiavi o o l'input del mouse, ad esempio i clic nel canale del TrackBar. Le posizioni logiche sono gli incrementi interi nell'intervallo compreso tra minimo e massimo per le posizioni del dispositivo di scorrimento. <br/>        |
| [**TBM \_ SETPOS**](tbm-setpos.md)                     | Imposta la posizione logica corrente del dispositivo di scorrimento in un TrackBar. <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SETPOSNOTIFY**](tbm-setposnotify.md)         | Imposta la posizione logica corrente del dispositivo di scorrimento in un TrackBar. <br/>                                                                                                                                                                                                                                         |
| [**\_SEtrange TBM**](tbm-setrange.md)                 | Imposta l'intervallo di posizioni logiche minime e massime per il dispositivo di scorrimento in un TrackBar. <br/>                                                                                                                                                                                                                  |
| [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)           | Imposta la posizione logica massima per il dispositivo di scorrimento in un TrackBar. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)           | Imposta la posizione logica minima per il dispositivo di scorrimento in un TrackBar. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETSEL**](tbm-setsel.md)                     | Imposta le posizioni iniziale e finale per l'intervallo di selezione disponibile in un TrackBar. <br/>                                                                                                                                                                                                                |
| [**\_SEselend TBM**](tbm-setselend.md)               | Imposta la posizione logica finale dell'intervallo di selezione corrente in un TrackBar. Questo messaggio viene ignorato se il TrackBar non ha lo stile [**\_ ENABLESELRANGE di TBS**](trackbar-control-styles.md) . <br/>                                                                              |
| [**TBM \_ SETSELSTART**](tbm-setselstart.md)           | Imposta la posizione logica iniziale dell'intervallo di selezione corrente in un TrackBar. Questo messaggio viene ignorato se il TrackBar non ha lo stile [**\_ ENABLESELRANGE di TBS**](trackbar-control-styles.md) . <br/>                                                                            |
| [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md)     | Imposta la lunghezza del dispositivo di scorrimento in un TrackBar. Questo messaggio viene ignorato se il TrackBar non ha lo stile [**\_ FIXEDLENGTH di TBS**](trackbar-control-styles.md) . <br/>                                                                                                                      |
| [**TBM \_ SETTIC**](tbm-settic.md)                     | Imposta un segno di graduazione in un TrackBar nella posizione logica specificata. <br/>                                                                                                                                                                                                                                      |
| [**TBM \_ SETTICFREQ**](tbm-setticfreq.md)             | Imposta la frequenza di intervallo per i segni di graduazione in un TrackBar. Se, ad esempio, la frequenza è impostata su due, viene visualizzato un segno di graduazione per ogni altro incremento nell'intervallo del TrackBar. L'impostazione predefinita per la frequenza è uno; ovvero ogni incremento nell'intervallo è associato a un segno di graduazione. <br/> |
| [**TBM \_ SETTIPSIDE**](tbm-settipside.md)             | Posiziona un controllo ToolTip utilizzato da un controllo TrackBar. I controlli TrackBar che usano le descrizioni comandi di [**TBS \_**](trackbar-control-styles.md) visualizzano le descrizioni comandi. <br/>                                                                                                                           |
| [**\_descrizioni comando TBM**](tbm-settooltips.md)           | Assegna un controllo ToolTip a un controllo TrackBar. <br/>                                                                                                                                                                                                                                                       |
| [**TBM \_ SETUNICODEFORMAT**](tbm-setunicodeformat.md) | Imposta il flag di formato carattere Unicode per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo. <br/>                                                                                                               |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                              | Contenuto                                                                                                                                                                                      |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_CUSTOMDRAW Nm (TrackBar)](nm-customdraw-trackbar.md)            | Inviato da un controllo TrackBar per notificare alle finestre padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>        |
| [\_RELEASEDCAPTURE Nm (TrackBar)](nm-releasedcapture-trackbar-.md) | Notifica alla finestra padre di un controllo TrackBar che il controllo sta rilasciando l'acquisizione del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/> |
| [\_THUMBPOSCHANGING Trbn](trbn-thumbposchanging.md)                | Notifica che la posizione del cursore in un controllo TrackBar sta cambiando. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                               |



 

### <a name="constants"></a>Costanti



| Argomento                                                  | Contenuto                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Valori di estrazione personalizzati](custom-draw-values.md)           | In questa sezione vengono elencati i valori utilizzati per identificare le parti di un controllo TrackBar. <br/>      |
| [Stili del controllo TrackBar](trackbar-control-styles.md) | Questa sezione contiene informazioni sugli stili usati con i controlli TrackBar. <br/> |



 

 

 





