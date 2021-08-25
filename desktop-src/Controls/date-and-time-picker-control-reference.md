---
title: Selezione data e ora
description: Questa sezione contiene informazioni sugli elementi DELL'API usati con i controlli selezione data e ora.
ms.assetid: vs|controls|~\controls\datetime\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd4dd1b29aa1bf7552b87f18a9ded05b67fc8e47770c01431af4da897f2b9733
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929481"
---
# <a name="date-and-time-picker"></a>Selezione data e ora

Questa sezione contiene informazioni sugli elementi DELL'API usati con i controlli selezione data e ora.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                                                    | Contenuto                                                                                                                                                     |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sui controlli selezione data e ora](date-and-time-picker-controls.md) | Un controllo di selezione data e ora *(DTP)* offre un'interfaccia semplice e intuitiva tramite la quale scambiare informazioni di data e ora con un utente.<br/> |
| [Uso dei controlli selezione data e ora](using-date-and-time-picker.md)    | In questa sezione vengono fornite informazioni e codice di esempio per l'implementazione di controlli selezione data e ora. <br/>                                                |



 

### <a name="macros"></a>Macro



| Argomento                                                                     | Contenuto                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)                 | Chiude il controllo selezione data e ora (DTP). Usare questa macro o inviare il [**messaggio DTM \_ CLOSEMONTHCAL**](dtm-closemonthcal.md) in modo esplicito.<br/>                                                                                                                     |
| [**DateTime \_ GetDateTimePickerInfo**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getdatetimepickerinfo) | Ottiene informazioni per un controllo DTP (Date and Time Picker) specificato.<br/>                                                                                                                                                                                              |
| [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize)                   | Ottiene le dimensioni necessarie per visualizzare il controllo senza ritaglio. Usare questa macro o inviare il [**messaggio DTM \_ GETIDEALSIZE in**](dtm-getidealsize.md) modo esplicito.<br/>                                                                                                        |
| [**\_GetMonthCal di DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal)                     | Ottiene l'handle per un controllo calendario mensile figlio (DTP) di una selezione data e ora. È possibile usare questa macro o inviare il [**messaggio DTM \_ GETMONTHCAL**](dtm-getmonthcal.md) in modo esplicito. <br/>                                                                               |
| [**GetMonthCalColor di DateTime \_**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor)           | Ottiene il colore per una determinata parte del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile usare questa macro o inviare il [**messaggio \_ DTM GETMCCOLOR**](dtm-getmccolor.md) in modo esplicito. <br/>                                                           |
| [**GetMonthCalFont di DateTime \_**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont)             | Ottiene il tipo di carattere attualmente utilizzato dal controllo calendario mensile figlio del controllo selezione data e ora (DTP). È possibile usare questa macro o inviare il [**messaggio \_ DTM GETMCFONT in**](dtm-getmcfont.md) modo esplicito. <br/>                                                      |
| [**\_GetMonthCalStyle di DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle)           | Ottiene lo stile di un controllo DTP specificato. Usare questa macro o inviare il messaggio [**DTM \_ GETMCSTYLE**](dtm-getmcstyle.md) in modo esplicito.<br/>                                                                                                                               |
| [**DateTime \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange)                           | Ottiene le ore di sistema minime e massime consentite correnti per un controllo di selezione data e ora (DTP). È possibile usare questa macro o inviare il [**messaggio \_ DTM GETRANGE**](dtm-getrange.md) in modo esplicito. <br/>                                                              |
| [**DateTime \_ GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime)                 | Ottiene l'ora attualmente selezionata da un controllo di selezione data e ora (DTP) e la inserisce in una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) specificata. È possibile usare questa macro o inviare il [**messaggio DTM \_ GETSYSTEMTIME**](dtm-getsystemtime.md) in modo esplicito. <br/> |
| [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat)                         | Imposta la visualizzazione di un controllo di selezione data e ora (DTP) in base a una determinata stringa di formato. È possibile usare questa macro o inviare il [**messaggio DTM \_ SETFORMAT in**](dtm-setformat.md) modo esplicito. <br/>                                                                          |
| [**\_SetMonthCalColor di DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor)           | Imposta il colore per una determinata parte del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile usare questa macro o inviare il [**messaggio DTM \_ SETMCCOLOR**](dtm-setmccolor.md) in modo esplicito. <br/>                                                           |
| [**\_SetMonthCalFont di DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont)             | Imposta il tipo di carattere che deve essere utilizzato dal controllo calendario mensile figlio del controllo selezione data e ora (DTP). È possibile usare questa macro o inviare in modo esplicito il [**messaggio DTM \_ SETMCFONT.**](dtm-setmcfont.md) <br/>                                                                |
| [**\_SetMonthCalStyle di DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle)           | Imposta lo stile per un controllo DTP specificato. Usare questa macro o inviare il [**messaggio DTM \_ SETMCSTYLE**](dtm-setmcstyle.md) in modo esplicito.<br/>                                                                                                                              |
| [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange)                           | Imposta le ore di sistema minime e massime consentite per un controllo di selezione data e ora (DTP). È possibile usare questa macro o inviare il [**messaggio DTM \_ SETRANGE**](dtm-setrange.md) in modo esplicito. <br/>                                                                       |
| [**DateTime \_ SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime)                 | Imposta un controllo di selezione data e ora (DTP) su una determinata data e ora. È possibile usare questa macro o inviare il [**messaggio DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md) in modo esplicito. <br/>                                                                                       |



 

