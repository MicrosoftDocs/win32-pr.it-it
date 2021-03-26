---
description: Elenca gli elementi utilizzati con la traccia eventi.
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: Riferimento traccia eventi
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 7e0ee4576b9b9d64a5766c6ab096ea34abc2b176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980575"
---
# <a name="event-tracing-reference"></a>Riferimento traccia eventi

Per scrivere applicazioni che incorporano la traccia eventi, usare gli elementi di programmazione seguenti:

-   [Enumerazioni di traccia eventi](/windows/desktop/api/_etw/#enumerations)
-   [Funzioni di traccia eventi](/windows/desktop/api/_etw/#functions)
-   [Interfacce di traccia eventi](/windows/desktop/api/_etw/#interfaces)
-   [Strutture di traccia eventi](/windows/desktop/api/_etw/#structures)
-   [Costanti di traccia eventi](event-tracing-constants.md)

Per informazioni dettagliate sugli esempi che usano questi elementi di programmazione, vedere [esempi di traccia eventi](event-tracing-samples.md).

Questa sezione contiene anche informazioni su:

-   [Strumenti](event-tracing-tools.md) forniti da ETW
-   [Definizioni di classi MOF](event-tracing-mof-classes.md) per gli eventi del kernel
-   [Qualificatori della classe MOF](event-tracing-mof-qualifiers.md) utilizzati durante la definizione delle classi di evento

## <a name="process-etw-traces-in-net-code"></a>Elaborare tracce ETW nel codice .NET

È anche possibile usare l' [API .NET TraceProcessing](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) per analizzare le tracce ETW per le applicazioni e altri componenti software. Questa API viene utilizzata internamente in Microsoft per analizzare i dati ETW prodotti dal sistema ingegneristico Windows e viene inoltre utilizzata per potenziare diverse tabelle in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer). Questa API è disponibile come pacchetto NuGet.

Per altre informazioni, vedi [questo articolo](/windows/apps/trace-processing/overview).
