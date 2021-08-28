---
description: Il provider WMIPerfClass e il provider WMIPerfInst forniscono dinamicamente i dati dei contatori delle prestazioni per le classi del contatore delle prestazioni WMI.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Librerie delle prestazioni e WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877623bcf27dffe71146df4f9c117da83941bd1d8e2ed46436a04c1d7ace95df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996411"
---
# <a name="performance-libraries-and-wmi"></a>Librerie delle prestazioni e WMI

Il [provider WMIPerfClass e](wmiperfclass-provider.md) il provider [WMIPerfInst](wmiperfinst-provider.md) forniscono dinamicamente i dati dei contatori delle prestazioni per le [classi](/windows/desktop/CIMWin32Prov/performance-counter-classes)del contatore delle prestazioni WMI.

## <a name="wmiperfclass-and-wmiperfinst-providers"></a>Provider WMIPerfClass e WMIPerfInst

[Il provider WMIPerfClass crea](wmiperfclass-provider.md) classi del [contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI all'inizializzazione del sistema. Il [provider WMIPerfInst fornisce](wmiperfinst-provider.md) in modo dinamico i dati dei contatori delle prestazioni per queste classi. Il provider WMIPerfClass fornisce classi sia per i contatori delle prestazioni versione 1 che per i contatori [delle prestazioni versione](/windows/desktop/PerfCtrs/performance-counters-portal)2.

I contatori della versione 1 sono disponibili nel Registro di sistema in **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Services**. I servizi che forniscono dati sulle prestazioni hanno una **sottochiave** Prestazioni. Le classi di prestazioni WMI create dai contatori della versione 1 non hanno "Counter" come parte del nome.

I **GUID** che identificano un provider di contatori delle prestazioni versione 2 sono disponibili nel Registro di sistema in **HKEY LOCAL MACHINE SOFTWARE \_ Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Perflib \\ \_ V2Providers**.

WMIPerfClass viene registrato come normale provider di classi WMI. WMIPerfInst è un provider di istanze WMI che fornisce dati da Performance Data Helper (PDH) per i contatori sia versione 1 che versione 2. Per altre informazioni, vedere [Uso delle funzioni PDH per l'utilizzo dei dati dei contatori](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> </dl>

 

 
