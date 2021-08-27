---
description: Elenca gli elementi utilizzati con la traccia eventi.
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: Informazioni di riferimento sulla traccia eventi
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 20aaf59de3419b4015f03b38db69839b6f258ccd561b1e918694396e875ae5a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083281"
---
# <a name="event-tracing-reference"></a>Informazioni di riferimento sulla traccia eventi

Usare gli elementi di programmazione seguenti per scrivere applicazioni che incorporano la traccia eventi:

-   [Enumerazioni di traccia eventi](/windows/desktop/api/_etw/#enumerations)
-   [Funzioni di traccia eventi](/windows/desktop/api/_etw/#functions)
-   [Interfacce di traccia eventi](/windows/desktop/api/_etw/#interfaces)
-   [Strutture di traccia eventi](/windows/desktop/api/_etw/#structures)
-   [Costanti di traccia eventi](event-tracing-constants.md)

Per informazioni dettagliate sugli esempi che usano questi elementi di programmazione, vedere [Event Tracing Samples](event-tracing-samples.md).

Questa sezione contiene anche informazioni su:

-   [Strumenti](event-tracing-tools.md) forniti da ETW
-   [Definizioni di classi MOF](event-tracing-mof-classes.md) per gli eventi del kernel
-   [Qualificatori di classe MOF](event-tracing-mof-qualifiers.md) usati durante la definizione delle classi di evento

## <a name="process-etw-traces-in-net-code"></a>Elaborare tracce ETW nel codice .NET

È anche possibile usare [l'API TraceProcessing .NET](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) per analizzare le tracce ETW per le applicazioni e altri componenti software. Questa API viene usata internamente in Microsoft per analizzare i dati ETW generati dal sistema di progettazione Windows e viene usata anche per creare più tabelle in [Windows analizzatore prestazioni](/windows-hardware/test/wpt/windows-performance-analyzer). Questa API è disponibile come pacchetto NuGet distribuzione.

Per altre informazioni, vedi [questo articolo](/windows/apps/trace-processing/overview).
