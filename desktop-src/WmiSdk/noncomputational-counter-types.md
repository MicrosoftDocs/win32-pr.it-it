---
description: Ai tipi di contatori non computazionali non è associata una formula. Il valore non elaborato è direttamente significativo.
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Tipi di contatori non computazionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ba2757f08dcb2256236117daf2ef3343004425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232401"
---
# <a name="noncomputational-counter-types"></a>Tipi di contatori non computazionali

Ai tipi di contatori non computazionali non è associata una formula. Il valore non elaborato è direttamente significativo.

La proprietà **FilesToBeIndexed** nella classe [**Win32 \_ PerfRawData \_ ContentIndex \_ IndexingService**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) è un esempio del contatore delle prestazioni del contatore delle prestazioni di tipo **\_ \_ RAWCOUNT** . Contiene un conteggio dei file che non sono stati indicizzati.

I tipi di contatori sono designati dalla costante definita in Winperf. h, disponibile in Microsoft Windows Software Development Kit (SDK). Nella tabella seguente sono elencati i tipi di contatori non computazionali forniti.



| CounterType                                                                                                 | Descrizione                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Prestazioni \_ \_Testo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale del contatore 2816<br/>                | Questo tipo di contatore mostra una stringa di testo a lunghezza variabile in Unicode. Non vengono visualizzati i valori calcolati.               |
| [Prestazioni \_ CONTATORE \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 65536<br/>           | Valore del contatore non elaborato che non richiede calcoli e rappresenta un campione che è l'ultimo valore osservato. |
| [Prestazioni \_ COUNTER \_ Large \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792<br/>    | Uguale al **contatore delle prestazioni \_ \_ RAWCOUNT**, ma una rappresentazione a 64 bit per valori più grandi.                                    |
| [Prestazioni \_ CONTATORE \_ RAWCOUNT \_ esadecimale](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0<br/>                  | Valore osservato più recentemente in formato esadecimale. Non visualizza una media.                                    |
| [Prestazioni \_ COUNTER \_ Large \_ RAWCOUNT \_ Hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))256<br/> | Uguale al **contatore delle prestazioni \_ \_ RAWCOUNT \_ Hex**, ma una rappresentazione a 64 bit in esadecimale da usare con valori di grandi dimensioni.        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

