---
description: I tipi di contatori degli algoritmi a lunghezza coda incrementano il numero di elementi in una coda a ogni intervallo di campionamento, come specificato dalla proprietà Frequency appropriata&\# 8212; Frequenza \_ PerfTime e così via.
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: Tipi di contatori degli algoritmi a lunghezza coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06665c2fb8fca014c7d722f0ea22cf7e86833ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226838"
---
# <a name="queue-length-algorithm-counter-types"></a>Tipi di contatori degli algoritmi a lunghezza coda

I tipi di contatori degli algoritmi a lunghezza coda incrementano il numero di elementi in una coda a ogni intervallo di campionamento, come specificato dalla frequenza di proprietà della frequenza appropriata \_ PerfTime e così via. Il risultato cotto divide il numero di campioni per produrre la lunghezza media della coda.

Un esempio è la proprietà **AvgDiskQueueLength** in [**Win32 \_ PerfRawData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md) che usa il contatore delle prestazioni 100 ns tipo di contatore di \_ \_ \_ tipo QUEUELEN \_ .



| Costante CounterType                                                                                                 | Descrizione                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Prestazioni \_ COUNTER \_ QUEUELEN \_ tipo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 4523008<br/>            | Lunghezza media di una coda a una risorsa nel tempo. Mostra la differenza tra le lunghezze di coda osservate durante gli ultimi due intervalli di campionamento divisa per la durata dell'intervallo.                       |
| [Prestazioni \_ CONTATORE \_ di \_ \_ tipo QUEUELEN di grandi dimensioni](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 4523264<br/>     | Lunghezza media di una coda a una risorsa nel tempo. I contatori di questo tipo mostrano la differenza tra le lunghezze di coda osservate durante gli ultimi due intervalli di campionamento, divisa per la durata dell'intervallo. |
| [Prestazioni \_ COUNTER \_ 100 NS \_ QUEUELEN \_ tipo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 5571840<br/>     | Lunghezza media di una coda a una risorsa nel tempo in unità di 100 nanosecondi.                                                                                                                                        |
| [Prestazioni \_ COUNTER \_ obj \_ time \_ QUEUELEN \_ tipo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 6620416<br/> | Tempo in cui un oggetto si trova in una coda.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

