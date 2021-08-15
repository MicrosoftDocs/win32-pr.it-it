---
description: I tipi di contatore dell'algoritmo queue-length incrementano il numero di elementi in una coda a ogni intervallo di campionamento, come specificato dalla proprietà frequency appropriata&\# 8212; Frequency \_ PerfTime e così via.
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: Tipi di contatori degli algoritmi di lunghezza della coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9fd3019e9a5e7150402266fd206d3f460f3d0ae3b07f4c6c7d51e82473e9dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316538"
---
# <a name="queue-length-algorithm-counter-types"></a>Tipi di contatori degli algoritmi di lunghezza della coda

I tipi di contatore dell'algoritmo queue-length incrementano il numero di elementi in una coda a ogni intervallo di campionamento, come specificato dalla proprietà frequency appropriata Frequency \_ PerfTime e così via. Il risultato positivo divide per il numero di campioni per produrre la lunghezza media della coda.

Un esempio è la proprietà **AvgDiskQueueLength** in [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) che usa il tipo di contatore PERF \_ COUNTER \_ 100NS \_ QUEUELEN \_ TYPE.



| Costante CounterType                                                                                                 | Descrizione                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ COUNTER \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008<br/>            | Lunghezza media di una coda in una risorsa nel tempo. Mostra la differenza tra le lunghezze di coda osservate durante gli ultimi due intervalli di campionamento divisa per la durata dell'intervallo.                       |
| [PERF \_ COUNTER \_ LARGE \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523264<br/>     | Lunghezza media di una coda in una risorsa nel tempo. I contatori di questo tipo mostrano la differenza tra le lunghezze di coda osservate durante gli ultimi due intervalli di campionamento, divisa per la durata dell'intervallo. |
| [PERF \_ COUNTER \_ 100NS \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840<br/>     | Lunghezza media di una coda per una risorsa nel tempo in unità di 100 nanosecondi.                                                                                                                                        |
| [PERF \_ COUNTER \_ OBJ \_ TIME \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 6620416<br/> | Ora in cui un oggetto si trova in una coda.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

