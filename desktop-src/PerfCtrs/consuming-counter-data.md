---
description: "È possibile utilizzare i dati sulle prestazioni utilizzando una delle interfacce seguenti: l'interfaccia PDH (Performance Data Helper), che fornisce accesso di alto livello ai dati dei provider di contatori delle prestazioni versione 1 e versione 2. Interfaccia del registro di sistema, che fornisce l'accesso di basso livello ai dati dai provider del contatore delle prestazioni. L'interfaccia della libreria delle prestazioni, che consente l'accesso diretto ai dati dai provider del contatore delle prestazioni della versione 2. L'interfaccia PDH è più facile da usare rispetto all'interfaccia del registro di sistema ed è consigliata per la maggior parte delle attività di raccolta dati sulle prestazioni. L'interfaccia PDH è essenzialmente un'astrazione di livello superiore della funzionalità fornita dall'interfaccia del registro di sistema. Usare l'interfaccia della libreria delle prestazioni solo se non è possibile usare le funzioni del livello di astrazione PDH."
ms.assetid: a42f6cdd-47e9-4f43-aeaf-37a5abb0fa36
title: Utilizzo dei dati del contatore
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: c8c50b29d8f898f544b021f7fe3f3fd0d4a2094e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312183"
---
# <a name="consuming-counter-data"></a>Utilizzo dei dati del contatore

I programmi che desiderano leggere e utilizzare i dati dei contatori delle prestazioni di Windows possono utilizzare una delle diverse interfacce appropriate per lo scenario.

- Gli script possono utilizzare le [classi del contatore delle prestazioni WMI](/windows/desktop/WmiSdk/monitoring-performance-data) o lo strumento [typeperf](/windows-server/administration/windows-commands/typeperf) .
- I programmi .NET possono utilizzare la [classe PerformanceCounter](/dotnet/api/system.diagnostics.performancecounter).
- La [libreria PDH (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md) fornisce accesso di alto livello ai dati dai provider di contatori delle prestazioni V1 e V2 tramite un'API Win32 (C/C++).
- L' [interfaccia del registro di sistema](using-the-registry-functions-to-consume-counter-data.md) consente di accedere ai dati dai provider di contatori delle prestazioni V1 e V2 tramite la `HKEY_PERFORMANCE_DATA` chiave del registro di sistema speciale.
- Le [funzioni consumer Perflib V2](using-the-perflib-functions-to-consume-counter-data.md) forniscono accesso di basso livello ai dati dei provider di contatori delle prestazioni V2 tramite un'API Win32 (C/C++).

L'interfaccia PDH è consigliata per la maggior parte delle attività di raccolta dei dati sulle prestazioni di C/C++ perché è più facile da usare rispetto alle interfacce PerfLib e del registro di sistema.
