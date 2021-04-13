---
title: Identificatori di protocollo
description: Gli identificatori di protocollo seguenti sono elencati anche in Routprot. h per il Windows SDK e iprtmib. h per Platform Software Development Kit (SDK).
ms.assetid: f67138b8-de5d-4907-a464-672d57864ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ac515eb4b5090c0b4f75fd923d8345538ff5e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338558"
---
# <a name="protocol-identifiers"></a>Identificatori di protocollo

Gli identificatori di protocollo seguenti sono elencati anche in Routprot. h per il Windows SDK e iprtmib. h per Platform Software Development Kit (SDK).

## <a name="ip-protocols"></a>Protocolli IP

I protocolli di routing seguenti sono associati al trasporto IP.



| Protocollo                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROTO \_ IP \_ other, MIB \_ IPPROTO \_ other                        | Un altro protocollo non è stato specificato nella RFC 1354.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| PROTO \_ IP \_ locale, MIB \_ IPPROTO \_ locale                        | Interfaccia locale.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ NETMGMT, MIB \_ IPPROTO \_ NETMGMT                    | Route statica. Questo valore viene usato per identificare le informazioni sulla route per il routing IP impostato tramite la gestione della rete, ad esempio il Dynamic Host Configuration Protocol (DCHP), il Simple Network Management Protocol (SNMP) o le chiamate alle funzioni [**CreateIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry)o [**SetIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-setipforwardentry) .                                                                                              |
| PROTO \_ IP \_ ICMP, MIB \_ IPPROTO \_ ICMP                          | Risultato del reindirizzamento ICMP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| PROTO \_ IP \_ EGP, MIB \_ IPPROTO \_ EGP                            | Il protocollo del gateway esterno (EGP), un protocollo di routing dinamico.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| PROTO \_ IP \_ GGP, MIB \_ IPPROTO \_ GGP                            | Protocollo Gateway-to-Gateway (GGP), un protocollo di routing dinamico.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ Hello, MIB \_ IPPROTO \_ Hello                        | Il protocollo Hellospeak, un protocollo di routing dinamico. Si tratta di una voce storica non più utilizzata ed è un protocollo di routing iniziale utilizzato dai router ARPANET originali che hanno eseguito software speciale denominato protocollo di routing Fuzzball, talvolta denominato Hellospeak, come descritto in RFC 891 e RFC 1305. Per altre informazioni, vedere [https://www.ietf.org/rfc/rfc891.txt](https://www.ietf.org/rfc/rfc891.txt) e [https://www.ietf.org/rfc/rfc1305.txt](https://tools.ietf.org/html/rfc1305). |
| PROTO \_ IP \_ RIP, MIB \_ IPPROTO \_ RIP                            | Berkeley Routing Information Protocol (RIP) o RIP-II, un protocollo di routing dinamico.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| il \_ protocollo IP proto \_ è \_ , \_ MIB IPPROTO \_ è \_                      | Protocollo di sistema intermedio intermedio (è), un protocollo di routing dinamico. Il protocollo IS-IS è stato sviluppato per l'uso nella suite di protocolli OSI (Open Systems Interconnection).                                                                                                                                                                                                                                                                                                                      |
| PROTO \_ IP \_ es \_ is, MIB \_ IPPROTO \_ es \_ is                      | Il protocollo end-to-Intermediate System (ES-IS), un protocollo di routing dinamico. Il protocollo ES-IS è stato sviluppato per l'uso nella suite di protocolli OSI (Open Systems Interconnection).                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ Cisco, MIB \_ IPPROTO \_ Cisco                        | Il protocollo IGRP (Cisco Interior Gateway Routing Protocol), un protocollo di routing dinamico.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PROTO \_ IP \_ BBN, MIB \_ IPPROTO \_ BBN                            | Bolt, Beranek e Newman (BBN) Interior Gateway Protocol (IGP) che ha utilizzato l'algoritmo SPF (Short Path First). Questo è un primo protocollo di routing dinamico.                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ OSPF, MIB \_ IPPROTO \_ OSPF                          | Protocollo OSPF (Short-Path First) aperto, un protocollo di routing dinamico.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ BGP, MIB \_ IPPROTO \_ BGP                            | Il Border Gateway Protocol (BGP), un protocollo di routing dinamico.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_protocollo BOOTP IP proto \_ , protocollo \_ BOOTP IPPROTO MIB \_                        | Protocollo bootstrap.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| PROTO \_ IPv6 \_ DHCPRELAY, MIB \_ IPV6PROTO \_ HDCPRELAY            | Protocollo di inoltro DHCPv6.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| PROTO \_ IP \_ NT \_ autostatic, MIB \_ IPNT \_ autostatic             | Voce specifica di Windows aggiunta in origine da un protocollo di routing, che ora è statico.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ NT \_ statico, MIB \_ IPNT \_ statico                     | Una voce specifica di Windows aggiunta come route statica dall'interfaccia utente di routing o da un comando di routing.                                                                                                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ NT \_ static \_ non \_ DOD, MIB \_ IPNT \_ statico \_ non \_ DOD | Una voce specifica di Windows aggiunta come route statica dall'interfaccia utente di routing o da un comando di routing, con la differenza che queste route non provocano la connessione su richiesta (DOD).                                                                                                                                                                                                                                                                                                                                                        |



 

Le route con un identificatore di protocollo di PROTO \_ IP \_ local includono:

-   Route di loopback
-   Route della subnet
-   Tutte le reti hanno trasmesso il routing per le interfacce sottonette
-   Tutte le route di broadcast "1"
-   Route multicast locale
-   Routing alla fine remota di un collegamento PPP

L'identificatore per gestione router IP è:

\_PID IPRTRMGR

Questo identificatore può essere utilizzato al posto di un identificatore del protocollo di routing per le chiamate MIB con gestione router IP. Questo identificatore viene usato per MIB-II, per l'invio di MIB e per alcune informazioni specifiche dell'azienda. Questo identificatore è elencato anche in Iprtrmib. h.

## <a name="ipx-protocols"></a>Protocolli IPX

I protocolli di routing seguenti sono associati al trasporto IPX.



| Protocollo            | Descrizione                          |
|---------------------|--------------------------------------|
| \_RIP protocollo \_ IPX  | Routing Information Protocol per IPX |
| \_protocollo IPX \_ SAP  | Protocollo degli annunci di servizio       |
| \_protocollo IPX \_ nlsp | Protocollo servizi di collegamento NetWare       |



 

L'identificatore per gestione router IPX è:

\_base protocollo \_ IPX

Utilizzare questo identificatore anziché un identificatore del protocollo di routing per le chiamate MIB con gestione router IPX.

 

 