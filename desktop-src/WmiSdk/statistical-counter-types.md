---
description: Le prestazioni di WMI ad alte prestazioni formattate provider di dati calcolano i tipi di contatori statistici su un numero specificato di campioni di dati del contatore non elaborati.
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: Tipi di contatori statistici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb97224b06881cbc3c8b1375c04a4df5be1095f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057859"
---
# <a name="statistical-counter-types"></a>Tipi di contatori statistici

Le prestazioni di WMI ad alte prestazioni [formattate provider di dati](formatted-performance-data-provider.md) calcolano i tipi di contatori statistici su un numero specificato di campioni di dati del contatore non elaborati. Gli algoritmi per i tipi di contatore non richiedono proprietà timestamp o Frequency ereditate, ad esempio **timestamp \_ PerfTime** o **Frequency \_ PerfTime**, che altri tipi di contatori richiedono.

I tipi di contatori statistici supportano invece un **qualificatore** che identifica il numero di campioni da usare. Un esempio viene raccolto quando viene chiamato il metodo [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) per l'oggetto prestazione. Per gli script, usare il metodo [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) . I dati calcolati contengono il risultato del calcolo eseguito sul numero di campioni **SampleWindow** dalla proprietà dati non elaborati. I dati non elaborati per il calcolo risultano frm il nome della proprietà specificato nel qualificatore del **contatore** .

Per ulteriori informazioni, vedere [ottenere dati statistici sulle prestazioni](obtaining-statistical-performance-data.md) e [accedere alle classi di prestazioni preinstallate WMI](accessing-wmi-preinstalled-performance-classes.md).



| Costante CounterType                    | Descrizione                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [media COOKer \_](cooker-average.md)   | Somma le osservazioni ripetute di una proprietà in una classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e divide la somma per il numero di osservazioni.                              |
| [massimo COOKer \_](cooker-max.md)           | Valore più grande da un set di osservazioni di una proprietà in una classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .                                                                    |
| [MIN COOKer \_](cooker-min.md)           | Valore più piccolo da un set di osservazioni di una proprietà in una classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .                                                                   |
| [intervallo di cottura \_](cooker-range.md)       | Differenza tra i valori [minimo](cooker-min.md) e [massimo](cooker-max.md) per un set di osservazioni non elaborate di una proprietà in una classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) . |
| [varianza del COOKer \_](cooker-variance.md) | Misura della variabilità che può essere usata per caratterizzare la dispersione per un set di osservazioni non elaborate di una proprietà in una classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .            |



 

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

 

 
