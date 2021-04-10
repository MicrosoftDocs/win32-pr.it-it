---
description: Il tipo di contatore delle prestazioni designa una formula necessaria per ottenere i contatori delle prestazioni calcolati. Si tratta degli stessi tipi di contatori utilizzati dal monitoraggio delle prestazioni di Windows.
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: Tipi di contatori delle prestazioni WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ac0d2c8afb1499fec44c983364b5e3278b864
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131147"
---
# <a name="wmi-performance-counter-types"></a>Tipi di contatori delle prestazioni WMI

Il [tipo di contatore](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) delle prestazioni designa una formula necessaria per ottenere i contatori delle prestazioni calcolati. Si tratta degli stessi tipi di contatori utilizzati dal [monitoraggio delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal)di Windows. Nelle classi di prestazioni WMI, i dati non elaborati per la formula del tipo di contatore provengono da una classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e il risultato calcolato viene trovato nella stessa proprietà denominata di una classe [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) corrispondente.

I tipi di contatore vengono visualizzati come qualificatore **CounterType** per le proprietà nelle classi [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e come qualificatore **CookingType** per le proprietà nelle classi [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .

Ad esempio, la proprietà **AvgDiskBytesPerRead** nella classe [**Win32 \_ PerfRawData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md) è l'origine dati non elaborata per la proprietà **AvgDiskBytesPerRead** nella classe [**Win32 \_ PerfFormattedData \_ perfdisk \_**](./retrieving-raw-and-formatted-performance-data.md)disco logico, che contiene gli stessi dati mostrati in Monitor di sistema.

Nell'elenco seguente vengono organizzate le descrizioni dei tipi di contatore per tipo funzionale:

-   [Tipi di contatori di base](base-counter-types.md)
-   [Tipi di contatori di algoritmi di base](basic-algorithm-counter-types.md)
-   [Tipi di contatori dell'algoritmo contatore](counter-algorithm-counter-types.md)
-   [Tipi di contatori non computazionali](noncomputational-counter-types.md)
-   [Tipi di contatori dell'algoritmo timer di precisione](precision-timer-algorithm-counter-types.md)
-   [Tipi di contatori degli algoritmi a lunghezza coda](queue-length-algorithm-counter-types.md)
-   [Tipi di contatori statistici](statistical-counter-types.md)
-   [Tipi di contatori degli algoritmi timer](timer-algorithm-counter-types.md)

 

 
