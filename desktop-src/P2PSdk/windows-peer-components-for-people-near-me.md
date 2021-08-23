---
description: Windows Componenti peer per Persone nelle vicinanze
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: Windows Componenti peer per Persone nelle vicinanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762ea58aa9738bfe01e23844dd146e4de8a6a5f76433ef969b60b30fb5886db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011499"
---
# <a name="windows-peer-components-for-people-near-me"></a>Windows Componenti peer per Persone nelle vicinanze

All'interno del file eseguibile Windows peer networking (P2phost.exe), l'architettura Persone nelle vicinanze [usa](people-near-me-architecture.md) i componenti seguenti:

### <a name="people-near-me"></a>Persone nelle vicinanze

Il componente Persone nelle vicinanze (PNM) avvia l'individuazione usando Individuazione servizi Web nella subnet locale per i nomi utente dei computer con supporto PNM.

### <a name="people-near-me-publisher"></a>Persone nelle vicinanze Publisher

Il Persone nelle vicinanze Publisher pubblica i nomi alternativi degli utenti connessi per indicare la disponibilità in altri computer che usano PNM nella subnet locale. L'utente connesso deve scegliere di pubblicare il nome alternativo prima che venga annunciato. Il nome alternativo viene pubblicato nella subnet usando l'individuazione dei servizi Web. È anche possibile pubblicare oggetti e applicazioni. Tuttavia, l'utente deve specificare la pubblicazione dell'oggetto e dell'applicazione per gli ambiti **'Persone nelle vicinanze'** o **'All'.**

### <a name="people-near-me-enumerator"></a>Persone nelle vicinanze Enumeratore

Il Persone nelle vicinanze Enumeratore enumera l'elenco di utenti nella subnet locale. Usando questo elenco, Individuazione servizi Web invia una query multicast e riceve le risposte. Dopo aver ottenuto l'elenco di nomi alternativi, un'applicazione può usare l'API per recuperare altri dati pubblicati dall'utente (crittografati tramite [SChannel),](windows-vista-components-for-people-near-me.md)ad esempio l'elenco di applicazioni registrate e tutti gli oggetti pubblicati.

Il processo di ricerca e enumerazione non viene effettuato automaticamente, ma deve essere avviato in modo esplicito da un utente o da un'applicazione accedendo a PNM. I risultati della ricerca sono l'elenco di nomi alternativi di altri utenti nella stessa subnet che pubblicano i nomi alternativi usando l'API PNM.

### <a name="publication-manager"></a>Gestione pubblicazioni

Il componente Gestione pubblicazioni è responsabile della pubblicazione di aggiornamenti della presenza, dell'applicazione o degli oggetti per i contatti o le persone nelle vicinanze sottoscritte o che esere esere il polling dei dati.

### <a name="peer-signaling"></a>Segnalazione peer

Il componente Peer Signaling gestisce la creazione di connessioni tra peer per lo scambio di dati. Ad Persone nelle vicinanze, la segnalazione peer viene usata quando un utente o un'applicazione invia la query unicast a un computer specifico per la chiave pubblica, le applicazioni e gli oggetti.

### <a name="receive-invitation-handlerux"></a>Receive Invitation Handler/UX

Il componente Receive Invitation Handler/UX riceve un invito in ingresso da un'altra persona, richiede all'utente di determinare se vuole avviare l'applicazione associata all'invito e quindi avvia l'applicazione in base all'utente che accetta l'invito. Un invito è un messaggio inviato da un'altra persona per avviare l'attività di collaborazione usando un'applicazione specifica installata nei computer dell'utente e annunciata dall'utente invitato.

### <a name="peer-security"></a>Sicurezza peer

Quando vengono inviati presenza, applicazione e oggetto, le informazioni vengono crittografate usando un canale SSL ([Schannel](windows-vista-components-for-people-near-me.md)). Il computer di avvio usa la chiave pubblica del computer invitato per negoziare una chiave privata usata per crittografare i dati successivi inviati tra i due peer.

 

 