### <a name="messages"></a>Messaggi



| Argomento                                                           | Contenuto                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DTM \_ CLOSEMONTHCAL**](dtm-closemonthcal.md)                 | Chiude un controllo DTP. Inviare questo messaggio in modo esplicito o usando la macro [**\_ DateTime CloseMonthCal.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)<br/>                                                                                                                                        |
| [**DTM \_ GETDATETIMEPICKERINFO**](dtm-getdatetimepickerinfo.md) | Ottiene informazioni su un controllo selezione data e ora (DTP).<br/>                                                                                                                                                                                                                  |
| [**DTM \_ GETIDEALSIZE**](dtm-getidealsize.md)                   | Ottiene le dimensioni necessarie per visualizzare il controllo senza ritaglio. Inviare questo messaggio in modo esplicito o usando la macro [**\_ DateTime GetIdealSize.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize)<br/>                                                                                                  |
| [**DTM \_ GETMCCOLOR**](dtm-getmccolor.md)                       | Ottiene il colore per una determinata parte del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime GetMonthCalColor.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) <br/>                                              |
| [**DTM \_ GETMCFONT**](dtm-getmcfont.md)                         | Ottiene il tipo di carattere attualmente utilizzato dal controllo calendario mensile figlio del controllo selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime GetMonthCalFont.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) <br/>                                         |
| [**DTM \_ GETMCSTYLE**](dtm-getmcstyle.md)                       | Ottiene lo stile di un controllo DTP. Inviare questo messaggio in modo esplicito o usando la macro [**\_ DateTime GetMonthCalStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle)<br/>                                                                                                                       |
| [**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)                     | Ottiene l'handle per un controllo calendario mensile figlio (DTP) di una selezione data e ora. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime GetMonthCal.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) <br/>                                                                              |
| [**DTM \_ GETRANGE**](dtm-getrange.md)                           | Ottiene le ore di sistema minime e massime consentite correnti per un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime GetRange.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) <br/>                                                              |
| [**DTM \_ GETSYSTEMTIME**](dtm-getsystemtime.md)                 | Ottiene l'ora attualmente selezionata da un controllo di selezione data e ora (DTP) e la inserisce in una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) specificata. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime GetSystemtime.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) <br/> |
| [**DTM \_ SETFORMAT**](dtm-setformat.md)                         | Imposta la visualizzazione di un controllo di selezione data e ora (DTP) in base a una determinata stringa di formato. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime SetFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) <br/>                                                                         |
| [**DTM \_ SETMCCOLOR**](dtm-setmccolor.md)                       | Imposta il colore per una determinata parte del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime SetMonthCalColor.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) <br/>                                              |
| [**DTM \_ SETMCFONT**](dtm-setmcfont.md)                         | Imposta il tipo di carattere che deve essere utilizzato dal controllo calendario mensile figlio del controllo selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime SetMonthCalFont.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont)<br/>                                                    |
| [**DTM \_ SETMCSTYLE**](dtm-setmcstyle.md)                       | Imposta lo stile di un controllo DTP. Inviare questo messaggio in modo esplicito o usando la macro [**\_ DateTime SetMonthCalStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle)<br/>                                                                                                                       |
| [**DTM \_ SETRANGE**](dtm-setrange.md)                           | Imposta le ore di sistema minime e massime consentite per un controllo di selezione data e ora. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime SetRange.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) <br/>                                                                      |
| [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md)                 | Imposta l'ora in un controllo di selezione data e ora . È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime SetSystemtime.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) <br/>                                                                                                   |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                   | Contenuto                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PRIMO PIANO \_ DTN](dtn-closeup.md)                         | Inviato da un controllo di selezione data e ora quando l'utente chiude il calendario mensile a discesa. Il calendario mensile viene chiuso quando l'utente sceglie una data dal calendario mensile o fa clic sulla freccia a discesa mentre il calendario è aperto. <br/>                                                                                                      |
| [DTN \_ DATETIMECHANGE](dtn-datetimechange.md)           | Inviato da un controllo di selezione data e ora ogni volta che si verifica una modifica. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                                                                                  |
| [ELENCO A DISCESA \_ DTN](dtn-dropdown.md)                       | Inviato da un controllo di selezione data e ora quando l'utente attiva il calendario mensile a discesa. <br/>                                                                                                                                                                                                                                               |
| [FORMATO \_ DTN](dtn-format.md)                           | Inviato da un controllo di selezione data e ora (DTP) per richiedere la visualizzazione del testo in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                                                       |
| [DTN \_ FORMATQUERY](dtn-formatquery.md)                 | Inviato da un controllo di selezione data e ora (DTP) per recuperare le dimensioni massime consentite della stringa che verrà visualizzata in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                           |
| [DTN \_ USERSTRING](dtn-userstring.md)                   | Inviato da un controllo di selezione data e ora quando un utente completa la modifica di una stringa nel controllo. Questo codice di notifica viene inviato solo dai controlli DTP impostati sullo stile [**\_ APPCANPARSE DTS.**](date-and-time-picker-control-styles.md) Questo messaggio viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/> |
| [DTN \_ WMKEYDOWN](dtn-wmkeydown.md)                     | Inviato da un controllo di selezione data e ora (DTP) quando l'utente digitare in un campo di callback. Questo messaggio viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                                                                             |
| [NM \_ KILLFOCUS (data e ora)](nm-killfocus-date-time.md) | Notifica alla finestra padre di un controllo selezione data e ora che il controllo ha perso lo stato attivo per l'input. [**NM \_ KILLFOCUS (data e ora)**](nm-killfocus-date-time.md) viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                 |
| [NM \_ SETFOCUS (data e ora)](nm-setfocus-date-time-.md)  | Notifica alla finestra padre di un controllo selezione data e ora che il controllo ha ricevuto lo stato attivo per l'input. [NM \_ SETFOCUS (data e ora)](nm-setfocus-date-time-.md) viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                  |



 

