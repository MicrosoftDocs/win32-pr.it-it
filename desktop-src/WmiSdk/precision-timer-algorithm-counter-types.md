---
description: I tipi di contatore dell'algoritmo del timer di precisione ottengono letture più accurate rispetto ai timer di sistema.
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: Tipi di contatori dell'algoritmo Precision Timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137d136db0b4dd579dfec4673b09ce216bef4042d9356b3938b79e7817e3d83a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131033"
---
# <a name="precision-timer-algorithm-counter-types"></a>Tipi di contatori dell'algoritmo Precision Timer

I tipi di contatore dell'algoritmo del timer di precisione ottengono letture più accurate rispetto ai timer di sistema. Il servizio che fornisce i dati fornisce anche un timestamp, che elimina gli errori che possono verificarsi a causa del tempo ridotto e variabile trascorso tra l'acquisizione del timestamp di sistema e la raccolta dei dati dalla DLL delle prestazioni. Questo timestamp di base per i timer di precisione è una proprietà \_ PERF PRECISION TIMESTAMP, che deve seguire immediatamente la proprietà \_ PERF PRECISION \_ \_ TIMER.



| Costante CounterType                                                                                         | Descrizione                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ PRECISION \_ SYSTEM \_ TIMER Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))541525248<br/> | Simile a PERF \_ COUNTER TIMER, ad eccezione del fatto che usa una base temporale definita dal \_ contatore anziché il timestamp di sistema.             |
| [PERF \_ PRECISION \_ 100NS \_ TIMER Decimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))542573824<br/>  | Simile a PERF 100NSEC TIMER, ad eccezione del fatto che usa una base temporale definita dal contatore \_ \_ 100ns anziché il timestamp 100ns di sistema. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

