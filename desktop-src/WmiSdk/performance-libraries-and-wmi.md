---
description: Il provider WMIPerfClass e il provider WMIPerfInst forniscono dinamicamente i dati dei contatori delle prestazioni per le classi del contatore delle prestazioni WMI.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Librerie di prestazioni e WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dedc9b98f492b3ab57e22cd1507f9e3651980a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308844"
---
# <a name="performance-libraries-and-wmi"></a>Librerie di prestazioni e WMI

Il [provider WMIPerfClass](wmiperfclass-provider.md) e il [provider WMIPerfInst](wmiperfinst-provider.md) forniscono dinamicamente i dati dei contatori delle prestazioni per le [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI.

## <a name="wmiperfclass-and-wmiperfinst-providers"></a>Provider WMIPerfClass e WMIPerfInst

Il [provider WMIPerfClass](wmiperfclass-provider.md) crea [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI all'inizializzazione del sistema. Il [provider WMIPerfInst](wmiperfinst-provider.md) fornisce dinamicamente i dati dei contatori delle prestazioni per queste classi. Il provider del provider WMIPerfClass fornisce le classi per i [contatori delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal)versione 1 e versione 2.

I contatori versione 1 si trovano nel registro di **sistema in HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Services**. I servizi che forniscono dati sulle prestazioni hanno una sottochiave **delle prestazioni** . Le classi di prestazioni WMI create dai contatori della versione 1 non includono "contatori" come parte del nome.

Il **GUID** che identifica un provider del contatore delle prestazioni versione 2 si trova nel registro di sistema in **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Perflib \\ \_ V2Providers**.

WMIPerfClass viene registrato come provider di classi WMI normale. WMIPerfInst è un provider di istanze WMI che fornisce dati dall'helper dei dati sulle prestazioni (PDH) per i contatori versione 1 e versione 2. Per ulteriori informazioni, vedere [utilizzo delle funzioni PDH per utilizzare i dati del contatore](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> </dl>

 

 
