---
description: La programmazione multicast è abilitata Windows Socket.
ms.assetid: f729945b-b469-4baf-ac06-2431ee2d0e71
title: Programmazione multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0582f9d03cd5614bbe284eb81cdcb40bea8233627564ec2d3603de11fb663e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858161"
---
# <a name="multicast-programming"></a>Programmazione multicast

La programmazione multicast è abilitata Windows Socket. Windows I socket abilitano Multicast Listener Discovery (MLD) versioni 1 (MLDv1) e 2 (MLDv2) in IPv6 e le versioni 2 (IGMPv2) e 3 (IGMPv3) di Internet Group Management Protocol tramite l'uso di opzioni socket o IOCL. Questa sezione descrive l'implementazione Windows, spiega come abilitare la programmazione multicast usando Windows Sockets e fornisce esempi di programmazione per illustrarne l'uso.

La seconda versione di IGMP, denominata IGMPv2, consente agli host di partecipare e lasciare gruppi multicast identificati da un indirizzo multicast IPv4 su un'interfaccia di rete specifica. Windows I socket consentono a un'applicazione di aggiungere e lasciare tali gruppi in socket specifici. Uno svantaggio di IGMPv2, tuttavia, è che qualsiasi indirizzo di origine IPv4 aggiunto al gruppo IGMPv2 può trasmettere a tutti i membri, potenzialmente inondando il gruppo e rendendolo inutilizzabile per le trasmissioni che richiedono un'origine primaria, ad esempio una stazione radio Internet. Il problema di IGMPv2 è l'impossibilità di scegliere in modo selettivo un singolo indirizzo di origine IPv4 (o anche alcune origini) e l'impossibilità di bloccare i mittenti (ad esempio emittenti non autorizzate o distruttori Denial of Service) per un determinato gruppo multicast. IGMPv3 risolve tali lacune.

Con Windows socket e IGMPv3, le applicazioni possono selezionare una particolare coppia di indirizzi di origine IPv4 multicast e gruppo multicast. Inoltre, Windows socket consente agli sviluppatori di consentire in modo selettivo altre emittenti in una determinata coppia di origine/gruppo o consente alle applicazioni di bloccare emittenti specifici. IGMPv3 è supportato in Windows Vista e versioni successive.

La prima versione di MLD in IPv6, denominata MLDv1, è molto simile a IGMPv2 e presenta le stesse limitazioni. MLDv1 consente agli host di aggiungere e lasciare gruppi multicast identificati da un indirizzo multicast IPv6 su un'interfaccia di rete specifica. Windows I socket consentono a un'applicazione di aggiungere e lasciare tali gruppi in socket specifici. Tuttavia, qualsiasi indirizzo di origine IPv6 aggiunto al gruppo MLDv1 può trasmettere a tutti i membri, potenzialmente inondando il gruppo e rendendolo inutilizzabile per le trasmissioni che richiedono un'origine primaria. Il problema di MLDv1 è l'impossibilità di scegliere in modo selettivo un singolo indirizzo di origine IPv6 (o anche alcune origini) e l'impossibilità di bloccare i mittenti (ad esempio emittenti non autorizzate o selettori Denial of Service) per un determinato gruppo multicast. MLDv2 risolve tali lacune.

Con Windows socket e MLDv2, le applicazioni possono selezionare una particolare coppia di indirizzi di origine IPv6 multicast e gruppo multicast. Inoltre, Windows socket consente agli sviluppatori di consentire in modo selettivo altre emittenti in una determinata coppia di origine/gruppo o consente alle applicazioni di bloccare emittenti specifici. MLDv2 è supportato in Windows Vista e versioni successive.

Esistono due approcci che un programmatore di applicazioni può adottare quando sviluppa applicazioni multicast in Windows. Il primo approccio è basato sul cambiamento. Le origini multicast vengono aggiunte o rimosse usando le opzioni socket, anche durante la trasmissione, in base alle esigenze. Il secondo approccio è basato sullo stato finale; gli indirizzi di origine e gli eventuali indirizzi inclusi/esclusi vengono specificati con un IOCTL. Ogni approccio è una procedura multicast valida, ma gli sviluppatori possono trovare l'uso di opzioni socket e l'approccio basato su modifiche più intuitivo e flessibile.

In questa sezione sono disponibili le pagine seguenti: 

| Page title (Titolo della pagina)                                                                             | Descrizione                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MLD e IGMP con Windows socket](igmp-and-windows-sockets.md)                     | Enumera le opzioni socket multicast disponibili per l'uso nella programmazione Windows Sockets, usando un approccio di programmazione basato su modifiche. Definisce due categorie di applicazioni multicast. |
| [Comportamento dell'opzione socket multicast](multicast-socket-option-behavior.md)               | Fornisce una tabella completa per illustrare le implicazioni e i requisiti della chiamata di opzioni socket multicast in un ordine particolare.                                                  |
| [Esempio di programmazione multicast](multicast-programming-sample.md)                       | Frammento di programmazione che illustra come usare le opzioni socket per abilitare applicazioni multicast in Windows.                                                                        |
| [Programmazione multicast basata sullo stato finale](final-state-based-multicast-programming.md) | Illustra l'approccio con stato finale e come usare gli IOCTL per la programmazione multicast con Windows Socket.                                                                               |
| [Porting di applicazioni broadcast in IPv6](porting-broadcast-applications-to-ipv6.md)   | Fornisce linee guida per la portabilità di applicazioni broadcast IPv4 in multicast IPv6.                                                                                                     |



 

 

 



