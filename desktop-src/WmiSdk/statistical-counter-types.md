---
description: La libreria WMI a prestazioni elevate formatta le provider di dati calcola i tipi di contatori statistici su un numero specificato di campioni di dati dei contatori non elaborati.
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: Tipi di contatori statistici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1289bae423305bac863afefaba8e5700268d98e594fe767d597c8470aa4f1ac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314820"
---
# <a name="statistical-counter-types"></a>Tipi di contatori statistici

La libreria WMI ad alte prestazioni [Formatted Performance provider di dati](formatted-performance-data-provider.md) calcola i tipi di contatori statistici su un numero specificato di campioni di dati dei contatori non elaborati. Gli algoritmi per i tipi di contatore non richiedono proprietà timestamp o frequency ereditate (ad esempio **TimeStamp \_ PerfTime** o **Frequency \_ PerfTime)** richieste da altri tipi di contatore.

I tipi di contatore statistici supportano invece **un qualificatore** che identifica il numero di campioni da usare. Un esempio viene raccolto quando viene chiamato [**il metodo Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) per l'oggetto prestazioni. Per gli script usare [**il metodo SWbemRefresher.Refresh.**](swbemrefresher-refresh.md) I dati calcolati contengono il risultato del calcolo eseguito sul numero **SampleWindow** di campioni dalla proprietà dei dati non elaborati. I dati non elaborati per il calcolo derivano dal nome della proprietà specificato nel qualificatore **Counter.**

Per altre informazioni, vedere [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md) and [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).



| Costante CounterType                    | Descrizione                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEDIA \_ COOKER](cooker-average.md)   | Somma le osservazioni ripetute di una proprietà in [**una classe \_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e divide la somma per il numero di osservazioni.                              |
| [COOKER \_ MAX](cooker-max.md)           | Valore più grande da un set di osservazioni di una proprietà in una [**classe \_ PerfRawData Win32.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)                                                                    |
| [COOKER \_ MIN](cooker-min.md)           | Valore più piccolo di un set di osservazioni di una proprietà in una [**classe \_ PerfRawData Win32.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)                                                                   |
| [COOKER \_ RANGE](cooker-range.md)       | Differenza tra i [valori Min](cooker-min.md) [e Max](cooker-max.md) per un set di osservazioni non elaborati di una proprietà in una classe [**\_ PerfRawData Win32.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) |
| [VARIANZA DEL \_ COOKER](cooker-variance.md) | Misura della variabilità che può essere usata per caratterizzare la dispersione per un set di osservazioni non elaborati di una proprietà in una [**classe \_ PerfRawData Win32.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md)
</dt> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> <dt>

[Aggiornamento dei dati WMI negli script](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[Accesso ai dati sulle prestazioni nello script](accessing-performance-data-in-script.md)
</dt> <dt>

[Accesso ai dati sulle prestazioni in C++](accessing-performance-data-in-c--.md)
</dt> </dl>

 

 
