---
description: Con l'ora di sistema vengono usate le funzioni seguenti.
ms.assetid: 3733f611-c6a1-4d48-b21e-ada3490c5de1
title: Funzioni temporali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1187c029bac34411fdca28dd3b27322478de678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316055"
---
# <a name="time-functions"></a>Funzioni temporali

Con l'ora di sistema vengono usate le funzioni seguenti.



| Funzione                                                                   | Descrizione                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**GetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtime)                                     | Recupera la data e l'ora di sistema corrente in formato UTC.                                              |
| [**GetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment)                 | Determina se il sistema applica rettifiche temporali periodiche al clock del giorno.          |
| [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata)                                    | Formatta un'ora di sistema come stringa temporale per le impostazioni locali specificate.                                         |
| [**NtQuerySystemTime**](/windows/desktop/api/Winternl/nf-winternl-ntquerysystemtime)                             | Restituisce l'ora di sistema.                                                                               |
| [**RtlLocalTimeToSystemTime**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)               | Converte l'ora locale specificata nell'ora di sistema.                                                      |
| [**RtlTimeToSecondsSince1970**](/windows/desktop/api/Winternl/nf-winternl-rtltimetosecondssince1970)             | Converte l'ora di sistema specificata nel numero di secondi trascorsi dal primo secondo del 1 ° gennaio 1970. |
| [**SetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtime)                                     | Imposta la data e l'ora di sistema correnti.                                                                 |
| [**SetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment)                 | Abilita o Disabilita le rettifiche temporali periodiche per l'orologio del sistema di ora del giorno.                       |
| [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)                       | Converte un'ora di sistema in un'ora di file.                                                                 |
| [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) | Converte un'ora UTC nell'ora locale corrispondente del fuso orario specificato.                               |
| [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime) | Converte un'ora locale in un'ora UTC.                                                                   |



 

Le funzioni seguenti vengono utilizzate con l'ora locale.



| Funzione                                                                                           | Descrizione                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-enumdynamictimezoneinformation)                           | Enumera le voci di informazioni sull'ora legale dinamiche archiviate nel registro di sistema.                                                             |
| [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime)                                         | Converte l'ora di un file UTC in un file locale.                                                                                                  |
| [**GetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation)                             | Recupera le impostazioni del fuso orario corrente e dell'ora legale dinamica.                                                                      |
| [**GetDynamicTimeZoneInformationEffectiveYears**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformationeffectiveyears) | Recupera un intervallo, espresso in anni, per il quale [**\_ \_ \_ le informazioni dinamiche sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information) hanno voci valide. |
| [**GetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime)                                                               | Recupera la data e l'ora locali correnti.                                                                                                      |
| [**GetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)                                           | Recupera le impostazioni correnti del fuso orario.                                                                                                       |
| [**GetTimeZoneInformationForYear**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear)                             | Recupera le impostazioni del fuso orario per l'anno e il fuso orario specificati.                                                                          |
| [**RtlLocalTimeToSystemTime**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)                                       | Converte l'ora locale specificata nell'ora di sistema.                                                                                               |
| [**SetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation)                             | Imposta le impostazioni del fuso orario corrente e dell'ora legale dinamica.                                                                           |
| [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime)                                                               | Imposta la data e l'ora locali correnti.                                                                                                           |
| [**SetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation)                                           | Imposta le impostazioni correnti del fuso orario.                                                                                                            |
| [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)                         | Converte un'ora UTC nell'ora locale corrispondente del fuso orario specificato.                                                                        |
| [**SystemTimeToTzSpecificLocalTimeEx**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltimeex)                     | Converte un'ora UTC con le impostazioni dell'ora legale dinamiche nell'ora locale corrispondente del fuso orario.                             |
| [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime)                         | Converte un'ora locale in un'ora UTC.                                                                                                            |
| [**TzSpecificLocalTimeToSystemTimeEx**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtimeex)                     | Converte un'ora locale con le impostazioni di ora legale dinamiche in ora UTC.                                                                   |



 

