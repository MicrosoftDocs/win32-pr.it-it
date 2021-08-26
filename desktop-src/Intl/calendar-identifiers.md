---
description: In questo argomento vengono definiti gli identificatori di calendario (tipo di dati CALID) utilizzati per specificare calendari diversi.
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: Identificatori di calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5f9f21aeff1143c4f981e3bfae20214f1b86e86307f7f32b103a19ef99b9803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083031"
---
# <a name="calendar-identifiers"></a>Identificatori di calendario

In questo argomento vengono definiti gli identificatori di calendario (tipo di dati CALID) utilizzati per specificare calendari diversi. Le applicazioni possono usare questi identificatori quando si usano le funzioni NLS e le funzioni di callback seguenti, che hanno parametri che accettano il tipo di dati CALID:

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



Identificatore del calendario

Significato

1

GREGORIANO \_ CAL

Gregoriano (localizzato)

2

CAL \_ \_ GREGORIANO US

Gregoriano (stringhe in inglese sempre)

3

CAL \_ JAPAN

Japanese Emperor Era

4

CAL \_ TAIWAN

Calendario taiwanese

5

COREA DI \_ CAL

Korean Tangun Era

6

CAL \_ HIJRI

Hijri (lunare arabo)

7

CAL \_ THAI

Thai

8

CAL \_ EBRAICO

Ebraico (lunare)

9

CAL \_ GREGORIAN \_ ME \_ FRENCH

Gregorian Middle East French

10

CAL \_ \_ GREGORIANO ARABO

Gregorian Arabic

11

CAL \_ GREGORIANO \_ XLIT \_ ENGLISH

Inglese traslitterato gregoriano

12

CAL \_ GREGORIANO \_ XLIT \_ FRANCESE

Francese traslitterato gregoriano

23

CAL \_ UMALQURA

**Windows Vista e versioni successive:** Calendario Um Al Qura (lunare arabo)



 

> [!Note]  
> Il divario nella numerazione tra gli identificatori CAL \_ GREGORIAN \_ XLIT \_ FRENCH e CAL \_ UMALQURA è intenzionale. L'elemento designato per CAL \_ UMALQURA è 23, non 13.

 

Inoltre, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) ed [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) consentono l'uso del valore ENUM ALL CALENDARS per richiedere un'enumerazione di tutti i \_ \_ calendari applicabili.

Valore

Significato

0xffffffff

ENUMERAZIONE \_ DI TUTTI \_ I CALENDARI

Tutti i calendari applicabili per le impostazioni locali specificate



 

 

 
