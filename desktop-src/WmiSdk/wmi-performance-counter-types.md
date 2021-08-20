---
description: Il tipo di contatore delle prestazioni definisce una formula necessaria per ottenere i contatori delle prestazioni calcolati. Si tratta degli stessi tipi di contatori usati dal monitoraggio Windows prestazioni.
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: Tipi di contatori delle prestazioni WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3338f67b457b3f28bc94ed38c79c17b30286aa73ec867842154d436a6696cee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118106965"
---
# <a name="wmi-performance-counter-types"></a>Tipi di contatori delle prestazioni WMI

Il tipo [di contatore delle](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) prestazioni definisce una formula necessaria per ottenere i contatori delle prestazioni calcolati. Si tratta degli stessi tipi di contatori usati Windows [monitoraggio delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal). Nelle classi di prestazioni WMI i dati non elaborati per la formula del tipo di contatore provengono da una classe [**\_ Win32 PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e il risultato calcolato si trova nella proprietà con lo stesso nome di una classe [**\_ Win32 PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) corrispondente.

I tipi di contatore vengono visualizzati come qualificatore **CounterType** per le proprietà nelle classi [**\_ Win32 PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e come qualificatore **CookingType** per le proprietà nelle [**classi \_ Win32 PerfFormattedData.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)

Ad esempio, la proprietà **AvgDiskBytesPerRead** nella classe [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) è l'origine dati non elaborata per la proprietà **AvgDiskBytesPerRead** nella classe [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), che contiene gli stessi dati illustrati in Monitoraggio di sistema.

L'elenco seguente organizza le descrizioni dei tipi di contatori in base al tipo funzionale:

-   [Tipi di contatore di base](base-counter-types.md)
-   [Tipi di contatore dell'algoritmo di base](basic-algorithm-counter-types.md)
-   [Tipi di contatore dell'algoritmo contatore](counter-algorithm-counter-types.md)
-   [Tipi di contatore non di riferimento](noncomputational-counter-types.md)
-   [Tipi di contatore dell'algoritmo Precision Timer](precision-timer-algorithm-counter-types.md)
-   [Tipi di contatore dell'algoritmo queue-length](queue-length-algorithm-counter-types.md)
-   [Tipi di contatori statistici](statistical-counter-types.md)
-   [Tipi di contatore dell'algoritmo timer](timer-algorithm-counter-types.md)

 

 
