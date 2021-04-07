---
title: Selezione data e ora
description: Questa sezione contiene informazioni sugli elementi API utilizzati con i controlli selezione data e ora.
ms.assetid: vs|controls|~\controls\datetime\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4e91b325b798ff465d8048cac2f0a9a72e5774
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103873038"
---
# <a name="date-and-time-picker"></a>Selezione data e ora

Questa sezione contiene informazioni sugli elementi API utilizzati con i controlli selezione data e ora.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                                                    | Contenuto                                                                                                                                                     |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sui controlli selezione data e ora](date-and-time-picker-controls.md) | Un *controllo di selezione data e ora (DTP)* fornisce un'interfaccia semplice e intuitiva tramite la quale scambiare le informazioni di data e ora con un utente.<br/> |
| [Uso di controlli selezione data e ora](using-date-and-time-picker.md)    | In questa sezione vengono fornite informazioni e codice di esempio per l'implementazione di controlli selezione data e ora. <br/>                                                |



 

### <a name="macros"></a>Macro



| Argomento                                                                     | Contenuto                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CloseMonthCal DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)                 | Chiude il controllo di selezione data e ora (DTP). Usare questa macro o inviare il [**messaggio \_ CLOSEMONTHCAL di DTM**](dtm-closemonthcal.md) in modo esplicito.<br/>                                                                                                                     |
| [**\_GetDateTimePickerInfo DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getdatetimepickerinfo) | Ottiene informazioni per un controllo di selezione data e ora specificato (DTP).<br/>                                                                                                                                                                                              |
| [**\_GetIdealSize DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize)                   | Ottiene le dimensioni necessarie per visualizzare il controllo senza ritagliare. Usare questa macro o inviare il [**messaggio \_ GETIDEALSIZE di DTM**](dtm-getidealsize.md) in modo esplicito.<br/>                                                                                                        |
| [**\_GetMonthCal DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal)                     | Ottiene l'handle per un controllo calendario mensile figlio (DTP) di selezione data e ora. È possibile usare questa macro o inviare il [**messaggio \_ GETMONTHCAL di DTM**](dtm-getmonthcal.md) in modo esplicito. <br/>                                                                               |
| [**\_GetMonthCalColor DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor)           | Ottiene il colore per una porzione specificata del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile usare questa macro o inviare il [**messaggio \_ GETMCCOLOR di DTM**](dtm-getmccolor.md) in modo esplicito. <br/>                                                           |
| [**\_GetMonthCalFont DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont)             | Ottiene il tipo di carattere attualmente utilizzato dal controllo Calendar Month del controllo di selezione data e ora (DTP). È possibile usare questa macro o inviare il [**messaggio \_ GETMCFONT di DTM**](dtm-getmcfont.md) in modo esplicito. <br/>                                                      |
| [**\_GetMonthCalStyle DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle)           | Ottiene lo stile di un controllo DTP specificato. Usare questa macro o inviare il [**messaggio \_ GETMCSTYLE di DTM**](dtm-getmcstyle.md) in modo esplicito.<br/>                                                                                                                               |
| [**\_Intervallo di valori DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange)                           | Ottiene l'ora di sistema corrente minima e massima consentita per un controllo di selezione data e ora (DTP). È possibile usare questa macro o inviare in modo esplicito il messaggio [**DTM \_ GetRange**](dtm-getrange.md) . <br/>                                                              |
| [**\_GetSystemtime DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime)                 | Ottiene l'ora attualmente selezionata da un controllo di selezione data e ora (DTP) e la inserisce in una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) specificata. È possibile usare questa macro o inviare il messaggio [**\_ GETSYSTEMTIME di DTM**](dtm-getsystemtime.md) in modo esplicito. <br/> |
| [**DateTime- \_ formato**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat)                         | Imposta la visualizzazione di un controllo di selezione data e ora (DTP) in base a una stringa di formato specificata. È possibile usare questa macro o inviare in modo esplicito il messaggio di [**\_ seformazione DTM**](dtm-setformat.md) . <br/>                                                                          |
| [**\_SetMonthCalColor DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor)           | Imposta il colore per una porzione specificata del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile usare questa macro o inviare il [**messaggio \_ SETMCCOLOR di DTM**](dtm-setmccolor.md) in modo esplicito. <br/>                                                           |
| [**\_SetMonthCalFont DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont)             | Imposta il tipo di carattere che verrà utilizzato dal controllo Calendar Month Child del controllo di selezione data e ora (DTP). È possibile usare questa macro o inviare in modo esplicito il messaggio [**\_ SETMCFONT di DTM**](dtm-setmcfont.md) . <br/>                                                                |
| [**\_SetMonthCalStyle DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle)           | Imposta lo stile per un controllo DTP specificato. Usare questa macro o inviare il [**messaggio \_ SETMCSTYLE di DTM**](dtm-setmcstyle.md) in modo esplicito.<br/>                                                                                                                              |
| [**\_Intervallo di valori DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange)                           | Imposta l'ora di sistema minima e massima consentita per un controllo di selezione data e ora (DTP). È possibile usare questa macro o inviare il messaggio di [**\_ SetRange DTM**](dtm-setrange.md) in modo esplicito. <br/>                                                                       |
| [**\_SetSystemtime DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime)                 | Imposta un controllo di selezione data e ora (DTP) su una data e un'ora specificate. È possibile usare questa macro o inviare il [**messaggio \_ SETSYSTEMTIME di DTM**](dtm-setsystemtime.md) in modo esplicito. <br/>                                                                                       |



 

