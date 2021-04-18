---
description: Per utilizzare i dati del contatore, vedere Utilizzo dei dati del contatore.
ms.assetid: fff8bc4a-3d7a-4d70-ba03-347f9f063c84
title: Utilizzo dei contatori delle prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: abc055a34f0937e056d1d983354fc0a3edf182a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312075"
---
# <a name="using-performance-counters"></a>Utilizzo dei contatori delle prestazioni

**I consumer** del contatore delle prestazioni sono componenti software che raccolgono e usano i dati dei contatori delle prestazioni. I consumer di esempio forniti da Microsoft includono Performance Monitor (perfmon.exe), Monitoraggio risorse (resmon.exe), gestione log (logman.exe) e typeperf.exe. I componenti software di terze parti possono inoltre raccogliere dati sulle prestazioni tramite le API di raccolta prestazioni o tramite le classi del contatore delle prestazioni WMI.

I **provider** di contatori delle prestazioni sono componenti software che pubblicano i dati dei contatori delle prestazioni. I contatori delle prestazioni possono essere forniti da componenti del sistema operativo, driver di dispositivo e servizi. Molti contatori delle prestazioni vengono forniti come parte del sistema operativo Windows. I contatori aggiuntivi possono essere forniti da componenti software di terze parti tramite le API del provider del contatore delle prestazioni.

- Utilizzare [gli strumenti del contatore delle prestazioni](performance-counters-tools.md) quando si desidera raccogliere o visualizzare i dati dei contatori da un sistema.
- Utilizzare le [API di consumer del contatore delle prestazioni](consuming-counter-data.md) quando si desidera scrivere un programma che raccoglie i dati dei contatori dal sistema locale.
- Utilizzare [le classi del contatore delle prestazioni WMI](/windows/desktop/WmiSdk/monitoring-performance-data) quando si desidera raccogliere i dati dei contatori da un sistema locale o remoto utilizzando WMI.
- Utilizzare le [API del provider del contatore delle prestazioni](providing-counter-data.md) quando si desidera pubblicare i dati dei contatori delle prestazioni dal componente software.

## <a name="see-also"></a>Vedi anche

[Informazioni sui contatori delle prestazioni](about-performance-counters.md)

[Riferimento ai contatori delle prestazioni](performance-counters-reference.md)
