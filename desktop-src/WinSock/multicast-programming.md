---
description: La programmazione multicast è abilitata tramite Windows Sockets.
ms.assetid: f729945b-b469-4baf-ac06-2431ee2d0e71
title: Programmazione multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67af0eeb087e8c6a5938f26a0644dc346d55cf51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526154"
---
# <a name="multicast-programming"></a>Programmazione multicast

La programmazione multicast è abilitata tramite Windows Sockets. Windows Sockets Abilita Multicast Listener Discovery (MLD) Versions 1 (MLDv1) e 2 (MLDv2) su IPv6 e Internet Group Management Protocol Versions 2 (IGMPv2) e 3 (IGMPv3) tramite l'utilizzo di opzioni socket o IOCTL. In questa sezione viene descritta l'implementazione di Windows, viene illustrato come abilitare la programmazione multicast utilizzando Windows Sockets e vengono forniti esempi di programmazione per illustrarne l'utilizzo.

La seconda versione di IGMP, in seguito denominata IGMPv2, consente agli host di aggiungere e lasciare gruppi multicast identificati da un indirizzo multicast IPv4 in un'interfaccia di rete specifica. Windows Sockets consente a un'applicazione di aggiungere e lasciare tali gruppi su socket specifici. Uno svantaggio di IGMPv2, tuttavia, è che qualsiasi indirizzo di origine IPv4 aggiunto al gruppo IGMPv2 può trasmettere a tutti i membri, potenzialmente sovraccaricare il gruppo e renderlo inutilizzabile per trasmissioni che richiedono un'origine primaria, ad esempio una stazione radio Internet. Il problema con IGMPv2 è l'impossibilità di scegliere in modo selettivo un singolo indirizzo di origine IPv4 (o anche alcune fonti) e l'impossibilità di bloccare i mittenti, ad esempio emittenti non autorizzati o autori di attacchi Denial of Service, per un determinato gruppo multicast. IGMPv3 risolve tali difetti.

Con Windows Sockets e IGMPv3, le applicazioni possono selezionare una particolare coppia di indirizzi di origine IPv4 multicast e gruppo multicast. Inoltre, Windows Sockets consente agli sviluppatori di consentire in modo selettivo altri emittenti in una determinata coppia di origine/gruppo oppure consente alle applicazioni di bloccare trasmissioni specifiche. IGMPv3 è supportato in Windows Vista e versioni successive.

La prima versione di MLD su IPv6, denominata MLDv1, è molto simile a IGMPv2 ed è soggetta alle stesse limitazioni. MLDv1 consente agli host di aggiungere e lasciare gruppi multicast identificati da un indirizzo multicast IPv6 in un'interfaccia di rete specifica. Windows Sockets consente a un'applicazione di aggiungere e lasciare tali gruppi su socket specifici. Tuttavia, qualsiasi indirizzo di origine IPv6 aggiunto al gruppo MLDv1 può trasmettere a tutti i membri, potenzialmente sovraccaricare il gruppo e renderlo inutilizzabile per trasmissioni che richiedono un'origine primaria. Il problema con MLDv1 è l'impossibilità di scegliere in modo selettivo un singolo indirizzo di origine IPv6 (o anche alcune fonti) e l'impossibilità di bloccare i mittenti, ad esempio emittenti non autorizzati o autori di attacchi Denial of Service, per un determinato gruppo multicast. MLDv2 risolve tali difetti.

Con Windows Sockets e MLDv2, le applicazioni possono selezionare una particolare coppia di indirizzi di origine IPv6 multicast e gruppo multicast. Inoltre, Windows Sockets consente agli sviluppatori di consentire in modo selettivo altri emittenti in una determinata coppia di origine/gruppo oppure consente alle applicazioni di bloccare trasmissioni specifiche. MLDv2 è supportato in Windows Vista e versioni successive.

Per lo sviluppo di applicazioni multicast in Windows sono disponibili due approcci che possono essere intrapresi da un programmatore di applicazioni. Il primo approccio è basato sulle modifiche. le origini multicast vengono aggiunte o rimosse usando le opzioni socket, anche nel corso della trasmissione, in base alle esigenze. Il secondo approccio è basato sullo stato finale; gli indirizzi di origine e gli eventuali indirizzi inclusi/esclusi vengono specificati con un IOCTL. Ogni approccio è una pratica di multicast valida, ma gli sviluppatori possono trovare le opzioni socket e l'approccio basato sulle modifiche più intuitivo e flessibile.

Questa sezione include le pagine seguenti: 

| Page title (Titolo della pagina)                                                                             | Descrizione                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MLD e IGMP con Windows Sockets](igmp-and-windows-sockets.md)                     | Enumera le opzioni del socket multicast disponibili per l'utilizzo nella programmazione Windows Sockets, utilizzando un approccio di programmazione basato sulle modifiche. Definisce due categorie di applicazioni multicast. |
| [Comportamento dell'opzione socket multicast](multicast-socket-option-behavior.md)               | Fornisce un'ampia tabella per illustrare le implicazioni e i requisiti della chiamata delle opzioni dei socket multicast in un ordine particolare.                                                  |
| [Esempio di programmazione multicast](multicast-programming-sample.md)                       | Frammento di programmazione che illustra come usare le opzioni socket per abilitare le applicazioni multicast in Windows.                                                                        |
| [Programmazione multicast basata sullo stato finale](final-state-based-multicast-programming.md) | Viene illustrato l'approccio di stato finale e viene illustrato come utilizzare IOCTL per la programmazione multicast con Windows Sockets.                                                                               |
| [Porting di applicazioni broadcast a IPv6](porting-broadcast-applications-to-ipv6.md)   | Vengono fornite le linee guida per il trasferimento di applicazioni broadcast IPv4 al multicast IPv6.                                                                                                     |



 

 

 



