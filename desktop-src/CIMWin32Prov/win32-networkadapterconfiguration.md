---
description: Rappresenta gli attributi e i comportamenti di una scheda di rete. Questa classe include proprietà e metodi aggiuntivi che supportano la gestione del protocollo TCP/IP indipendente dalla scheda di rete.
ms.assetid: 690b46ed-a065-4973-b044-0df4e81e41a1
ms.tgt_platform: multiple
title: Classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration
- Win32_NetworkAdapterConfiguration.Caption
- Win32_NetworkAdapterConfiguration.Description
- Win32_NetworkAdapterConfiguration.SettingID
- Win32_NetworkAdapterConfiguration.ArpAlwaysSourceRoute
- Win32_NetworkAdapterConfiguration.ArpUseEtherSNAP
- Win32_NetworkAdapterConfiguration.DatabasePath
- Win32_NetworkAdapterConfiguration.DeadGWDetectEnabled
- Win32_NetworkAdapterConfiguration.DefaultIPGateway
- Win32_NetworkAdapterConfiguration.DefaultTOS
- Win32_NetworkAdapterConfiguration.DefaultTTL
- Win32_NetworkAdapterConfiguration.DHCPEnabled
- Win32_NetworkAdapterConfiguration.DHCPLeaseExpires
- Win32_NetworkAdapterConfiguration.DHCPLeaseObtained
- Win32_NetworkAdapterConfiguration.DHCPServer
- Win32_NetworkAdapterConfiguration.DNSDomain
- Win32_NetworkAdapterConfiguration.DNSDomainSuffixSearchOrder
- Win32_NetworkAdapterConfiguration.DNSEnabledForWINSResolution
- Win32_NetworkAdapterConfiguration.DNSHostName
- Win32_NetworkAdapterConfiguration.DNSServerSearchOrder
- Win32_NetworkAdapterConfiguration.DomainDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.ForwardBufferMemory
- Win32_NetworkAdapterConfiguration.FullDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.GatewayCostMetric
- Win32_NetworkAdapterConfiguration.IGMPLevel
- Win32_NetworkAdapterConfiguration.Index
- Win32_NetworkAdapterConfiguration.InterfaceIndex
- Win32_NetworkAdapterConfiguration.IPAddress
- Win32_NetworkAdapterConfiguration.IPConnectionMetric
- Win32_NetworkAdapterConfiguration.IPEnabled
- Win32_NetworkAdapterConfiguration.IPFilterSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPPortSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPSecPermitIPProtocols
- Win32_NetworkAdapterConfiguration.IPSecPermitTCPPorts
- Win32_NetworkAdapterConfiguration.IPSecPermitUDPPorts
- Win32_NetworkAdapterConfiguration.IPSubnet
- Win32_NetworkAdapterConfiguration.IPUseZeroBroadcast
- Win32_NetworkAdapterConfiguration.IPXAddress
- Win32_NetworkAdapterConfiguration.IPXEnabled
- Win32_NetworkAdapterConfiguration.IPXFrameType
- Win32_NetworkAdapterConfiguration.IPXMediaType
- Win32_NetworkAdapterConfiguration.IPXNetworkNumber
- Win32_NetworkAdapterConfiguration.IPXVirtualNetNumber
- Win32_NetworkAdapterConfiguration.KeepAliveInterval
- Win32_NetworkAdapterConfiguration.KeepAliveTime
- Win32_NetworkAdapterConfiguration.MACAddress
- Win32_NetworkAdapterConfiguration.MTU
- Win32_NetworkAdapterConfiguration.NumForwardPackets
- Win32_NetworkAdapterConfiguration.PMTUBHDetectEnabled
- Win32_NetworkAdapterConfiguration.PMTUDiscoveryEnabled
- Win32_NetworkAdapterConfiguration.ServiceName
- Win32_NetworkAdapterConfiguration.TcpipNetbiosOptions
- Win32_NetworkAdapterConfiguration.TcpMaxConnectRetransmissions
- Win32_NetworkAdapterConfiguration.TcpMaxDataRetransmissions
- Win32_NetworkAdapterConfiguration.TcpNumConnections
- Win32_NetworkAdapterConfiguration.TcpUseRFC1122UrgentPointer
- Win32_NetworkAdapterConfiguration.TcpWindowSize
- Win32_NetworkAdapterConfiguration.WINSEnableLMHostsLookup
- Win32_NetworkAdapterConfiguration.WINSHostLookupFile
- Win32_NetworkAdapterConfiguration.WINSPrimaryServer
- Win32_NetworkAdapterConfiguration.WINSScopeID
- Win32_NetworkAdapterConfiguration.WINSSecondaryServer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bccbe7fc44e75c2448d2eda800fe3c14cd13a9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127470"
---
# <a name="win32_networkadapterconfiguration-class"></a><span data-ttu-id="249c7-104">Win32 \_ NetworkAdapterConfiguration (classe)</span><span class="sxs-lookup"><span data-stu-id="249c7-104">Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="249c7-105">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkAdapterConfiguration Win32** rappresenta gli attributi e i comportamenti di una scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-105">The **Win32\_NetworkAdapterConfiguration** [WMI class](../wmisdk/retrieving-a-class.md)represents the attributes and behaviors of a network adapter.</span></span> <span data-ttu-id="249c7-106">Questa classe include proprietà e metodi aggiuntivi che supportano la gestione del protocollo TCP/IP indipendente dalla scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-106">This class includes extra properties and methods that support the management of the TCP/IP protocol that are independent from the network adapter.</span></span>

