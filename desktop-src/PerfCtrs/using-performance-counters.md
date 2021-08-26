---
description: Per utilizzare i dati dei contatori, vedere Utilizzo dei dati dei contatori.
ms.assetid: fff8bc4a-3d7a-4d70-ba03-347f9f063c84
title: Utilizzo dei contatori delle prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 18bb017a34fb23188c20e81bce28c171c50dcb4d43cd52d458e92be99b7d03a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033211"
---
# <a name="using-performance-counters"></a>Utilizzo dei contatori delle prestazioni

I consumer **dei contatori** delle prestazioni sono componenti software che raccolgono e usano i dati dei contatori delle prestazioni. Gli esempi di consumer forniti da Microsoft includono Monitor prestazioni (perfmon.exe), Monitoraggio risorse (resmon.exe), Log Manager (logman.exe) e typeperf.exe. I componenti software di terze parti possono anche raccogliere dati sulle prestazioni tramite API di raccolta delle prestazioni o tramite classi di contatori delle prestazioni WMI.

I provider di **contatori delle** prestazioni sono componenti software che pubblicano i dati dei contatori delle prestazioni. I contatori delle prestazioni possono essere forniti da componenti del sistema operativo, driver di dispositivo e servizi. Molti contatori delle prestazioni vengono forniti come parte del Windows operativo. I componenti software di terze parti possono fornire contatori aggiuntivi tramite le API del provider di contatori delle prestazioni.

- Usare [gli strumenti del contatore](performance-counters-tools.md) delle prestazioni quando si desidera raccogliere o visualizzare i dati dei contatori da un sistema.
- Usare [le API consumer del contatore delle prestazioni](consuming-counter-data.md) quando si vuole scrivere un programma che raccoglie i dati dei contatori dal sistema locale.
- Usare [le classi di contatori delle](/windows/desktop/WmiSdk/monitoring-performance-data) prestazioni WMI quando si vogliono raccogliere dati dei contatori da un sistema locale o remoto tramite WMI.
- Usare [le API del provider di contatori delle prestazioni](providing-counter-data.md) quando si vogliono pubblicare i dati dei contatori delle prestazioni dal componente software.

## <a name="see-also"></a>Vedi anche

[Informazioni sui contatori delle prestazioni](about-performance-counters.md)

[Informazioni di riferimento per i contatori delle prestazioni](performance-counters-reference.md)
