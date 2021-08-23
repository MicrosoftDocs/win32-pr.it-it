---
description: I tipi di contatore dell'algoritmo contatore possono calcolare le percentuali o le medie dei byte per un campione o per un periodo di tempo per una determinata operazione.
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: Tipi di contatore dell'algoritmo contatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5568d4df0d1b50fd55a4f9d007d6506cf59a8f67a05885c21d64a6be8812536c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131433"
---
# <a name="counter-algorithm-counter-types"></a>Tipi di contatore dell'algoritmo contatore

I tipi di contatore dell'algoritmo contatore possono calcolare le percentuali o le medie dei byte per un campione o per un periodo di tempo per una determinata operazione.

La **proprietà AvgDiskBytesPerTransfer** nella classe [**\_ PerfRawData \_ PerfDisk \_ PhysicalDisk win32**](/previous-versions//aa394308(v=vs.85)) usa il tipo di contatore PERF \_ AVERAGE \_ BULK. In questo caso, il trasferimento è l'operazione e il numero accumulato di byte inviati sono i dati del contatore. Per due esempi, la divisione della differenza di byte accumulati per la differenza nei trasferimenti accumulati produrrà il numero medio di byte per trasferimento durante il periodo tra i campioni.

Vengono forniti gli algoritmi di contatore seguenti:



| CounterType                                                                                              | Descrizione                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ AVERAGE \_ BULK](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 1073874176<br/>       | Numero medio di elementi elaborati durante un'operazione. Questo tipo di contatore visualizza un rapporto tra gli elementi elaborati (ad esempio i byte inviati) e il numero di operazioni completate e richiede una proprietà di base con PERF AVERAGE BASE come \_ \_ tipo di contatore. |
| [PERF \_ COUNTER \_ COUNTER Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))272696320<br/>     | Numero medio di operazioni completate durante ogni secondo dell'intervallo di campionamento. .                                                                                                                                                                          |
| [PERF \_ ESEMPIO \_ COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4260864<br/>        | Numero medio di operazioni completate in un secondo. Questo tipo di contatore richiede una proprietà di base con il tipo di contatore PERF \_ SAMPLE \_ BASE.                                                                                                                   |
| [PERF \_ CONTATOR \_ BULK \_ COUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Numero decimale 272696576<br/> | Numero medio di operazioni completate durante ogni secondo dell'intervallo di campionamento. Questo tipo di contatore è lo stesso del tipo COUNTER PERF, ma usa campi più grandi \_ \_ per contenere valori più grandi.                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