<span data-ttu-id="249c7-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="249c7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="249c7-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="249c7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="249c7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="249c7-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C515-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  boolean  ArpAlwaysSourceRoute;
  boolean  ArpUseEtherSNAP;
  string   DatabasePath;
  boolean  DeadGWDetectEnabled;
  string   DefaultIPGateway[];
  uint8    DefaultTOS;
  uint8    DefaultTTL;
  boolean  DHCPEnabled;
  datetime DHCPLeaseExpires;
  datetime DHCPLeaseObtained;
  string   DHCPServer;
  string   DNSDomain;
  string   DNSDomainSuffixSearchOrder[];
  boolean  DNSEnabledForWINSResolution;
  string   DNSHostName;
  string   DNSServerSearchOrder[];
  boolean  DomainDNSRegistrationEnabled;
  uint32   ForwardBufferMemory;
  boolean  FullDNSRegistrationEnabled;
  uint16   GatewayCostMetric[];
  uint8    IGMPLevel;
  uint32   Index;
  uint32   InterfaceIndex;
  string   IPAddress[];
  uint32   IPConnectionMetric;
  boolean  IPEnabled;
  boolean  IPFilterSecurityEnabled;
  boolean  IPPortSecurityEnabled;
  string   IPSecPermitIPProtocols[];
  string   IPSecPermitTCPPorts[];
  string   IPSecPermitUDPPorts[];
  string   IPSubnet[];
  boolean  IPUseZeroBroadcast;
  string   IPXAddress;
  boolean  IPXEnabled;
  uint32   IPXFrameType[];
  uint32   IPXMediaType;
  string   IPXNetworkNumber[];
  string   IPXVirtualNetNumber;
  uint32   KeepAliveInterval;
  uint32   KeepAliveTime;
  string   MACAddress;
  uint32   MTU;
  uint32   NumForwardPackets;
  boolean  PMTUBHDetectEnabled;
  boolean  PMTUDiscoveryEnabled;
  string   ServiceName;
  uint32   TcpipNetbiosOptions;
  uint32   TcpMaxConnectRetransmissions;
  uint32   TcpMaxDataRetransmissions;
  uint32   TcpNumConnections;
  boolean  TcpUseRFC1122UrgentPointer;
  uint16   TcpWindowSize;
  boolean  WINSEnableLMHostsLookup;
  string   WINSHostLookupFile;
  string   WINSPrimaryServer;
  string   WINSScopeID;
  string   WINSSecondaryServer;
};
```

## <a name="members"></a><span data-ttu-id="249c7-110">Members</span><span class="sxs-lookup"><span data-stu-id="249c7-110">Members</span></span>

<span data-ttu-id="249c7-111">La classe **Win32 \_ NetworkAdapterConfiguration** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="249c7-111">The **Win32\_NetworkAdapterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="249c7-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="249c7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="249c7-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="249c7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="249c7-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="249c7-114">Methods</span></span>

<span data-ttu-id="249c7-115">La classe **Win32 \_ NetworkAdapterConfiguration** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="249c7-115">The **Win32\_NetworkAdapterConfiguration** class has these methods.</span></span>



| <span data-ttu-id="249c7-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="249c7-116">Method</span></span>                                                                                                                       | <span data-ttu-id="249c7-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="249c7-117">Description</span></span>                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="249c7-118">**DisableIPSec**</span><span class="sxs-lookup"><span data-stu-id="249c7-118">**DisableIPSec**</span></span>](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="249c7-119">Disabilita IPsec in questa scheda di rete abilitata per TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="249c7-119">Disables IPsec on this TCP/IP-enabled network adapter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="249c7-120">**EnableDHCP**</span><span class="sxs-lookup"><span data-stu-id="249c7-120">**EnableDHCP**</span></span>](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="249c7-121">Abilita il Dynamic Host Configuration Protocol (DHCP) per il servizio con questa scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-121">Enables the Dynamic Host Configuration Protocol (DHCP) for service with this network adapter.</span></span><br/>                                              |
| [<span data-ttu-id="249c7-122">**EnableDNS**</span><span class="sxs-lookup"><span data-stu-id="249c7-122">**EnableDNS**</span></span>](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | <span data-ttu-id="249c7-123">Abilita il Domain Name System (DNS) per il servizio in questa scheda di rete associata a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="249c7-123">Enables the Domain Name System (DNS) for service on this TCP/IP-bound network adapter.</span></span><br/>                                                     |
| [<span data-ttu-id="249c7-124">**EnableIPFilterSec**</span><span class="sxs-lookup"><span data-stu-id="249c7-124">**EnableIPFilterSec**</span></span>](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="249c7-125">Abilita IPsec a livello globale in tutte le schede di rete con binding IP.</span><span class="sxs-lookup"><span data-stu-id="249c7-125">Enables IPsec globally across all IP-bound network adapters.</span></span><br/>                                                                               |
| [<span data-ttu-id="249c7-126">**EnableIPSec**</span><span class="sxs-lookup"><span data-stu-id="249c7-126">**EnableIPSec**</span></span>](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="249c7-127">Abilita IPsec su questa specifica scheda di rete abilitata per TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="249c7-127">Enables IPsec on this specific TCP/IP-enabled network adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="249c7-128">**EnableStatic**</span><span class="sxs-lookup"><span data-stu-id="249c7-128">**EnableStatic**</span></span>](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="249c7-129">Abilita l'indirizzamento TCP/IP statico per la scheda di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="249c7-129">Enables static TCP/IP addressing for the target network adapter.</span></span><br/>                                                                           |
| [<span data-ttu-id="249c7-130">**EnableWINS**</span><span class="sxs-lookup"><span data-stu-id="249c7-130">**EnableWINS**</span></span>](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="249c7-131">Abilita le impostazioni WINS specifiche per TCP/IP, ma indipendente dalla scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-131">Enables WINS settings specific to TCP/IP, but independent of the network adapter.</span></span><br/>                                                          |
| [<span data-ttu-id="249c7-132">**ReleaseDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="249c7-132">**ReleaseDHCPLease**</span></span>](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="249c7-133">Rilascia l'indirizzo IP associato a una specifica scheda di rete abilitata per DHCP.</span><span class="sxs-lookup"><span data-stu-id="249c7-133">Releases the IP address bound to a specific DHCP-enabled network adapter.</span></span><br/>                                                                  |
| [<span data-ttu-id="249c7-134">**ReleaseDHCPLeaseAll**</span><span class="sxs-lookup"><span data-stu-id="249c7-134">**ReleaseDHCPLeaseAll**</span></span>](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | <span data-ttu-id="249c7-135">Rilascia gli indirizzi IP associati a tutte le schede di rete abilitate per DHCP.</span><span class="sxs-lookup"><span data-stu-id="249c7-135">Releases the IP addresses bound to all DHCP-enabled network adapters.</span></span><br/>                                                                      |
| [<span data-ttu-id="249c7-136">**RenewDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="249c7-136">**RenewDHCPLease**</span></span>](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | <span data-ttu-id="249c7-137">Rinnovare l'indirizzo IP in specifiche schede di rete abilitate per DHCP.</span><span class="sxs-lookup"><span data-stu-id="249c7-137">Renews the IP address on specific DHCP-enabled network adapters.</span></span><br/>                                                                           |
| [<span data-ttu-id="249c7-138">**RenewDHCPLeaseAll**</span><span class="sxs-lookup"><span data-stu-id="249c7-138">**RenewDHCPLeaseAll**</span></span>](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="249c7-139">Rinnova gli indirizzi IP in tutte le schede di rete abilitate per DHCP.</span><span class="sxs-lookup"><span data-stu-id="249c7-139">Renews the IP addresses on all DHCP-enabled network adapters.</span></span><br/>                                                                              |
| [<span data-ttu-id="249c7-140">**SetArpAlwaysSourceRoute**</span><span class="sxs-lookup"><span data-stu-id="249c7-140">**SetArpAlwaysSourceRoute**</span></span>](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="249c7-141">Imposta la trasmissione di query ARP da parte del protocollo TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="249c7-141">Sets the transmission of ARP queries by the TCP/IP.</span></span><br/>                                                                                        |
| [<span data-ttu-id="249c7-142">**SetArpUseEtherSNAP**</span><span class="sxs-lookup"><span data-stu-id="249c7-142">**SetArpUseEtherSNAP**</span></span>](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | <span data-ttu-id="249c7-143">Consente ai pacchetti Ethernet di usare la codifica SNAP 802,3.</span><span class="sxs-lookup"><span data-stu-id="249c7-143">Enables Ethernet packets to use 802.3 SNAP encoding.</span></span><br/>                                                                                       |
| [<span data-ttu-id="249c7-144">**SetDatabasePath**</span><span class="sxs-lookup"><span data-stu-id="249c7-144">**SetDatabasePath**</span></span>](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="249c7-145">Imposta il percorso dei file di database Internet standard (host, LMHOSTS, reti e protocolli).</span><span class="sxs-lookup"><span data-stu-id="249c7-145">Sets the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span><br/>                                           |
| [<span data-ttu-id="249c7-146">**SetDeadGWDetect**</span><span class="sxs-lookup"><span data-stu-id="249c7-146">**SetDeadGWDetect**</span></span>](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="249c7-147">Abilita il rilevamento del gateway non attivo.</span><span class="sxs-lookup"><span data-stu-id="249c7-147">Enables dead gateway detection.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="249c7-148">**SetDefaultTOS**</span><span class="sxs-lookup"><span data-stu-id="249c7-148">**SetDefaultTOS**</span></span>](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="249c7-149">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="249c7-149">Obsolete.</span></span> <span data-ttu-id="249c7-150">Questo metodo imposta il valore predefinito del tipo di servizio (TOS) nell'intestazione dei pacchetti IP in uscita.</span><span class="sxs-lookup"><span data-stu-id="249c7-150">This method sets the default Type of Service (TOS) value in the header of outgoing IP packets.</span></span><br/>                                   |
| [<span data-ttu-id="249c7-151">**SetDefaultTTL**</span><span class="sxs-lookup"><span data-stu-id="249c7-151">**SetDefaultTTL**</span></span>](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="249c7-152">Imposta il valore TTL (time to Live) predefinito nell'intestazione dei pacchetti IP in uscita.</span><span class="sxs-lookup"><span data-stu-id="249c7-152">Sets the default Time to Live (TTL) value in the header of outgoing IP packets.</span></span><br/>                                                            |
| [<span data-ttu-id="249c7-153">**SetDNSDomain**</span><span class="sxs-lookup"><span data-stu-id="249c7-153">**SetDNSDomain**</span></span>](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="249c7-154">Imposta il dominio DNS.</span><span class="sxs-lookup"><span data-stu-id="249c7-154">Sets the DNS domain.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="249c7-155">**SetDNSServerSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="249c7-155">**SetDNSServerSearchOrder**</span></span>](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="249c7-156">Imposta l'ordine di ricerca del server sotto forma di matrice di elementi.</span><span class="sxs-lookup"><span data-stu-id="249c7-156">Sets the server search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="249c7-157">**SetDNSSuffixSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="249c7-157">**SetDNSSuffixSearchOrder**</span></span>](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="249c7-158">Imposta l'ordine di ricerca dei suffissi come una matrice di elementi.</span><span class="sxs-lookup"><span data-stu-id="249c7-158">Sets the suffix search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="249c7-159">**SetDynamicDNSRegistration**</span><span class="sxs-lookup"><span data-stu-id="249c7-159">**SetDynamicDNSRegistration**</span></span>](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | <span data-ttu-id="249c7-160">Indica la registrazione DNS dinamica degli indirizzi IP per questa scheda associata a IP.</span><span class="sxs-lookup"><span data-stu-id="249c7-160">Indicates dynamic DNS registration of IP addresses for this IP-bound adapter.</span></span><br/>                                                              |
| [<span data-ttu-id="249c7-161">**SetForwardBufferMemory**</span><span class="sxs-lookup"><span data-stu-id="249c7-161">**SetForwardBufferMemory**</span></span>](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | <span data-ttu-id="249c7-162">Specifica la quantità di memoria allocata dall'IP per archiviare i dati dei pacchetti nella coda dei pacchetti del router.</span><span class="sxs-lookup"><span data-stu-id="249c7-162">Specifies how much memory IP allocates to store packet data in the router packet queue.</span></span><br/>                                                    |
| [<span data-ttu-id="249c7-163">**Gateway**</span><span class="sxs-lookup"><span data-stu-id="249c7-163">**SetGateways**</span></span>](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="249c7-164">Specifica un elenco di gateway per il routing dei pacchetti destinati a una subnet diversa da quella a cui è connessa questa scheda.</span><span class="sxs-lookup"><span data-stu-id="249c7-164">Specifies a list of gateways for routing packets destined for a different subnet than the one this adapter is connected to.</span></span><br/>                |
| [<span data-ttu-id="249c7-165">**SetIGMPLevel**</span><span class="sxs-lookup"><span data-stu-id="249c7-165">**SetIGMPLevel**</span></span>](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="249c7-166">Imposta la misura in cui il sistema supporta il multicast IP e partecipa al protocollo di gestione dei gruppi Internet.</span><span class="sxs-lookup"><span data-stu-id="249c7-166">Sets the extent to which the system supports IP multicasting and participates in the Internet Group Management Protocol.</span></span><br/>                   |
| [<span data-ttu-id="249c7-167">**SetIPConnectionMetric**</span><span class="sxs-lookup"><span data-stu-id="249c7-167">**SetIPConnectionMetric**</span></span>](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="249c7-168">Imposta la metrica di routing associata a questo adapter associato a IP.</span><span class="sxs-lookup"><span data-stu-id="249c7-168">Sets the routing metric associated with this IP-bound adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="249c7-169">**SetIPUseZeroBroadcast**</span><span class="sxs-lookup"><span data-stu-id="249c7-169">**SetIPUseZeroBroadcast**</span></span>](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="249c7-170">Imposta l'utilizzo broadcast IP zero.</span><span class="sxs-lookup"><span data-stu-id="249c7-170">Sets IP zero broadcast usage.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="249c7-171">**SetIPXFrameTypeNetworkPairs**</span><span class="sxs-lookup"><span data-stu-id="249c7-171">**SetIPXFrameTypeNetworkPairs**</span></span>](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | <span data-ttu-id="249c7-172">Imposta le coppie di fotogrammi/numero di rete IPX (Internetworking Packet Exchange) per questa scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-172">Sets Internetworking Packet Exchange (IPX) network number/frame pairs for this network adapter.</span></span><br/>                                            |
| [<span data-ttu-id="249c7-173">**SetIPXVirtualNetworkNumber**</span><span class="sxs-lookup"><span data-stu-id="249c7-173">**SetIPXVirtualNetworkNumber**</span></span>](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | <span data-ttu-id="249c7-174">Imposta il numero di rete virtuale IPX (Internetworking Packet Exchange) nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="249c7-174">Sets the Internetworking Packet Exchange (IPX) virtual network number on the target computer system.</span></span><br/>                                       |
| [<span data-ttu-id="249c7-175">**SetKeepAliveInterval**</span><span class="sxs-lookup"><span data-stu-id="249c7-175">**SetKeepAliveInterval**</span></span>](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="249c7-176">Imposta l'intervallo che separa le ritrasmissioni keep-alive fino a quando non viene ricevuta una risposta.</span><span class="sxs-lookup"><span data-stu-id="249c7-176">Sets the interval separating Keep Alive Retransmissions until a response is received.</span></span><br/>                                                      |
| [<span data-ttu-id="249c7-177">**SetKeepAliveTime**</span><span class="sxs-lookup"><span data-stu-id="249c7-177">**SetKeepAliveTime**</span></span>](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="249c7-178">Imposta la frequenza con cui TCP tenta di verificare che una connessione inattiva sia ancora disponibile inviando un pacchetto keep-alive.</span><span class="sxs-lookup"><span data-stu-id="249c7-178">Sets how often TCP attempts to verify that an idle connection is still available by sending a Keep Alive packet.</span></span><br/>                           |
| [<span data-ttu-id="249c7-179">**SetMTU**</span><span class="sxs-lookup"><span data-stu-id="249c7-179">**SetMTU**</span></span>](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | <span data-ttu-id="249c7-180">Imposta l'unità di trasmissione massima (MTU) predefinita per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-180">Sets the default Maximum Transmission Unit (MTU) for a network interface.</span></span><br/> <span data-ttu-id="249c7-181">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="249c7-181">This method is not supported.</span></span><br/>                         |
| [<span data-ttu-id="249c7-182">**SetNumForwardPackets**</span><span class="sxs-lookup"><span data-stu-id="249c7-182">**SetNumForwardPackets**</span></span>](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="249c7-183">Imposta il numero di intestazioni di pacchetti IP allocate per la coda dei pacchetti router.</span><span class="sxs-lookup"><span data-stu-id="249c7-183">Sets the number of IP packet headers allocated for the router packet queue.</span></span><br/>                                                                |
| [<span data-ttu-id="249c7-184">**SetPMTUBHDetect**</span><span class="sxs-lookup"><span data-stu-id="249c7-184">**SetPMTUBHDetect**</span></span>](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="249c7-185">Abilita il rilevamento di router black hole.</span><span class="sxs-lookup"><span data-stu-id="249c7-185">Enables detection of Black Hole routers.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="249c7-186">**SetPMTUDiscovery**</span><span class="sxs-lookup"><span data-stu-id="249c7-186">**SetPMTUDiscovery**</span></span>](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="249c7-187">Abilita l'individuazione dell'unità di trasmissione massima (MTU).</span><span class="sxs-lookup"><span data-stu-id="249c7-187">Enables Maximum Transmission Unit (MTU) discovery.</span></span><br/>                                                                                         |
| [<span data-ttu-id="249c7-188">**SetTcpipNetbios consente**</span><span class="sxs-lookup"><span data-stu-id="249c7-188">**SetTcpipNetbios**</span></span>](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="249c7-189">Imposta l'operazione predefinita di NetBIOS su TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="249c7-189">Sets the default operation of NetBIOS over TCP/IP.</span></span><br/>                                                                                         |
| [<span data-ttu-id="249c7-190">**SetTcpMaxConnectRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="249c7-190">**SetTcpMaxConnectRetransmissions**</span></span>](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | <span data-ttu-id="249c7-191">Imposta il numero di tentativi TCP per la ritrasmissione di una richiesta di connessione prima dell'interruzione.</span><span class="sxs-lookup"><span data-stu-id="249c7-191">Sets the number of attempts TCP will retransmit a connect request before aborting.</span></span><br/>                                                         |
| [<span data-ttu-id="249c7-192">**SetTcpMaxDataRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="249c7-192">**SetTcpMaxDataRetransmissions**</span></span>](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | <span data-ttu-id="249c7-193">Imposta il numero di volte in cui TCP ritrasmetterà un singolo segmento di dati prima di interrompere la connessione.</span><span class="sxs-lookup"><span data-stu-id="249c7-193">Sets the number of times TCP will retransmit an individual data segment before aborting the connection.</span></span><br/>                                    |
| [<span data-ttu-id="249c7-194">**SetTcpNumConnections**</span><span class="sxs-lookup"><span data-stu-id="249c7-194">**SetTcpNumConnections**</span></span>](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="249c7-195">Imposta il numero massimo di connessioni che TCP potrebbe avere aperto simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="249c7-195">Sets the maximum number of connections that TCP may have open simultaneously.</span></span><br/>                                                              |
| [<span data-ttu-id="249c7-196">**SetTcpUseRFC1122UrgentPointer**</span><span class="sxs-lookup"><span data-stu-id="249c7-196">**SetTcpUseRFC1122UrgentPointer**</span></span>](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | <span data-ttu-id="249c7-197">Specifica se TCP utilizza la specifica RFC 1122 per i dati urgenti o la modalità utilizzata dai sistemi derivati da Berkeley Software Design (BSD).</span><span class="sxs-lookup"><span data-stu-id="249c7-197">Specifies whether TCP uses the RFC 1122 specification for urgent data, or the mode used by Berkeley Software Design (BSD) derived systems.</span></span><br/> |
| [<span data-ttu-id="249c7-198">**SetTcpWindowSize**</span><span class="sxs-lookup"><span data-stu-id="249c7-198">**SetTcpWindowSize**</span></span>](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="249c7-199">Imposta le dimensioni massime della finestra di ricezione TCP offerte dal sistema.</span><span class="sxs-lookup"><span data-stu-id="249c7-199">Sets the maximum TCP Receive Window size offered by the system.</span></span><br/>                                                                            |
| [<span data-ttu-id="249c7-200">**SetWINSServer**</span><span class="sxs-lookup"><span data-stu-id="249c7-200">**SetWINSServer**</span></span>](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="249c7-201">Imposta i server WINS (Windows Internet Naming Service) primari e secondari in questa scheda di rete associata a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="249c7-201">Sets the primary and secondary Windows Internet Naming Service (WINS) servers on this TCP/IP-bound network adapter.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="249c7-202">Proprietà</span><span class="sxs-lookup"><span data-stu-id="249c7-202">Properties</span></span>

<span data-ttu-id="249c7-203">La classe **Win32 \_ NetworkAdapterConfiguration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="249c7-203">The **Win32\_NetworkAdapterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="249c7-204">**ArpAlwaysSourceRoute**</span><span class="sxs-lookup"><span data-stu-id="249c7-204">**ArpAlwaysSourceRoute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-205">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-207">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| ArpAlwaysSourceRoute")</span><span class="sxs-lookup"><span data-stu-id="249c7-207">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpAlwaysSourceRoute")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-208">Se **true**, TCP/IP trasmette le query ARP (Address Resolution Protocol) con il routing del codice sorgente abilitato nelle reti token ring.</span><span class="sxs-lookup"><span data-stu-id="249c7-208">If **TRUE**, TCP/IP transmits Address Resolution Protocol (ARP) queries with source routing enabled on Token Ring networks.</span></span> <span data-ttu-id="249c7-209">Per impostazione predefinita (FALSE), ARP esegue prima una query senza routing del codice sorgente, quindi tenta di eseguire il routing del codice sorgente se non viene ricevuta alcuna risposta.</span><span class="sxs-lookup"><span data-stu-id="249c7-209">By default (FALSE), ARP first queries without source routing, and then retries with source routing enabled if no reply is received.</span></span> <span data-ttu-id="249c7-210">Il routing del codice sorgente consente il routing dei pacchetti di rete tra diversi tipi di reti.</span><span class="sxs-lookup"><span data-stu-id="249c7-210">Source routing allows the routing of network packets across different types of networks.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-211">**ArpUseEtherSNAP**</span><span class="sxs-lookup"><span data-stu-id="249c7-211">**ArpUseEtherSNAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-212">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-214">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| ArpUseEtherSNAP")</span><span class="sxs-lookup"><span data-stu-id="249c7-214">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpUseEtherSNAP")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-215">Se il valore è **true**, i pacchetti Ethernet seguono la codifica di SNAP (Sub-Network Access Protocol) IEEE 802,3.</span><span class="sxs-lookup"><span data-stu-id="249c7-215">If **TRUE**, Ethernet packets follow the IEEE 802.3 Sub-Network Access Protocol (SNAP) encoding.</span></span> <span data-ttu-id="249c7-216">Impostando questo parametro su 1 si impone a TCP/IP di trasmettere i pacchetti Ethernet utilizzando la codifica di SNAP 802,3.</span><span class="sxs-lookup"><span data-stu-id="249c7-216">Setting this parameter to 1 forces TCP/IP to transmit Ethernet packets by using 802.3 SNAP encoding.</span></span> <span data-ttu-id="249c7-217">Per impostazione predefinita (FALSE), lo stack trasmette i pacchetti in formato Ethernet DIX.</span><span class="sxs-lookup"><span data-stu-id="249c7-217">By default (FALSE), the stack transmits packets in DIX Ethernet format.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-218">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="249c7-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="249c7-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-221">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="249c7-221">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="249c7-222">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="249c7-222">Short textual description of the current object.</span></span>

<span data-ttu-id="249c7-223">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="249c7-223">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="249c7-224">**DatabasePath**</span><span class="sxs-lookup"><span data-stu-id="249c7-224">**DatabasePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="249c7-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-227">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| DatabasePath")</span><span class="sxs-lookup"><span data-stu-id="249c7-227">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DatabasePath")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-228">Percorso file di Windows valido per i file di database Internet standard (host, LMHOSTS, reti e protocolli).</span><span class="sxs-lookup"><span data-stu-id="249c7-228">Valid Windows file path to standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span> <span data-ttu-id="249c7-229">Il percorso del file viene utilizzato dall'interfaccia Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="249c7-229">The file path is used by the Windows Sockets interface.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-230">**DeadGWDetectEnabled**</span><span class="sxs-lookup"><span data-stu-id="249c7-230">**DeadGWDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-231">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-233">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| EnableDeadGWDetect")</span><span class="sxs-lookup"><span data-stu-id="249c7-233">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDeadGWDetect")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-234">Se **true**, si verifica il rilevamento del gateway inattivo.</span><span class="sxs-lookup"><span data-stu-id="249c7-234">If **TRUE**, dead gateway detection occurs.</span></span> <span data-ttu-id="249c7-235">Se questa funzionalità è abilitata, Transmission Control Protocol (TCP) richiede il protocollo IP (Internet Protocol) per passare a un gateway di backup se ritrasmette un segmento più volte senza ricevere una risposta.</span><span class="sxs-lookup"><span data-stu-id="249c7-235">With this feature enabled, Transmission Control Protocol (TCP) asks Internet Protocol (IP) to change to a backup gateway if it retransmits a segment several times without receiving a response.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-236">**DefaultIPGateway**</span><span class="sxs-lookup"><span data-stu-id="249c7-236">**DefaultIPGateway**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-237">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="249c7-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="249c7-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-239">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \| GatewayPredefinito")</span><span class="sxs-lookup"><span data-stu-id="249c7-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|DefaultGateway")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-240">Matrice di indirizzi IP di gateway predefiniti usati dal computer.</span><span class="sxs-lookup"><span data-stu-id="249c7-240">Array of IP addresses of default gateways that the computer system uses.</span></span>

<span data-ttu-id="249c7-241">Esempio: "192.168.12.1 192.168.46.1"</span><span class="sxs-lookup"><span data-stu-id="249c7-241">Example: "192.168.12.1 192.168.46.1"</span></span>

</dd> <dt>

<span data-ttu-id="249c7-242">**DefaultTOS**</span><span class="sxs-lookup"><span data-stu-id="249c7-242">**DefaultTOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-243">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="249c7-243">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-245">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| DefaultTOS")</span><span class="sxs-lookup"><span data-stu-id="249c7-245">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTOS")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-246">Valore predefinito del tipo di servizio (TOS) impostato nell'intestazione dei pacchetti IP in uscita.</span><span class="sxs-lookup"><span data-stu-id="249c7-246">Default Type Of Service (TOS) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="249c7-247">La richiesta di commenti (RFC) 791 definisce i valori.</span><span class="sxs-lookup"><span data-stu-id="249c7-247">Request for Comments (RFC) 791 defines the values.</span></span> <span data-ttu-id="249c7-248">Valore predefinito: 0 (zero), intervallo valido: 0-255.</span><span class="sxs-lookup"><span data-stu-id="249c7-248">Default: 0 (zero), Valid Range: 0 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-249">**DefaultTTL**</span><span class="sxs-lookup"><span data-stu-id="249c7-249">**DefaultTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-250">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="249c7-250">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-252">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| DefaultTTL")</span><span class="sxs-lookup"><span data-stu-id="249c7-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTTL")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-253">Valore predefinito TTL (time to Live) impostato nell'intestazione dei pacchetti IP in uscita.</span><span class="sxs-lookup"><span data-stu-id="249c7-253">Default Time To Live (TTL) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="249c7-254">La durata (TTL) specifica il numero di router che un pacchetto IP può attraversare per raggiungere la destinazione prima di essere scartato.</span><span class="sxs-lookup"><span data-stu-id="249c7-254">The TTL specifies the number of routers an IP packet can pass through to reach its destination before being discarded.</span></span> <span data-ttu-id="249c7-255">Ogni router decrementa di uno il numero di TTL di un pacchetto mentre passa attraverso ed Elimina i pacchetti, se il valore TTL è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="249c7-255">Each router decrements by one the TTL count of a packet as it passes through and discards the packets—if the TTL is 0 (zero).</span></span> <span data-ttu-id="249c7-256">Valore predefinito: 32, intervallo valido: 1-255.</span><span class="sxs-lookup"><span data-stu-id="249c7-256">Default: 32, Valid Range: 1 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-257">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="249c7-257">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="249c7-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="249c7-260">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="249c7-260">Textual description of the current object.</span></span>

<span data-ttu-id="249c7-261">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="249c7-261">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="249c7-262">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="249c7-262">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-263">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-263">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-265">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP")</span><span class="sxs-lookup"><span data-stu-id="249c7-265">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|EnableDHCP")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-266">Se **true**, il server DHCP (Dynamic Host Configuration Protocol) assegna automaticamente un indirizzo IP al sistema quando stabilisce una connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-266">If **TRUE**, the dynamic host configuration protocol (DHCP) server automatically assigns an IP address to the computer system when establishing a network connection.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-267">**DHCPLeaseExpires**</span><span class="sxs-lookup"><span data-stu-id="249c7-267">**DHCPLeaseExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-268">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="249c7-268">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-270">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| LeaseTerminatesTime")</span><span class="sxs-lookup"><span data-stu-id="249c7-270">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseTerminatesTime")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-271">Data e ora di scadenza per un indirizzo IP con lease assegnato al computer dal server DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="249c7-271">Expiration date and time for a leased IP address that was assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="249c7-272">Esempio: 20521201000230,000000000</span><span class="sxs-lookup"><span data-stu-id="249c7-272">Example: 20521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="249c7-273">**DHCPLeaseObtained**</span><span class="sxs-lookup"><span data-stu-id="249c7-273">**DHCPLeaseObtained**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-274">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="249c7-274">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-276">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| LeaseObtainedTime")</span><span class="sxs-lookup"><span data-stu-id="249c7-276">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseObtainedTime")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-277">Data e ora in cui è stato ottenuto il lease per l'indirizzo IP assegnato al computer dal server DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="249c7-277">Date and time the lease was obtained for the IP address assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="249c7-278">Esempio: 19521201000230,000000000</span><span class="sxs-lookup"><span data-stu-id="249c7-278">Example: 19521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="249c7-279">**DHCPServer**</span><span class="sxs-lookup"><span data-stu-id="249c7-279">**DHCPServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-280">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="249c7-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-282">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| dhcpserver")</span><span class="sxs-lookup"><span data-stu-id="249c7-282">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|DhcpServer")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-283">Indirizzo IP del server DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="249c7-283">IP address of the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="249c7-284">Esempio: "10.55.34.2"</span><span class="sxs-lookup"><span data-stu-id="249c7-284">Example: "10.55.34.2"</span></span>

</dd> <dt>

<span data-ttu-id="249c7-285">**DNSDomain**</span><span class="sxs-lookup"><span data-stu-id="249c7-285">**DNSDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="249c7-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-288">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| Domain")</span><span class="sxs-lookup"><span data-stu-id="249c7-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Domain")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-289">Nome dell'organizzazione seguito da un punto e un'estensione che indica il tipo di organizzazione, ad esempio "microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="249c7-289">Organization name followed by a period and an extension that indicates the type of organization, such as "microsoft.com".</span></span> <span data-ttu-id="249c7-290">Il nome può essere una qualsiasi combinazione di lettere da A A Z, i numeri da 0 A 9 e il trattino (-), più il carattere punto (.) utilizzato come separatore.</span><span class="sxs-lookup"><span data-stu-id="249c7-290">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span>

<span data-ttu-id="249c7-291">Esempio: "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="249c7-291">Example: "microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="249c7-292">**DNSDomainSuffixSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="249c7-292">**DNSDomainSuffixSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-293">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="249c7-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="249c7-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-295">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| Searching")</span><span class="sxs-lookup"><span data-stu-id="249c7-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|SearchList")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-296">Matrice di suffissi di dominio DNS da accodare alla fine dei nomi host durante la risoluzione del nome.</span><span class="sxs-lookup"><span data-stu-id="249c7-296">Array of DNS domain suffixes to be appended to the end of host names during name resolution.</span></span> <span data-ttu-id="249c7-297">Quando si tenta di risolvere un nome di dominio completo (FQDN) da un nome di solo host, il sistema aggiungerà prima di tutto il nome di dominio locale.</span><span class="sxs-lookup"><span data-stu-id="249c7-297">When attempting to resolve a fully qualified domain name (FQDN) from a host-only name, the system will first append the local domain name.</span></span> <span data-ttu-id="249c7-298">Se l'operazione non riesce, il sistema utilizzerà l'elenco dei suffissi di dominio per creare nomi di dominio completi aggiuntivi nell'ordine elencato ed eseguirà una query sui server DNS per ciascuno di essi.</span><span class="sxs-lookup"><span data-stu-id="249c7-298">If this is not successful, the system will use the domain suffix list to create additional FQDNs in the order listed and query DNS servers for each.</span></span>

<span data-ttu-id="249c7-299">Esempio: "samples.microsoft.com example.microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="249c7-299">Example: "samples.microsoft.com example.microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="249c7-300">**DNSEnabledForWINSResolution**</span><span class="sxs-lookup"><span data-stu-id="249c7-300">**DNSEnabledForWINSResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-301">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-303">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| EnableDNS")</span><span class="sxs-lookup"><span data-stu-id="249c7-303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDNS")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-304">Se **true**, il Domain Name System (DNS) è abilitato per la risoluzione dei nomi sulla risoluzione di Windows Internet Naming Service (WINS).</span><span class="sxs-lookup"><span data-stu-id="249c7-304">If **TRUE**, the Domain Name System (DNS) is enabled for name resolution over Windows Internet Naming Service (WINS) resolution.</span></span> <span data-ttu-id="249c7-305">Se il nome non può essere risolto con DNS, la richiesta del nome viene trasmessa a WINS per la risoluzione.</span><span class="sxs-lookup"><span data-stu-id="249c7-305">If the name cannot be resolved using DNS, the name request is forwarded to WINS for resolution.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-306">**DNSHostName**</span><span class="sxs-lookup"><span data-stu-id="249c7-306">**DNSHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="249c7-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-309">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| hostname")</span><span class="sxs-lookup"><span data-stu-id="249c7-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Hostname")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-310">Nome host utilizzato per identificare il computer locale per l'autenticazione da parte di alcune utilità.</span><span class="sxs-lookup"><span data-stu-id="249c7-310">Host name used to identify the local computer for authentication by some utilities.</span></span> <span data-ttu-id="249c7-311">Altre utilità basate su TCP/IP possono usare questo valore per acquisire il nome del computer locale.</span><span class="sxs-lookup"><span data-stu-id="249c7-311">Other TCP/IP-based utilities can use this value to acquire the name of the local computer.</span></span> <span data-ttu-id="249c7-312">I nomi host vengono archiviati nei server DNS di una tabella che esegue il mapping dei nomi agli indirizzi IP per l'utilizzo da DNS.</span><span class="sxs-lookup"><span data-stu-id="249c7-312">Host names are stored on DNS servers in a table that maps names to IP addresses for use by DNS.</span></span> <span data-ttu-id="249c7-313">Il nome può essere una qualsiasi combinazione di lettere da A A Z, i numeri da 0 A 9 e il trattino (-), più il carattere punto (.) utilizzato come separatore.</span><span class="sxs-lookup"><span data-stu-id="249c7-313">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span> <span data-ttu-id="249c7-314">Per impostazione predefinita, questo valore è il nome del computer di rete Microsoft, ma l'amministratore di rete può assegnare un altro nome host senza influire sul nome del computer.</span><span class="sxs-lookup"><span data-stu-id="249c7-314">By default, this value is the Microsoft networking computer name, but the network administrator can assign another host name without affecting the computer name.</span></span>

<span data-ttu-id="249c7-315">Esempio: "corpdns"</span><span class="sxs-lookup"><span data-stu-id="249c7-315">Example: "corpdns"</span></span>

</dd> <dt>

<span data-ttu-id="249c7-316">**DNSServerSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="249c7-316">**DNSServerSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-317">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="249c7-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="249c7-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-319">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| nameserver")</span><span class="sxs-lookup"><span data-stu-id="249c7-319">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NameServer")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-320">Matrice di indirizzi IP del server da utilizzare nell'esecuzione di query per i server DNS.</span><span class="sxs-lookup"><span data-stu-id="249c7-320">Array of server IP addresses to be used in querying for DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-321">**DomainDNSRegistrationEnabled**</span><span class="sxs-lookup"><span data-stu-id="249c7-321">**DomainDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-322">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="249c7-324">Se **true**, gli indirizzi IP per questa connessione vengono registrati in DNS con il nome di dominio della connessione, oltre a essere registrati con il nome DNS completo del computer.</span><span class="sxs-lookup"><span data-stu-id="249c7-324">If **TRUE**, the IP addresses for this connection are registered in DNS under the domain name of this connection in addition to being registered under the computer's full DNS name.</span></span> <span data-ttu-id="249c7-325">Il nome di dominio della connessione viene impostato tramite il metodo [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() o assegnato da DSCP.</span><span class="sxs-lookup"><span data-stu-id="249c7-325">The domain name of this connection is either set using the [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() method or assigned by DSCP.</span></span> <span data-ttu-id="249c7-326">Il nome registrato è il nome host del computer a cui è stato aggiunto il nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="249c7-326">The registered name is the host name of the computer with the domain name appended.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-327">**ForwardBufferMemory**</span><span class="sxs-lookup"><span data-stu-id="249c7-327">**ForwardBufferMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-328">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="249c7-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-330">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="249c7-330">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-331">Memoria allocata dall'IP per archiviare i dati dei pacchetti nella coda dei pacchetti del router.</span><span class="sxs-lookup"><span data-stu-id="249c7-331">Memory allocated by IP to store packet data in the router packet queue.</span></span> <span data-ttu-id="249c7-332">Quando lo spazio del buffer viene riempito, il router inizia a scartare i pacchetti in modo casuale dalla propria coda.</span><span class="sxs-lookup"><span data-stu-id="249c7-332">When this buffer space is filled, the router begins discarding packets at random from its queue.</span></span> <span data-ttu-id="249c7-333">I buffer di dati della coda di pacchetti hanno una lunghezza di 256 byte, quindi il valore di questo parametro deve essere un multiplo di 256.</span><span class="sxs-lookup"><span data-stu-id="249c7-333">Packet queue data buffers are 256 bytes in length, so the value of this parameter should be a multiple of 256.</span></span> <span data-ttu-id="249c7-334">Più buffer vengono concatenati per i pacchetti più grandi.</span><span class="sxs-lookup"><span data-stu-id="249c7-334">Multiple buffers are chained together for larger packets.</span></span> <span data-ttu-id="249c7-335">L'intestazione IP per un pacchetto viene archiviata separatamente.</span><span class="sxs-lookup"><span data-stu-id="249c7-335">The IP header for a packet is stored separately.</span></span> <span data-ttu-id="249c7-336">Questo parametro viene ignorato e non vengono allocati buffer se il router IP non è abilitato.</span><span class="sxs-lookup"><span data-stu-id="249c7-336">This parameter is ignored and no buffers are allocated if the IP router is not enabled.</span></span> <span data-ttu-id="249c7-337">La dimensione del buffer può variare dall'MTU di rete a un valore inferiore a 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="249c7-337">The buffer size can range from the network MTU to a value smaller than 0xFFFFFFFF.</span></span> <span data-ttu-id="249c7-338">Valore predefinito: 74240 (pacchetti da 50 1480 byte, arrotondati a un multiplo di 256).</span><span class="sxs-lookup"><span data-stu-id="249c7-338">Default: 74240 (fifty 1480-byte packets, rounded to a multiple of 256).</span></span>

</dd> <dt>

<span data-ttu-id="249c7-339">**FullDNSRegistrationEnabled**</span><span class="sxs-lookup"><span data-stu-id="249c7-339">**FullDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-340">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-340">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="249c7-342">Se **true**, gli indirizzi IP per questa connessione sono registrati in DNS con il nome DNS completo del computer.</span><span class="sxs-lookup"><span data-stu-id="249c7-342">If **TRUE**, the IP addresses for this connection are registered in DNS under the computer's full DNS name.</span></span> <span data-ttu-id="249c7-343">Il nome DNS completo del computer viene visualizzato nella scheda **Identificazione rete** dell'applicazione di sistema nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="249c7-343">The full DNS name of the computer is displayed on the **Network Identification** tab in the System application in Control Panel.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-344">**GatewayCostMetric**</span><span class="sxs-lookup"><span data-stu-id="249c7-344">**GatewayCostMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-345">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="249c7-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="249c7-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="249c7-347">Matrice di valori di metrica dei costi interi (compresi tra 1 e 9999) da usare per il calcolo delle route più veloci, più affidabili o meno a elevato utilizzo di risorse.</span><span class="sxs-lookup"><span data-stu-id="249c7-347">Array of integer cost metric values (ranging from 1 to 9999) to be used in calculating the fastest, most reliable, or least resource-intensive routes.</span></span> <span data-ttu-id="249c7-348">Questo argomento ha una corrispondenza uno-a-uno con la proprietà **DefaultIPGateway** .</span><span class="sxs-lookup"><span data-stu-id="249c7-348">This argument has a one-to-one correspondence with the **DefaultIPGateway** property.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-349">**IGMPLevel**</span><span class="sxs-lookup"><span data-stu-id="249c7-349">**IGMPLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-350">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="249c7-350">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-352">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| IGMPLevel")</span><span class="sxs-lookup"><span data-stu-id="249c7-352">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IGMPLevel")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-353">Extent a cui il sistema supporta il multicast IP e partecipa al protocollo IGMP (Internet Group Management Protocol).</span><span class="sxs-lookup"><span data-stu-id="249c7-353">Extent to which the system supports IP multicast and participates in the Internet Group Management Protocol (IGMP).</span></span> <span data-ttu-id="249c7-354">Al livello 0 (zero), il sistema non fornisce alcun supporto per il multicast.</span><span class="sxs-lookup"><span data-stu-id="249c7-354">At level 0 (zero), the system provides no multicast support.</span></span> <span data-ttu-id="249c7-355">Al livello 1, il sistema può inviare solo pacchetti multicast IP.</span><span class="sxs-lookup"><span data-stu-id="249c7-355">At level 1, the system may only send IP multicast packets.</span></span> <span data-ttu-id="249c7-356">Al livello 2, il sistema può inviare pacchetti multicast IP e partecipare completamente a IGMP per ricevere pacchetti multicast.</span><span class="sxs-lookup"><span data-stu-id="249c7-356">At level 2, the system may send IP multicast packets and fully participate in IGMP to receive multicast packets.</span></span>

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span data-ttu-id="249c7-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**Nessun multicast** (0)</span><span class="sxs-lookup"><span data-stu-id="249c7-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**No Multicast** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span data-ttu-id="249c7-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**Multicast IP** (1)</span><span class="sxs-lookup"><span data-stu-id="249c7-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**IP Multicast** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span data-ttu-id="249c7-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**Multicast IP & IGMP** (2)</span><span class="sxs-lookup"><span data-stu-id="249c7-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP & IGMP multicast** (2)</span></span>


</dt> <dd>

<span data-ttu-id="249c7-360">Multicast IP e IGMP (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="249c7-360">IP and IGMP Multicast (default)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="249c7-361">**Index**</span><span class="sxs-lookup"><span data-stu-id="249c7-361">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-362">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="249c7-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-364">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="249c7-364">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-365">Numero di indice della configurazione della scheda di rete Windows.</span><span class="sxs-lookup"><span data-stu-id="249c7-365">Index number of the Windows network adapter configuration.</span></span> <span data-ttu-id="249c7-366">Il numero di indice viene usato quando è disponibile più di una configurazione.</span><span class="sxs-lookup"><span data-stu-id="249c7-366">The index number is used when there is more than one configuration available.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-367">**IndiceInterfaccia**</span><span class="sxs-lookup"><span data-stu-id="249c7-367">**InterfaceIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-368">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="249c7-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="249c7-370">Valore di indice che identifica in modo univoco un'interfaccia di rete locale.</span><span class="sxs-lookup"><span data-stu-id="249c7-370">Index value that uniquely identifies a local network interface.</span></span> <span data-ttu-id="249c7-371">Il valore in questa proprietà corrisponde al valore della proprietà **IndiceInterfaccia** nell'istanza di [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) che rappresenta l'interfaccia di rete nella tabella di route.</span><span class="sxs-lookup"><span data-stu-id="249c7-371">The value in this property is the same as the value in the **InterfaceIndex** property in the instance of [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) that represents the network interface in the route table.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-372">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="249c7-372">**IPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-373">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="249c7-373">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="249c7-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-375">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ TCPIP \| IPAddress")</span><span class="sxs-lookup"><span data-stu-id="249c7-375">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip\|IPAddress")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-376">Matrice di tutti gli indirizzi IP associati alla scheda di rete corrente.</span><span class="sxs-lookup"><span data-stu-id="249c7-376">Array of all of the IP addresses associated with the current network adapter.</span></span> <span data-ttu-id="249c7-377">Questa proprietà può contenere indirizzi IPv6 o IPv4.</span><span class="sxs-lookup"><span data-stu-id="249c7-377">This property can contain either IPv6 addresses or IPv4 addresses.</span></span> <span data-ttu-id="249c7-378">Per ulteriori informazioni, vedere [supporto di IPv6 e IPv4 in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="249c7-378">For more information, see [IPv6 and IPv4 Support in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="249c7-379">Esempio di indirizzo IPv6: "2010:836B: 4179:: 836B: 4179"</span><span class="sxs-lookup"><span data-stu-id="249c7-379">Example IPv6 address: "2010:836B:4179::836B:4179"</span></span>

</dd> <dt>

<span data-ttu-id="249c7-380">**IPConnectionMetric**</span><span class="sxs-lookup"><span data-stu-id="249c7-380">**IPConnectionMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-381">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="249c7-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="249c7-383">Costo dell'utilizzo delle route configurate per l'adapter associato IP ed è il valore ponderato per le route nella tabella di routing IP.</span><span class="sxs-lookup"><span data-stu-id="249c7-383">Cost of using the configured routes for the IP bound adapter and is the weighted value for those routes in the IP routing table.</span></span> <span data-ttu-id="249c7-384">Se sono presenti più route a una destinazione nella tabella di routing IP, viene utilizzata la route con la metrica più bassa.</span><span class="sxs-lookup"><span data-stu-id="249c7-384">If there are multiple routes to a destination in the IP routing table, the route with the lowest metric is used.</span></span> <span data-ttu-id="249c7-385">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="249c7-385">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-386">**IPEnabled**</span><span class="sxs-lookup"><span data-stu-id="249c7-386">**IPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-387">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-389">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ tcpip")</span><span class="sxs-lookup"><span data-stu-id="249c7-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-390">Se **true**, TCP/IP è associato e abilitato in questa scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-390">If **TRUE**, TCP/IP is bound and enabled on this network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-391">**IPFilterSecurityEnabled**</span><span class="sxs-lookup"><span data-stu-id="249c7-391">**IPFilterSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-392">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-392">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-394">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| IPFilterSecurityEnabled")</span><span class="sxs-lookup"><span data-stu-id="249c7-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-395">Se **true**, la sicurezza della porta IP è abilitata a livello globale in tutte le schede di rete associate a IP e i valori di sicurezza associati alle singole schede di rete sono attivati.</span><span class="sxs-lookup"><span data-stu-id="249c7-395">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters and the security values associated with individual network adapters are in effect.</span></span> <span data-ttu-id="249c7-396">Questa proprietà viene utilizzata insieme a **IPSecPermitTCPPorts**, **IPSecPermitUDPPorts** e **IPSecPermitIPProtocols**.</span><span class="sxs-lookup"><span data-stu-id="249c7-396">This property is used in conjunction with **IPSecPermitTCPPorts**, **IPSecPermitUDPPorts**, and **IPSecPermitIPProtocols**.</span></span> <span data-ttu-id="249c7-397">Se **false**, la sicurezza del filtro IP viene disabilitata in tutte le schede di rete e consente il flusso non filtrato di tutto il traffico di porta e protocollo.</span><span class="sxs-lookup"><span data-stu-id="249c7-397">If **FALSE**, IP filter security is disabled across all network adapters and allows all port and protocol traffic to flow unfiltered.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-398">**IPPortSecurityEnabled**</span><span class="sxs-lookup"><span data-stu-id="249c7-398">**IPPortSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-399">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-399">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-401">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration \| IPFilterSecurityEnabled")</span><span class="sxs-lookup"><span data-stu-id="249c7-401">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapterConfiguration\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-402">Se **true**, la sicurezza della porta IP è abilitata a livello globale in tutte le schede di rete con binding IP.</span><span class="sxs-lookup"><span data-stu-id="249c7-402">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters.</span></span> <span data-ttu-id="249c7-403">Questa proprietà è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="249c7-403">This property is obsolete.</span></span> <span data-ttu-id="249c7-404">Al posto di questa proprietà, è consigliabile usare **IPFilterSecurityEnabled**.</span><span class="sxs-lookup"><span data-stu-id="249c7-404">In place of this property, you should use **IPFilterSecurityEnabled**.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-405">**IPSecPermitIPProtocols**</span><span class="sxs-lookup"><span data-stu-id="249c7-405">**IPSecPermitIPProtocols**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-406">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="249c7-406">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="249c7-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-408">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| RawIPAllowedProtocols")</span><span class="sxs-lookup"><span data-stu-id="249c7-408">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|RawIPAllowedProtocols")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-409">Matrice dei protocolli di cui è consentita l'esecuzione su IP.</span><span class="sxs-lookup"><span data-stu-id="249c7-409">Array of the protocols permitted to run over the IP.</span></span> <span data-ttu-id="249c7-410">L'elenco di protocolli viene definito utilizzando il metodo [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="249c7-410">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="249c7-411">L'elenco può essere vuoto o contenere valori numerici.</span><span class="sxs-lookup"><span data-stu-id="249c7-411">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="249c7-412">Un valore numerico pari a 0 (zero) indica che è stata concessa l'autorizzazione di accesso per tutti i protocolli.</span><span class="sxs-lookup"><span data-stu-id="249c7-412">A numeric value of 0 (zero) indicates access permission is granted for all protocols.</span></span> <span data-ttu-id="249c7-413">Una stringa vuota indica che non è consentita l'esecuzione di protocolli quando **IPFilterSecurityEnabled** è **true**.</span><span class="sxs-lookup"><span data-stu-id="249c7-413">An empty string indicates that no protocols are permitted to run when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-414">**IPSecPermitTCPPorts**</span><span class="sxs-lookup"><span data-stu-id="249c7-414">**IPSecPermitTCPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-415">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="249c7-415">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="249c7-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-417">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TCPAllowedPorts")</span><span class="sxs-lookup"><span data-stu-id="249c7-417">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TCPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-418">Matrice delle porte a cui verrà concessa l'autorizzazione di accesso per TCP.</span><span class="sxs-lookup"><span data-stu-id="249c7-418">Array of the ports that will be granted access permission for TCP.</span></span> <span data-ttu-id="249c7-419">L'elenco di protocolli viene definito utilizzando il metodo [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="249c7-419">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="249c7-420">L'elenco può essere vuoto o contenere valori numerici.</span><span class="sxs-lookup"><span data-stu-id="249c7-420">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="249c7-421">Un valore numerico pari a 0 (zero) indica che è stata concessa l'autorizzazione di accesso per tutte le porte.</span><span class="sxs-lookup"><span data-stu-id="249c7-421">A numeric value of 0 (zero)indicates access permission is granted for all ports.</span></span> <span data-ttu-id="249c7-422">Una stringa vuota indica che alle porte non è concessa l'autorizzazione di accesso quando **IPFilterSecurityEnabled** è **true**.</span><span class="sxs-lookup"><span data-stu-id="249c7-422">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-423">**IPSecPermitUDPPorts**</span><span class="sxs-lookup"><span data-stu-id="249c7-423">**IPSecPermitUDPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-424">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="249c7-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="249c7-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-426">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| UDPAllowedPorts")</span><span class="sxs-lookup"><span data-stu-id="249c7-426">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UDPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-427">Matrice delle porte a cui verrà concessa l'autorizzazione di accesso UDP (User Datagram Protocol).</span><span class="sxs-lookup"><span data-stu-id="249c7-427">Array of the ports that will be granted User Datagram Protocol (UDP) access permission.</span></span> <span data-ttu-id="249c7-428">L'elenco di protocolli viene definito utilizzando il metodo [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="249c7-428">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="249c7-429">L'elenco può essere vuoto o contenere valori numerici.</span><span class="sxs-lookup"><span data-stu-id="249c7-429">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="249c7-430">Un valore numerico pari a 0 (zero) indica che è stata concessa l'autorizzazione di accesso per tutte le porte.</span><span class="sxs-lookup"><span data-stu-id="249c7-430">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="249c7-431">Una stringa vuota indica che alle porte non è concessa l'autorizzazione di accesso quando **IPFilterSecurityEnabled** è **true**.</span><span class="sxs-lookup"><span data-stu-id="249c7-431">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-432">**IPSubnet**</span><span class="sxs-lookup"><span data-stu-id="249c7-432">**IPSubnet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-433">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="249c7-433">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="249c7-434">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-435">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| \| submask Parameters")</span><span class="sxs-lookup"><span data-stu-id="249c7-435">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|SubnetMask")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-436">Matrice di tutte le subnet mask associate alla scheda di rete corrente.</span><span class="sxs-lookup"><span data-stu-id="249c7-436">Array of all of the subnet masks associated with the current network adapter.</span></span>

<span data-ttu-id="249c7-437">Esempio: "255.255.0.0"</span><span class="sxs-lookup"><span data-stu-id="249c7-437">Example: "255.255.0.0"</span></span>

</dd> <dt>

<span data-ttu-id="249c7-438">**IPUseZeroBroadcast**</span><span class="sxs-lookup"><span data-stu-id="249c7-438">**IPUseZeroBroadcast**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-439">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-440">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-441">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| parametro UseZeroBroadcast")</span><span class="sxs-lookup"><span data-stu-id="249c7-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UseZeroBroadcast")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-442">Se **true**, vengono usati gli zeri IP-broadcast (0.0.0.0) e il sistema usa le trasmissioni-broadcast (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="249c7-442">If **TRUE**, IP zeros-broadcasts are used (0.0.0.0), and the system uses ones-broadcasts (255.255.255.255).</span></span> <span data-ttu-id="249c7-443">I sistemi informatici usano in genere le trasmissioni, ma quelle derivate dalle implementazioni di BSD usano gli zeri.</span><span class="sxs-lookup"><span data-stu-id="249c7-443">Computer systems generally use ones-broadcasts, but those derived from BSD implementations use zeros-broadcasts.</span></span> <span data-ttu-id="249c7-444">I sistemi che non utilizzano le stesse trasmissioni non interagiscono nella stessa rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-444">Systems that do not use that same broadcasts will not interoperate on the same network.</span></span> <span data-ttu-id="249c7-445">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="249c7-445">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-446">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="249c7-446">**IPXAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-447">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="249c7-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-448">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-449">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Sockets versione 2 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| IPX \_ Address")</span><span class="sxs-lookup"><span data-stu-id="249c7-449">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Sockets Version 2\|[**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt)\|IPX\_ADDRESS")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-450">La tecnologia IPX (Internet-Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.</span><span class="sxs-lookup"><span data-stu-id="249c7-450">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-451">**IPXEnabled**</span><span class="sxs-lookup"><span data-stu-id="249c7-451">**IPXEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-452">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-452">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-453">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-454">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="249c7-454">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-455">La tecnologia IPX (Internet-Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.</span><span class="sxs-lookup"><span data-stu-id="249c7-455">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-456">**IPXFrameType**</span><span class="sxs-lookup"><span data-stu-id="249c7-456">**IPXFrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-457">Tipo di dati: matrice **UInt32**</span><span class="sxs-lookup"><span data-stu-id="249c7-457">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="249c7-458">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-459">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ NWLNKIPX \\ \\ Parameters \| PktType")</span><span class="sxs-lookup"><span data-stu-id="249c7-459">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|PktType")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-460">La tecnologia IPX (Internet-Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.</span><span class="sxs-lookup"><span data-stu-id="249c7-460">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

<span data-ttu-id="249c7-461">**Ethernet II** (0)</span><span class="sxs-lookup"><span data-stu-id="249c7-461">**Ethernet II** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="249c7-462">**Ethernet 802,3** (1)</span><span class="sxs-lookup"><span data-stu-id="249c7-462">**Ethernet 802.3** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

<span data-ttu-id="249c7-463">**Ethernet 802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="249c7-463">**Ethernet 802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

<span data-ttu-id="249c7-464">**Snap** -in Ethernet (3)</span><span class="sxs-lookup"><span data-stu-id="249c7-464">**Ethernet SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

<span data-ttu-id="249c7-465">**Automatico** (255)</span><span class="sxs-lookup"><span data-stu-id="249c7-465">**AUTO** (255)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="249c7-466">**IPXMediaType**</span><span class="sxs-lookup"><span data-stu-id="249c7-466">**IPXMediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-467">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="249c7-467">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-468">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-469">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ NWLNKIPX \\ \\ Parameters \| mediaType")</span><span class="sxs-lookup"><span data-stu-id="249c7-469">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|MediaType")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-470">La tecnologia IPX (Internet-Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.</span><span class="sxs-lookup"><span data-stu-id="249c7-470">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="249c7-471">**Ethernet** (1)</span><span class="sxs-lookup"><span data-stu-id="249c7-471">**Ethernet** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="249c7-472">**Token ring** (2)</span><span class="sxs-lookup"><span data-stu-id="249c7-472">**Token ring** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="249c7-473">**FDDI** (3)</span><span class="sxs-lookup"><span data-stu-id="249c7-473">**FDDI** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="249c7-474">**ARCNET** (8)</span><span class="sxs-lookup"><span data-stu-id="249c7-474">**ARCNET** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="249c7-475">**IPXNetworkNumber**</span><span class="sxs-lookup"><span data-stu-id="249c7-475">**IPXNetworkNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-476">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="249c7-476">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="249c7-477">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-478">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ NWLNKIPX \\ \\ Parameters \| numerorete")</span><span class="sxs-lookup"><span data-stu-id="249c7-478">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|NetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-479">La tecnologia IPX (Internet-Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.</span><span class="sxs-lookup"><span data-stu-id="249c7-479">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-480">**IPXVirtualNetNumber**</span><span class="sxs-lookup"><span data-stu-id="249c7-480">**IPXVirtualNetNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-481">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="249c7-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-482">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-483">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ NWLNKIPX \\ \\ Parameters \| VirtualNetworkNumber")</span><span class="sxs-lookup"><span data-stu-id="249c7-483">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|VirtualNetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-484">La tecnologia IPX (Internet-Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.</span><span class="sxs-lookup"><span data-stu-id="249c7-484">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-485">**KeepAliveInterval**</span><span class="sxs-lookup"><span data-stu-id="249c7-485">**KeepAliveInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-486">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="249c7-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-487">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-488">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| keepAliveInterval"), [**unità**](../wmisdk/standard-qualifiers.md) ("millisecondi")</span><span class="sxs-lookup"><span data-stu-id="249c7-488">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-489">L'intervallo separa le ritrasmissioni keep-alive fino a quando non viene ricevuta una risposta.</span><span class="sxs-lookup"><span data-stu-id="249c7-489">Interval separating Keep Alive Retransmissions until a response is received.</span></span> <span data-ttu-id="249c7-490">Dopo la ricezione di una risposta, il ritardo fino a quando la trasmissione Keep-Alive successiva viene nuovamente controllata dal valore di **KeepAliveTime**.</span><span class="sxs-lookup"><span data-stu-id="249c7-490">After a response is received, the delay until the next Keep Alive Transmission is again controlled by the value of **KeepAliveTime**.</span></span> <span data-ttu-id="249c7-491">La connessione verrà interrotta dopo che il numero di ritrasmissioni specificato da **TcpMaxDataRetransmissions** non è stato risposto.</span><span class="sxs-lookup"><span data-stu-id="249c7-491">The connection will be aborted after the number of retransmissions specified by **TcpMaxDataRetransmissions** have gone unanswered.</span></span> <span data-ttu-id="249c7-492">Valore predefinito: 1000, intervallo valido: 1-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="249c7-492">Default: 1000, Valid Range: 1 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-493">**KeepAliveTime**</span><span class="sxs-lookup"><span data-stu-id="249c7-493">**KeepAliveTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-494">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="249c7-494">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-495">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-496">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| keepAliveInterval"), [**unità**](../wmisdk/standard-qualifiers.md) ("millisecondi")</span><span class="sxs-lookup"><span data-stu-id="249c7-496">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-497">La proprietà **KeepAliveTime** indica la frequenza con cui il protocollo TCP tenta di verificare che una connessione inattiva sia ancora intatta inviando un pacchetto keep-alive.</span><span class="sxs-lookup"><span data-stu-id="249c7-497">The **KeepAliveTime** property indicates how often the TCP attempts to verify that an idle connection is still intact by sending a Keep Alive Packet.</span></span> <span data-ttu-id="249c7-498">Un sistema remoto raggiungibile rileverà la trasmissione keep-alive.</span><span class="sxs-lookup"><span data-stu-id="249c7-498">A remote system that is reachable will acknowledge the keep alive transmission.</span></span> <span data-ttu-id="249c7-499">I pacchetti Keep-Alive non vengono inviati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="249c7-499">Keep Alive packets are not sent by default.</span></span> <span data-ttu-id="249c7-500">Questa funzionalità può essere abilitata in una connessione da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="249c7-500">This feature may be enabled in a connection by an application.</span></span> <span data-ttu-id="249c7-501">Valore predefinito: 7,2 milioni (due ore).</span><span class="sxs-lookup"><span data-stu-id="249c7-501">Default: 7,200,000 (two hours).</span></span>

</dd> <dt>

<span data-ttu-id="249c7-502">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="249c7-502">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-503">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="249c7-503">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-504">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-505">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| device input and Output functions \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="249c7-505">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-506">Indirizzo MAC (Media Access Control) della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-506">Media Access Control (MAC) address of the network adapter.</span></span> <span data-ttu-id="249c7-507">Un indirizzo MAC viene assegnato dal produttore per identificare in modo univoco la scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-507">A MAC address is assigned by the manufacturer to uniquely identify the network adapter.</span></span>

<span data-ttu-id="249c7-508">Esempio: "00:80: C7:8F: 6C: 96"</span><span class="sxs-lookup"><span data-stu-id="249c7-508">Example: "00:80:C7:8F:6C:96"</span></span>

</dd> <dt>

<span data-ttu-id="249c7-509">**MTU**</span><span class="sxs-lookup"><span data-stu-id="249c7-509">**MTU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-510">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="249c7-510">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-511">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-512">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="249c7-512">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-513">Esegue l'override dell'unità di trasmissione massima (MTU) predefinita per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-513">Overrides the default Maximum Transmission Unit (MTU) for a network interface.</span></span> <span data-ttu-id="249c7-514">MTU è la dimensione massima del pacchetto (inclusa l'intestazione di trasporto) che il trasporto trasmetterà sulla rete sottostante.</span><span class="sxs-lookup"><span data-stu-id="249c7-514">The MTU is the maximum packet size (including the transport header) that the transport will transmit over the underlying network.</span></span> <span data-ttu-id="249c7-515">Il datagramma IP può estendersi su più pacchetti.</span><span class="sxs-lookup"><span data-stu-id="249c7-515">The IP datagram can span multiple packets.</span></span> <span data-ttu-id="249c7-516">L'intervallo di questo valore si estende alla dimensione minima del pacchetto (68) al valore MTU supportato dalla rete sottostante.</span><span class="sxs-lookup"><span data-stu-id="249c7-516">The range of this value spans the minimum packet size (68) to the MTU supported by the underlying network.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-517">**NumForwardPackets**</span><span class="sxs-lookup"><span data-stu-id="249c7-517">**NumForwardPackets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-518">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="249c7-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-519">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-520">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| NumForwardPackets")</span><span class="sxs-lookup"><span data-stu-id="249c7-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NumForwardPackets")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-521">Numero di intestazioni di pacchetti IP allocate per la coda dei pacchetti router.</span><span class="sxs-lookup"><span data-stu-id="249c7-521">Number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="249c7-522">Quando tutte le intestazioni sono in uso, il router inizierà a eliminare i pacchetti dalla coda in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="249c7-522">When all headers are in use, the router will begin to discard packets from the queue at random.</span></span> <span data-ttu-id="249c7-523">Questo valore deve essere almeno uguale al valore di **ForwardBufferMemory** diviso per la dimensione massima dei dati IP delle reti connesse al router.</span><span class="sxs-lookup"><span data-stu-id="249c7-523">This value should be at least as large as the **ForwardBufferMemory** value divided by the maximum IP data size of the networks connected to the router.</span></span> <span data-ttu-id="249c7-524">Il valore non deve essere maggiore del valore di **ForwardBufferMemory** diviso per 256, poiché per ogni pacchetto vengono utilizzati almeno 256 byte di memoria del buffer di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="249c7-524">It should be no larger than the **ForwardBufferMemory** value divided by 256, since at least 256 bytes of forward buffer memory are used for each packet.</span></span> <span data-ttu-id="249c7-525">Il numero ottimale di pacchetti di avanzamento per una determinata dimensione di **ForwardBufferMemory** dipende dal tipo di traffico sulla rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-525">The optimal number of forward packets for a given **ForwardBufferMemory** size depends on the type of traffic on the network.</span></span> <span data-ttu-id="249c7-526">Tra questi due valori.</span><span class="sxs-lookup"><span data-stu-id="249c7-526">It will be somewhere between these two values.</span></span> <span data-ttu-id="249c7-527">Se il router non è abilitato, questo parametro viene ignorato e non vengono allocate intestazioni.</span><span class="sxs-lookup"><span data-stu-id="249c7-527">If the router is not enabled, this parameter is ignored and no headers are allocated.</span></span> <span data-ttu-id="249c7-528">Valore predefinito: 50, intervallo valido: 1-0xFFFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="249c7-528">Default: 50, Valid Range: 1 - 0xFFFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-529">**PMTUBHDetectEnabled**</span><span class="sxs-lookup"><span data-stu-id="249c7-529">**PMTUBHDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-530">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-530">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-531">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-531">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-532">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| EnablePMTUBHDetect")</span><span class="sxs-lookup"><span data-stu-id="249c7-532">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUBHDetect")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-533">Se **true**, il rilevamento di router black hole si verifica mentre TCP individua il percorso dell'unità di trasmissione massima.</span><span class="sxs-lookup"><span data-stu-id="249c7-533">If **TRUE**, detection of black hole routers occurs while TCP discovers the path of the Maximum Transmission Unit.</span></span> <span data-ttu-id="249c7-534">Un router black hole non restituisce messaggi non raggiungibili della destinazione ICMP quando è necessario frammentare un datagramma IP con il bit not Fragment impostato.</span><span class="sxs-lookup"><span data-stu-id="249c7-534">A black hole router does not return ICMP Destination Unreachable messages when it needs to fragment an IP datagram with the Don't Fragment bit set.</span></span> <span data-ttu-id="249c7-535">TCP dipende dalla ricezione di questi messaggi per l'esecuzione dell'individuazione MTU del percorso.</span><span class="sxs-lookup"><span data-stu-id="249c7-535">TCP depends on receiving these messages to perform Path MTU Discovery.</span></span> <span data-ttu-id="249c7-536">Se questa funzionalità è abilitata, TCP tenterà di inviare segmenti senza il bit non frammento impostato se diverse ritrasmissioni di un segmento non vengono riconosciute.</span><span class="sxs-lookup"><span data-stu-id="249c7-536">With this feature enabled, TCP will try to send segments without the Don't Fragment bit set if several retransmissions of a segment go unacknowledged.</span></span> <span data-ttu-id="249c7-537">Se il segmento viene riconosciuto come risultato, la MSS verrà ridotta e il bit not Fragment verrà impostato in pacchetti futuri sulla connessione.</span><span class="sxs-lookup"><span data-stu-id="249c7-537">If the segment is acknowledged as a result, the MSS will be decreased and the Don't Fragment bit will be set in future packets on the connection.</span></span> <span data-ttu-id="249c7-538">L'abilitazione del rilevamento di buchi neri aumenta il numero massimo di ritrasmissioni eseguite per un determinato segmento.</span><span class="sxs-lookup"><span data-stu-id="249c7-538">Enabling black hole detection increases the maximum number of retransmissions performed for a given segment.</span></span> <span data-ttu-id="249c7-539">Il valore predefinito di questa proprietà è **false**.</span><span class="sxs-lookup"><span data-stu-id="249c7-539">The default value of this property is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-540">**PMTUDiscoveryEnabled consente**</span><span class="sxs-lookup"><span data-stu-id="249c7-540">**PMTUDiscoveryEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-541">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-541">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-542">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-543">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| EnablePMTUDiscovery")</span><span class="sxs-lookup"><span data-stu-id="249c7-543">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUDiscovery")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-544">Se **true**, il percorso dell'unità di trasmissione massima (MTU) viene individuato sul percorso di un host remoto.</span><span class="sxs-lookup"><span data-stu-id="249c7-544">If **TRUE**, the Maximum Transmission Unit (MTU) path is discovered over the path to a remote host.</span></span> <span data-ttu-id="249c7-545">Scoprendo il percorso MTU e limitando i segmenti TCP a queste dimensioni, TCP può eliminare la frammentazione nei router lungo il percorso che connette le reti con MTU diversi.</span><span class="sxs-lookup"><span data-stu-id="249c7-545">By discovering the MTU path and limiting TCP segments to this size, TCP can eliminate fragmentation at routers along the path that connect networks with different MTUs.</span></span> <span data-ttu-id="249c7-546">La frammentazione influisce negativamente sulla velocità effettiva TCP e sulla congestione della rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-546">Fragmentation adversely affects TCP throughput and network congestion.</span></span> <span data-ttu-id="249c7-547">Impostando questo parametro su **false** , viene usato un MTU di 576 byte per tutte le connessioni che non sono computer nella subnet locale.</span><span class="sxs-lookup"><span data-stu-id="249c7-547">Setting this parameter to **FALSE** causes an MTU of 576 bytes to be used for all connections that are not to machines on the local subnet.</span></span> <span data-ttu-id="249c7-548">Il valore predefinito è **true**.</span><span class="sxs-lookup"><span data-stu-id="249c7-548">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-549">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="249c7-549">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-550">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="249c7-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-551">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-551">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-552">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")</span><span class="sxs-lookup"><span data-stu-id="249c7-552">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ServiceName")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-553">Nome del servizio della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-553">Service name of the network adapter.</span></span> <span data-ttu-id="249c7-554">Questo nome è in genere più breve del nome completo del prodotto.</span><span class="sxs-lookup"><span data-stu-id="249c7-554">This name is usually shorter than the full product name.</span></span>

<span data-ttu-id="249c7-555">Esempio: "Elnkii"</span><span class="sxs-lookup"><span data-stu-id="249c7-555">Example: "Elnkii"</span></span>

</dd> <dt>

<span data-ttu-id="249c7-556">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="249c7-556">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-557">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="249c7-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-558">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-559">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="249c7-559">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="249c7-560">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="249c7-560">Identifier by which the current object is known.</span></span>

<span data-ttu-id="249c7-561">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="249c7-561">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="249c7-562">**TcpipNetbiosOptions**</span><span class="sxs-lookup"><span data-stu-id="249c7-562">**TcpipNetbiosOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-563">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="249c7-563">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-564">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-564">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="249c7-565">Bitmap delle possibili impostazioni correlate a NetBIOS su TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="249c7-565">Bitmap of the possible settings related to NetBIOS over TCP/IP.</span></span> <span data-ttu-id="249c7-566">I valori sono identificati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="249c7-566">Values are identified in the following list.</span></span>

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

<span data-ttu-id="249c7-567">**EnableNetbiosViaDhcp** (0)</span><span class="sxs-lookup"><span data-stu-id="249c7-567">**EnableNetbiosViaDhcp** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

<span data-ttu-id="249c7-568">**EnableNetbios** (1)</span><span class="sxs-lookup"><span data-stu-id="249c7-568">**EnableNetbios** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

<span data-ttu-id="249c7-569">**DisableNetbios** (2)</span><span class="sxs-lookup"><span data-stu-id="249c7-569">**DisableNetbios** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="249c7-570">**TcpMaxConnectRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="249c7-570">**TcpMaxConnectRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-571">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="249c7-571">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-572">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-573">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TcpMaxConnectRetransmissions")</span><span class="sxs-lookup"><span data-stu-id="249c7-573">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxConnectRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-574">Numero di tentativi effettuati da TCP per ritrasmettere una richiesta di connessione prima di terminare la connessione.</span><span class="sxs-lookup"><span data-stu-id="249c7-574">Number of times TCP attempts to retransmit a Connect Request before terminating the connection.</span></span> <span data-ttu-id="249c7-575">Il timeout di ritrasmissione iniziale è di 3 secondi.</span><span class="sxs-lookup"><span data-stu-id="249c7-575">The initial retransmission timeout is 3 seconds.</span></span> <span data-ttu-id="249c7-576">Il timeout di ritrasmissione raddoppia per ogni tentativo.</span><span class="sxs-lookup"><span data-stu-id="249c7-576">The retransmission timeout doubles for each attempt.</span></span> <span data-ttu-id="249c7-577">Valore predefinito: 3, intervallo valido: 0-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="249c7-577">Default: 3, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-578">**TcpMaxDataRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="249c7-578">**TcpMaxDataRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-579">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="249c7-579">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-580">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-581">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TcpMaxDataRetransmissions")</span><span class="sxs-lookup"><span data-stu-id="249c7-581">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxDataRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-582">Numero di volte in cui TCP ritrasmette un singolo segmento di dati (segmento non di connessione) prima di terminare la connessione.</span><span class="sxs-lookup"><span data-stu-id="249c7-582">Number of times TCP retransmits an individual data segment (nonconnect segment) before terminating the connection.</span></span> <span data-ttu-id="249c7-583">Il timeout di ritrasmissione raddoppia con ogni ritrasmissione successiva in una connessione.</span><span class="sxs-lookup"><span data-stu-id="249c7-583">The retransmission timeout doubles with each successive retransmission on a connection.</span></span> <span data-ttu-id="249c7-584">Valore predefinito: 5, intervallo valido: 0-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="249c7-584">Default: 5, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-585">**TcpNumConnections**</span><span class="sxs-lookup"><span data-stu-id="249c7-585">**TcpNumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-586">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="249c7-586">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-587">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-587">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-588">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TcpNumConnections")</span><span class="sxs-lookup"><span data-stu-id="249c7-588">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpNumConnections")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-589">Numero massimo di connessioni che TCP può aprire contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="249c7-589">Maximum number of connections that TCP can have open simultaneously.</span></span> <span data-ttu-id="249c7-590">Impostazione predefinita: 0xFFFFFE, intervallo valido: 0-0xFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="249c7-590">Default: 0xFFFFFE, Valid Range: 0 - 0xFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-591">**TcpUseRFC1122UrgentPointer**</span><span class="sxs-lookup"><span data-stu-id="249c7-591">**TcpUseRFC1122UrgentPointer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-592">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-592">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-593">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-593">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-594">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TcpUseRFC1122UrgentPointer")</span><span class="sxs-lookup"><span data-stu-id="249c7-594">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpUseRFC1122UrgentPointer")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-595">Se **true**, TCP utilizza la specifica RFC 1122 per i dati urgenti.</span><span class="sxs-lookup"><span data-stu-id="249c7-595">If **TRUE**, TCP uses the RFC 1122 specification for urgent data.</span></span> <span data-ttu-id="249c7-596">Se **false** (impostazione predefinita), TCP utilizza la modalità utilizzata dai sistemi derivati di Berkeley Software Design (BSD).</span><span class="sxs-lookup"><span data-stu-id="249c7-596">If **FALSE** (default), TCP uses the mode used by Berkeley Software Design (BSD) derived systems.</span></span> <span data-ttu-id="249c7-597">I due meccanismi interpretano il puntatore urgente in modo diverso e non sono interoperativi.</span><span class="sxs-lookup"><span data-stu-id="249c7-597">The two mechanisms interpret the urgent pointer differently and are not interoperable.</span></span> <span data-ttu-id="249c7-598">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="249c7-598">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-599">**TcpWindowSize**</span><span class="sxs-lookup"><span data-stu-id="249c7-599">**TcpWindowSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-600">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="249c7-600">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-601">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-601">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-602">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="249c7-602">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-603">Dimensioni massime della finestra di ricezione TCP offerte dal sistema.</span><span class="sxs-lookup"><span data-stu-id="249c7-603">Maximum TCP Receive Window size offered by the system.</span></span> <span data-ttu-id="249c7-604">Nella finestra di ricezione viene specificato il numero di byte che un mittente può trasmettere senza ricevere un riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="249c7-604">The Receive Window specifies the number of bytes a sender may transmit without receiving an acknowledgment.</span></span> <span data-ttu-id="249c7-605">In generale, le finestre di ricezione più grandi migliorano le prestazioni rispetto alle reti ad alto ritardo e a larghezza di banda elevata.</span><span class="sxs-lookup"><span data-stu-id="249c7-605">In general, larger receiving windows will improve performance over high-delay and high-bandwidth networks.</span></span> <span data-ttu-id="249c7-606">Per migliorare l'efficienza, la finestra di ricezione deve essere un multiplo pari delle dimensioni del segmento massimo TCP (MSS).</span><span class="sxs-lookup"><span data-stu-id="249c7-606">For efficiency, the receiving window should be an even multiple of the TCP Maximum Segment Size (MSS).</span></span> <span data-ttu-id="249c7-607">Impostazione predefinita: quattro volte la dimensione massima dei dati TCP o un multiplo pari delle dimensioni dei dati TCP arrotondati al multiplo più vicino di 8192.</span><span class="sxs-lookup"><span data-stu-id="249c7-607">Default: Four times the maximum TCP data size or an even multiple of TCP data size rounded up to the nearest multiple of 8192.</span></span> <span data-ttu-id="249c7-608">Il valore predefinito per le reti Ethernet è 8760.</span><span class="sxs-lookup"><span data-stu-id="249c7-608">Ethernet networks default to 8760.</span></span> <span data-ttu-id="249c7-609">Intervallo valido: 0-65535.</span><span class="sxs-lookup"><span data-stu-id="249c7-609">Valid range: 0 - 65535.</span></span>

> [!Note]  
> <span data-ttu-id="249c7-610">Windows Vista: questa proprietà accede alla `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` voce del registro di sistema, che non viene usata nell'implementazione corrente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="249c7-610">Windows Vista: This property accesses the `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` registry entry, which is not used in the current implementation of the operating system.</span></span>

 

</dd> <dt>

<span data-ttu-id="249c7-611">**WINSEnableLMHostsLookup**</span><span class="sxs-lookup"><span data-stu-id="249c7-611">**WINSEnableLMHostsLookup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-612">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="249c7-612">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-613">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-613">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-614">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| EnableLMHOSTS")</span><span class="sxs-lookup"><span data-stu-id="249c7-614">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableLMHOSTS")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-615">Se **true**, vengono usati i file di ricerca locali.</span><span class="sxs-lookup"><span data-stu-id="249c7-615">If **TRUE**, local lookup files are used.</span></span> <span data-ttu-id="249c7-616">I file di ricerca conterranno una mappa degli indirizzi IP ai nomi host.</span><span class="sxs-lookup"><span data-stu-id="249c7-616">Lookup files will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="249c7-617">Se sono presenti nel sistema locale, saranno disponibili in% SystemRoot% \\ system32 \\ drivers e \\ così via.</span><span class="sxs-lookup"><span data-stu-id="249c7-617">If they exist on the local system, they will be found in %SystemRoot%\\system32\\drivers\\etc.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-618">**WINSHostLookupFile**</span><span class="sxs-lookup"><span data-stu-id="249c7-618">**WINSHostLookupFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-619">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="249c7-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-620">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-620">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-621">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) \| \\ \\ drivers \\ \\ etc \\ \\ LMHOSTS")</span><span class="sxs-lookup"><span data-stu-id="249c7-621">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|[**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)\|\\\\drivers\\\\etc\\\\lmhosts")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-622">Percorso di un file di ricerca WINS nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="249c7-622">Path to a WINS lookup file on the local system.</span></span> <span data-ttu-id="249c7-623">Questo file conterrà una mappa degli indirizzi IP ai nomi host.</span><span class="sxs-lookup"><span data-stu-id="249c7-623">This file will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="249c7-624">Se il file specificato in questa proprietà viene trovato, verrà copiato nella cartella% SystemRoot% \\ system32 \\ drivers \\ del sistema locale.</span><span class="sxs-lookup"><span data-stu-id="249c7-624">If the file specified in this property is found, it will be copied to the %SystemRoot%\\system32\\drivers\\etc folder of the local system.</span></span> <span data-ttu-id="249c7-625">Valido solo se la proprietà **WINSEnableLMHostsLookup** è **true**.</span><span class="sxs-lookup"><span data-stu-id="249c7-625">Valid only if the **WINSEnableLMHostsLookup** property is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-626">**WINSPrimaryServer**</span><span class="sxs-lookup"><span data-stu-id="249c7-626">**WINSPrimaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-627">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="249c7-627">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-628">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-629">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| device input and Output functions \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="249c7-629">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-630">Indirizzo IP del server WINS primario.</span><span class="sxs-lookup"><span data-stu-id="249c7-630">IP address for the primary WINS server.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-631">**WINSScopeID**</span><span class="sxs-lookup"><span data-stu-id="249c7-631">**WINSScopeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-632">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="249c7-632">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-633">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-633">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-634">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| elemento ScopeId")</span><span class="sxs-lookup"><span data-stu-id="249c7-634">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ScopeID")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-635">Valore aggiunto alla fine del nome NetBIOS che isola un gruppo di sistemi informatici che comunicano tra loro.</span><span class="sxs-lookup"><span data-stu-id="249c7-635">Value appended to the end of the NetBIOS name that isolates a group of computer systems communicating with only each other.</span></span> <span data-ttu-id="249c7-636">Viene utilizzato per tutte le transazioni NetBIOS su comunicazioni TCP/IP dal sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="249c7-636">It is used for all NetBIOS transactions over TCP/IP communications from that computer system.</span></span> <span data-ttu-id="249c7-637">I computer configurati con identificatori di ambito identici sono in grado di comunicare con questo computer.</span><span class="sxs-lookup"><span data-stu-id="249c7-637">Computers configured with identical scope identifiers are able to communicate with this computer.</span></span> <span data-ttu-id="249c7-638">I client TCP/IP con identificatori di ambito diversi ignorano i pacchetti provenienti da computer con questo identificatore di ambito.</span><span class="sxs-lookup"><span data-stu-id="249c7-638">TCP/IP clients with different scope identifiers disregard packets from computers with this scope identifier.</span></span> <span data-ttu-id="249c7-639">Valido solo quando il metodo [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) viene eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="249c7-639">Valid only when the [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) method executes successfully.</span></span>

</dd> <dt>

<span data-ttu-id="249c7-640">**WINSSecondaryServer**</span><span class="sxs-lookup"><span data-stu-id="249c7-640">**WINSSecondaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249c7-641">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="249c7-641">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="249c7-642">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="249c7-642">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="249c7-643">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| device input and Output functions \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="249c7-643">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="249c7-644">Indirizzo IP del server WINS secondario.</span><span class="sxs-lookup"><span data-stu-id="249c7-644">IP address for the secondary WINS server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="249c7-645">Commenti</span><span class="sxs-lookup"><span data-stu-id="249c7-645">Remarks</span></span>

<span data-ttu-id="249c7-646">La classe **Win32 \_ NetworkAdapterConfiguration** deriva dall' [**\_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="249c7-646">The **Win32\_NetworkAdapterConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="examples"></a><span data-ttu-id="249c7-647">Esempio</span><span class="sxs-lookup"><span data-stu-id="249c7-647">Examples</span></span>

<span data-ttu-id="249c7-648">Nell'esempio di codice VBScript [Information Retriever WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) della raccolta TechNet viene utilizzata la classe **Win32 \_ NetworkAdapterConfiguration** per recuperare le informazioni di configurazione di rete da un numero di computer remoti.</span><span class="sxs-lookup"><span data-stu-id="249c7-648">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_NetworkAdapterConfiguration** class to retrieve network configuration information from a number of remote computers.</span></span>

<span data-ttu-id="249c7-649">L'esempio relativo a [Get-ComputerInfo-query computer da computer locale/remoto-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell nella raccolta TechNet usa una serie di chiamate a hardware e software, tra cui **Win32 \_ NetworkAdapterConfiguration**, per visualizzare informazioni su un sistema locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="249c7-649">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_NetworkAdapterConfiguration**, to display information about a local or remote system.</span></span>

<span data-ttu-id="249c7-650">Il codice di PowerShell seguente consente di recuperare le impostazioni di configurazione per l'adapter Microsoft ISTAP.</span><span class="sxs-lookup"><span data-stu-id="249c7-650">The following PowerShell code retrieves the configuration settings for the Microsoft ISTAP Adapter.</span></span>


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



<span data-ttu-id="249c7-651">Nell'esempio C seguente \# vengono recuperati la descrizione e il numero di indice di tutte le istanze di configurazione della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-651">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="249c7-652">Si noti che \# in questo esempio C viene utilizzato lo spazio dei nomi [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , che in genere è più efficiente delle classi WMI dello spazio dei nomi [System. Management](/dotnet/api/system.management) .</span><span class="sxs-lookup"><span data-stu-id="249c7-652">Note that this C\# sample uses the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace, which generally scales more efficiently than the [System.Management](/dotnet/api/system.management) namespace WMI classes.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
{
   CimSession session = CimSession.Create("localHost");
   IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapterConfiguration");

   foreach (CimInstance cimObj in queryInstance)
   {
      Console.WriteLine(cimObj.CimInstanceProperties["Index"].ToString());
      Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
      Console.WriteLine();
   }

Console.ReadLine();
}
```



