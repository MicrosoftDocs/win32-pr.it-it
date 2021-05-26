---
title: Informazioni sui controlli selezione data e ora
description: Un controllo di selezione data e ora (DTP) offre un'interfaccia semplice e intuitiva tramite la quale scambiare informazioni di data e ora con un utente.
ms.assetid: 6749c3ae-2c52-4183-ac4e-68ca7ebf1e13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182381c40b636683255e95ba0680a1245ef0adf3
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424221"
---
# <a name="about-date-and-time-picker-controls"></a>Informazioni sui controlli selezione data e ora

Un controllo di selezione data e ora *(DTP)* offre un'interfaccia semplice e intuitiva tramite la quale scambiare informazioni di data e ora con un utente. Ad esempio, con un controllo DTP è possibile chiedere all'utente di immettere una data e quindi recuperare facilmente la selezione.

Vengono trattati i seguenti argomenti:

-   [Selezione data e ora Interfaccia utente](#date-and-time-picker-user-interface)
-   [Stili e formati del controllo Selezione data e ora](#date-and-time-picker-control-styles-and-formats)
    -   [Formati predefiniti](#preset-formats)
    -   [Formati personalizzati](#custom-formats)
    -   [Stringhe di formato](#format-strings)
    -   [Campi di callback](#callback-fields)
-   [Messaggi di notifica del controllo Selezione data e ora](#date-and-time-picker-control-notification-messages)
-   [Argomenti correlati](#related-topics)

> [!Note]
> Windows non supporta date precedenti alla 1601. Per informazioni [**dettagliate, vedere**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) la struttura FILETIME.
>
> Il controllo è basato sul calendario gregoriano, introdotto nel 1753. Non calcola le date coerenti con il calendario giuliano.

## <a name="date-and-time-picker-user-interface"></a>Selezione data e ora Interfaccia utente

L'area client di un controllo di selezione data e ora (DTP) visualizza informazioni su data o ora o su entrambi e funge da interfaccia tramite la quale gli utenti modificano le informazioni. La data può essere selezionata da un calendario o usando un controllo up-down. L'ora può essere modificata digitando nei campi definiti dalle stringhe di formato [del controllo](#format-strings). Facoltativamente, il controllo visualizza una casella di controllo. Quando viene selezionato, è possibile recuperare il valore nel controllo . In caso contrario, il controllo viene considerato non inizializzato.

La figura seguente mostra una finestra che contiene tre controlli selezione data. Il primo controllo selezione data è stato creato con lo stile [**DTS \_ SHOWNONE,**](date-and-time-picker-control-styles.md) il secondo con lo stile [**\_ UPDOWN DTS**](date-and-time-picker-control-styles.md) e il terzo senza stili speciali. Nel terzo controllo l'utente ha fatto clic sulla freccia giù per visualizzare il calendario.

![Screenshot di una finestra che illustra tre stili dei controlli selezione data](images/dtpdatepick.png)

La figura seguente mostra una finestra con tre controlli che contengono l'ora.

Il primo controllo è stato creato con lo stile [**\_ TIMEFORMAT DTS**](date-and-time-picker-control-styles.md) e mostra l'ora nell'ora predefinita, costituita da quattro campi. L'utente può digitare un valore valido in uno di questi campi oppure selezionare il campo e modificare il valore usando il controllo verso l'alto o i tasti di direzione.

Il secondo controllo mostra un formato personalizzato impostato usando [**DateTime \_ SetFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) Come per il primo controllo, l'utente può modificare i campi dell'ora digitando o usando i tasti di direzione. Il giorno della settimana può essere modificato selezionando una data dal calendario che si apre quando l'utente fa clic sulla freccia giù.

Il terzo controllo mostra come è possibile aggiungere testo arbitrario al controllo. L'utente può selezionare un'ora (da 1 a 24) digitando, usando i tasti di direzione o usando il controllo di scorrimento.

![Screenshot di una finestra che mostra tre controlli che contengono l'ora](images/dtpdatetimepick.png)

Il controllo DTP aggiorna automaticamente le informazioni interne in base all'input dell'utente. Il controllo riconosce quanto segue come input valido.



| Categoria di input | Descrizione                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tasti di direzione     | Il controllo accetta i tasti di direzione per spostarsi tra i campi nel controllo e modificare i valori. L'utente può premere i tasti o per spostarsi nel controllo Se l'utente tenta di spostarsi oltre l'ultimo campo in una determinata direzione, lo stato attivo della tastiera "va a capo" nel campo sul lato opposto del controllo. Le chiavi e modificano i valori nel campo corrente in modo incrementale. |
| Fine e home page   | Il controllo accetta le chiavi virtuali VK END e VK HOME per modificare rispettivamente il valore all'interno del campo corrente e i limiti superiore \_ \_ e inferiore.                                                                                                                                                                                                                          |
| Tasti funzione  | La chiave attiva la modalità di modifica. Il tasto fa sì che il controllo per visualizzare un controllo calendario mensile a discesa (premendo anche questa operazione).                                                                                                                                                                                                                                          |
| Numeri        | Il controllo accetta l'input numerico in segmenti di due caratteri. Se il valore immesso dall'utente non è valido ,ad esempio impostando il mese su 14, il controllo lo rifiuta e reimposta la visualizzazione sul valore precedente.                                                                                                                                                                |
| Più e meno | Il controllo accetta i tasti virtuali VK ADD e VK SUBTRACT dal tastierino numerico per incrementare e \_ \_ decrementare il valore nel campo corrente.                                                                                                                                                                                                                             |



 

I controlli DTP che non usano lo stile [**\_ DTS UPDOWN**](date-and-time-picker-control-styles.md) visualizzano un pulsante freccia. Se l'utente fa clic su questo pulsante, viene selezionato un controllo calendario mensile. L'utente può selezionare una data specifica facendo clic su un'area del calendario.

## <a name="date-and-time-picker-control-styles-and-formats"></a>Stili e formati del controllo Selezione data e ora

I controlli selezione data e ora [](date-and-time-picker-control-styles.md) hanno diversi stili di controllo selezione data e ora che determinano l'aspetto e il comportamento di un controllo. Specificare lo stile durante la creazione del controllo con *il parametro dwStyle* di [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Per recuperare o modificare lo stile della finestra dopo aver creato il controllo, usare [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

### <a name="preset-formats"></a>Formati predefiniti

Sono disponibili tre formati predefiniti per la visualizzazione della data e uno per la visualizzazione dell'ora. Impostare questi formati scegliendo uno degli stili di finestra seguenti.



|   Formato                                                                                                    |   Descrizione                                                         |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**DTS \_ LONGDATEFORMAT**](date-and-time-picker-control-styles.md)                 | La visualizzazione sarà simile alla seguente: "Friday, April 19, 1996".      |
| [**DTS \_ SHORTDATEFORMAT**](date-and-time-picker-control-styles.md)               | La visualizzazione sarà simile a: "4/19/96".                     |
| [**DTS \_ SHORTDATECENTURYFORMAT**](date-and-time-picker-control-styles.md) | **Versione 5.80.** La visualizzazione sarà simile alla seguente: "4/19/1996". |
| [**DTS \_ TIMEFORMAT**](date-and-time-picker-control-styles.md)                         | La visualizzazione sarà simile a: "5:31:42 PM".                  |



 

### <a name="custom-formats"></a>Formati personalizzati

Un controllo DTP si basa su una stringa di formato per determinare come verranno visualizzati i campi di informazioni. Se i formati predefiniti non sono sufficienti, è possibile creare un formato personalizzato definendo una stringa di formato personalizzata. I formati personalizzati offrono maggiore flessibilità per un'applicazione. Consentono di specificare l'ordine in cui il controllo visualizza i campi di informazioni. È possibile includere il testo del corpo e i campi di callback per richiedere informazioni all'utente. Dopo aver creato la stringa, assegnarla al controllo DTP con un [**messaggio \_ DTM SETFORMAT.**](dtm-setformat.md)

### <a name="format-strings"></a>Stringhe di formato

Una stringa di formato DTP è costituita da una serie di elementi che rappresentano una particolare informazione e ne definiscono il formato di visualizzazione. Gli elementi verranno visualizzati nell'ordine in cui sono visualizzati nella stringa di formato.

Gli elementi di formato di data e ora verranno sostituiti dalla data e dall'ora effettive. Sono definiti dai gruppi di caratteri seguenti.



| Elemento | Descrizione                                                                       |
|---------|-----------------------------------------------------------------------------------|
| "d"     | Giorno a una o due cifre.                                                        |
| "dd"    | Giorno a due cifre. I valori di giorno a cifra singola sono preceduti da uno zero.                |
| "ddd"   | Abbreviazione del giorno della settimana a tre caratteri.                                         |
| "dddd"  | Nome completo del giorno della settimana.                                                            |
| "h"     | Ora a una o due cifre nel formato a 12 ore.                                     |
| "hh"    | Ora a due cifre nel formato a 12 ore. I valori a cifra singola sono preceduti da uno zero. |
| "H"     | Ora a una o due cifre nel formato a 24 ore.                                     |
| "HH"    | Ora a due cifre nel formato a 24 ore. I valori a cifra singola sono preceduti da uno zero. |
| "m"     | Minuto a una o due cifre.                                                     |
| "mm"    | Minuto a due cifre. I valori a cifra singola sono preceduti da uno zero.                 |
| "M"     | Numero di mese a una o due cifre.                                               |
| "MM"    | Numero di mese a due cifre. I valori a cifra singola sono preceduti da uno zero.           |
| "MMM"   | Abbreviazione del mese di tre caratteri.                                           |
| "MMMM"  | Nome completo del mese.                                                              |
| "t"     | L'abbreviazione AM/PM di una lettera (ovvero AM viene visualizzata come "A").              |
| "tt"    | L'abbreviazione AM/PM di due lettere, ovvero AM, viene visualizzata come "AM".             |
| "yy"    | Le ultime due cifre dell'anno (ovvero 1996 verrebbero visualizzate come "96").       |
| "yyyy"  | L'intero anno (ovvero il 1996 verrebbe visualizzato come "1996").                       |



 

Per rendere le informazioni più leggibili, è possibile aggiungere testo del corpo alla stringa di formato racchiuderla tra virgolette singole. Gli spazi e i segni di punteggiatura non devono essere racchiusi tra virgolette.

> [!Note]  
> I caratteri non di formattazione non delimitati da virgolette singole comportano una visualizzazione imprevedibile da parte del controllo DTP.

Ad esempio, per visualizzare la data corrente nel formato "'Today is: 04:22:31 Tuesday Mar 23, 1996", la stringa di formato è "'Today is: 'hh':'m':'s ddd MMM dd', 'yyyy". Per includere una virgoletta singola nel testo del corpo, usare due virgolette singole consecutive. Ad esempio, "'Don't forget' MMM dd',' yyyy" produce un output simile al seguente: Don't forget Mar 23, 1996. Non è necessario usare le virgolette con la virgola, quindi anche "'Don't forget' MMM dd, yyyy" è valido e produce lo stesso output.

### <a name="callback-fields"></a>Campi di callback

Oltre alle stringhe di formato standard [e](#format-strings) al testo del corpo, è anche possibile definire determinate parti della visualizzazione come [campi callback.](#callback-fields) Questi campi possono essere usati per eseguire query sull'utente per ottenere informazioni. Per dichiarare un campo di callback, includere uno o più caratteri "X" (codice ASCII 88) in qualsiasi punto della stringa di formato. È possibile creare campi di callback con un'identità univoca ripetendo il carattere "X". La stringa di formato "XX dddd MMM dd", "yyy XXX" contiene quindi due campi di callback univoci, "XX" e "XXX". Analogamente ad altri campi di controllo DTP, i campi di callback vengono visualizzati in ordine da sinistra a destra in base alla relativa posizione nella stringa di formato.

Quando il controllo DTP analizza la stringa di formato e rileva un campo di callback, invia i codici di notifica [DTN \_ FORMAT](dtn-format.md) e [DTN \_ FORMATQUERY.](dtn-formatquery.md) L'elemento della stringa di formato corrispondente al campo di callback è incluso nelle notifiche per consentire all'applicazione ricevente di determinare il campo di callback su cui viene eseguita la query. Il proprietario del controllo deve rispondere a queste notifiche per assicurarsi che le informazioni personalizzate siano visualizzate correttamente.

## <a name="date-and-time-picker-control-notification-messages"></a>Messaggi di notifica del controllo Selezione data e ora

Un controllo di selezione data e ora (DTP) invia codici di notifica quando riceve l'input o i processi dell'utente e reagisce ai campi di callback. L'elemento padre del controllo riceve questi codici di notifica sotto forma di [**messaggi WM \_ NOTIFY.**](wm-notify.md)

I codici di notifica seguenti vengono usati con i controlli DTP.



| Codice di notifica                             | Descrizione                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DTN \_ CLOSEUP](dtn-closeup.md)               | Indica che il calendario mensile a discesa sta per essere rimosso.                                                                                                                                               |
| [DTN \_ DATETIMECHANGE](dtn-datetimechange.md) | Segnala una modifica all'interno del controllo DTP.                                                                                                                                                                          |
| [ELENCO A DISCESA DTN \_](dtn-dropdown.md)             | Indica che il calendario mensile a discesa sta per essere visualizzato.                                                                                                                                             |
| [FORMATO \_ DTN](dtn-format.md)                 | Richiede la visualizzazione del testo in una parte della stringa di formato descritta come campo di callback.                                                                                                                         |
| [DTN \_ FORMATQUERY](dtn-formatquery.md)       | Richiede informazioni sulla dimensione massima consentita del testo da visualizzare in un campo di callback.                                                                                                            |
| [DTN \_ USERSTRING](dtn-userstring.md)         | Segnala la fine dell'operazione di modifica di un utente all'interno del controllo . Questa notifica viene inviata solo dai controlli DTP che usano lo [**stile \_ APPCANPARSE DTS.**](date-and-time-picker-control-styles.md) |
| [DTN \_ WMKEYDOWN](dtn-wmkeydown.md)           | Segnala che l'utente ha premuto un tasto in un campo di callback del controllo DTP.                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul controllo Selezione data e ora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 