Le funzioni seguenti vengono utilizzate con l'ora del file.



| Funzione                                                   | Descrizione                                                                                                     |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**CompareFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime)                 | Confronta due volte i file.                                                                                        |
| [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) | Converte l'ora di un file UTC in un file locale.                                                                  |
| [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)       | Converte un file in formato ora di sistema.                                                                     |
| [**GetFileTime ha provocato**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime)                         | Recupera la data e l'ora di creazione del file o della directory specificata, dell'ultimo accesso e dell'Ultima modifica. |
| [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) | Recupera la data e l'ora di sistema corrente in formato UTC.                                                       |
| [**LocalFileTimeToFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-localfiletimetofiletime) | Converte l'ora di un file locale in un file in base all'ora UTC.                                                         |
| [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime)                         | Imposta la data e l'ora in cui è stato creato, ultimo accesso o Ultima modifica la directory o il file specificato.       |
| [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)       | Converte un'ora di sistema in un'ora di file.                                                                          |



 

Le funzioni seguenti vengono utilizzate con la data e l'ora di MS-DOS.



| Funzione                                               | Descrizione                                          |
|--------------------------------------------------------|------------------------------------------------------|
| [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) | Converte i valori di data e ora di MS-DOS in un'ora di file. |
| [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) | Converte l'ora di un file in valori di data e ora di MS-DOS. |



 

Le funzioni seguenti vengono utilizzate con l'ora di Windows.



| Funzione                                 | Descrizione                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) | Recupera le informazioni sull'intervallo di sistema.                                                                  |
| [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount)     | Recupera il numero di millisecondi trascorsi dall'avvio del sistema, fino a 49,7 giorni. |
| [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) | Recupera il numero di millisecondi trascorsi dall'avvio del sistema.                  |



 

Le funzioni seguenti vengono utilizzate con i contatori delle prestazioni ad alta risoluzione.



| Funzione                                                              | Descrizione                                                             |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)     | Recupera il valore corrente del contatore delle prestazioni ad alta risoluzione. |
| [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) | Recupera la frequenza del contatore delle prestazioni ad alta risoluzione.     |



 

Le funzioni seguenti vengono utilizzate con il contatore delle prestazioni ausiliario.



| Funzione                                                                                           | Descrizione                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QueryAuxiliaryCounterFrequency**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryauxiliarycounterfrequency)                           | Esegue una query sulla frequenza dei contatori ausiliari.                                                                                                                                                                      |
| [**ConvertAuxiliaryCounterToPerformanceCounter**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertauxiliarycountertoperformancecounter) | Converte il valore del contatore ausiliario specificato nel valore del contatore delle prestazioni corrispondente. fornisce facoltativamente l'errore di conversione stimato in nanosecondi a causa di latenze e massima possibile deriva. |
| [**ConvertPerformanceCounterToAuxiliaryCounter**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertperformancecountertoauxiliarycounter) | Converte il valore del contatore delle prestazioni specificato nel valore del contatore ausiliario corrispondente; fornisce facoltativamente l'errore di conversione stimato in nanosecondi a causa di latenze e massima possibile deriva. |



 

La funzione seguente viene utilizzata con il tempo di interrupt.



| Funzione                                                                       | Descrizione                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)                               | Ottiene il conteggio corrente del tempo di interrupt.                                                                                                                                                                                                                |
| [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)                 | Ottiene il conteggio del tempo di interrupt corrente, in un formato più preciso rispetto a [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) .                                                                                                                             |
| [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)               | Ottiene il conteggio del tempo di interrupt non distorta corrente. Il numero di interrupt-Time non distorta non include il tempo impiegato dal sistema per la sospensione o l'ibernazione.                                                                                                    |
| [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) | Ottiene il numero corrente di interrupt non distorta, in un formato più preciso rispetto a [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) . Il numero di interrupt-Time non distorta non include il tempo impiegato dal sistema per la sospensione o l'ibernazione. |



 

 

 
