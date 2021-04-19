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
# <a name="ipv6-and-ipv4-support-in-wmi"></a><span data-ttu-id="48b9a-104">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="48b9a-104">IPv6 and IPv4 Support in WMI</span></span>

<span data-ttu-id="48b9a-105">Il [provider di route IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI e le classi di rete forniscono i dati per gli indirizzi IPv4.</span><span class="sxs-lookup"><span data-stu-id="48b9a-105">WMI [IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) and network classes supply data for IPv4 addresses.</span></span> <span data-ttu-id="48b9a-106">A partire da Windows Vista, WMI fornisce anche il supporto limitato per le funzionalità di rete IPv6.</span><span class="sxs-lookup"><span data-stu-id="48b9a-106">Starting with Windows Vista, WMI also provides limited support for IPv6 network capabilities.</span></span>

## <a name="wmi-ip-data"></a><span data-ttu-id="48b9a-107">Dati IP WMI</span><span class="sxs-lookup"><span data-stu-id="48b9a-107">WMI IP Data</span></span>

<span data-ttu-id="48b9a-108">Le classi seguenti forniscono solo i dati IPv4:</span><span class="sxs-lookup"><span data-stu-id="48b9a-108">The following classes supply only IPv4 data:</span></span>

-   [<span data-ttu-id="48b9a-109">**\_IP4RouteTable Win32**</span><span class="sxs-lookup"><span data-stu-id="48b9a-109">**Win32\_IP4RouteTable**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [<span data-ttu-id="48b9a-110">**\_IP4PersistedRouteTable Win32**</span><span class="sxs-lookup"><span data-stu-id="48b9a-110">**Win32\_IP4PersistedRouteTable**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [<span data-ttu-id="48b9a-111">**\_IP4RouteTableEvent Win32**</span><span class="sxs-lookup"><span data-stu-id="48b9a-111">**Win32\_IP4RouteTableEvent**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [<span data-ttu-id="48b9a-112">**\_ActiveRoute Win32**</span><span class="sxs-lookup"><span data-stu-id="48b9a-112">**Win32\_ActiveRoute**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [<span data-ttu-id="48b9a-113">**\_NetworkAdapter Win32**</span><span class="sxs-lookup"><span data-stu-id="48b9a-113">**Win32\_NetworkAdapter**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapter)

<span data-ttu-id="48b9a-114">Le classi seguenti forniscono i dati sia per IPv4 che per IPv6.</span><span class="sxs-lookup"><span data-stu-id="48b9a-114">The following classes supply data for both IPv4 and IPv6.</span></span>

-   [<span data-ttu-id="48b9a-115">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="48b9a-115">**Win32\_NetworkAdapterConfiguration**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    <span data-ttu-id="48b9a-116">La proprietà **IpAddess** contiene l'indirizzo IPv6 del computer in una rete IPv6.</span><span class="sxs-lookup"><span data-stu-id="48b9a-116">The **IpAddess** property contains the IPv6 address of the computer in an IPv6 network.</span></span>

-   [<span data-ttu-id="48b9a-117">**\_PingStatus Win32**</span><span class="sxs-lookup"><span data-stu-id="48b9a-117">**Win32\_PingStatus**</span></span>](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    <span data-ttu-id="48b9a-118">[**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) può restituire dati per gli indirizzi IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="48b9a-118">[**Win32\_PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) can return data for either IPv4 or IPv6 addresses.</span></span>

## <a name="ipv4-and-ipv6-connections-to-wmi"></a><span data-ttu-id="48b9a-119">Connessioni IPv4 e IPv6 a WMI</span><span class="sxs-lookup"><span data-stu-id="48b9a-119">IPv4 and IPv6 Connections to WMI</span></span>

<span data-ttu-id="48b9a-120">Quando ci si connette a uno spazio dei nomi WMI in un computer remoto, nel computer di destinazione deve essere in esecuzione lo stesso software IP del computer che si connette.</span><span class="sxs-lookup"><span data-stu-id="48b9a-120">When connecting to a WMI namespace on a remote computer, the target computer must be running the same IP software as the connecting computer.</span></span> <span data-ttu-id="48b9a-121">Un computer che esegue IPv4, ad esempio, non è in grado di connettersi a un computer che esegue IPv6, anche se la connessione viene tentata utilizzando un nome computer nella chiamata a [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md)o utilizzando la `winmgmts` connessione moniker.</span><span class="sxs-lookup"><span data-stu-id="48b9a-121">For example, a computer running IPv4 cannot connect to a computer running IPv6, even if the connection is attempted by using a computer name in the call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), or by using the `winmgmts` moniker connection.</span></span> <span data-ttu-id="48b9a-122">È anche vero il contrario: un computer che esegue solo IPv6 non è in grado di connettersi a un computer che esegue solo IPv4.</span><span class="sxs-lookup"><span data-stu-id="48b9a-122">The reverse is also true: a computer running only IPv6 cannot connect to a computer running only IPv4.</span></span>

<span data-ttu-id="48b9a-123">Se nel computer di destinazione sono in esecuzione sia IPv4 che IPv6, è possibile effettuare una connessione da un computer che esegue uno dei due software IP.</span><span class="sxs-lookup"><span data-stu-id="48b9a-123">If the target computer is running both IPv4 and IPv6, then a connection can be made from a computer running either IP software.</span></span> <span data-ttu-id="48b9a-124">È possibile specificare un nome di computer o un indirizzo IP in formato IPv4 o IPv6 nella connessione a uno spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="48b9a-124">A computer name or an IP address in either IPv4 or IPv6 format can be supplied in the connection to a WMI namespace.</span></span>

<span data-ttu-id="48b9a-125">Un computer che esegue sia IPv4 che IPv6 e si connette a un computer di destinazione che esegue solo IPv4 o solo IPv6 deve fornire un indirizzo IP nel formato appropriato per il software IP del computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="48b9a-125">A computer that runs both IPv4 and IPv6 and connects to a target computer running only IPv4 or only IPv6 must supply an IP address in the appropriate format for the target computer IP software.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48b9a-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48b9a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48b9a-127">Informazioni su WMI</span><span class="sxs-lookup"><span data-stu-id="48b9a-127">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
