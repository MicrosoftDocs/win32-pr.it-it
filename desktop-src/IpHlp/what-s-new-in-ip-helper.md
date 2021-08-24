---
description: Novità dell'helper IP
ms.assetid: fa9d72d0-2f9c-433d-b05a-8423664b2e3e
title: Novità dell'helper IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3141797e96442f34a94c2d2afc37585ce6dbc944e7fb35cf9b4602afa042c95a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897621"
---
# <a name="whats-new-in-ip-helper"></a>Novità dell'helper IP

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 e Windows Server 2012

Le funzionalità seguenti sono state aggiunte alle API helper IP in Windows 8 e Windows Server 2012.

Funzione che recupera stime cronologiche della larghezza di banda per una connessione di rete. Per altre informazioni, vedere:

-   [**GetIpNetworkConnectionBandwidthEstimates**](/windows/desktop/api/Netioapi/nf-netioapi-getipnetworkconnectionbandwidthestimates)

Struttura che contiene informazioni sulle stime della larghezza di banda disponibili e sulla varianza associata, come determinato dallo stack TCP/IP. Per altre informazioni, vedere:

-   [**INFORMAZIONI SULLA LARGHEZZA \_ DI BANDA \_ NL**](/windows/desktop/api/Nldef/ns-nldef-nl_bandwidth_information)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

Le funzionalità seguenti sono state aggiunte alle API helper IP in Windows 7 e Windows Server 2008 R2.

Funzioni che convertono un indirizzo Ethernet tra un formato binario e un formato stringa per l'indirizzo MAC Ethernet. Per altre informazioni, vedere:

-   [**RtlEthernetAddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetaddresstostringa)
-   [**RtlEthernetStringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetstringtoaddressa)

## <a name="windows-server-2008-and-windows-vista-sp1"></a>Windows Server 2008 e Windows Vista SP1

Le funzioni seguenti sono state aggiunte alle API helper IP in Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).

Funzione che funziona con IPv4 e Internet Control Message Protocol (ICMP). Per altre informazioni, vedere:

-   [**IcmpSendEcho2Ex**](/windows/desktop/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)

## <a name="windows-vista"></a>Windows Vista

I gruppi di funzioni seguenti sono stati aggiunti alle API helper IP Windows Vista e versioni successive.

Funzioni che funzionano con IPv6 e IPv4 per la conversione dell'interfaccia. Per altre informazioni, vedere:

-   [**ConvertInterfaceAliasToLuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [**ConvertInterfaceGuidToLuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [**ConvertInterfaceIndexToLuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [**ConvertInterfaceLuidToGuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [**ConvertInterfaceLuidToIndex**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [**ConvertInterfaceLuidToNameA**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [**ConvertInterfaceLuidToNameW**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [**ConvertInterfaceNameToLuidA**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [**ConvertInterfaceNameToLuidW**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [**if \_ indextoname**](/windows/desktop/api/Netioapi/nf-netioapi-if_indextoname)
-   [**if \_ nametoindex**](/windows/desktop/api/Netioapi/nf-netioapi-if_nametoindex)

Funzioni che funzionano con IPv6 e IPv4 per la gestione dell'interfaccia. Per altre informazioni, vedere:

-   [**GetIfEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getifentry2)
-   [**GetIfStackTable**](/windows/desktop/api/Netioapi/nf-netioapi-getifstacktable)
-   [**GetIfTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2)
-   [**GetIfTable2Ex**](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2ex)
-   [**GetInvertedIfStackTable**](/windows/desktop/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [**GetIpInterfaceEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [**GetIpInterfaceTable**](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [**InitializeIpInterfaceEntry**](/windows/desktop/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [**SetIpInterfaceEntry**](/windows/desktop/api/Netioapi/nf-netioapi-setipinterfaceentry)

Funzioni che funzionano con IPv6 e IPv4 per la gestione degli indirizzi IP. Per altre informazioni, vedere:

-   [**CreateAnycastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [**CreateUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [**DeleteAnycastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [**DeleteUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [**GetAnycastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [**GetAnycastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [**GetMulticastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [**GetMulticastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [**GetUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [**GetUnicastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [**InitializeUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [**SetUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-setunicastipaddressentry)

Funzione che funziona con IPv6 e IPv4 per la gestione della memoria delle tabelle IP. Per altre informazioni, vedere:

-   [**FreeMibTable**](/windows/desktop/api/Netioapi/nf-netioapi-freemibtable)

Funzioni che funzionano sia con IPv6 che con IPv4 per la gestione degli indirizzi adiacenti IP. Per altre informazioni, vedere:

-   [**CreateIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-createipnetentry2)
-   [**DeleteIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [**FlushIpNetTable2**](/windows/desktop/api/Netioapi/nf-netioapi-flushipnettable2)
-   [**GetIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getipnetentry2)
-   [**GetIpNetTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getipnettable2)
-   [**ResolveIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [**ResolveNeighbor**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [**SetIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-setipnetentry2)

Funzioni che funzionano con IPv6 e IPv4 per la gestione del percorso IP. Per altre informazioni, vedere:

-   [**FlushIpPathTable**](/windows/desktop/api/Netioapi/nf-netioapi-flushippathtable)
-   [**GetIpPathEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getippathentry)
-   [**GetIpPathTable**](/windows/desktop/api/Netioapi/nf-netioapi-getippathtable)

Funzioni che funzionano con IPv6 e IPv4 per la gestione delle route IP. Per altre informazioni, vedere:

-   [**CreateIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [**DeleteIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [**GetBestRoute2**](/windows/desktop/api/Netioapi/nf-netioapi-getbestroute2)
-   [**GetIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [**GetIpForwardTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [**InitializeIpForwardEntry**](/windows/desktop/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [**SetIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [**SetIpStatisticsEx**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)

Funzioni che funzionano sia con IPv6 che con IPv4 per la notifica. Per altre informazioni, vedere:

-   [**CancelMibChangeNotify2**](/windows/desktop/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [**NotifyIpInterfaceChange**](/windows/desktop/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [**NotifyRouteChange2**](/windows/desktop/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [**NotifyUnicastIpAddressChange**](/windows/desktop/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

Funzioni di utilità che funzionano con gli indirizzi IP. Per altre informazioni, vedere:

-   [**ConvertIpv4MaskToLength**](/windows/desktop/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [**ConvertLengthToIpv4Mask**](/windows/desktop/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [**CreateSortedAddressPairs**](/windows/desktop/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [**ParseNetworkString**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

Funzioni che funzionano con Transmission Control Protocol (TCP) e UDP (User Datagram Protocol) per recuperare la tabella di connessione TCP IPv6 o IPv4 o la tabella del listener UDP. Per altre informazioni, vedere:

-   [**GetTcp6Table**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [**GetTcp6Table2**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [**GetTcpTable2**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [**GetUdp6Table**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudp6table)

Funzioni che funzionano con Transmission Control Protocol (TCP) per recuperare statistiche TCP estese in una connessione. Per altre informazioni, vedere:

-   [**GetPerTcp6ConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [**GetPerTcpConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [**SetPerTcp6ConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [**SetPerTcpConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)

Nuove funzioni che funzionano per la Teredo client IPv6. Per altre informazioni, vedere:

-   [**GetTeredoPort**](/windows/desktop/api/Netioapi/nf-netioapi-getteredoport)
-   [**NotifyTeredoPortChange**](/windows/desktop/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

Funzioni di utilità che forniscono conversioni tra indirizzi IP e rappresentazioni di stringa di indirizzi IP. Per altre informazioni, vedere:

-   [**RtlIpv4AddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [**RtlIpv4AddressToStringEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [**RtlIpv4StringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [**RtlIpv4StringToAddressEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [**RtlIpv6AddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [**RtlIpv6AddressToStringEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [**RtlIpv6StringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [**RtlIpv6StringToAddressEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

Funzioni che forniscono prenotazioni persistenti per un blocco consecutivo di porte TCP o UDP nel computer locale. Per altre informazioni, vedere:

-   [**CreatePersistentTcpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [**CreatePersistentUdpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [**DeletePersistentTcpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [**DeletePersistentUdpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [**LookupPersistentTcpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [**LookupPersistentUdpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="windows-server-2003"></a>Windows Server 2003

Le funzioni seguenti sono state aggiunte alle API helper IP in Windows Server 2003 e versioni successive:

-   [**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))
-   [**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))

## <a name="windows-xp-sp2"></a>Windows XP SP2

Le funzioni seguenti sono state aggiunte alle API helper IP in Windows XP con Service Pack 2 (SP2) e versioni successive:

-   [**GetOwnerModuleFromTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [**GetOwnerModuleFromTcp6Entry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [**GetOwnerModuleFromUdpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [**GetOwnerModuleFromUdp6Entry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)

 

 
