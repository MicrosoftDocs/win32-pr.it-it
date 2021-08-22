---
description: Il provider del contatore delle prestazioni è un provider ad alte prestazioni che fornisce dati dei contatori delle prestazioni non elaborati alle classi di contatori delle prestazioni WMI derivate da Win32 \_ PerfRawData. Il \_ \_ nome dell'istanza Win32Provider &\# 0034; NT5 \_ GenericPerfProvider \_ V1&\# 0034;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Provider contatore prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c846d66cd183e866623004cacfbcb630ac68480fab8dd58eca2b5a4dc6d2f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050529"
---
# <a name="performance-counter-provider"></a>Provider contatore prestazioni

\[Il provider del contatore delle prestazioni non è più disponibile per l'uso. Usare invece il provider [WMIPerfInst.](wmiperfinst-provider.md)\]

Il provider del contatore delle prestazioni è un provider ad alte prestazioni che fornisce dati dei contatori delle prestazioni non elaborati alle classi del contatore delle prestazioni [WMI](/windows/desktop/CIMWin32Prov/performance-counter-classes) derivate da [**Win32 \_ PerfRawData.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) Il [**\_ \_ nome dell'istanza Win32Provider**](--win32provider.md) è "NT5 \_ GenericPerfProvider \_ V1".

Le [**classi \_ Win32 PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) si trovano nello spazio dei nomi WMI \\ "CIMv2 radice". Ogni classe di prestazioni WMI corrisponde a un oggetto prestazioni in una libreria di prestazioni. Le proprietà di queste classi rappresentano i contatori per l'oggetto . Il nome della classe WMI per un oggetto contatore non elaborato è nel formato * Nome oggetto nome servizio *Win32 \_ \_ \_ PerfRawData***.* \_ *\_* \_ Ad esempio, il nome della classe WMI che contiene i contatori dei dischi logici è [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).

È possibile usare la classe [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) corrispondente per ottenere i dati sulle prestazioni pre-calcolati visualizzati in [*Monitoraggio di sistema.*](gloss-s.md) Ad esempio, usare la [**classe \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk Win32**](./retrieving-raw-and-formatted-performance-data.md) per ottenere i dati del disco pre-calcolati.

Per altre informazioni su come scrivere un client in grado di accedere ai dati sulle prestazioni non elaborati, vedere Accesso ai dati sulle [prestazioni in C++.](accessing-performance-data-in-c--.md)

Come provider ad alte prestazioni, il provider del contatore delle prestazioni implementa l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) standard, nonché il metodo [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) e i metodi [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) seguenti:

-   [**CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [**CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [**CreateRefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [**GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [**QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [**StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider WMI](wmi-providers.md)
</dt> </dl>

 

 
