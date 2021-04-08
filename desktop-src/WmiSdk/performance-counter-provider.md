---
description: Il provider del contatore delle prestazioni è un provider a prestazioni elevate che fornisce dati del contatore delle prestazioni non elaborati alle classi del contatore delle prestazioni WMI derivate da Win32 \_ PerfRawData. Il \_ \_ nome dell'istanza di Win32Provider è &\# 0034; NT5 \_ GenericPerfProvider \_ V1&\# 0034;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Provider contatore prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9288da5ac20bff6340950ba2a3506d9128200cfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058221"
---
# <a name="performance-counter-provider"></a>Provider contatore prestazioni

\[Il provider del contatore delle prestazioni non è più disponibile per l'utilizzo. Usare invece il provider [wmiperfinst](wmiperfinst-provider.md) .\]

Il provider del contatore delle prestazioni è un provider a prestazioni elevate che fornisce dati del contatore delle prestazioni non elaborati alle [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata). Il nome dell'istanza di [**\_ \_ Win32Provider**](--win32provider.md) è "NT5 \_ GenericPerfProvider \_ V1".

Le classi [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) si trovano nello \\ spazio dei nomi WMI "root CIMv2". Ogni classe di prestazioni WMI corrisponde a un oggetto prestazione in una libreria delle prestazioni. Le proprietà di queste classi rappresentano i contatori per l'oggetto. Il nome della classe WMI per un oggetto contatore non elaborato ha il formato ** \_ Win32 \_ \_ PerfRawData* nome servizio nome \_ *\_* oggetto \_ * * *. Ad esempio, il nome della classe WMI che contiene i contatori del disco logico è [**Win32 \_ PerfRawData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md).

È possibile utilizzare la classe [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) corrispondente per ottenere i dati sulle prestazioni pre-calcolati visualizzati in [*Monitor di sistema*](gloss-s.md). Ad esempio, usare la classe [**Win32 \_ PerfFormattedData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md) per ottenere i dati del disco precalcolati.

Per ulteriori informazioni su come scrivere un client in grado di accedere ai dati sulle prestazioni non elaborati, vedere [accesso ai dati sulle prestazioni in C++](accessing-performance-data-in-c--.md).

Come provider a prestazioni elevate, il provider del contatore delle prestazioni implementa l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) standard, nonché il metodo [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) e i metodi [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) seguenti:

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

 

 
