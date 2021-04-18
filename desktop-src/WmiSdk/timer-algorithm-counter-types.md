---
description: I tipi di contatori degli algoritmi timer sono basati sulla quantità di utilizzo maggiore dell'oggetto prestazioni in un periodo di campionamento.
ms.assetid: 4ec49efc-2b0f-4205-8b58-fb121da32b4e
ms.tgt_platform: multiple
title: Tipi di contatori degli algoritmi timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee815e6740c8736d0a7f2194b25e521368bbe96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318854"
---
# <a name="timer-algorithm-counter-types"></a>Tipi di contatori degli algoritmi timer

I tipi di contatori degli algoritmi timer sono basati sulla quantità di utilizzo maggiore dell'oggetto prestazioni in un periodo di campionamento. I dati del contatore sono una misura quantistica crescente dell'attività totale per un oggetto fino al momento in cui viene preso l'esempio. La differenza tra i due esempi indica il tempo totale durante il quale l'oggetto è attivo durante l'intervallo di campionamento.

La divisione in base al periodo di campionamento comporta una percentuale di tempo in cui l'oggetto è attivo durante un periodo di tempo. La divisione per il numero di interrupt di polling interni determina l'utilizzo medio tra gli esempi di polling.

Ad esempio, la proprietà **AvgDiskSecPerRead** nella classe [**Win32 \_ PerfRawData \_ perfdisk \_ PhysicalDisk**](/previous-versions//aa394308(v=vs.85)) usa il **\_ \_ timer medio delle prestazioni** CounterType. Calcola il tempo medio in secondi di una lettura di dati dal disco e richiede la proprietà di base **AvgDiskSecPerRead \_ base**. A differenza **del \_ \_ timer del contatore delle prestazioni**, la base del timer medio rappresenta un numero di operazioni di accumulo e i dati del contatore sono un valore di tempo di esecuzione, il che significa che, una volta diviso per la base temporale, viene restituito il tempo totale di tutte le operazioni in secondi.



| Costante tipo di contatore                                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_timer contatore \_ prestazioni](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimale 541132032<br/>             | Tempo medio durante il quale un componente è attivo come percentuale del tempo di campionamento totale.<br/>                                                                                                                                                                                                                                                                                                         |
| [\_timer contatore \_ prestazioni \_ inv](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimale 557909248<br/>        | Percentuale media di tempo osservata durante l'intervallo di campionamento che l'oggetto non è attivo. Questo tipo di contatore è identico a **Perf \_ 100NSEC \_ timer \_ inv** , ad eccezione del fatto che misura il tempo in unità di cicli del timer delle prestazioni del sistema anziché in unità 100 ns.<br/>                                                                                                                       |
| [\_timer medio \_ prestazioni](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimale 805438464<br/>             | Tempo medio per il completamento di un processo o di un'operazione. Questo tipo di contatore visualizza un rapporto tra il tempo totale trascorso dell'intervallo di campionamento e il numero di processi o operazioni completate durante tale periodo di tempo.<br/> Questo tipo di contatore richiede una proprietà di base con **prestazioni \_ medie di \_ base** come tipo di contatore.<br/>                                                                         |
| [\_Timer 100NSEC \_ perf](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimale 542180608<br/>             | Tempo attivo di un componente come percentuale del tempo totale trascorso in unità di 100 ns dell'intervallo di campionamento.<br/>                                                                                                                                                                                                                                                                          |
| [\_Timer di 100NSEC Perf \_ \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimale 558957824<br/>        | Percentuale di tempo in cui l'oggetto non è stato utilizzato. Questo tipo di contatore è identico **al \_ timer del contatore \_ \_** delle prestazioni, ad eccezione del fatto che misura il tempo in unità 100 ns anziché nei cicli del timer delle prestazioni di sistema.<br/>                                                                                                                                                                                   |
| [\_contatore prestazioni \_ \_ multitimer](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimale 574686464<br/>      | Tempo attivo di uno o più componenti come percentuale del tempo totale dell'intervallo di campionamento. Questo tipo di contatore differisce **da \_ Perf \_ 100NSEC \_ multitimer** in quanto misura il tempo in unità di cicli del timer delle prestazioni di sistema, invece che in unità 100 ns.<br/> Questo tipo di contatore richiede una proprietà di base con il contatore delle prestazioni per il tipo di contatore **\_ \_ \_ multibase** .<br/>        |
| [\_contatore delle \_ prestazioni \_ multitimer \_ inv](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimale 591463680<br/> | Tempo inattivo di uno o più componenti come percentuale del tempo totale dell'intervallo di campionamento. Questo tipo di contatore è diverso **da \_ Perf \_ 100NSEC \_ multitimer \_ inv** in quanto misura il tempo in unità di cicli del timer delle prestazioni di sistema, invece che in unità 100 ns.<br/> Questo tipo di contatore richiede una proprietà di base con il contatore delle prestazioni per il tipo di contatore **\_ \_ \_ multibase** .<br/> |
| [PRESTAZIONI \_ 100NSEC \_ \_ multitimer](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimale 575735040<br/>      | Questo tipo di contatore mostra il tempo attivo di uno o più componenti come percentuale del tempo totale (unità 100 ns) dell'intervallo di campionamento.<br/> Questo tipo di contatore richiede una proprietà di base con il contatore delle prestazioni per il tipo di contatore **\_ \_ \_ multibase** .<br/>                                                                                                                                     |
| [PERF \_ 100NSEC \_ \_ multitimer \_ inv](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimale 592512256<br/> | Tempo inattivo di uno o più componenti come percentuale del tempo totale dell'intervallo di campionamento. I contatori di questo tipo misurano il tempo in unità 100 ns.<br/> Questo tipo di contatore richiede una proprietà di base con il contatore delle prestazioni per il tipo di contatore **\_ \_ \_ multibase** .<br/>                                                                                                                          |
| [\_ \_ timer ora obj \_ perf](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimale 543229184<br/>           | Timer a 64 bit nelle unità specifiche dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

