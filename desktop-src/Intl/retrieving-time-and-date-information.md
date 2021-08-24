---
description: Questo argomento include istruzioni per l'uso delle funzioni NLS nelle applicazioni per recuperare informazioni su data e ora, nonché dati sulla durata. Se l'applicazione deve rendere persistenti i dati, vedere Uso dei dati delle impostazioni locali permanenti.
ms.assetid: 1880ff8f-110c-4661-8b1f-afe1d8d2a38d
title: Recupero di informazioni su ora e data
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f461f12cb1c6324892a415142c159ba570759128e61dd02b53a7cceebccc57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040411"
---
# <a name="retrieving-time-and-date-information"></a>Recupero di informazioni su ora e data

Questo argomento include istruzioni per l'uso delle [](time-and-date.md) funzioni NLS nelle applicazioni per recuperare informazioni su data e ora, nonché dati sulla durata. Se l'applicazione deve rendere persistenti i dati, vedere [Uso dei dati delle impostazioni locali persistenti](using-persistent-locale-data.md).

**Windows Vista e versioni successive:** Le funzioni descritte in questo argomento possono recuperare dati dalle [impostazioni locali personalizzate.](custom-locales.md) In particolare, possono essere usati per personalizzare i formati di data e ora. Ad esempio, è possibile avere un formato di ora, ad esempio "hhHmm'ss'", che determina stringhe di ora come "12H34'12''".

## <a name="retrieve-time-information"></a>Recuperare informazioni sull'ora

L'applicazione può ottenere stringhe in qualsiasi momento in un formato appropriato per le impostazioni locali correnti usando le [**funzioni GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) e [**GetTimeFormatEx.**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) Entrambe le funzioni controllano ognuno dei valori di ora in una struttura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) valida per determinare che si trova nell'intervallo di valori appropriato, ignorando le parti di data della struttura. Se uno dei valori di ora non è compreso nell'intervallo corretto, la funzione ha esito negativo con il codice ERROR \_ INVALID \_ PARAMETER. La funzione non restituisce errori per una stringa di formato non valido, ma costituisce semplicemente la migliore stringa temporale possibile.

> [!Note]  
> Le funzioni di tempo NLS non includono millisecondi come parte di una stringa di ora formattata.

 

Per ottenere il formato dell'ora senza eseguire alcuna formattazione effettiva, l'applicazione può usare la [**funzione GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx,**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) specificando la costante [LOCALE \_ STIMEFORMAT](locale-stime-constants.md) nella chiamata.

**Usare gli indicatori di tempo**

Esempi di marcatori di tempo sono "AM" e "PM" per l'inglese (Stati Uniti) e "de". e "du". per spagnolo (Messico). Se si specifica TIME NOTIMEMARKER nella chiamata a \_ [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) o [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex), la funzione rimuove i separatori che precedono e segue l'indicatore di ora. Se esiste un indicatore di ora e il flag TIME NOTIMEMARKER non è impostato nella chiamata, la funzione localizza l'indicatore di ora in base all'identificatore delle impostazioni \_ locali specificato.

**Rimuovere i separatori che precedono minuti e secondi**

L'applicazione può chiamare [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) o [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) con TIME NOMINUTESORSECONDS o TIME NOSECONDS specificati per rimuovere i separatori che precedono gli elementi \_ \_ minutes e/o seconds.

**Usare il formato 24 ore**

Se l'applicazione supporta il formato a 24 ore, può chiamare [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) o [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) con TIME \_ FORCE24HOURFORMAT. A meno che non sia impostato il \_ flag TIME NOTIMEMARKER, la funzione visualizza qualsiasi indicatore di tempo esistente.

## <a name="retrieve-date-information"></a>Recuperare informazioni sulla data

