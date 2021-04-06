---
description: I tipi di contatori dell'algoritmo timer di precisione ottengono letture più accurate rispetto ai timer di sistema.
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: Tipi di contatori dell'algoritmo timer di precisione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a8864587fedc915678dfa4a9e578ca051e1262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759770"
---
# <a name="precision-timer-algorithm-counter-types"></a>Tipi di contatori dell'algoritmo timer di precisione

I tipi di contatori dell'algoritmo timer di precisione ottengono letture più accurate rispetto ai timer di sistema. Il servizio che fornisce i dati fornisce anche un timestamp, che elimina gli errori che possono verificarsi a causa del tempo ridotto e variabile che trascorre tra l'acquisizione del timestamp di sistema e la raccolta dei dati dalla DLL di prestazioni. Questo timestamp di base per i timer di precisione è una \_ \_ proprietà timestamp precisione prestazioni, che deve seguire immediatamente la \_ \_ Proprietà Timer precisione prestazioni.



| Costante CounterType                                                                                         | Descrizione                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Prestazioni \_ \_ \_ Timer di sistema precisione](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 541525248<br/> | Simile al \_ \_ timer del contatore delle prestazioni, con la differenza che usa una base temporale definita dal contatore anziché il timestamp di sistema.             |
| [Prestazioni \_ PRECISIONE \_ 100 NS \_ timer](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 542573824<br/>  | Simile al \_ timer perf 100NSEC \_ , ad eccezione del fatto che usa una base di tempo definita per il contatore 100 ns anziché il timestamp del 100 NS di sistema. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

