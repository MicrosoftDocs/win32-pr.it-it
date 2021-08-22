---
description: Windows Socket abilita l'individuazione del listener multicast (MLD) in IPv6 e il Internet Group Management Protocol (IGMP) in IPv4 per le applicazioni multicast tramite l'uso di opzioni socket e IOCL.
ms.assetid: a5de4273-e86e-4f13-b068-256cb38706d4
title: MLD e IGMP con Windows Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2c550cf2c1463f5b646efc286c05010274d3cb44e13b9559302452bccb81c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051649"
---
# <a name="mld-and-igmp-using-windows-sockets"></a>MLD e IGMP con Windows Socket

Windows Socket abilita l'individuazione del listener multicast (MLD) in IPv6 e il Internet Group Management Protocol (IGMP) in IPv4 per le applicazioni multicast tramite l'uso di opzioni socket e IOCL. Questa pagina descrive le opzioni socket che abilitano la programmazione multicast e descrive come vengono usate. Per le definizioni di ogni opzione socket, vedere la [pagina Opzioni](socket-options.md) socket.

Per informazioni sull'uso degli IOCL per la programmazione multicast, vedere [Programmazione multicast](final-state-based-multicast-programming.md) basata sullo stato finale più avanti in questa sezione.

In Windows Vista e versioni successive è disponibile un set di opzioni socket per la programmazione multicast che supporta gli indirizzi IPv6 e IPv4. Queste opzioni socket sono indipendenti da IP e possono essere usate sia in IPv6 che in IPv4. In IPv6, queste opzioni socket usano MLDv2. In IPv4, queste opzioni socket usano IGMPv3. Queste opzioni indipendenti da IP sono le opzioni socket preferite per la programmazione multicast Windows Vista e versioni successive. Windows Sockets usa le opzioni socket seguenti: 

