---
description: Questo argomento include istruzioni per l'uso delle funzioni NLS nelle applicazioni per recuperare informazioni su data e ora, oltre ai dati relativi alla durata. Se l'applicazione deve salvare in modo permanente i dati, vedere Utilizzo di dati locali permanenti.
ms.assetid: 1880ff8f-110c-4661-8b1f-afe1d8d2a38d
title: Recupero di informazioni su data e ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2c2fa1d15de2c1ba5587a981373ff14b1c1c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315913"
---
# <a name="retrieving-time-and-date-information"></a>Recupero di informazioni su data e ora

Questo argomento include istruzioni per l'uso delle funzioni NLS nelle applicazioni per recuperare informazioni su [data e ora](time-and-date.md) , oltre ai dati relativi alla durata. Se l'applicazione deve salvare in modo permanente i dati, vedere [utilizzo di dati locali permanenti](using-persistent-locale-data.md).

**Windows Vista e versioni successive:** Le funzioni descritte in questo argomento possono recuperare dati da [impostazioni locali personalizzate](custom-locales.md). In particolare, possono essere usati per personalizzare i formati di data e ora. Ad esempio, è possibile avere un formato di ora quale "hhHmm'ss" ", ottenendo stringhe temporali come" 12H34 "12" ".

## <a name="retrieve-time-information"></a>Recuperare le informazioni sull'ora

L'applicazione può ottenere stringhe per qualsiasi ora in un formato appropriato per le impostazioni locali correnti usando le funzioni [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) e [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) . Entrambe le funzioni controllano ognuno dei valori temporali in una struttura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) valida per determinare che rientra nell'intervallo di valori appropriato, ignorando le parti della data della struttura. Se uno dei valori di ora è esterno all'intervallo corretto, la funzione ha esito negativo e il parametro ERROR del codice \_ non è valido \_ . La funzione non restituisce errori per una stringa di formato non valida, ma costituisce semplicemente la migliore stringa di tempo possibile.

> [!Note]  
> Le funzioni del tempo NLS non includono i millisecondi come parte di una stringa di tempo formattata.

 

Per ottenere il formato dell'ora senza eseguire alcuna formattazione effettiva, l'applicazione può usare la funzione [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) , specificando la costante [ \_ STIMEFORMAT delle impostazioni locali](locale-stime-constants.md) nella chiamata.

**Usa marcatori temporali**

Esempi di marcatori temporali sono "AM" e "PM" per l'inglese (Stati Uniti) e "de". e "du". per spagnolo (Messico). Se \_ nella chiamata a [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) o [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex)viene specificato Time NOTIMEMARKER, la funzione rimuove i separatori precedenti e successivi all'indicatore di tempo. Se è presente un marcatore temporale e il \_ flag NOTIMEMARKER dell'ora non è impostato nella chiamata, la funzione localizza l'indicatore di ora in base all'identificatore delle impostazioni locali specificato.

**Rimuovi separatori precedenti minuti e secondi**

L'applicazione può chiamare [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) o [**GETTIMEFORMATEX**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) con l'ora \_ NOMINUTESORSECONDS o l'ora in secondi \_ specificata per rimuovere i separatori che precedono gli elementi minuti e/o secondi.

**Usa il formato a 24 ore**

Se l'applicazione supporta il formato a 24 ore, può chiamare [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) o [**GETTIMEFORMATEX**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) con l'ora \_ FORCE24HOURFORMAT. A meno che non \_ sia impostato il flag Time NOTIMEMARKER, la funzione Visualizza un indicatore temporale esistente.

## <a name="retrieve-date-information"></a>Recuperare le informazioni sulla data

