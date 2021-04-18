---
description: A partire da Windows Vista, il provider WmiPerfInst fornisce dati del contatore delle prestazioni non elaborati e formattati dinamicamente alle classi del contatore delle prestazioni WMI derivate da \_ Perf Win32.
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: Provider WmiPerfInst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374568de0780b18b1e3036eb7fc6ce7247b46039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310321"
---
# <a name="wmiperfinst-provider"></a>Provider WmiPerfInst

A partire da Windows Vista, il provider WmiPerfInst fornisce dati del contatore delle prestazioni non elaborati e formattati dinamicamente alle [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI derivate da [**\_ Perf Win32**](/windows/desktop/CIMWin32Prov/win32-perf). Questo provider sostituisce il [provider di dati delle prestazioni formattato](formatted-performance-data-provider.md), noto anche come "provider di contatori cotti" e il [provider del contatore delle prestazioni](performance-counter-provider.md).

Il provider WmiPerfInst fornisce dati alle classi WMI fornite dal provider [wmiperfclass](wmiperfclass-provider.md) . Questo provider è un bridge tra le istanze di PDH (Performance Data Helper) e le classi di prestazioni WMI fornite dal provider WmiPerfClass. Quando WmiPerfInst riceve una query per i dati, carica la classe e usa i [qualificatori](qualifiers-specific-to-wmi-performance-classes.md) della classe e della proprietà per individuare le istanze di PDH. Per ulteriori informazioni, vedere [utilizzo delle funzioni PDH per utilizzare i dati del contatore](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).

Non è consigliabile sviluppare nuovi oggetti prestazione creando un provider WMI a prestazioni elevate e dipendono dal processo di [*adattamento dell'adattatore ADAP*](gloss-r.md) per trasferire i dati alle librerie delle prestazioni. L'eccezione si verifica quando si sviluppa un driver Windows Driver Model e si desidera fornire dati sulle prestazioni. Mentre il processo dell'adattatore inverso continua a funzionare per la compatibilità con le versioni precedenti, il metodo consigliato prevede l'uso dei [contatori delle prestazioni versione 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).

Il nome dell'istanza di [**\_ \_ Win32Provider**](--win32provider.md) di questo provider è "WmiPerfInst".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider WMI](wmi-providers.md)
</dt> <dt>

[Librerie di prestazioni e WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> </dl>

 

 
