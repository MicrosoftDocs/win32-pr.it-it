---
description: Windows Vista introduce un numero elevato di funzioni che usano i nomi delle impostazioni locali anziché gli identificatori delle impostazioni locali.
ms.assetid: e88c31b2-b1da-40ae-b512-67b8ad409b95
title: Chiamata delle funzioni "Locale Name"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc97490f21c54a187f2db31c6ee5c7eaa6c45e64069f9be9594c99e2376ef04e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754891"
---
# <a name="calling-the-locale-name-functions"></a>Chiamata delle funzioni "Locale Name"

Windows Vista introduce un numero elevato di funzioni che usano i nomi [delle impostazioni locali](locale-names.md) anziché gli identificatori delle impostazioni [locali](locale-identifiers.md). Queste nuove funzioni offrono un buon supporto [per le](custom-locales.md)impostazioni locali supplementari e molte di esse forniscono funzionalità aggiuntive non disponibili nelle funzioni NLS precedenti. Alcune di esse, ad esempio le nuove funzioni di enumerazione, rappresentano anche miglioramenti della progettazione.

> [!Note]  
> Le applicazioni destinate all'esecuzione solo in Windows Vista e versioni successive devono usare le funzioni "nome delle impostazioni locali" in preferenza alle funzioni NLS che usano identificatori delle impostazioni locali.

 

Nella tabella seguente sono elencate le funzioni dei nomi delle impostazioni locali insieme alle funzioni precedenti che è possibile sostituire.



| Funzioni che usano nomi delle impostazioni locali                                     | Funzioni che usano identificatori delle impostazioni locali                                                             |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)                       | [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)                                                         |
| [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)             | [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [ **EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) |
| [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)               | [**EnumDateFormats**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [ **EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)     |
| [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)               | [**EnumSystemLocales**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesa)                                                 |
| [**EnumTimeFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumtimeformatsex)                   | [**EnumTimeFormats**](/windows/desktop/api/Winnls/nf-winnls-enumtimeformatsa)                                                     |
| [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)                       | [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)                                                         |
| [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)                   | [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)                                                     |
| [**GetCurrencyFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getcurrencyformatex)               | [**GetCurrencyFormat**](/windows/desktop/api/Winnls/nf-winnls-getcurrencyformata)                                                 |
| [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)                       | [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)                                                         |
| [**GetDurationFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getdurationformatex)               | [**GetDurationFormat**](/windows/desktop/api/Winnls/nf-winnls-getdurationformat)                                                 |
| [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)                       | [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)                                                         |
| [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex)                       | [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion)                                                         |
| [**GetNumberFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getnumberformatex)                   | [**GetNumberFormat**](/windows/desktop/api/Winnls/nf-winnls-getnumberformata)                                                     |
| [**GetSystemDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) | [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid)                                           |
| [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex)                       | [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata)                                                         |
| [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename)     | [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid)                                               |
| [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)                   | [**IsValidLocale**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocale)                                                         |
| [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)                           | [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                                                             |



 

## <a name="example"></a>Esempio

Un esempio che illustra l'uso di diverse funzioni basate sui nomi delle impostazioni locali è disponibile in [NLS: Name-based APIs Sample (Esempio](nls--name-based-apis-sample.md)di API basate sui nomi).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto linguistico nazionale](using-national-language-support.md)
</dt> </dl>

 

 
