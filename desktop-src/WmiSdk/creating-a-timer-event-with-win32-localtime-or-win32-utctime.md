---
description: È possibile usare il modello standard di eventi intrinseci e filtri eventi in combinazione con le \_ classi Win32 LocalTime o Win32 \_ UTCTime per ricevere una notifica temporizzata.
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
ms.openlocfilehash: 011b2270a80f6b632e832f77e8e7c528228801b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233467"
---
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a>Creazione di un evento timer con Win32 \_ LocalTime o Win32 \_ UTCTime

È possibile usare il modello standard di eventi intrinseci e filtri eventi in combinazione con le classi [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) per ricevere una notifica temporizzata. Il metodo intrinseco è una modalità consigliata per la generazione di eventi temporizzati, in quanto è coerente con il resto del modello di eventi Microsoft e supporta condizioni di pianificazione complesse.

Le classi [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) e [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) sono classi singleton nello \\ spazio dei nomi CIMV2 radice che rappresentano il clock di sistema. Quando viene eseguita una query, **Win32 \_ localtime** restituisce l'ora corrente al momento del recupero dei dati in un orario a 24 ore con riferimento locale. La classe **Win32 \_ UTCTime** restituisce l'ora corrente con riferimento UTC.

**Per generare eventi temporizzati o ripetuti con Win32 \_ LocalTime o Win32 \_ UTCTime**

-   Configurare un filtro eventi di notifica intrinseco per [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [**\_ UTCTime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) che richiede la notifica per una data e un'ora specifiche.

Ad esempio, se l'ora locale in ora legale è di 4 ore il percorso è GMT-8, quindi [**Win32 \_ localtime. hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) restituisce 16 e [**Win32 \_ UTCTime. hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) restituisce 23.

Nell'esempio di codice seguente viene illustrato come creare un filtro eventi che segnali un evento ripetuto ogni giorno a mezzanotte.

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

 

 