| Opzione socket               | Tipo di argomento                                            |
|-----------------------------|----------------------------------------------------------|
| ORIGINE DEL BLOCCO \_ \_ MCAST        | [**GRUPPO \_ Struttura SOURCE \_ REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| MCAST \_ JOIN \_ GROUP          | [**GRUPPO \_ Struttura REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req)                |
| MCAST \_ JOIN \_ SOURCE \_ GROUP  | [**GRUPPO \_ Struttura SOURCE \_ REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| MCAST \_ LEAVE \_ GROUP         | [**GRUPPO \_ Struttura REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req)                |
| MCAST \_ LEAVE \_ SOURCE \_ GROUP | [**GRUPPO \_ Struttura SOURCE \_ REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| MCAST \_ UNBLOCK \_ SOURCE      | [**GRUPPO \_ Struttura SOURCE \_ REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |



 

È disponibile un set di opzioni socket per la programmazione multicast che supporta solo indirizzi IPv6. Queste opzioni socket usano MLDv1 o MLDv2. La versione di MLD usata dipende dalla versione di Windows. MLDv2 è supportato in Windows Vista e versioni successive. Windows Sockets usa le opzioni socket seguenti: 

| Opzione socket          | Tipo di argomento                             |
|------------------------|-------------------------------------------|
| AGGIUNTA APPARTENENZA IPV6 \_ \_  | [**Struttura \_ mreq ipv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |
| APPARTENENZA DROP \_ IPV6 \_ | [**Struttura \_ mreq ipv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |



 

È disponibile un set di opzioni socket per la programmazione multicast che supporta solo indirizzi IPv4. Queste opzioni socket usano IGMPv3 o IGMPv2. La versione di IGMP usata dipende dalla versione di Windows. IGMPv3 è supportato in Windows Vista e versioni successive. Windows Sockets usa le opzioni socket seguenti:

| Opzione socket                | Tipo di argomento                                        |
|------------------------------|------------------------------------------------------|
| AGGIUNTA \_ \_ DELL'APPARTENENZA IP          | [**Struttura \_ ip mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| AGGIUNTA \_ \_ DELL'APPARTENENZA \_ ALL'ORIGINE IP  | [**Struttura \_ di \_ origine ip mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| ORIGINE \_ DEL BLOCCO \_ IP            | [**Struttura \_ di \_ origine ip mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| APPARTENENZA \_ ALL'ELIMINAZIONE \_ IP         | [**Struttura \_ ip mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| APPARTENENZA \_ \_ ALL'ORIGINE DI RILASCIO \_ IP | [**Struttura \_ di \_ origine ip mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| ORIGINE \_ DI SBLOCCO \_ IP          | [**Struttura \_ di \_ origine ip mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |



 

Quando IGMPv3 è disponibile, le opzioni IP \_ ADD \_ SOURCE \_ MEMBERSHIP, IP BLOCK SOURCE, IP DROP SOURCE MEMBERSHIP e \_ IP UNBLOCK \_ \_ \_ \_ \_ \_ SOURCE vengono gestite in modo più efficiente perché il router può gestire il filtro. Quando è disponibile solo IGMPv2, l'host deve gestire il filtro.

Esistono due categorie in cui è probabile che la maggior parte delle applicazioni cada: any-source e controlled-source.

-   **Le applicazioni any-source** accettano tutte le origini per impostazione predefinita, consentendo di disattivare le singole origini in base alle esigenze. Un esempio di applicazione any-source è una videoconferenza che consente a tutti i destinatari di partecipare.
-   **Le applicazioni di origine** controllata limitano le origini a un determinato elenco, ad esempio una stazione radio Internet o la trasmissione di un evento di grande valore. Il processo di utilizzo delle opzioni socket è leggermente diverso per ognuna.

In Windows Vista e versioni successive, i passaggi seguenti si applicano alle applicazioni di qualsiasi origine:

- Usare **MCAST \_ JOIN GROUP \_ per** unirsi a un gruppo.  
- Usare **MCAST \_ BLOCK \_ SOURCE** per disattivare una determinata origine, se necessario.  
- Usare **MCAST \_ UNBLOCK \_ SOURCE** per consentire nuovamente un'origine bloccata, se necessario.  
- Usare **MCAST \_ LEAVE \_ GROUP** per uscire dal gruppo.  

In Windows Vista e versioni successive, per le applicazioni con origine controllata si applicano i passaggi seguenti:

- Usare **MCAST \_ JOIN SOURCE \_ GROUP \_ per** unire ogni coppia gruppo/origine.  
- Usare **MCAST \_ LEAVE SOURCE \_ \_ GROUP** per lasciare ogni gruppo/origine oppure **MCAST LEAVE \_ \_ GROUP** per lasciare tutte le origini, se lo stesso indirizzo di gruppo viene usato da tutte le origini.  

I passaggi seguenti si applicano alle applicazioni di qualsiasi origine:

- Usare **IP ADD MEMBERSHIP \_ \_ per** aggiungere un gruppo (**IPV6 \_ ADD \_ MEMBERSHIP** per IPv6).  
- Usare **IP \_ BLOCK \_ SOURCE** per disattivare una determinata origine, se necessario.  
- Usare **IP \_ UNBLOCK \_ SOURCE** per consentire nuovamente un'origine bloccata, se necessario.  
- Usare **IP \_ DROP \_ MEMBERSHIP** per uscire dal gruppo (**IPV6 \_ DROP \_ MEMBERSHIP** per IPv6).  

I passaggi seguenti si applicano alle applicazioni di origine controllata:

- Usare **IP ADD SOURCE MEMBERSHIP \_ \_ \_ per** unire ogni coppia gruppo/origine.  
- Usare **IP DROP SOURCE \_ \_ \_ MEMBERSHIP** per uscire da ogni gruppo/origine oppure usare **IP DROP \_ \_ MEMBERSHIP** per lasciare tutte le origini, se lo stesso indirizzo di gruppo viene usato da tutte le origini.  

All'ordine in cui vengono impostate queste opzioni socket sono associate regole. Per informazioni e sulla risoluzione dei problemi relativi alle opzioni socket multicast, vedere Comportamento delle opzioni [socket multicast](multicast-socket-option-behavior.md).