### <a name="messages"></a>Messaggi



| Argomento                                                           | Contenuto                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CLOSEMONTHCAL DTM**](dtm-closemonthcal.md)                 | Chiude un controllo DTP. Inviare questo messaggio in modo esplicito o utilizzando la macro [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) .<br/>                                                                                                                                        |
| [**\_GETDATETIMEPICKERINFO DTM**](dtm-getdatetimepickerinfo.md) | Ottiene informazioni su un controllo di selezione data e ora (DTP).<br/>                                                                                                                                                                                                                  |
| [**\_GETIDEALSIZE DTM**](dtm-getidealsize.md)                   | Ottiene le dimensioni necessarie per visualizzare il controllo senza ritagliare. Inviare questo messaggio in modo esplicito o utilizzando la macro [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) .<br/>                                                                                                  |
| [**\_GETMCCOLOR DTM**](dtm-getmccolor.md)                       | Ottiene il colore per una porzione specificata del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) . <br/>                                              |
| [**\_GETMCFONT DTM**](dtm-getmcfont.md)                         | Ottiene il tipo di carattere attualmente utilizzato dal controllo Calendar Month del controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) . <br/>                                         |
| [**\_GETMCSTYLE DTM**](dtm-getmcstyle.md)                       | Ottiene lo stile di un controllo DTP. Inviare questo messaggio in modo esplicito o utilizzando la macro [**DateTime \_ GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) .<br/>                                                                                                                       |
| [**\_GETMONTHCAL DTM**](dtm-getmonthcal.md)                     | Ottiene l'handle per un controllo calendario mensile figlio (DTP) di selezione data e ora. È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) . <br/>                                                                              |
| [**DTM \_ GETrange**](dtm-getrange.md)                           | Ottiene l'ora di sistema corrente minima e massima consentita per un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) . <br/>                                                              |
| [**\_GETSYSTEMTIME DTM**](dtm-getsystemtime.md)                 | Ottiene l'ora attualmente selezionata da un controllo di selezione data e ora (DTP) e la inserisce in una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) specificata. È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) . <br/> |
| [**\_formato DTM**](dtm-setformat.md)                         | Imposta la visualizzazione di un controllo di selezione data e ora (DTP) in base a una stringa di formato specificata. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**DateTime \_ seformatt**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) . <br/>                                                                         |
| [**\_SETMCCOLOR DTM**](dtm-setmccolor.md)                       | Imposta il colore per una porzione specificata del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) . <br/>                                              |
| [**\_SETMCFONT DTM**](dtm-setmcfont.md)                         | Imposta il tipo di carattere che verrà utilizzato dal controllo Calendar Month Child del controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) .<br/>                                                    |
| [**\_SETMCSTYLE DTM**](dtm-setmcstyle.md)                       | Imposta lo stile di un controllo DTP. Inviare questo messaggio in modo esplicito o utilizzando la macro [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) .<br/>                                                                                                                       |
| [**\_SEtrange DTM**](dtm-setrange.md)                           | Imposta l'ora di sistema minima e massima consentita per un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) . <br/>                                                                      |
| [**\_SETSYSTEMTIME DTM**](dtm-setsystemtime.md)                 | Imposta l'ora in un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) . <br/>                                                                                                   |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                   | Contenuto                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [primo piano DTN \_](dtn-closeup.md)                         | Inviato da un controllo di selezione data e ora (DTP) quando l'utente chiude il calendario mensile a discesa. Il calendario mensile viene chiuso quando l'utente sceglie una data del calendario mensile o fa clic sulla freccia a discesa mentre il calendario è aperto. <br/>                                                                                                      |
| [\_DATETIMECHANGE DTN](dtn-datetimechange.md)           | Inviato da un controllo di selezione data e ora (DTP) ogni volta che viene apportata una modifica. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                                                                                  |
| [\_elenco a discesa DTN](dtn-dropdown.md)                       | Inviato da un controllo di selezione data e ora (DTP) quando l'utente attiva il calendario mensile a discesa. <br/>                                                                                                                                                                                                                                               |
| [\_formato DTN](dtn-format.md)                           | Inviato da un controllo di selezione data e ora (DTP) per richiedere il testo da visualizzare in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                                                       |
| [\_FORMATQUERY DTN](dtn-formatquery.md)                 | Inviato da un controllo di selezione data e ora (DTP) per recuperare la dimensione massima consentita della stringa che verrà visualizzata in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                           |
| [\_USERSTRING DTN](dtn-userstring.md)                   | Inviato da un controllo di selezione data e ora (DTP) quando un utente completa la modifica di una stringa nel controllo. Questo codice di notifica viene inviato solo dai controlli DTP impostati sullo stile [**DTS \_ APPCANPARSE**](date-and-time-picker-control-styles.md) . Questo messaggio viene inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) . <br/> |
| [\_WMKEYDOWN DTN](dtn-wmkeydown.md)                     | Inviato da un controllo di selezione data e ora (DTP) quando l'utente digita in un campo di callback. Questo messaggio viene inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) . <br/>                                                                                                                                                                             |
| [NM \_ KILLFOCUS (data/ora)](nm-killfocus-date-time.md) | Notifica alla finestra padre di un controllo selezione data e ora che il controllo ha perso lo stato attivo per l'input. [**Nm \_ KILLFOCUS (data/ora)**](nm-killfocus-date-time.md) viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                 |
| [\_Stato SetFocus di Nm (data/ora)](nm-setfocus-date-time-.md)  | Notifica alla finestra padre di un controllo selezione data e ora che il controllo ha ricevuto lo stato attivo per l'input. [Nm \_ SetFocus (data/ora)](nm-setfocus-date-time-.md) viene inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) . <br/>                                                                                                                  |



 

