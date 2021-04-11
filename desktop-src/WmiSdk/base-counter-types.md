---
description: Per alcune formule sono necessarie sia una proprietà del contatore che una proprietà di base.
ms.assetid: c14be351-e712-40bd-bab7-5b9ef6cd8a00
ms.tgt_platform: multiple
title: Tipi di contatori di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e481fbf093245813d0ce0de2b5f7906316c2378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233110"
---
# <a name="base-counter-types"></a>Tipi di contatori di base

Per alcune formule sono necessarie sia una proprietà del contatore che una proprietà di base. Il valore di base è il denominatore nella formula per il tipo di contatore. Nelle classi di [contatori delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) dei dati non elaborati derivati da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), la proprietà di base deve seguire immediatamente la proprietà del contatore. Il nome della proprietà di base deve essere uguale a quello del contatore precedente, con l'aggiunta di **\_ base** .

Ad esempio, la proprietà **AvgDiskBytesPerRead** in [**Win32 \_ PerfRawData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md) contiene il valore non elaborato, in byte, trasferito dal disco durante le operazioni di lettura. Dispone di una proprietà di base, **AvgDiskBytesPerRead \_ base**, che rappresenta il numero accumulato di operazioni. Quando WMI applica la formula per il tipo di contatore specificato, la **\_ \_ base media delle prestazioni**, **AvgDiskBytesPerRead** è divisa per la **\_ base AvgDiskBytesPerRead** per produrre il valore medio. Questo valore viene visualizzato in Monitor di sistema e viene archiviato nella proprietà [**Win32 \_ PerfFormattedData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md) corrispondente. Le proprietà di base vengono utilizzate solo nelle classi di dati non elaborati.

Nelle classi derivate da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), il qualificatore del **contatore** specifica la proprietà del numeratore nella classe RAW e il qualificatore di **base** specifica la proprietà del denominatore base.

Nella tabella seguente sono elencati i valori costanti **CounterType** .



| Costante CounterType                                                                                      | Descrizione                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Prestazioni \_ Media \_ ](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale base 1073939458<br/>        | Valore di base utilizzato per calcolare i tipi di contatori medi per le prestazioni del **\_ \_ timer** e delle **prestazioni \_ \_** .                                                                                             |
| [Prestazioni \_ CONTATORE \_ \_ multibase](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 1107494144<br/> | Valore di base utilizzato per calcolare **il \_ contatore delle prestazioni \_ \_ multitimer**, contatore delle prestazioni multitimer **\_ \_ \_ \_ inv**, **Perf \_ 100NSEC \_ \_ multitimer** e **Perf \_ 100NSEC \_ \_ multitimer \_ inv** tipi di contatori. |
| [Prestazioni \_ Valore decimale di \_ \_ base grezzo grande](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073939712<br/>     | Valore di base trovato nel calcolo della **\_ \_ frazione non elaborata delle prestazioni**, 64 bit.                                                                                                                         |
| [Prestazioni \_ Decimale \_ base RAW](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073939459<br/>            | Valore di base utilizzato per calcolare il tipo di contatore della **\_ \_ frazione non elaborata delle prestazioni** .                                                                                                                           |
| [Prestazioni \_ ESEMPIO di \_ base](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 1073939457<br/>         | Valore di base usato per calcolare **il \_ \_ contatore di esempio delle prestazioni** e i tipi di contatore delle **\_ \_ frazioni di esempio** delle prestazioni.                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md)
</dt> <dt>

[Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))
</dt> </dl>

 

