---
description: Mentre il sistema usa l'ora basata su UTC internamente, le applicazioni visualizzano in genere l'ora locale, ovvero la data e l'ora del giorno per il fuso orario.
ms.assetid: a6570ec5-ac77-427a-86d9-32cbecc62e37
title: Ora locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95835b76f09ae328c3e1509da68e0fbd989286b2e2669efc9f2280dbce72e35a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764000"
---
# <a name="local-time"></a>Ora locale

Anche se il sistema usa l'ora basata su UTC internamente, le applicazioni visualizzano in genere l'ora **locale,** ovvero la data e l'ora del giorno per il fuso orario. Pertanto, per garantire risultati corretti, è necessario sapere se una funzione prevede di ricevere un'ora basata su UTC o un'ora locale e se la funzione restituisce un'ora basata su UTC o un'ora locale.

Le impostazioni correnti del fuso orario controllano il modo in cui il sistema esegue la conversione tra l'ora UTC e l'ora locale. È possibile recuperare le impostazioni correnti del fuso orario usando la [**funzione GetTimeZoneInformation.**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation) La funzione copia il risultato in una struttura [**TIME \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) e restituisce un valore che indica se l'ora locale si trova attualmente nell'ora solare o nell'ora legale . È possibile impostare le impostazioni del fuso orario usando la [**funzione SetTimeZoneInformation.**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation) Per supportare i limiti per l'ora legale che cambiano da anno a anno, usare le [**funzioni GetTimeZoneInformationForYear**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear), [**GetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation) e [**SetDynamicTimeZoneInformation.**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation)

Per recuperare l'ora locale, usare la [**funzione GetLocalTime.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime) **GetLocalTime** converte l'ora di sistema in un'ora locale in base alle impostazioni correnti del fuso orario e copia il risultato in una [**struttura SYSTEMTIME.**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) È possibile impostare l'ora di sistema usando la [**funzione SetLocalTime.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime) **SetLocalTime presuppone** che sia stata specificata un'ora locale ed esegue la conversione in formato UTC prima di impostare l'ora di sistema.

Quando si chiama [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime), il sistema usa le informazioni sul fuso orario corrente, inclusa l'impostazione dell'ora legale, per eseguire la conversione. Si noti che il sistema usa l'impostazione dell'ora legale dell'ora corrente, non la nuova ora impostata. Pertanto, per garantire il risultato corretto, chiamare **SetLocalTime** una seconda volta, ora che la prima chiamata ha aggiornato l'impostazione dell'ora legale.

Per convertire un'ora basata su UTC in un'ora locale, usare la [**funzione SystemTimeToTzSpecificLocalTime.**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) Per convertire un'ora locale in un'ora basata su UTC, usare la [**funzione TzSpecificLocalTimeToSystemTime.**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime)

 

 
