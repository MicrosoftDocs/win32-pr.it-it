---
description: A partire da Windows Vista, il provider WmiPerfInst fornisce dinamicamente i dati dei contatori delle prestazioni non elaborati e formattati alle classi del contatore delle prestazioni WMI derivate da Win32 \_ Perf.
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: WmiPerfInst Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a781fc1dc48f0e16d1c25e03eff1b2ab3c80fcd7058d1b49f95912b392d241
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049749"
---
# <a name="wmiperfinst-provider"></a>WmiPerfInst Provider

A partire da Windows Vista, il provider WmiPerfInst fornisce dinamicamente i dati dei contatori delle prestazioni non elaborati e formattati alle classi del contatore delle prestazioni [WMI](/windows/desktop/CIMWin32Prov/performance-counter-classes) derivate da [**Win32 \_ Perf.**](/windows/desktop/CIMWin32Prov/win32-perf) Questo provider sostituisce [l'provider di dati](formatted-performance-data-provider.md)formattato , noto anche come "provider di contatori delle prestazioni" e il provider di [contatori delle prestazioni](performance-counter-provider.md).

Il provider WmiPerfInst fornisce i dati alle classi WMI fornite dal provider [WMIPerfClass.](wmiperfclass-provider.md) Questo provider è un ponte tra le istanze dell'helper dati delle prestazioni (PDH) e le classi di prestazioni WMI fornite dal provider WmiPerfClass. Quando WmiPerfInst riceve una query per i dati, carica [](qualifiers-specific-to-wmi-performance-classes.md) la classe e usa i qualificatori di classe e proprietà per individuare le istanze PDH. Per altre informazioni, vedere [Uso delle funzioni PDH per utilizzare i dati dei contatori.](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data)

Non è consigliabile sviluppare nuovi oggetti prestazioni creando un provider WMI a prestazioni elevate e dipendere dal processo [*dell'adattatore*](gloss-r.md) inverso ADAP per trasferire i dati alle librerie delle prestazioni. L'eccezione si verifica quando si sviluppa un driver Windows driver e si vogliono fornire dati sulle prestazioni. Mentre il processo dell'adattatore inverso continua a funzionare per garantire la compatibilità con le versioni precedenti, il metodo consigliato è usare i contatori delle prestazioni [versione 6.0.](/windows/desktop/PerfCtrs/performance-counters-portal)

Il [**\_ \_ nome dell'istanza Win32Provider**](--win32provider.md) di questo provider è "WmiPerfInst".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider WMI](wmi-providers.md)
</dt> <dt>

[Librerie delle prestazioni e WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> </dl>

 

 