### <a name="structures"></a>Strutture



| Argomento                                                  | Contenuto                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATETIMEPICKERINFO**](/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo)       | Contiene informazioni su un controllo DTP. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange)           | Contiene informazioni su una modifica effettuata in un controllo di selezione data e ora (DTP). Questa struttura viene utilizzata con il codice di notifica [ \_ DATETIMECHANGE di DTN](dtn-datetimechange.md) . <br/>                                                                                                                                                                                     |
| [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata)           | Contiene informazioni su una parte della stringa di formato che definisce un campo di callback in un controllo di selezione data e ora (DTP). Contiene la sottostringa che definisce il campo di callback e contiene un buffer per ricevere la stringa che verrà visualizzata nel campo callback. Questa struttura viene utilizzata con il codice di notifica del [ \_ formato DTN](dtn-format.md) . <br/>               |
| [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) | Contiene informazioni su un campo di callback del controllo DTP (data e ora). Contiene una sottostringa (tratto dalla stringa di formato del controllo) che definisce un campo di callback. La struttura riceve la dimensione massima consentita del testo che verrà visualizzato nel campo callback. Questa struttura viene utilizzata con il codice di notifica [ \_ FORMATQUERY di DTN](dtn-formatquery.md) . <br/> |
| [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa)           | Contiene informazioni specifiche di un'operazione di modifica che si è verificata in un controllo di selezione data e ora (DTP). Questo messaggio viene usato con il codice di notifica [ \_ USERSTRING di DTN](dtn-userstring.md) . <br/>                                                                                                                                                                                |
| [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna)     | Trasporta le informazioni utilizzate per descrivere e gestire un codice di notifica [ \_ WMKEYDOWN DTN](dtn-wmkeydown.md) . <br/>                                                                                                                                                                                                                                                                               |



 

### <a name="constants"></a>Costanti



| Argomento                                                                          | Contenuto                                                                                |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Stili del controllo selezione data e ora](date-and-time-picker-control-styles.md) | Gli stili della finestra elencati di seguito sono specifici dei controlli selezione data e ora.<br/> |



 

 