Un'applicazione può recuperare stringhe per qualsiasi data in un formato appropriato per le impostazioni locali correnti usando le [**funzioni GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) e [**GetDateFormatEx.**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) Entrambe le funzioni controllano ogni valore di data anno, mese, giorno e giorno della settimana in una struttura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) valida, ignorando le parti dell'ora della struttura . Il nome del giorno, il nome abbreviato del giorno, il nome del mese e il nome del mese abbreviato sono tutti localizzati in base all'identificatore delle impostazioni locali. Se il giorno della settimana non è corretto, la funzione usa il valore corretto e non restituisce alcun errore. Se uno degli altri valori di data non è compreso nell'intervallo corretto, la funzione ha esito negativo con il codice ERROR \_ INVALID \_ PARAMETER. La funzione non restituisce errori per una stringa di formato non valido, ma costituisce semplicemente la stringa di data migliore possibile.

Se l'applicazione richiede il formato di data per un calendario specifico, deve usare [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) o [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex), passando l'identificatore [**di calendario appropriato.**](calendar-identifiers.md) Per restituire tutti i formati di data per un calendario specifico, l'applicazione può usare [**EnumCalendarInfoEx,**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) [**EnumCalendarInfoEx,**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex) [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)o [**EnumDateFormatsEx.**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)

**Specificare un calendario alternativo**

L'applicazione può chiamare [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) o [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) con il flag DATE USE ALT CALENDAR per usare il formato \_ predefinito per il calendario alternativo \_ \_ specificato. Se non esiste alcun formato predefinito per il calendario alternativo, la funzione usa le sostituzioni utente.

Per ottenere il formato della data per un calendario alternativo, l'applicazione può usare [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx con**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) la costante [LOCALE \_ IOPTIONALCALENDAR.](locale-ioptionalcalendar.md)

**Specificare il tipo di data**

Se l'applicazione vuole usare il formato di data breve, specifica DATE SHORTDATE nella chiamata a \_ [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) o [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex). È possibile ottenere un formato di data lunga specificando DATE \_ LONGDATE nella chiamata di funzione. Se non viene specificato alcun flag e *lpFormat* è impostato su **NULL,** la funzione usa DATE \_ SHORTDATE come valore predefinito.

Per ottenere il formato di data breve e lunga per il calendario delle impostazioni locali predefinito, l'applicazione deve usare la [**funzione GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la costante [LOCALE \_ SSHORTDATE](locale-sshortdate.md) o [LOCALE \_ SLONGDATE.](locale-slongdate.md)

**Specificare l'immagine del formato data**

L'applicazione può specificare un'immagine in formato data utilizzata da [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) o [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) per formare la stringa di data. Se è necessario il formato della data per le impostazioni locali specificate, l'applicazione può chiamare la funzione con *lpFormat* impostato su **NULL.** Se il parametro non è impostato su **NULL,** la funzione usa le impostazioni locali solo per le informazioni non specificate nella stringa di formato dell'immagine, ad esempio i nomi dei giorni e dei mesi per le impostazioni locali.

L'applicazione può racchiudere qualsiasi testo che deve rimanere nel formato esatto tra virgolette singole. È anche possibile usare una virgoletta singola come carattere di escape per consentire la visualizzazione del segno stesso nella stringa di data. Tuttavia, la sequenza di escape deve essere racchiusa tra due virgolette singole. Ad esempio, per visualizzare la data come "May '93", la stringa di formato è: "MMMM '''yy".

## <a name="retrieve-duration-information"></a>Recuperare informazioni sulla durata

**Windows Vista e versioni successive:** Le funzioni [**GetDurationFormat**](/windows/desktop/api/Winnls/nf-winnls-getdurationformat) e [**GetDurationFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getdurationformatex) sono disponibili per ottenere formati di durata per le impostazioni locali, incluse le impostazioni locali personalizzate. Per ottenere il formato di durata predefinito per le impostazioni locali, l'applicazione deve usare la [**funzione GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la costante [LOCALE \_ SDURATION.](locale-sduration.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto linguistico nazionale](about-national-language-support.md)
</dt> <dt>

[Ora e data](time-and-date.md)
</dt> <dt>

[Uso di dati delle impostazioni locali permanenti](using-persistent-locale-data.md)
</dt> </dl>

 

 