<span data-ttu-id="249c7-653">Nell'esempio C seguente \# vengono recuperati la descrizione e il numero di indice di tutte le istanze di configurazione della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="249c7-653">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="249c7-654">Si noti che \# in questo esempio C viene utilizzato lo spazio dei nomi [System. Management](/dotnet/api/system.management) originale, che è stato sostituito da [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="249c7-654">Note that this C\# sample uses the original [System.Management](/dotnet/api/system.management) namespace, which has been superceded by [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).</span></span>


```CSharp
using System.Management;
...
static void oldSchoolQueryInstanceFunc()
{

   ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapterConfiguration");
   ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);

   ManagementObjectCollection queryCollection = searcher.Get();
   foreach (ManagementObject m in queryCollection)
   {
      Console.WriteLine("Index : {0}", m["Index"]);
      Console.WriteLine("Description : {0}", m["Description"]);
      Console.WriteLine();
   }
   Console.ReadLine();
}
```



<span data-ttu-id="249c7-655">Nell'esempio seguente vengono recuperate le informazioni dalla classe **Win32 \_ NetworkAdapterConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="249c7-655">The following example retrieves information from the **Win32\_NetworkAdapterConfiguration** class.</span></span>


```VB
on error resume next


PrintAll_NICAdapter_information()

'PrintOnlyEnabled_NICAdapter_information()


Function PrintAll_NICAdapter_information()


    strComputer = "."

    Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")


    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration",,48)


    i = 0

    For Each objItem in colItems

        i = i + 1

        Wscript.Echo "-----------------------------------"

        Wscript.Echo "Win32_NetworkAdapterConfiguration instance: " & i

        Wscript.Echo "-----------------------------------"

        

        strDefaultIPGateway = GetMultiString_FromArray(objitem.DefaultIPGateway, ", ")

        Wscript.Echo "MACAddress                  : " & vbtab & objItem.MACAddress
        Wscript.Echo "Description                 : " & vbtab & objItem.Description
        Wscript.Echo "DHCPEnabled                 : " & vbtab & objItem.DHCPEnabled

        strIPAddress=GetMultiString_FromArray(objitem.IPAddress, ", ")

        Wscript.Echo "IPAddress                   : " & vbtab & strIPAddress

        strIPSubnet = GetMultiString_FromArray(objitem.IPSubnet, ", ")

        Wscript.Echo "IPSubnet                    : " & vbtab & strIPSubnet
        Wscript.Echo "IPConnectionMetric          : " & vbtab & objItem.IPConnectionMetric
        Wscript.Echo "DHCPLeaseExpires            : " & vbtab & objItem.DHCPLeaseExpires
        Wscript.Echo "DHCPLeaseObtained           : " & vbtab & objItem.DHCPLeaseObtained
        Wscript.Echo "DHCPServer                  : " & vbtab & objItem.DHCPServer
        Wscript.Echo "DNSDomain                   : " & vbtab & objItem.DNSDomain
        Wscript.Echo "IPEnabled                   : " & vbtab & objItem.IPEnabled
        Wscript.Echo "DefaultIPGateway            : " & vbtab & strDefaultIPGateway
        Wscript.Echo "GatewayCostMetric           : " & vbtab & strGatewayCostMetric
        Wscript.Echo "IPFilterSecurityEnabled     : " & vbtab & objItem.IPFilterSecurityEnabled
        Wscript.Echo "IPPortSecurityEnabled       : " & vbtab & objItem.IPPortSecurityEnabled

        strDNSDomainSuffixSearchOrder = GetMultiString_FromArray(objitem.DNSDomainSuffixSearchOrder, ", ")

        Wscript.Echo "DNSDomainSuffixSearchOrder  : " & vbtab & strDNSDomainSuffixSearchOrder
        Wscript.Echo "DNSEnabledForWINSResolution : " & vbtab & objItem.DNSEnabledForWINSResolution
        Wscript.Echo "DNSHostName                 : " & vbtab & objItem.DNSHostName

        

        strDNSServerSearchOrder = GetMultiString_FromArray(objitem.DNSServerSearchOrder, ", ")

        Wscript.Echo "DNSServerSearchOrder        : " & vbtab & strDNSServerSearchOrder
        Wscript.Echo "DomainDNSRegistrationEnabled: " & vbtab & objItem.DomainDNSRegistrationEnabled
        Wscript.Echo "ForwardBufferMemory         : " & vbtab & objItem.ForwardBufferMemory
        Wscript.Echo "FullDNSRegistrationEnabled  : " & vbtab & objItem.FullDNSRegistrationEnabled

        strGatewayCostMetric = GetMultiString_FromArray(objitem.GatewayCostMetric, ", ")

        Wscript.Echo "IGMPLevel                   : " & vbtab & objItem.IGMPLevel
        Wscript.Echo "Index                       : " & vbtab & objItem.Index

        strIPSecPermitIPProtocols = GetMultiString_FromArray(objitem.IPSecPermitIPProtocols, ", ")

        Wscript.Echo "IPSecPermitIPProtocols      : " & vbtab & strIPSecPermitIPProtocols


        strIPSecPermitTCPPorts =GetMultiString_FromArray(objitem.IPSecPermitTCPPorts, ", ")

        Wscript.Echo "IPSecPermitTCPPorts         : " & vbtab & strIPSecPermitTCPPorts


        strIPSecPermitUDPPorts = GetMultiString_FromArray(objitem.IPSecPermitUDPPorts, ", ")

        Wscript.Echo "IPSecPermitUDPPorts         : " & vbtab & strIPSecPermitUDPPorts


        Wscript.Echo "IPUseZeroBroadcast          : " & vbtab & objItem.IPUseZeroBroadcast
        Wscript.Echo "IPXAddress                  : " & vbtab & objItem.IPXAddress
        Wscript.Echo "IPXEnabled                  : " & vbtab & objItem.IPXEnabled

        strIPXFrameType=GetMultiString_FromArray(objitem.IPXFrameType, ", ")

        Wscript.Echo "IPXFrameType                : " & vbtab & strIPXFrameType


        strIPXNetworkNumber=GetMultiString_FromArray(objitem.IPXNetworkNumber, ", ")

        Wscript.Echo "IPXNetworkNumber            : " & vbtab & strIPXNetworkNumber
        Wscript.Echo "IPXVirtualNetNumber         : " & vbtab & objItem.IPXVirtualNetNumber
        Wscript.Echo "KeepAliveInterval           : " & vbtab & objItem.KeepAliveInterval

        Wscript.Echo "KeepAliveTime               : " & vbtab & objItem.KeepAliveTime
        Wscript.Echo "MTU                         : " & vbtab & objItem.MTU
        Wscript.Echo "NumForwardPackets           : " & vbtab & objItem.NumForwardPackets
        Wscript.Echo "PMTUBHDetectEnabled         : " & vbtab & objItem.PMTUBHDetectEnabled
        Wscript.Echo "PMTUDiscoveryEnabled        : " & vbtab & objItem.PMTUDiscoveryEnabled
        Wscript.Echo "ServiceName                 : " & vbtab & objItem.ServiceName
        Wscript.Echo "SettingID                   : " & vbtab & objItem.SettingID
        Wscript.Echo "TcpipNetbiosOptions         : " & vbtab & objItem.TcpipNetbiosOptions
        Wscript.Echo "TcpMaxConnectRetransmissions: " & vbtab & objItem.TcpMaxConnectRetransmissions
        Wscript.Echo "TcpMaxDataRetransmissions   : " & vbtab & objItem.TcpMaxDataRetransmissions
        Wscript.Echo "TcpNumConnections           : " & vbtab & objItem.TcpNumConnections
        Wscript.Echo "TcpUseRFC1122UrgentPointer  : " & vbtab & objItem.TcpUseRFC1122UrgentPointer
        Wscript.Echo "TcpWindowSize               : " & vbtab & objItem.TcpWindowSize
        Wscript.Echo "WINSEnableLMHostsLookup     : " & vbtab & objItem.WINSEnableLMHostsLookup
        Wscript.Echo "WINSHostLookupFile          : " & vbtab & objItem.WINSHostLookupFile
        Wscript.Echo "WINSPrimaryServer           : " & vbtab & objItem.WINSPrimaryServer
        Wscript.Echo "WINSScopeID                 : " & vbtab & objItem.WINSScopeID
        Wscript.Echo "WINSSecondaryServer         : " & vbtab & objItem.WINSSecondaryServer
        Wscript.Echo "ArpAlwaysSourceRoute        : " & vbtab & objItem.ArpAlwaysSourceRoute
        Wscript.Echo "ArpUseEtherSNAP             : " & vbtab & objItem.ArpUseEtherSNAP
        Wscript.Echo "DatabasePath                : " & vbtab & objItem.DatabasePath
        Wscript.Echo "DeadGWDetectEnabled         : " & vbtab & objItem.DeadGWDetectEnabled

        Wscript.Echo "DefaultTOS                  : " & vbtab & objItem.DefaultTOS
        Wscript.Echo "DefaultTTL                  : " & vbtab & objItem.DefaultTTL

        

    Next

End Function ' Function PrintAll_NICAdapter_information()


' Script to get comprehensive nic info

sub appendCollection(msg, colctn, nm)

    i=0
    for each t in colctn
        msg = msg & "nic." & nm & "["&i&"]: " & t & vbCRLF
        i = i + 1
    next
end sub


Function PrintOnlyEnabled_NICAdapter_information()

    strComputer = "."

    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colNicConfigs = objWMIService.ExecQuery ("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled = True")


    for each nic in colNicConfigs

        msg = "nic.ArpAlwaysSourceRoute: " & nic.ArpAlwaysSourceRoute & vbCRLF _
        & "nic.ArpUseEtherSNAP: " & nic.ArpUseEtherSNAP & vbCRLF _
        & "nic.Caption: " & nic.Caption & vbCRLF _
        & "nic.DatabasePath: " & nic.DatabasePath & vbCRLF _
        & "nic.DeadGWDetectEnabled: " & nic.DeadGWDetectEnabled & vbCRLF _
        & "nic.DefaultTOS: " & nic.DefaultTOS & vbCRLF _
        & "nic.DefaultTTL: " & nic.DefaultTTL & vbCRLF _
        & "nic.Description: " & nic.Description & vbCRLF _
        & "nic.DHCPEnabled: " & nic.DHCPEnabled & vbCRLF _
        & "nic.DHCPLeaseExpires: " & nic.DHCPLeaseExpires & vbCRLF _
        & "nic.DHCPLeaseObtained: " & nic.DHCPLeaseObtained & vbCRLF _
        & "nic.DHCPServer: " & nic.DHCPServer & vbCRLF _
        & "nic.DNSDomain: " & nic.DNSDomain & vbCRLF _
        & "nic.DNSEnabledForWINSResolution: " & nic.DNSEnabledForWINSResolution & vbCRLF _
        & "nic.DNSHostName: " & nic.DNSHostName & vbCRLF _
        & "nic.DomainDNSRegistrationEnabled: " & nic.DomainDNSRegistrationEnabled & vbCRLF _
        & "nic.DNSDomainSuffixSearchOrder: " & nic.DNSDomainSuffixSearchOrder & vbCRLF _
        & "nic.ForwardBufferMemory: " & nic.ForwardBufferMemory & vbCRLF _
        & "nic.FullDNSRegistrationEnabled: " & nic.FullDNSRegistrationEnabled & vbCRLF _
        & "nic.IGMPLevel: " & nic.IGMPLevel & vbCRLF _
        & "nic.Index: " & nic.Index & vbCRLF _
        & "nic.IPConnectionMetric: " & nic.IPConnectionMetric & vbCRLF _
        & "nic.IPEnabled: " & nic.IPEnabled & vbCRLF _
        & "nic.IPFilterSecurityEnabled: " & nic.IPFilterSecurityEnabled & vbCRLF _
        & "nic.IPPortSecurityEnabled: " & nic.IPPortSecurityEnabled & vbCRLF _
        & "nic.IPUseZeroBroadcast: " & nic.IPUseZeroBroadcast & vbCRLF _
        & "nic.IPXAddress: " & nic.IPXAddress & vbCRLF _
        & "nic.IPXEnabled: " & nic.IPXEnabled & vbCRLF _
        & "nic.IPXFrameType: " & nic.IPXFrameType & vbCRLF _
        & "nic.IPXMediaType: " & nic.IPXMediaType & vbCRLF _
        & "nic.IPXNetworkNumber: " & nic.IPXNetworkNumber & vbCRLF _
        & "nic.IPXVirtualNetNumber: " & nic.IPXVirtualNetNumber & vbCRLF _
        & "nic.KeepAliveInterval: " & nic.KeepAliveInterval & vbCRLF _
        & "nic.KeepAliveTime: " & nic.KeepAliveTime & vbCRLF _
        & "nic.MACAddress: " & nic.MACAddress & vbCRLF _
        & "nic.MTU: " & nic.MTU & vbCRLF _
        & "nic.NumForwardPackets: " & nic.NumForwardPackets & vbCRLF _
        & "nic.PMTUBHDetectEnabled: " & nic.PMTUBHDetectEnabled & vbCRLF _
        & "nic.PMTUDiscoveryEnabled: " & nic.PMTUDiscoveryEnabled & vbCRLF _
        & "nic.ServiceName: " & nic.ServiceName & vbCRLF _
        & "nic.SettingID: " & nic.SettingID & vbCRLF _
        & "nic.TcpipNetbiosOptions: " & nic.TcpipNetbiosOptions & vbCRLF _
        & "nic.TcpMaxConnectRetransmissions: " & nic.TcpMaxConnectRetransmissions & vbCRLF _
        & "nic.TcpMaxDataRetransmissions: " & nic.TcpMaxDataRetransmissions & vbCRLF _
        & "nic.TcpNumConnections: " & nic.TcpNumConnections & vbCRLF _
        & "nic.TcpUseRFC1122UrgentPointer: " & nic.TcpUseRFC1122UrgentPointer & vbCRLF _
        & "nic.TcpWindowSize: " & nic.TcpWindowSize & vbCRLF _
        & "nic.WINSEnableLMHostsLookup: " & nic.WINSEnableLMHostsLookup & vbCRLF _
        & "nic.WINSHostLookupFile: " & nic.WINSHostLookupFile & vbCRLF _
        & "nic.WINSPrimaryServer: " & nic.WINSPrimaryServer & vbCRLF _
        & "nic.WINSScopeID: " & nic.WINSScopeID & vbCRLF _
        & "nic.WINSSecondaryServer: " & nic.WINSSecondaryServer & vbCRLF _
        '& "nic.InterfaceIndex: " & "|"&nic.InterfaceIndex & vbCRLF _


        appendCollection msg, nic.DefaultIPGateway, "DefaultIPGateway"
        appendCollection msg, nic.DNSServerSearchOrder, "DNSServerSearchOrder"
        appendCollection msg, nic.GatewayCostMetric, "GatewayCostMetric"
        appendCollection msg, nic.IPAddress, "IPAddress"
        appendCollection msg, nic.IPSecPermitIPProtocols, "IPSecPermitIPProtocols"
        appendCollection msg, nic.IPSecPermitTCPPorts, "IPSecPermitTCPPorts"
        appendCollection msg, nic.IPSecPermitUDPPorts, "IPSecPermitUDPPorts"
        appendCollection msg, nic.IPSubnet, "IPSubnet"


        WScript.Echo msg

    next


    'Vista only code???

    'Set colAdapters = objWMIService.Execquery ("SELECT * FROM Win32_NetworkAdapter WHERE NetEnabled = True")

    'For Each nic in colAdapters

    ' msg = "nic.DeviceId: " & nic.DeviceId & vbCRLF _

    ' & "nic.Name: " & nic.Name & vbCRLF _

    '

    'Next

End Function 'Function PrintOnlyEnabled_NICAdapter_information()

Function GetMultiString_FromArray( ArrayString, Seprator)

    If IsNull ( ArrayString ) Then

        StrMultiArray = ArrayString

    else

        StrMultiArray = Join( ArrayString, Seprator )

   end if

   GetMultiString_FromArray = StrMultiArray

End Function
```



