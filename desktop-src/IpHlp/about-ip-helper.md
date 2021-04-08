---
description: Internet Protocol Helper (helper IP) facilita l'amministrazione della rete del computer locale consentendo alle applicazioni di recuperare informazioni sulla configurazione di rete del computer locale e di modificare la configurazione.
ms.assetid: 9eb8af78-612f-406c-ab92-4623b10a510e
title: Informazioni su helper IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50587b4abdcbad0cddd6d6ce3281c908fdebef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049512"
---
# <a name="about-ip-helper"></a>Informazioni su helper IP

Internet Protocol Helper (helper IP) facilita l'amministrazione della rete del computer locale consentendo alle applicazioni di recuperare informazioni sulla configurazione di rete del computer locale e di modificare la configurazione. IP Helper fornisce anche meccanismi di notifica per garantire che un'applicazione venga notificata quando vengono modificati determinati aspetti della configurazione di rete del computer locale.

Molte delle funzioni helper IP passano parametri della struttura che rappresentano i tipi di dati associati alla tecnologia di [base delle informazioni di gestione](/previous-versions/windows/desktop/mib/about-management-information-base) . Le funzioni di supporto IP utilizzano queste strutture per rappresentare varie informazioni di rete, ad esempio le voci della cache ARP. Poiché queste strutture vengono usate anche dall'API MIB, sono descritte nella Guida di riferimento di base per le [informazioni di gestione](/previous-versions/windows/desktop/mib/management-information-base-reference). Sebbene l'API helper IP usi queste strutture, l'helper IP è distinto da Management Information Base (MIB) e Simple Network Management Protocol (SNMP).

La documentazione dell'helper IP usa i termini "adapter" e "Interface". Un "adapter" è un termine legacy costituito da una forma abbreviata di scheda di rete che in origine faceva riferimento a una forma di hardware di rete. Un adapter è un'astrazione a livello di Datalink.

"Interface" è un termine più recente usato nei documenti RFC IETF. Le RFC definiscono un'interfaccia come un concetto astratto che rappresenta l'allegato di un nodo a un collegamento. Un'interfaccia è un'astrazione a livello di IP.

I termini dell'adapter e dell'interfaccia vengono usati in modo invariato nella documentazione dell'helper IP. Nella documentazione dell'helper IP, un elenco di adapter potrebbe includere un'interfaccia WAN software e l'interfaccia di loopback (nessuno dei due si riferisce a un dispositivo hardware). Nelle API helper IP, è presente un mapping uno-a-uno degli adapter alle interfacce.

L'helper IP offre funzionalità nelle seguenti aree:

-   [Recupero di informazioni sulla configurazione di rete](retrieving-information-about-network-configuration.md)
-   [Gestione delle schede di rete](managing-network-adapters.md)
-   [Gestione delle interfacce](managing-interfaces.md)
-   [Gestione degli indirizzi IP](managing-ip-addresses.md)
-   [Uso del protocollo di risoluzione degli indirizzi](using-the-address-resolution-protocol.md)
-   [Recupero di informazioni sul protocollo Internet e sul Internet Control Message Protocol](retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol.md)
-   [Gestione del routing](managing-routing.md)
-   [Ricezione della notifica degli eventi di rete](receiving-notification-of-network-events.md)
-   [Recupero di informazioni sul Transmission Control Protocol e sul protocollo del datagramma utente](retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol.md)

 

 
