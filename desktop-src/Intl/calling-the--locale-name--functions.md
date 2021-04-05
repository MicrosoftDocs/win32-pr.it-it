---
description: In Windows Vista è stato introdotto un numero elevato di funzioni che utilizzano nomi di impostazioni locali anziché identificatori delle impostazioni locali.
ms.assetid: e88c31b2-b1da-40ae-b512-67b8ad409b95
title: Chiamata delle funzioni "nome delle impostazioni locali"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58c15d2d9fe7721eb162f8c7cf96084bd4afa2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751151"
---
# <a name="calling-the-locale-name-functions"></a>Chiamata delle funzioni "nome delle impostazioni locali"

In Windows Vista è stato introdotto un numero elevato di funzioni che utilizzano [nomi di impostazioni locali](locale-names.md) anziché [identificatori delle impostazioni locali](locale-identifiers.md). Queste nuove funzioni forniscono un supporto efficace per le [impostazioni locali supplementari](custom-locales.md)e molte di esse forniscono funzionalità aggiuntive non disponibili nelle funzioni NLS precedenti. Alcuni di essi, ad esempio le nuove funzioni di enumerazione, rappresentano anche miglioramenti della progettazione.

> [!Note]  
> Le applicazioni progettate per essere eseguite solo in Windows Vista e versioni successive devono usare le funzioni "nome delle impostazioni locali" in preferenza alle funzioni NLS che usano gli identificatori delle impostazioni locali.

 

Nella tabella seguente sono elencate le funzioni nome impostazioni locali con le funzioni meno recenti che è possibile sostituire.



| Funzioni che usano nomi delle impostazioni locali                                     | Funzioni che usano gli identificatori delle impostazioni locali                                                             |
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

Un esempio che illustra l'uso di diverse funzioni in base ai nomi delle impostazioni locali è disponibile nell' [esempio NLS: Name-based Apis](nls--name-based-apis-sample.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto per le lingue nazionali](using-national-language-support.md)
</dt> </dl>

 

 
