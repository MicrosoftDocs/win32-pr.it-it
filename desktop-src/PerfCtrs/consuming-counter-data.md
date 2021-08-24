---
description: "È possibile utilizzare i dati sulle prestazioni usando una delle interfacce seguenti: l'interfaccia PDH (Performance Data Helper), che fornisce accesso di alto livello ai dati da provider di contatori delle prestazioni sia della versione 1 che della versione 2. Interfaccia del Registro di sistema, che fornisce l'accesso di basso livello ai dati dai provider dei contatori delle prestazioni. Interfaccia della libreria delle prestazioni, che fornisce l'accesso diretto ai dati dai provider dei contatori delle prestazioni della versione 2. L'interfaccia PDH è più facile da usare rispetto all'interfaccia del Registro di sistema ed è consigliata per la maggior parte delle attività di raccolta dei dati sulle prestazioni. L'interfaccia PDH è essenzialmente un'astrazione di livello superiore della funzionalità fornita dall'interfaccia del Registro di sistema. Usare l'interfaccia della libreria delle prestazioni solo se non è possibile usare le funzioni del livello di astrazione PDH."
ms.assetid: a42f6cdd-47e9-4f43-aeaf-37a5abb0fa36
title: Utilizzo dei dati dei contatori
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: f3abcc6dd5a385ebffdc887516613efb76b53359e5f8995bc28ba7f6239187b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775681"
---
# <a name="consuming-counter-data"></a>Utilizzo dei dati dei contatori

I programmi che vogliono leggere e usare i dati Windows contatore delle prestazioni possono usare una delle diverse interfacce appropriate per lo scenario.

- Gli script possono usare le [classi dei contatori delle prestazioni WMI](/windows/desktop/WmiSdk/monitoring-performance-data) o lo strumento [TypePerf.](/windows-server/administration/windows-commands/typeperf)
- I programmi .NET possono usare [la classe PerformanceCounter](/dotnet/api/system.diagnostics.performancecounter).
- La [libreria PDH (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md) fornisce accesso di alto livello ai dati dai provider di contatori delle prestazioni V1 e V2 tramite un'API Win32 (C/C++).
- [L'interfaccia del Registro di](using-the-registry-functions-to-consume-counter-data.md) sistema fornisce l'accesso ai dati dai provider di contatori delle prestazioni V1 e V2 tramite la chiave speciale del Registro di `HKEY_PERFORMANCE_DATA` sistema.
- Le [funzioni consumer PerfLib V2](using-the-perflib-functions-to-consume-counter-data.md) forniscono accesso di basso livello ai dati dai provider di contatori delle prestazioni V2 tramite un'API Win32 (C/C++).

L'interfaccia PDH è consigliata per la maggior parte delle attività di raccolta dei dati sulle prestazioni C/C++ perché è più facile da usare rispetto alle interfacce Registry e PerfLib.
