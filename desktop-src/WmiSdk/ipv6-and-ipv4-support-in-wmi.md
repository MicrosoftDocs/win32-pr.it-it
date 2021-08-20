---
description: Il provider di route IP WMI e le classi di rete forniscono i dati per gli indirizzi IPv4. A partire da Windows Vista, WMI offre anche un supporto limitato per le funzionalità di rete IPv6.
ms.assetid: 8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8
ms.tgt_platform: multiple
title: Supporto di IPv6 e IPv4 in WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea400d6c896220dcde5c15d40481444a77ffb309eac8bfdc50cb06ab634c384
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819299"
---
# <a name="ipv6-and-ipv4-support-in-wmi"></a>Supporto di IPv6 e IPv4 in WMI

Il [provider di route IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI e le classi di rete forniscono i dati per gli indirizzi IPv4. A partire da Windows Vista, WMI offre anche un supporto limitato per le funzionalità di rete IPv6.

## <a name="wmi-ip-data"></a>Dati IP WMI

Le classi seguenti forniscono solo dati IPv4:

-   [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [**Win32 \_ IP4PersistedRouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [**Win32 \_ ActiveRoute**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)

Le classi seguenti forniscono dati sia per IPv4 che per IPv6.

-   [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    La **proprietà IpAddess** contiene l'indirizzo IPv6 del computer in una rete IPv6.

-   [**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    [**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) può restituire dati per indirizzi IPv4 o IPv6.

## <a name="ipv4-and-ipv6-connections-to-wmi"></a>Connessioni IPv4 e IPv6 a WMI

Quando ci si connette a uno spazio dei nomi WMI in un computer remoto, il computer di destinazione deve eseguire lo stesso software IP del computer che si connette. Ad esempio, un computer che esegue IPv4 non può connettersi a un computer che esegue IPv6, anche se la connessione viene tentata utilizzando un nome computer nella chiamata a [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md)o tramite la connessione `winmgmts` moniker. È vero anche il contrario: un computer che esegue solo IPv6 non può connettersi a un computer che esegue solo IPv4.

Se il computer di destinazione esegue sia IPv4 che IPv6, è possibile stabilire una connessione da un computer che esegue uno dei due software IP. È possibile specificare un nome computer o un indirizzo IP in formato IPv4 o IPv6 nella connessione a uno spazio dei nomi WMI.

Un computer che esegue sia IPv4 che IPv6 e si connette a un computer di destinazione che esegue solo IPv4 o solo IPv6 deve fornire un indirizzo IP nel formato appropriato per il software IP del computer di destinazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> </dl>

 

 
