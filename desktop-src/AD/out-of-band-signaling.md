---
title: Segnalazione fuori banda
description: La collaborazione di applicazioni che condividono dati comuni tramite la directory può usare la segnalazione fuori banda per evitare avallamento della versione e aggiornamenti parziali.
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06aab6482c9ad7af8e7c9b505b528b3559adb81f990b4d83681e44f418fadc66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185418"
---
# <a name="out-of-band-signaling"></a>Segnalazione fuori banda

La collaborazione di applicazioni che condividono dati comuni tramite la directory può usare la segnalazione fuori banda per evitare avallamento della versione e aggiornamenti parziali. In parole semplici, le applicazioni cooperanti usano un meccanismo separato dalla replica di directory per informare reciprocmente le modifiche nei dati comuni condivisi. La segnalazione fuori banda è la più efficace quando viene usata in combinazione con un meccanismo di controllo delle versioni. Ciò consente al partner che rileva la modifica di notificare ai partner remoti la versione dei dati condivisi da attendere.

Tornando all'esempio RPC fornito nella sezione "Skew versione" di Replication [Behavior in Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), il server RPC può richiamare i client connessi per informarli dello spostamento in un nuovo server: "I am going to move. Attendere, la replica porterà il nuovo indirizzo a breve", in modo che il client possa gestire il periodo di transizione.

Le applicazioni che richiedono l'applicazione di criteri identici per comunicare tra loro possono usare la segnalazione fuori banda per garantire che un nuovo criterio non sia utilizzato fino a quando tutte le parti coinvolte non lo hanno ricevuto. Ad esempio, se il criterio IPsec (Internet Protocol Security) tra due computer viene modificato, un agente nel computer di origine può contattare un agente nel computer di destinazione per negoziare l'applicazione dei criteri modificati, con il computer di origine che ritarda l'applicazione fino a quando il computer di destinazione non riceve anche i nuovi criteri.

 

 




