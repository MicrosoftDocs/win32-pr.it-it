---
description: I tipi di contatore dell'algoritmo contatore possono calcolare le frequenze o i byte medi per un campione o per un periodo di tempo per un'operazione specifica.
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: Tipi di contatori dell'algoritmo contatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bd55a2a9cc9cc9193a86ffe740ebfa856c0ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346746"
---
# <a name="counter-algorithm-counter-types"></a>Tipi di contatori dell'algoritmo contatore

I tipi di contatore dell'algoritmo contatore possono calcolare le frequenze o i byte medi per un campione o per un periodo di tempo per un'operazione specifica.

La proprietà **AvgDiskBytesPerTransfer** nella classe [**Win32 \_ PerfRawData \_ perfdisk \_ PhysicalDisk**](/previous-versions//aa394308(v=vs.85)) usa l' \_ CounterType bulk media delle prestazioni \_ . In questo caso, il trasferimento è l'operazione e il numero di byte di accumulo inviati è costituito dai dati del contatore. Per due esempi, dividendo la differenza tra i byte accumulati e la differenza nell'accumulo dei trasferimenti, viene generato il numero medio di byte per trasferimento durante il periodo tra gli esempi.

Sono disponibili gli algoritmi dei contatori seguenti:



| CounterType                                                                                              | Descrizione                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Prestazioni \_ 1073874176 \_ ](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale in blocco medio<br/>       | Numero medio di elementi elaborati durante un'operazione. Questo tipo di contatore visualizza un rapporto tra gli elementi elaborati (ad esempio i byte inviati) e il numero di operazioni completate e richiede una proprietà di base con prestazioni \_ medie di \_ base come tipo di contatore. |
| [Prestazioni \_ Contatore \_ contatore decimale](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))272696320<br/>     | Numero medio di operazioni completate durante ogni secondo dell'intervallo di campionamento. .                                                                                                                                                                          |
| [Prestazioni \_ \_Contatore campione](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 4260864<br/>        | Numero medio di operazioni completate in un secondo. Questo tipo di contatore richiede una proprietà di base con la base di esempio delle prestazioni del tipo di contatore \_ \_ .                                                                                                                   |
| [Prestazioni \_ CONTATORE \_ \_ conteggio bulk numero](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 272696576<br/> | Numero medio di operazioni completate durante ogni secondo dell'intervallo di campionamento. Questo tipo di contatore è identico al \_ \_ tipo di contatore di contatori delle prestazioni, ma usa campi di dimensioni maggiori per contenere valori più grandi.                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

