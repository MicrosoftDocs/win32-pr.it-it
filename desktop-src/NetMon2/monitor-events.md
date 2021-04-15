---
description: I monitoraggi sono progettati per utilizzare Strumentazione gestione Windows (WMI) per attivare eventi in computer locali o remoti.
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: Monitorare gli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98241081d8a59c33ab173447eaedd903e72eb09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485148"
---
# <a name="monitor-events"></a>Monitorare gli eventi

I monitoraggi sono progettati per utilizzare [Strumentazione gestione Windows](/windows/desktop/WmiSdk/wmi-start-page) (WMI) per attivare eventi in computer locali o remoti.

> [!Note]  
> Poiché i monitoraggi utilizzano un'acquisizione in tempo reale, possono solo acquisire i dati nel computer locale. Si tratta di una limitazione dell'interfaccia **IRTC** del provider di pacchetti di rete. Tuttavia, utilizzando gli eventi WMI, i dati acquisiti possono essere esaminati localmente mentre gli eventi possono essere inviati a computer locali o remoti.

 

I monitoraggi non comunicano direttamente con WMI. Il [*servizio di controllo di monitoraggio*](m.md) (MCSVC) fornisce un'interfaccia (denominata [IMonitorEventer](imonitoreventer.md)), che può essere usata dal monitoraggio per ottenere una struttura di dati degli eventi e riempirla con le informazioni rilevanti. MCSVC può quindi inviare la struttura dei dati dell'evento a WMI, che a sua volta genera l'evento.

 

 
