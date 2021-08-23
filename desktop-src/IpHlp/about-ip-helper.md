---
description: Internet Protocol Helper (helper IP) consente l'amministrazione di rete del computer locale consentendo alle applicazioni di recuperare informazioni sulla configurazione di rete del computer locale e di modificare tale configurazione.
ms.assetid: 9eb8af78-612f-406c-ab92-4623b10a510e
title: Informazioni sull'helper IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77445eb999b08bda038fbffc4de5d440b7a3e79c3fa921d50f6da4ccc1f42237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014189"
---
# <a name="about-ip-helper"></a>Informazioni sull'helper IP

Internet Protocol Helper (helper IP) consente l'amministrazione di rete del computer locale consentendo alle applicazioni di recuperare informazioni sulla configurazione di rete del computer locale e di modificare tale configurazione. L'helper IP fornisce anche meccanismi di notifica per garantire che un'applicazione sia notificata quando alcuni aspetti della configurazione della rete del computer locale cambiano.

Molte delle funzioni helper IP passano parametri della struttura che rappresentano i tipi di dati associati alla [tecnologia Management Information Base.](/previous-versions/windows/desktop/mib/about-management-information-base) Le funzioni helper IP usano queste strutture per rappresentare varie informazioni di rete, ad esempio le voci della cache ARP. Poiché queste strutture vengono usate anche dall'API MIB, sono descritte in [Management Information Base Reference](/previous-versions/windows/desktop/mib/management-information-base-reference). Anche se l'API helper IP usa queste strutture, l'helper IP è distinto da Management Information Base (MIB) e Simple Network Management Protocol (SNMP).

La documentazione dell'helper IP usa ampiamente i termini "adapter" e "interface". Una "scheda" è un termine legacy che è una forma abbreviata di scheda di rete che originariamente fa riferimento a una qualche forma di hardware di rete. Un adattatore è un'astrazione a livello di collegamento dati.

Un'interfaccia è un termine più recente usato nei documenti RFC IETF. Le RFC definiscono un'interfaccia come concetto astratto che rappresenta l'allegato di un nodo a un collegamento. Un'interfaccia è un'astrazione a livello di IP.

I termini della scheda e dell'interfaccia vengono usati in modo piuttosto intercambiabile nella documentazione dell'helper IP. Nella documentazione dell'helper IP, un elenco di schede può includere un'interfaccia WAN software e l'interfaccia di loopback (nessuna di queste si riferisce a un dispositivo hardware). Nelle API helper IP è presente un mapping uno-a-uno delle schede alle interfacce.

L'helper IP offre funzionalità nelle aree seguenti:

-   [Recupero di informazioni sulla configurazione di rete](retrieving-information-about-network-configuration.md)
-   [Gestione delle schede di rete](managing-network-adapters.md)
-   [Gestione delle interfacce](managing-interfaces.md)
-   [Gestione degli indirizzi IP](managing-ip-addresses.md)
-   [Uso del protocollo di risoluzione degli indirizzi](using-the-address-resolution-protocol.md)
-   [Recupero di informazioni sul protocollo Internet e sul Internet Control Message Protocol](retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol.md)
-   [Gestione del routing](managing-routing.md)
-   [Ricezione di notifiche di eventi di rete](receiving-notification-of-network-events.md)
-   [Recupero di informazioni sull'Transmission Control Protocol e sul protocollo di datagrammi utente](retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol.md)

 

 
