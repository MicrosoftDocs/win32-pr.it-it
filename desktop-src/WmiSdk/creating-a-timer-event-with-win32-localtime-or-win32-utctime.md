---
description: È possibile usare il modello standard di eventi intrinseci e filtri eventi in combinazione con le classi Win32 LocalTime o Win32 UTCTime per ricevere \_ una notifica a \_ tempo.
ms.assetid: 89ba41e2-c9b5-4914-b8cb-13d21ff03402
ms.tgt_platform: multiple
title: Creazione di un evento timer con Win32_LocalTime o Win32_UTCTime
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f2dc2c3cbec2b87693920c0ed5ca113f7e6a04c9648f0ef2cc4bca9b4fa90f8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612411"
---
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a>Creazione di un evento timer con Win32 \_ LocalTime o Win32 \_ UTCTime

È possibile usare il modello standard di eventi intrinseci e filtri eventi in combinazione con le [**classi Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) per ricevere una notifica a tempo. Il metodo intrinseco è un modo consigliato per generare eventi a tempo, in quanto è coerente con il resto del modello di eventi Microsoft e supporta condizioni di pianificazione complesse.

Le [**classi Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) e [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) sono classi singleton nello spazio dei nomi \\ cimv2 radice che rappresentano l'orologio di sistema. Quando viene eseguita una query, **Win32 \_ LocalTime** restituisce l'ora corrente al momento del recupero dei dati in un orologio di 24 ore con riferimento locale. La **classe Win32 \_ UTCTime** restituisce l'ora corrente con riferimento UTC.

**Per generare eventi temporici o ripetuti con Win32 \_ LocalTime o Win32 \_ UTCTime**

-   Configurare un filtro eventi di notifica intrinseco [**per Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) che richiede una notifica per una data e un'ora specifiche.

Ad esempio, se l'ora locale in Ora legale è 4:00 e il percorso è GMT -8, quindi [**Win32 \_ LocalTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) restituisce 16 e [**Win32 \_ UTCTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) restituisce 23.

L'esempio di codice seguente descrive come creare un filtro eventi che segnala un evento ripetuto ogni giorno a mezzanotte.

``` syntax
// Win32_LocalTime and Win32_UTCTime reside in root\cimv2 namespace. 
// Defining the EventNamespace allows the filter
// to be compiled in any namespace.
instance of __EventFilter as $FILT1
{
 Name  = "wake-up call";
 Query = "SELECT * FROM __InstanceModificationEvent WHERE "    
 "TargetInstance ISA \"Win32_LocalTime\" AND "
 "TargetInstance.Hour = 0 AND TargetInstance.Minute = 0 AND "
 "TargetInstance.Second = 0";
 QueryLanguage = "WQL";
 EventNamespace = "root\\cimv2";
};
```

 

 
