---
description: In questo argomento vengono illustrate considerazioni specifiche sulla sicurezza quando si utilizza l'infrastruttura peer.
ms.assetid: 088a2111-f4ee-4bec-98a9-ac138950958b
title: Considerazioni relative alla sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd3078834b3a69f988d17e5cbfd5fa1bd1591e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883646"
---
# <a name="security-considerations"></a>Considerazioni relative alla sicurezza

In questo argomento vengono illustrate considerazioni specifiche sulla sicurezza quando si utilizza l'infrastruttura peer.

Quando si sviluppa un'applicazione peer usando l'infrastruttura peer, per motivi di sicurezza è necessario prendere in considerazione le autorizzazioni per la directory, l'accesso Guest ai servizi di rete peer, la divulgazione di informazioni e l'implementazione del provider di servizi di sicurezza.

## <a name="directory-permissions"></a>Autorizzazioni directory

I servizi di rete peer-to-peer archiviano i dati nella struttura di directory del profilo utente di un utente. Un utente deve disporre delle autorizzazioni di scrittura nel sottoalbero dei **dati dell'applicazione** del profilo. Per impostazione predefinita, questo elenco di controllo di accesso (ACL) viene impostato correttamente, ma un utente può modificarlo manualmente.

## <a name="guest-access-to-peer-networking-services"></a>Accesso Guest ai servizi di rete peer

Un account Guest e i membri del gruppo di **sicurezza Windows guest** non hanno accesso alla maggior parte dei servizi peer. Le applicazioni devono avere un accesso utente locale o superiore.

## <a name="information-disclosure"></a>Diffusione di informazioni

La divulgazione di informazioni include l'indirizzo, il database, l'identità e le credenziali di gruppo. Le sezioni seguenti identificano e definiscono la divulgazione di informazioni.

**Divulgazione di indirizzi** Il protocollo PNRP (Peer Name Resolution Protocol) è un servizio di risoluzione dell'identificatore che consente di risolvere un identificatore di nome peer in un indirizzo IP. Analogamente a DNS, PNRP pubblica un indirizzo IP in modo che gli utenti che conoscono l'identificatore corrispondente possano risolverlo in tale indirizzo.

-   La pubblicazione di un identificatore in PNRP significa che qualsiasi utente può risolvere l'identificatore nell'indirizzo IP pubblicato e determinare l'indirizzo IP del servizio PNRP che ha pubblicato l'identità.
-   L'infrastruttura di raggruppamento peer pubblica automaticamente il nome del gruppo peer dell'istanza del gruppo locale in PNRP. Durante la connessione a un gruppo peer, chiunque conosca il nome peer per il gruppo può risolvere gli indirizzi dei membri attivi e conosce l'indirizzo corrente di ogni utente.

La possibilità di un utente di connettersi ad altri membri del gruppo peer o a nodi del grafo peer mentre si è connessi è una funzionalità principale della rete peer. Durante la connessione a un gruppo o a un grafo peer, l'indirizzo IP corrente di un utente può essere pubblicato in un record di presenza all'interno del gruppo o del grafo peer. Per impostazione predefinita, chiunque partecipi al gruppo o al grafo peer può enumerare i membri del gruppo o del grafo e determinare gli indirizzi correnti dei membri. Si tratta di una proprietà di raggruppamento peer e di grafici peer configurabile.

**Divulgazione di database** Le infrastrutture per il raggruppamento e il grafo dei record dei database vengono archiviate nel file system locale. Qualsiasi utente di Windows con accesso amministrativo al file system locale (ad esempio un amministratore locale) può accedere teoricamente ai dati nel grafico del peer locale o nel database di gruppo. Questo è coerente con la capacità degli amministratori locali di accedere ai dati nel computer locale.

**Divulgazione di identità e credenziali di gruppo** Per il raggruppamento peer-to-peer è necessario che i membri stabiliscano connessioni tra loro per l'autenticazione mediante catene di certificati X. 509 modificate. Come parte dell'autenticazione, vengono scambiate le catene di identità e di appartenenza a gruppi (GMC) corrispondenti del membro.

Durante la connessione a un gruppo peer, l'infrastruttura di raggruppamento peer pubblica il nome peer del gruppo con PNRP. Come parte della normale operazione PNRP, la catena di GMC per tale gruppo può essere fornita ad altre istanze PNRP per dimostrare l'autorizzazione a pubblicare il nome peer del gruppo.

## <a name="security-service-provider-implementation"></a>Implementazione del provider di servizi di sicurezza

L'infrastruttura di Peer Graphing è protetta come il provider di servizi di sicurezza (SSP) implementato dallo sviluppatore di applicazioni. Maggiore è il livello di sicurezza del provider di servizi condivisi, maggiore è la sicurezza dell'applicazione per la rappresentazione grafica dei peer.

 

 