Un'applicazione può recuperare le stringhe per qualsiasi data in un formato appropriato per le impostazioni locali correnti usando le funzioni [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) e [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) . Entrambe le funzioni controllano ognuno dei valori di data anno, mese, giorno e giorno della settimana in una struttura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) valida, ignorando le parti temporali della struttura. Il nome del giorno, il nome abbreviato del giorno, il nome del mese e il nome abbreviato del mese sono tutti localizzati in base all'identificatore delle impostazioni locali. Se il giorno della settimana non è corretto, la funzione utilizza il valore corretto e non restituisce alcun errore. Se uno degli altri valori di data non è compreso nell'intervallo corretto, la funzione ha esito negativo e il parametro ERROR del codice \_ non è valido \_ . La funzione non restituisce errori per una stringa di formato non valida, ma costituisce semplicemente la stringa di data migliore possibile.

Se l'applicazione richiede il formato della data per un determinato calendario, deve usare [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) o [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex), passando l' [**identificatore di calendario**](calendar-identifiers.md)appropriato. Per restituire tutti i formati di data per un determinato calendario, l'applicazione può usare [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)o [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).

**Specificare un calendario alternativo**

L'applicazione può chiamare [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) o [**GETDATEFORMATEX**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) con la data del flag \_ usare \_ ALT Calendar per \_ usare il formato predefinito per il calendario alternativo specificato. Se non esiste un formato predefinito per il calendario alternativo, la funzione utilizza le sostituzioni utente.

Per ottenere il formato della data per un calendario alternativo, l'applicazione può usare [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la costante [ \_ IOPTIONALCALENDAR delle impostazioni locali](locale-ioptionalcalendar.md) .

**Specificare il tipo di data**

Se l'applicazione vuole usare il formato di data breve, specifica la data \_ shortdate nella chiamata a [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) o [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex). È possibile ottenere un formato di data estesa specificando DATE \_ LONGDATE nella chiamata di funzione. Se non viene specificato alcun flag e *lpFormat* è impostato su **null**, la funzione utilizzerà date \_ shortdate come valore predefinito.

Per ottenere il formato di data breve e lungo per il calendario predefinito delle impostazioni locali, l'applicazione deve usare la funzione [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la costante delle impostazioni locali [ \_ SSHORTDATE](locale-sshortdate.md) o le [impostazioni locali \_ SLONGDATE](locale-slongdate.md) .

**Specificare l'immagine del formato della data**

L'applicazione può specificare un'immagine di formato data che [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) o [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) USA per creare la stringa di data. Se il formato della data per le impostazioni locali specificate è obbligatorio, l'applicazione può chiamare la funzione con *lpFormat* impostato su **null**. Se il parametro non è impostato su **null**, la funzione utilizza le impostazioni locali solo per le informazioni non specificate nella stringa di formato immagine, ad esempio i nomi dei giorni e dei mesi per le impostazioni locali.

L'applicazione può racchiudere qualsiasi testo che deve rimanere nella forma esatta racchiusa tra virgolette singole. Una virgoletta singola può essere usata anche come carattere di escape per consentire la visualizzazione del contrassegno stesso nella stringa di data. Tuttavia, la sequenza di escape deve essere racchiusa tra due virgolette singole. Ad esempio, per visualizzare la data come "maggio" 93 ", la stringa di formato è:" MMMM "'" yy ".

## <a name="retrieve-duration-information"></a>Recuperare le informazioni sulla durata

**Windows Vista e versioni successive:** Le funzioni [**GetDurationFormat**](/windows/desktop/api/Winnls/nf-winnls-getdurationformat) e [**GetDurationFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getdurationformatex) sono disponibili per ottenere i formati di durata per le impostazioni locali, incluse le impostazioni locali personalizzate. Per ottenere il formato di durata predefinito per le impostazioni locali, l'applicazione deve usare la funzione [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la costante [ \_ SDURATION delle impostazioni locali](locale-sduration.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto per le lingue nazionali](about-national-language-support.md)
</dt> <dt>

[Data e ora](time-and-date.md)
</dt> <dt>

[Utilizzo di dati locali persistenti](using-persistent-locale-data.md)
</dt> </dl>

 

 
