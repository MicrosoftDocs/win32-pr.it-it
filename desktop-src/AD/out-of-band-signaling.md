---
title: Segnalazione fuori banda
description: Le applicazioni cooperating che condividono dati comuni mediante la directory possono utilizzare la segnalazione fuori banda per evitare l'asimmetria di versione e gli aggiornamenti parziali.
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc630bfdf3a2700ab187cd24bbfc5a52def1103
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044103"
---
# <a name="out-of-band-signaling"></a>Segnalazione fuori banda

Le applicazioni cooperating che condividono dati comuni mediante la directory possono utilizzare la segnalazione fuori banda per evitare l'asimmetria di versione e gli aggiornamenti parziali. In poche parole, le applicazioni cooperative utilizzano un meccanismo separato dalla replica di directory per informare le modifiche nei dati comuni condivisi. La segnalazione fuori banda è più efficace se usata in combinazione con un meccanismo di controllo delle versioni, in modo da consentire al partner di rilevare la modifica per notificare ai partner remoti la versione dei dati condivisi da attendere.

Tornando all'esempio di RPC indicato nella sezione "asimmetria della versione" del [comportamento della replica in Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), il server RPC potrebbe richiamarlo nei client connessi per informare gli utenti del passaggio a un nuovo server: "lo spostamento verrà eseguito. In base alla replica, il nuovo indirizzo viene portato a breve "in modo che il client possa gestire il periodo di transizione.

Le applicazioni che richiedono criteri identici per poter comunicare tra loro possono utilizzare la segnalazione fuori banda per assicurarsi che un nuovo criterio non venga utilizzato fino a quando non tutte le parti coinvolte lo ricevono. Se, ad esempio, i criteri di Internet Protocol Security (IPsec) tra due computer vengono modificati, un agente nel computer di origine potrebbe contattare un agente nel computer di destinazione per negoziare l'applicazione dei criteri modificati, con la macchina di origine che ritarda l'applicazione fino a quando il computer di destinazione non ha ricevuto anche il nuovo criterio.

 

 




