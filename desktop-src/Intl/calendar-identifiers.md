---
description: Questo argomento definisce gli identificatori di calendario (tipo di dati CALId) usati per specificare calendari diversi.
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: Identificatori del calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9b931aea4a186af0849dfe8f6642c53744d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751154"
---
# <a name="calendar-identifiers"></a>Identificatori del calendario

Questo argomento definisce gli identificatori di calendario (tipo di dati CALId) usati per specificare calendari diversi. Le applicazioni possono usare questi identificatori quando usano le funzioni NLS e le funzioni di callback seguenti, che hanno parametri che accettano il tipo di dati CALId:

-   [**ConvertSystemTimeToCalDateTime**](convertsystemtimetocaldatetime.md)
-   [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)
-   [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)
-   [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)
-   [**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))
-   [**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))
-   [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)
-   [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)
-   [**GetCalendarSupportedDateRange**](getcalendarsupporteddaterange.md)
-   [**IsCalendarLeapYear**](iscalendarleapyear.md)
-   [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)

Vengono definiti i valori seguenti. Tutti gli altri valori sono riservati. Questi valori non possono essere combinati tra loro.



Identificatore calendario

Significato

1

\_gregoriano Cal

Gregoriano (localizzato)

2

CAL \_ Gregorian \_ US

Gregoriano (stringhe inglesi sempre)

3

CAL \_ Giappone

Era giapponese imperatore

4

CAL \_ Taiwan

Calendario di Taiwan

5

CAL \_ Corea

Era Tangun coreano

6

\_Hijri Cal

Hijri (arabo lunare)

7

CAL \_ Thai

Thai

8

\_inglese Cal

Ebraico (lunare)

9

CAL \_ gregoriano \_ \_ francese

Gregorian Middle East French

10

CAL \_ gregoriano \_ arabo

Gregorian Arabic

11

CAL \_ gregoriano \_ XLIT \_ inglese

Lingua inglese (gregoriano) traslitterato

12

CAL \_ gregoriano \_ XLIT \_ francese

Gregoriano traslitterato francese

23

\_UMALQURA Cal

**Windows Vista e versioni successive:** Calendario Um al Qura (arabo lunare)



 

> [!Note]  
> Il gap di numerazione tra gli identificatori CAL \_ gregoriano \_ XLIT \_ francese e Cal \_ UMALQURA è intenzionale. L'indicatore per CAL \_ UMALQURA è 23, non 13.

 

Inoltre, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) e [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) consentono l'uso del valore enum \_ All \_ Calendars per richiedere un'enumerazione di tutti i calendari applicabili.

Valore

Significato

0xFFFFFFFF

ENUMERA \_ tutti i \_ calendari

Tutti i calendari applicabili per le impostazioni locali specificate



 

 

 
