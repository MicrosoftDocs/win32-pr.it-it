---
description: I monitoraggi sono progettati per l'Windows wmi (Management Instrumentation) per la gestione degli eventi nei computer locali o remoti.
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: Monitorare gli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe76ddd8df02694f871899e0b172dda3529fc29c0e16b6b4a65e2ad15bd2ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995481"
---
# <a name="monitor-events"></a>Monitorare gli eventi

I monitoraggi sono progettati per [l'Windows wmi (Management Instrumentation)](/windows/desktop/WmiSdk/wmi-start-page) per la gestione degli eventi nei computer locali o remoti.

> [!Note]  
> Poiché i monitoraggi usano un'acquisizione in tempo reale, possono acquisire dati solo nel computer locale. Si tratta di una limitazione dell'interfaccia **IRTC** del provider di pacchetti di rete. Tuttavia, usando gli eventi WMI, i dati acquisiti possono essere esaminati localmente, mentre gli eventi possono essere inviati a computer locali o remoti.

 

I monitoraggi non comunicano direttamente con WMI. Il [*servizio di controllo di*](m.md) monitoraggio (MCSVC) fornisce un'interfaccia ( denominata [IMonitorEventer](imonitoreventer.md)), che il monitoraggio può usare per ottenere una struttura di dati degli eventi e riempirla con le informazioni pertinenti. MCSVC può quindi inviare la struttura dei dati dell'evento a WMI, che a sua volta genera l'evento.

 

 
