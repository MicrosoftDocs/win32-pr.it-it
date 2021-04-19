---
description: Il provider di route IP WMI e le classi di rete forniscono i dati per gli indirizzi IPv4. A partire da Windows Vista, WMI fornisce anche il supporto limitato per le funzionalità di rete IPv6.
ms.assetid: 8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8
ms.tgt_platform: multiple
title: Supporto di IPv6 e IPv4 in WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107872b2a65ffe02f34245a39e0a803d2ac53a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315210"
---
# <a name="ipv6-and-ipv4-support-in-wmi"></a>Supporto di IPv6 e IPv4 in WMI

Il [provider di route IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI e le classi di rete forniscono i dati per gli indirizzi IPv4. A partire da Windows Vista, WMI fornisce anche il supporto limitato per le funzionalità di rete IPv6.

## <a name="wmi-ip-data"></a>Dati IP WMI

Le classi seguenti forniscono solo i dati IPv4:

-   [**\_IP4RouteTable Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [**\_IP4PersistedRouteTable Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [**\_IP4RouteTableEvent Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [**\_ActiveRoute Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [**\_NetworkAdapter Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapter)

Le classi seguenti forniscono i dati sia per IPv4 che per IPv6.

-   [**\_NetworkAdapterConfiguration Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    La proprietà **IpAddess** contiene l'indirizzo IPv6 del computer in una rete IPv6.

-   [**\_PingStatus Win32**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    [**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) può restituire dati per gli indirizzi IPv4 o IPv6.

## <a name="ipv4-and-ipv6-connections-to-wmi"></a>Connessioni IPv4 e IPv6 a WMI

Quando ci si connette a uno spazio dei nomi WMI in un computer remoto, nel computer di destinazione deve essere in esecuzione lo stesso software IP del computer che si connette. Un computer che esegue IPv4, ad esempio, non è in grado di connettersi a un computer che esegue IPv6, anche se la connessione viene tentata utilizzando un nome computer nella chiamata a [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md)o utilizzando la `winmgmts` connessione moniker. È anche vero il contrario: un computer che esegue solo IPv6 non è in grado di connettersi a un computer che esegue solo IPv4.

Se nel computer di destinazione sono in esecuzione sia IPv4 che IPv6, è possibile effettuare una connessione da un computer che esegue uno dei due software IP. È possibile specificare un nome di computer o un indirizzo IP in formato IPv4 o IPv6 nella connessione a uno spazio dei nomi WMI.

Un computer che esegue sia IPv4 che IPv6 e si connette a un computer di destinazione che esegue solo IPv4 o solo IPv6 deve fornire un indirizzo IP nel formato appropriato per il software IP del computer di destinazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> </dl>

 

 