### <a name="structures"></a>Strutture



| Argomento                                                  | Contenuto                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATETIMEPICKERINFO**](/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo)       | Contiene informazioni su un controllo DTP. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange)           | Contiene informazioni su una modifica apportata in un controllo di selezione data e ora . Questa struttura viene utilizzata con il [codice di notifica \_ DTN DATETIMECHANGE.](dtn-datetimechange.md) <br/>                                                                                                                                                                                     |
| [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata)           | Contiene informazioni su una parte della stringa di formato che definisce un campo di callback all'interno di un controllo di selezione data e ora . Contiene la sottostringa che definisce il campo di callback e contiene un buffer per ricevere la stringa che verrà visualizzata nel campo di callback. Questa struttura viene utilizzata con il [codice di notifica DTN \_ FORMAT.](dtn-format.md) <br/>               |
| [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) | Contiene informazioni su un campo di callback del controllo selezione data e ora (DTP). Contiene una sottostringa (tratta dalla stringa di formato del controllo) che definisce un campo di callback. La struttura riceve la dimensione massima consentita del testo che verrà visualizzato nel campo callback. Questa struttura viene utilizzata con il [codice di notifica \_ DTN FORMATQUERY.](dtn-formatquery.md) <br/> |
| [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa)           | Contiene informazioni specifiche di un'operazione di modifica eseguita in un controllo di selezione data e ora . Questo messaggio viene usato con il [codice di notifica \_ DTN USERSTRING.](dtn-userstring.md) <br/>                                                                                                                                                                                |
| [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna)     | Contiene le informazioni usate per descrivere e gestire un [codice di notifica \_ WMKEYDOWN DTN.](dtn-wmkeydown.md) <br/>                                                                                                                                                                                                                                                                               |



 

### <a name="constants"></a>Costanti



| Argomento                                                                          | Contenuto                                                                                |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Stili del controllo Selezione data e ora](date-and-time-picker-control-styles.md) | Gli stili della finestra elencati di seguito sono specifici dei controlli selezione data e ora.<br/> |



 

 

