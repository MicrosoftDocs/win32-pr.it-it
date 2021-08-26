---
title: Identificatori di protocollo
description: Gli identificatori di protocollo seguenti sono elencati anche in Routprot.h per Windows SDK e iprtmib.h per Platform Software Development Kit (SDK).
ms.assetid: f67138b8-de5d-4907-a464-672d57864ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dafcbcd028b5c8d4f58172565b34c93cff8d8f9ff766c055e3d8a956cfbb0aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036471"
---
# <a name="protocol-identifiers"></a>Identificatori di protocollo

Gli identificatori di protocollo seguenti sono elencati anche in Routprot.h per Windows SDK e iprtmib.h per Platform Software Development Kit (SDK).

## <a name="ip-protocols"></a>Protocolli IP

I protocolli di routing seguenti sono associati al trasporto IP.



| Protocollo                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROTO \_ IP \_ OTHER, MIB \_ IPPROTO \_ OTHER                        | Altro protocollo non specificato in RFC 1354.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| PROTO \_ IP \_ LOCAL, MIB \_ IPPROTO \_ LOCAL                        | Interfaccia locale.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ NETMGMT, MIB \_ IPPROTO \_ NETMGMT                    | Route statica. Questo valore viene usato per identificare le informazioni di route per il routing IP impostato tramite la gestione di rete, ad esempio Dynamic Host Configuration Protocol (DCHP), Simple Network Management Protocol (SNMP) o tramite chiamate [**alle funzioni CreateIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry)o [**SetIpForwardEntry.**](/windows/desktop/api/iphlpapi/nf-iphlpapi-setipforwardentry)                                                                                              |
| PROTO \_ IP \_ ICMP, MIB \_ IPPROTO \_ ICMP                          | Risultato del reindirizzamento ICMP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| PROTO \_ IP \_ EGP, MIB \_ IPPROTO \_ EGP                            | EGP (Exterior Gateway Protocol), un protocollo di routing dinamico.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| PROTO \_ IP \_ GGP, MIB \_ IPPROTO \_ GGP                            | Gateway-to-Gateway Protocol (GGP), un protocollo di routing dinamico.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ HELLO, MIB \_ IPPROTO \_ HELLO                        | Protocollo Hellospeak, un protocollo di routing dinamico. Si tratta di una voce cronologica non più in uso ed era un protocollo di routing anticipato usato dai router ARPANET originali che esempevano software speciale denominato protocollo di routing Fuzzball, talvolta denominato Hellospeak, come descritto in RFC 891 e RFC 1305. Per altre informazioni, vedere [https://www.ietf.org/rfc/rfc891.txt](https://www.ietf.org/rfc/rfc891.txt) e [https://www.ietf.org/rfc/rfc1305.txt](https://tools.ietf.org/html/rfc1305). |
| RIP \_ IP \_ PROTO, RIP \_ IPPROTO MIB \_                            | L'Routing Information Protocol Berkeley (RIP) o RIP-II, un protocollo di routing dinamico.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ IS \_ IS, MIB \_ IPPROTO \_ IS \_ IS                      | Protocollo IS-IS (Intermediate System-to-Intermediate System), un protocollo di routing dinamico. Il protocollo IS-IS è stato sviluppato per l'uso nella suite di protocolli OSI (Open Systems Interconnection).                                                                                                                                                                                                                                                                                                                      |
| PROTO \_ IP \_ ES \_ IS, MIB \_ IPPROTO \_ ES \_ IS                      | Protocollo End System-to-Intermediate System (ES-IS), un protocollo di routing dinamico. Il protocollo ES-IS è stato sviluppato per l'uso nella suite di protocolli OSI (Open Systems Interconnection).                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ CISCO, MIB \_ IPPROTO \_ CISCO                        | Cisco Interior Gateway Routing Protocol (IGRP), un protocollo di routing dinamico.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| BBN \_ IP \_ PROTO, MIB \_ IPPROTO \_ BBN                            | Bolt, Beranek e Newman (BBN) Interior Gateway Protocol (IGP) che usava l'algoritmo SPF (Shortest Path First). Si tratta di un protocollo di routing dinamico iniziale.                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ OSPF, MIB \_ IPPROTO \_ OSPF                          | Protocollo OSPF (Open Shortest Path First), un protocollo di routing dinamico.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ BGP, MIB \_ IPPROTO \_ BGP                            | Il Border Gateway Protocol (BGP), un protocollo di routing dinamico.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| AVVIO \_ IP \_ PROTO, BOOTP \_ IPPROTO \_ MIB                        | Protocollo Bootstrap.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| PROTO \_ IPV6 \_ DHCPRELAY, MIB \_ IPV6PROTO \_ HDCPRELAY            | Protocollo di inoltro DHCPv6.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| PROTO \_ IP \_ NT \_ AUTOSTATIC, MIB \_ IPNT \_ AUTOSTATIC             | Una Windows voce specifica aggiunta originariamente da un protocollo di routing, ma che è ora statica.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ NT \_ STATIC, MIB \_ IPNT \_ STATIC                     | Una Windows voce specifica aggiunta come route statica dall'interfaccia utente di routing o da un comando di routing.                                                                                                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP NT STATICO NON \_ \_ \_ \_ DOD, MIB \_ IPNT STATICO NON \_ \_ \_ DOD | Una Windows voce specifica aggiunta come route statica dall'interfaccia utente di routing o da un comando di routing, con la differenza che queste route non causano il dial on demand (DOD).                                                                                                                                                                                                                                                                                                                                                        |



 

Le route con un identificatore di protocollo DI PROTO \_ IP \_ LOCAL includono:

-   Route di loopback
-   Route della subnet
-   Route di trasmissione di tutte le reti per le interfacce con subnet
-   Tutta la route di trasmissione "1"
-   Route multicast locale
-   Route all'estremità remota di un collegamento PPP

L'identificatore per gestione router IP è:

IPRTRMGR \_ PID

Questo identificatore può essere usato al posto di un identificatore del protocollo di routing per le chiamate MIB con gestione router IP. Questo identificatore viene usato per MIB-II, mib di inoltro e alcune informazioni specifiche dell'organizzazione. Questo identificatore è elencato anche in Iprtrmib.h.

## <a name="ipx-protocols"></a>Protocolli IPX

I protocolli di routing seguenti sono associati al trasporto IPX.



| Protocollo            | Descrizione                          |
|---------------------|--------------------------------------|
| RIP DEL PROTOCOLLO IPX \_ \_  | Routing Information Protocol per IPX |
| SAP DEL PROTOCOLLO IPX \_ \_  | Protocollo di annuncio del servizio       |
| PROTOCOLLO IPX \_ \_ NLSP | Protocollo NetWare Link Services       |



 

L'identificatore per gestione router IPX è:

BASE DEL PROTOCOLLO IPX \_ \_

Usare questo identificatore invece di un identificatore del protocollo di routing per le chiamate MIB con gestione router IPX.

 

 