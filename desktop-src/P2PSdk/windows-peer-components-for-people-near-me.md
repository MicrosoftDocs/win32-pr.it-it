---
description: Componenti peer di Windows per persone nelle vicinanze
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: Componenti peer di Windows per persone nelle vicinanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c780ccad1abd5ce04c1672f66561285831e5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967526"
---
# <a name="windows-peer-components-for-people-near-me"></a>Componenti peer di Windows per persone nelle vicinanze

All'interno del file eseguibile principale di Windows Peer Networking (P2phost.exe), l' [architettura persone nelle vicinanze](people-near-me-architecture.md) usa i componenti seguenti:

### <a name="people-near-me"></a>Persone nelle vicinanze

Il componente persone nelle vicinanze (persone nelle vicinanze) avvia l'individuazione tramite l'individuazione dei servizi Web nella subnet locale per i nomi utente dei computer con supporto per persone nelle vicinanze.

### <a name="people-near-me-publisher"></a>Publisher persone nelle vicinanze

Il componente server di pubblicazione persone nelle vicinanze pubblica gli alias degli utenti connessi per indicare la disponibilità ad altri computer che usano persone nelle vicinanze sulla subnet locale. L'utente connesso deve scegliere di pubblicare il nome alternativo prima che venga annunciato. Il nome alternativo viene pubblicato nella subnet mediante l'individuazione dei servizi Web. Inoltre, gli oggetti e le applicazioni possono essere pubblicati. Tuttavia, l'utente deve specificare la pubblicazione di oggetti e applicazioni per gli ambiti '**people near me**'**o ' all'**.

### <a name="people-near-me-enumerator"></a>Enumeratore people near me

Il componente enumeratore people near me enumera l'elenco di utenti nella subnet locale. Utilizzando questo elenco, l'individuazione dei servizi Web invia una query multicast e riceve le risposte. Una volta ottenuta l'elenco di nomi alternativi, un'applicazione può usare l'API per recuperare più dati pubblicati dall'utente (crittografato con [Schannel](windows-vista-components-for-people-near-me.md)), ad esempio l'elenco di applicazioni registrate e tutti gli oggetti da pubblicare.

Il processo di ricerca e enumerazione non viene eseguito automaticamente, ma deve essere avviato in modo esplicito da un utente o da un'applicazione tramite l'accesso a persone nelle vicinanze. I risultati della ricerca sono l'elenco di nomi alternativi di altri utenti nella stessa subnet che annunciano i propri soprannomi usando l'API persone nelle vicinanze.

### <a name="publication-manager"></a>Responsabile pubblicazione

Il componente responsabile della pubblicazione è responsabile della pubblicazione degli aggiornamenti della presenza, dell'applicazione o dell'oggetto a contatti o persone nelle vicinanze che hanno effettuato la sottoscrizione o eseguono il polling dei dati.

### <a name="peer-signaling"></a>Segnalazione peer

Il componente di segnalazione del peer gestisce la creazione di connessioni tra peer per scambiare dati. Per le persone nelle vicinanze, la segnalazione del peer viene usata quando un utente o un'applicazione invia la query unicast a un computer specifico per la chiave pubblica, le applicazioni e gli oggetti.

### <a name="receive-invitation-handlerux"></a>Gestore di invito di ricezione/UX

Il componente gestore dell'invito di ricezione/UX riceve un invito in ingresso da un altro utente, chiede all'utente di stabilire se desidera avviare l'applicazione associata all'invito e quindi avvia l'applicazione in base all'utente che accetta l'invito. Un invito è un messaggio di un'altra persona per avviare l'attività di collaborazione usando un'applicazione specifica installata in entrambi i computer dell'utente e viene annunciata dall'utente invitato.

### <a name="peer-security"></a>Sicurezza peer

Quando la presenza, l'applicazione e l'oggetto vengono inviati, le informazioni vengono crittografate tramite un canale SSL ([Schannel](windows-vista-components-for-people-near-me.md)). Il computer di origine utilizza la chiave pubblica del computer invitato per negoziare una chiave privata utilizzata per crittografare i dati successivi inviati tra i due peer.

 

 



