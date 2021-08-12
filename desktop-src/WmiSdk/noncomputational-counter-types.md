---
description: Ai tipi di contatore non di calcolo non è associata una formula. Il valore non elaborato è direttamente significativo.
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Tipi di contatore non di tipo non numerico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a05da34058ceeb99ab60d8cc3d4f72cb3eec85194e48bb707a929eb2f68aa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555161"
---
# <a name="noncomputational-counter-types"></a>Tipi di contatore non di tipo non numerico

Ai tipi di contatore non di calcolo non è associata una formula. Il valore non elaborato è direttamente significativo.

La **proprietà FilesToBeIndexed** nella [**classe Win32 \_ PerfRawData \_ ContentIndex \_ IndexingService**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) è un esempio del tipo di contatore **PERF COUNTER \_ \_ RAWCOUNT.** Contiene un numero di file che non sono stati indicizzati.

I tipi di contatore sono designati dalla costante definita in Winperf.h in Microsoft Windows Software Development Kit (SDK). Nella tabella seguente sono elencati i tipi di contatore non di riferimento forniti.



| CounterType                                                                                                 | Descrizione                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ COUNTER \_ TEXT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 2816<br/>                | Questo tipo di contatore mostra una stringa di testo a lunghezza variabile in Unicode. Non visualizza i valori calcolati.               |
| [PERF \_ COUNTER \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65536<br/>           | Valore del contatore non elaborato che non richiede calcoli e rappresenta un campione che è solo l'ultimo valore osservato. |
| [PERF \_ COUNTER \_ LARGE \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792<br/>    | Uguale a **PERF \_ COUNTER \_ RAWCOUNT,** ma rappresentazione a 64 bit per valori più grandi.                                    |
| [PERF \_ CONTATORE \_ RAWCOUNT \_ HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0<br/>                  | Valore osservato più di recente in formato esadecimale. Non visualizza una media.                                    |
| [PERF \_ COUNTER \_ LARGE \_ RAWCOUNT \_ HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 256<br/> | Uguale a **PERF \_ COUNTER \_ RAWCOUNT \_ HEX,** ma una rappresentazione a 64 bit in formato esadecimale da usare con valori di grandi dimensioni.        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

