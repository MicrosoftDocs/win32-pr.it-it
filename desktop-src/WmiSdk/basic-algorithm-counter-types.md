---
description: Rappresenta le differenze tra i campioni nel tempo e spesso usa un valore di base per il calcolo.
ms.assetid: 613268ab-386b-421d-a5b5-aab6a065999c
ms.tgt_platform: multiple
title: Tipi di contatori di algoritmi di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70514c10b2695aa940d48341752ef647dcca9719
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316575"
---
# <a name="basic-algorithm-counter-types"></a>Tipi di contatori di algoritmi di base

I tipi di contatori di base dell'algoritmo rappresentano in genere le differenze tra i campioni nel tempo e spesso utilizzano un valore di base per il calcolo. Ad esempio, la proprietà **PercentFreeSpace** della classe [**Win32 \_ PerfFormattedData \_ perfdisk \_ PhysicalDisk**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) rappresenta il rapporto tra lo spazio libero disponibile nell'unità disco fisico e lo spazio totale utilizzabile fornito dall'unità disco fisica selezionata. Questa classe contiene anche il valore di base, **PercentFreeSpace \_ base**. La percentuale di spazio libero su disco si ottiene dividendo **PercentFreeSpace** per **PercentFreeSpace \_ base** e moltiplicando per il 100%.

Sono disponibili gli algoritmi di base nella tabella seguente.



| Costante CounterType                                                                                    | Descrizione                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Prestazioni \_ Decimale \_ frazione non elaborata](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))537003008<br/>       | Rapporto tra un subset e il relativo set come percentuale. Questo tipo di contatore visualizza solo la percentuale corrente, non una media nel tempo.                                    |
| [Prestazioni \_ \_Frazione di esempio](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 549585920<br/>    | Rapporto medio tra gli accessi e tutte le operazioni durante gli ultimi due intervalli di campionamento. Questo tipo di contatore richiede una proprietà di base con il tipo di contatore di base di esempio delle prestazioni \_ \_ . |
| [Prestazioni \_ CONTATORE \_ Delta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 4195328<br/>        | Questo tipo di contatore mostra la variazione dell'attributo misurato tra i due intervalli di campionamento più recenti.                                                         |
| [Prestazioni \_ CONTATORE \_ \_ Delta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale grande 4195584<br/> | Uguale al \_ contatore \_ delle prestazioni Delta, ma una rappresentazione a 64 bit per valori più grandi.                                                                                        |
| [Prestazioni \_ \_Tempo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale trascorso 807666944<br/>       | Tempo totale tra il momento in cui il processo è stato avviato e l'ora in cui questo valore viene calcolato.                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

