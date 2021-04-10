---
title: Informazioni sui controlli selezione data e ora
description: Un controllo di selezione data e ora (DTP) fornisce un'interfaccia semplice e intuitiva tramite la quale scambiare le informazioni di data e ora con un utente.
ms.assetid: 6749c3ae-2c52-4183-ac4e-68ca7ebf1e13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04604c01a73aa8f2ebb8542061412372faee5282
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047478"
---
# <a name="about-date-and-time-picker-controls"></a>Informazioni sui controlli selezione data e ora

Un *controllo di selezione data e ora (DTP)* fornisce un'interfaccia semplice e intuitiva tramite la quale scambiare le informazioni di data e ora con un utente. Ad esempio, con un controllo DTP è possibile chiedere all'utente di immettere una data e quindi recuperare facilmente la selezione.

Vengono trattati i seguenti argomenti:

-   [Interfaccia utente selezione data e ora](#date-and-time-picker-user-interface)
-   [Stili e formati del controllo selezione data e ora](#date-and-time-picker-control-styles-and-formats)
    -   [Formati predefiniti](#preset-formats)
    -   [Formati personalizzati](#custom-formats)
    -   [Stringhe di formato](#format-strings)
    -   [Campi callback](#callback-fields)
-   [Messaggi di notifica del controllo selezione data e ora](#date-and-time-picker-control-notification-messages)
-   [Argomenti correlati](#related-topics)

> [!Note]
> Windows non supporta le date precedenti alla 1601. Per informazioni dettagliate, vedere la struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .
>
> Il controllo è basato sul calendario gregoriano, introdotto in 1753. Non verranno calcolate le date coerenti con il calendario Giuliano.

## <a name="date-and-time-picker-user-interface"></a>Interfaccia utente selezione data e ora

L'area client di un controllo di selezione data e ora (DTP) Visualizza le informazioni di data e ora, o entrambe, e funge da interfaccia tramite la quale gli utenti modificano le informazioni. È possibile selezionare la data da un calendario oppure utilizzare un controllo di scorrimento. è possibile modificare l'ora digitando i campi definiti dalle [stringhe di formato](#format-strings)del controllo. Facoltativamente, il controllo Visualizza una casella di controllo. Quando questa opzione è selezionata, è possibile recuperare il valore nel controllo; in caso contrario, il controllo viene considerato non inizializzato.

Nella figura seguente è illustrata una finestra che contiene tre controlli di selezione data. Il primo controllo selezione data è stato creato con lo [**stile \_ SHOWNONE DTS**](date-and-time-picker-control-styles.md) , il secondo con lo stile di [**\_ Abbasso DTS**](date-and-time-picker-control-styles.md) e il terzo senza stili speciali. Nel terzo controllo, l'utente ha fatto clic sulla freccia rivolta verso il basso per visualizzare il calendario.

![Screenshot di una finestra che illustra tre stili dei controlli di selezione data](images/dtpdatepick.png)

Nella figura seguente è illustrata una finestra con tre controlli che contengono l'ora.

Il primo controllo è stato creato con lo stile [**DTS \_ TimeFormat**](date-and-time-picker-control-styles.md) e indica l'ora predefinita, che è costituita da quattro campi. L'utente può digitare un valore valido in uno di questi campi oppure selezionare il campo e modificare il valore usando il controllo di scorrimento o i tasti di direzione.

Il secondo controllo Mostra un set di formati personalizzato utilizzando [**DateTime \_ seformatt**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat). Come nel primo controllo, l'utente può modificare i campi temporali digitando o usando i tasti di direzione. È possibile modificare il giorno della settimana selezionando una data del calendario che verrà visualizzata quando l'utente fa clic sulla freccia verso il basso.

Il terzo controllo Mostra il modo in cui è possibile aggiungere testo arbitrario al controllo. L'utente può selezionare un'ora (da 1 a 24) digitando, usando i tasti di direzione, oppure usando il controllo di scorrimento.

![Screenshot di una finestra che mostra tre controlli che contengono l'ora](images/dtpdatetimepick.png)

Il controllo DTP aggiorna automaticamente le informazioni interne in base all'input dell'utente. Il controllo riconosce quanto segue come input valido.



| Categoria di input | Descrizione                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tasti di direzione     | Il controllo accetta i tasti di direzione per spostarsi tra i campi nel controllo e modificare i valori. L'utente può premere i tasti o per spostarsi tra il controllo se l'utente tenta di spostarsi oltre l'ultimo campo in una determinata direzione, lo stato attivo della tastiera "esegue il wrapping" al campo sul lato opposto del controllo. Le chiavi e modificano i valori nel campo corrente in modo incrementale. |
| Fine e Home   | Il controllo accetta le \_ chiavi virtuali di base VK e VK \_ per modificare il valore nel campo corrente con i limiti superiore e inferiore, rispettivamente.                                                                                                                                                                                                                          |
| Tasti funzione  | La chiave attiva la modalità di modifica. La chiave fa sì che il controllo visualizzi un controllo di calendario mensile a discesa. questa operazione viene eseguita anche premendo.                                                                                                                                                                                                                                          |
| Numeri        | Il controllo accetta l'input numerico in segmenti di due caratteri. Se il valore immesso dall'utente non è valido (ad esempio, impostando il mese su 14), il controllo lo rifiuta e reimposta la visualizzazione sul valore precedente.                                                                                                                                                                |
| Più e meno | Il controllo accetta le \_ chiavi virtuali per l'aggiunta e la sottrazione del numero VK \_ dal tastierino numerico per incrementare e decrementare il valore nel campo corrente.                                                                                                                                                                                                                             |



 

I controlli DTP che non utilizzano lo stile di suddivisione [**DTS \_**](date-and-time-picker-control-styles.md) visualizzano un pulsante freccia. Se l'utente fa clic su questo pulsante, il controllo di calendario mensile diminuisce. L'utente può selezionare una data specifica facendo clic su un'area del calendario.

## <a name="date-and-time-picker-control-styles-and-formats"></a>Stili e formati del controllo selezione data e ora

I controlli di selezione data e ora (DTP) hanno diversi [stili di controllo selezione data e ora](date-and-time-picker-control-styles.md) che determinano l'aspetto e il comportamento di un controllo. Specificare lo stile durante la creazione del controllo con il parametro *dwStyle* di [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Per recuperare o modificare lo stile della finestra dopo aver creato il controllo, usare [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

### <a name="preset-formats"></a>Formati predefiniti

Sono disponibili tre formati predefiniti per la visualizzazione della data e di uno per la visualizzazione dell'ora. Impostare questi formati scegliendo uno degli stili della finestra seguenti.



|                                                                                                       |                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**\_LONGDATEFORMAT DTS**](date-and-time-picker-control-styles.md)                 | Lo schermo sarà simile al seguente: "Friday, 19 aprile 1996".      |
| [**\_SHORTDATEFORMAT DTS**](date-and-time-picker-control-styles.md)               | La visualizzazione sarà simile alla seguente: "4/19/96".                     |
| [**\_SHORTDATECENTURYFORMAT DTS**](date-and-time-picker-control-styles.md) | **Versione 5,80**. La visualizzazione sarà simile alla seguente: "4/19/1996". |
| [**\_TimeFormat DTS**](date-and-time-picker-control-styles.md)                         | La visualizzazione sarà simile alla seguente: "5:31:42 PM".                  |



 

### <a name="custom-formats"></a>Formati personalizzati

Un controllo DTP si basa su una stringa di formato per determinare come vengono visualizzati i campi delle informazioni. Se i formati predefiniti non sono sufficienti, è possibile creare un formato personalizzato definendo una stringa di formato personalizzata. I formati personalizzati offrono maggiore flessibilità per un'applicazione. Consentono di specificare l'ordine in cui il controllo visualizzerà i campi delle informazioni. È possibile includere il testo del corpo e i campi di callback per richiedere informazioni all'utente. Una volta creata, la stringa viene assegnata al controllo DTP con un messaggio [**di \_ formato DTM**](dtm-setformat.md) .

### <a name="format-strings"></a>Stringhe di formato

Una stringa di formato DTP è costituita da una serie di elementi che rappresentano una particolare parte delle informazioni e ne definiscono il formato di visualizzazione. Gli elementi verranno visualizzati nell'ordine in cui sono visualizzati nella stringa di formato.

Gli elementi di formato di data e ora verranno sostituiti dalla data e dall'ora effettive. Sono definiti dai gruppi di caratteri seguenti.



| Elemento | Descrizione                                                                       |
|---------|-----------------------------------------------------------------------------------|
| "d"     | Giorno a una o due cifre.                                                        |
| "dd"    | Giorno a due cifre. I valori del giorno a una sola cifra sono preceduti da uno zero.                |
| "ddd"   | Abbreviazione del giorno della settimana di tre caratteri.                                         |
| "dddd"  | Nome completo del giorno della settimana.                                                            |
| "h"     | Ora a una o due cifre nel formato a 12 ore.                                     |
| "hh"    | Ora a due cifre nel formato a 12 ore. I valori a una sola cifra sono preceduti da uno zero. |
| "H"     | Ora a una o due cifre nel formato a 24 ore.                                     |
| "HH"    | Ora a due cifre nel formato a 24 ore. I valori a una sola cifra sono preceduti da uno zero. |
| "m"     | Minuto a una o due cifre.                                                     |
| "mm"    | Minuto a due cifre. I valori a una sola cifra sono preceduti da uno zero.                 |
| "M"     | Numero del mese a una o due cifre.                                               |
| "MM"    | Numero del mese a due cifre. I valori a una sola cifra sono preceduti da uno zero.           |
| "MMM"   | Abbreviazione del mese di tre caratteri.                                           |
| "MMMM"  | Nome completo del mese.                                                              |
| "t"     | L'abbreviazione AM/PM di una lettera (ovvero, AM viene visualizzata come "A").              |
| "tt"    | L'abbreviazione di due lettere AM/PM, ovvero AM viene visualizzata come "AM".             |
| "yy"    | Le ultime due cifre dell'anno (ovvero 1996 verrebbero visualizzate come "96").       |
| "yyyy"  | L'anno completo (ovvero 1996 verrebbe visualizzato come "1996").                       |



 

Per rendere più leggibili le informazioni, è possibile aggiungere il testo del corpo alla stringa di formato racchiudendo il testo tra virgolette singole. Non è necessario racchiudere tra virgolette gli spazi e i segni di punteggiatura.

> [!Note]  
> I caratteri non formattati che non sono delimitati da virgolette singole comporteranno una visualizzazione imprevedibile del controllo DTP.

Ad esempio, per visualizzare la data corrente con il formato "' Today is: 04:22:31 martedì mar 23, 1996", la stringa di formato è "' Today is:' HH ':''' s dddd MMM DD ',' aaaa". Per includere una virgoletta singola nel testo del corpo, usare due virgolette singole consecutive. Ad esempio, "" non dimenticare "MMM DD", "aaaa" produce un output simile al seguente: non dimenticare il 23 marzo 1996. Non è necessario usare le virgolette con la virgola, quindi "" non dimenticare che anche ' MMM GG, aaaa "è valido e produce lo stesso output.

### <a name="callback-fields"></a>Campi callback

Oltre alle [stringhe di formato](#format-strings) standard e al testo del corpo, è anche possibile definire determinate parti della visualizzazione come [campi callback](#callback-fields). Questi campi possono essere utilizzati per eseguire una query sull'utente per ottenere informazioni. Per dichiarare un campo di callback, includere uno o più caratteri "X" (codice ASCII 88) in qualsiasi punto della stringa di formato. È possibile creare campi di callback che hanno un'identità univoca ripetendo il carattere "X". La stringa di formato "XX dddd MMM DD", "yyy XXX" contiene quindi due campi di callback univoci, ovvero "XX" e "XXX". Analogamente ad altri campi del controllo DTP, i campi di callback vengono visualizzati nell'ordine da sinistra a destra in base alla relativa posizione nella stringa di formato.

Quando il controllo DTP analizza la stringa di formato e rileva un campo di callback, invia il [ \_ formato DTN](dtn-format.md) e i codici di notifica [ \_ FORMATQUERY DTN](dtn-formatquery.md) . L'elemento stringa di formato corrispondente al campo di callback è incluso nelle notifiche per consentire all'applicazione ricevente di determinare quale campo di callback viene sottoposto a query. Il proprietario del controllo deve rispondere a queste notifiche per assicurarsi che le informazioni personalizzate siano visualizzate correttamente.

## <a name="date-and-time-picker-control-notification-messages"></a>Messaggi di notifica del controllo selezione data e ora

Un controllo di selezione data e ora (DTP) Invia i codici di notifica quando riceve input o processi utente e reagisce ai campi di callback. L'elemento padre del controllo riceve i codici di notifica sotto forma di messaggi di [**\_ notifica WM**](wm-notify.md) .

I codici di notifica seguenti vengono utilizzati con i controlli di impaginazione.



| Codice di notifica                             | Descrizione                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [primo piano DTN \_](dtn-closeup.md)               | Indica che il calendario mensile a discesa sta per essere rimosso.                                                                                                                                               |
| [\_DATETIMECHANGE DTN](dtn-datetimechange.md) | Segnala una modifica all'interno del controllo DTP.                                                                                                                                                                          |
| [\_elenco a discesa DTN](dtn-dropdown.md)             | Indica che il calendario mensile a discesa sta per essere visualizzato.                                                                                                                                             |
| [\_formato DTN](dtn-format.md)                 | Richiede il testo da visualizzare in una parte della stringa di formato descritta come campo di callback.                                                                                                                         |
| [\_FORMATQUERY DTN](dtn-formatquery.md)       | Richiede informazioni sulla dimensione massima consentita del testo da visualizzare in un campo di callback.                                                                                                            |
| [\_USERSTRING DTN](dtn-userstring.md)         | Segnala la fine dell'operazione di modifica di un utente all'interno del controllo. Questa notifica viene inviata solo dai controlli DTP che utilizzano lo stile [**DTS \_ APPCANPARSE**](date-and-time-picker-control-styles.md) . |
| [\_WMKEYDOWN DTN](dtn-wmkeydown.md)           | Segnala che l'utente ha premuto un tasto in un campo di callback del controllo DTP.                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al controllo selezione data e ora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 