## <a name="requirements"></a><span data-ttu-id="249c7-656">Requisiti</span><span class="sxs-lookup"><span data-stu-id="249c7-656">Requirements</span></span>



| <span data-ttu-id="249c7-657">Requisito</span><span class="sxs-lookup"><span data-stu-id="249c7-657">Requirement</span></span> | <span data-ttu-id="249c7-658">Valore</span><span class="sxs-lookup"><span data-stu-id="249c7-658">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="249c7-659">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="249c7-659">Minimum supported client</span></span><br/> | <span data-ttu-id="249c7-660">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="249c7-660">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="249c7-661">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="249c7-661">Minimum supported server</span></span><br/> | <span data-ttu-id="249c7-662">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="249c7-662">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="249c7-663">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="249c7-663">Namespace</span></span><br/>                | <span data-ttu-id="249c7-664">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="249c7-664">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="249c7-665">MOF</span><span class="sxs-lookup"><span data-stu-id="249c7-665">MOF</span></span><br/>                      | <dl> <span data-ttu-id="249c7-666"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="249c7-666"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="249c7-667">DLL</span><span class="sxs-lookup"><span data-stu-id="249c7-667">DLL</span></span><br/>                      | <dl> <span data-ttu-id="249c7-668"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="249c7-668"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="249c7-669">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="249c7-669">See also</span></span>

<dl> <dt>

[<span data-ttu-id="249c7-670">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="249c7-670">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="249c7-671">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="249c7-671">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="249c7-672">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="249c7-672">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[<span data-ttu-id="249c7-673">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="249c7-673">WMI Tasks: Accounts and Domains</span></span>](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[<span data-ttu-id="249c7-674">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="249c7-674">IPv6 and IPv4 Support in WMI</span></span>](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
