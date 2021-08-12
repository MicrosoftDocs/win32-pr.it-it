---
description: I tipi di contatori dell'algoritmo Timer si basano sulla quantità di utilizzo maggiore dell'oggetto prestazione in un periodo di campionamento.
ms.assetid: 4ec49efc-2b0f-4205-8b58-fb121da32b4e
ms.tgt_platform: multiple
title: Tipi di contatori dell'algoritmo Timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e3a606babb005eca7f01f75f735cd6d6a9da29c9c1427c56614c318f9465f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554015"
---
# <a name="timer-algorithm-counter-types"></a>Tipi di contatori dell'algoritmo Timer

I tipi di contatori dell'algoritmo Timer si basano sulla quantità di utilizzo maggiore dell'oggetto prestazione in un periodo di campionamento. I dati del contatore sono una misura quantistica crescente dell'attività totale per un oggetto fino al momento in cui si verifica il campione. La differenza tra i due campioni indica il tempo totale in cui l'oggetto è attivo durante il periodo di tempo di campionamento.

La divisione per il periodo di campionamento comporta una percentuale di tempo in cui l'oggetto è attivo durante un periodo di tempo. La divisione per il numero di interrupt di polling interni determina l'utilizzo medio tra i campioni di polling.

Ad esempio, la **proprietà AvgDiskSecPerRead** nella classe [**\_ \_ PerfRawData PerfDisk \_ PhysicalDisk di Win32**](/previous-versions//aa394308(v=vs.85)) usa il tipo di contatore **PERF AVERAGE \_ \_ TIMER.** Calcola il tempo medio in secondi di una lettura dei dati dal disco e richiede la proprietà di base **AvgDiskSecPerRead \_ Base.** A differenza di **PERF \_ COUNTER \_ TIMER,** la base media del timer rappresenta un numero accumulato di operazioni e i dati del contatore sono un valore di tempo di esecuzione, il che significa che, quando diviso per la base temporale, produce il tempo totale di tutte le operazioni in secondi.



| Costante del tipo di contatore                                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TIMER \_ CONTATORE \_ PRESTAZIONI](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Numero 541132032<br/>             | Tempo medio in cui un componente è attivo come percentuale del tempo di campionamento totale.<br/>                                                                                                                                                                                                                                                                                                         |
| [INV \_ TIMER \_ \_ CONTATORE PRESTAZIONI](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Numero 557909248<br/>        | Percentuale media di tempo osservata durante l'intervallo di campionamento in cui l'oggetto non è attivo. Questo tipo di contatore è identico a **PERF \_ 100NSEC \_ TIMER \_ INV,** ad eccezione del fatto che misura il tempo in unità di tick del timer delle prestazioni di sistema anziché in unità 100n.<br/>                                                                                                                       |
| [TIMER MEDIO \_ \_ PERF](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Numero 805438464<br/>             | Tempo medio necessario per completare un processo o un'operazione. Questo tipo di contatore visualizza un rapporto tra il tempo trascorso totale dell'intervallo di campionamento e il numero di processi o operazioni completate durante tale periodo.<br/> Questo tipo di contatore richiede una proprietà di base **con PERF \_ AVERAGE \_ BASE** come tipo di contatore.<br/>                                                                         |
| [PERF \_ 100NSEC \_ TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Numero 542180608<br/>             | Tempo attivo di un componente come percentuale del tempo totale trascorso in unità di 100 giorni dell'intervallo di campionamento.<br/>                                                                                                                                                                                                                                                                          |
| [PERF \_ 100NSEC \_ TIMER \_ INV](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Numero 558957824<br/>        | Percentuale di tempo in cui l'oggetto non è stato utilizzato. Questo tipo di contatore è identico a **PERF \_ COUNTER TIMER \_ \_ INV,** ad eccezione del fatto che misura il tempo in unità 100n anziché in tick timer delle prestazioni di sistema.<br/>                                                                                                                                                                                   |
| [TIMER \_ MULTI-TIMER \_ DEL \_ CONTATORE DELLE PRESTAZIONI](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Numero 574686464<br/>      | Tempo attivo di uno o più componenti come percentuale del tempo totale dell'intervallo di campionamento. Questo tipo di contatore è diverso da **PERF \_ 100NSEC \_ MULTI \_ TIMER** in quanto misura il tempo in unità di tick del timer delle prestazioni di sistema, anziché in unità 100n.<br/> Questo tipo di contatore richiede una proprietà di base con **il tipo di contatore PERF \_ COUNTER MULTI \_ \_ BASE.**<br/>        |
| [CONTATORE \_ PRESTAZIONI MULTI TIMER \_ \_ \_ INV](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Numero 591463680<br/> | Tempo di inattività di uno o più componenti come percentuale del tempo totale dell'intervallo di campionamento. Questo tipo di contatore è diverso da **PERF \_ 100NSEC \_ MULTI TIMER \_ \_ INV** in quanto misura il tempo in unità di tick del timer delle prestazioni del sistema, anziché in unità 100n.<br/> Questo tipo di contatore richiede una proprietà di base con **il tipo di contatore PERF \_ COUNTER MULTI \_ \_ BASE.**<br/> |
| [PERF \_ 100NSEC \_ MULTI \_ TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Numero 575735040<br/>      | Questo tipo di contatore mostra il tempo attivo di uno o più componenti come percentuale del tempo totale (100 unità) dell'intervallo di campionamento.<br/> Questo tipo di contatore richiede una proprietà di base con **il tipo di contatore PERF \_ COUNTER MULTI \_ \_ BASE.**<br/>                                                                                                                                     |
| [PERF \_ 100NSEC \_ MULTI \_ TIMER \_ INV](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Numero 592512256<br/> | Tempo di inattività di uno o più componenti come percentuale del tempo totale dell'intervallo di campionamento. I contatori di questo tipo misurano il tempo in unità 100ns.<br/> Questo tipo di contatore richiede una proprietà di base con **il tipo di contatore PERF \_ COUNTER MULTI \_ \_ BASE.**<br/>                                                                                                                          |
| [TIMER TEMPORALE \_ OBJ \_ \_ PERF](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Numero 543229184<br/>           | Timer a 64 bit in unità specifiche dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

