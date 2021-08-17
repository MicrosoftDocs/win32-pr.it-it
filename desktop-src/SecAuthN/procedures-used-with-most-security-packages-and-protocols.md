---
description: Il modello SSPI (Security Support Provider Interface) fornisce un'unica interfaccia per un'applicazione di trasporto client/server usando i vari pacchetti di sicurezza disponibili in un computer o in una rete.
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: Procedure utilizzate con la maggior parte dei pacchetti e dei protocolli di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 611ecbf7f2a124ea9352a71c7197d298f30a43391e3692303fcd3f7bc533cc4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920750"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a>Procedure utilizzate con la maggior parte dei pacchetti e dei protocolli di sicurezza

Il [*modello SSPI (Security Support Provider Interface)*](../secgloss/s-gly.md) fornisce un'unica interfaccia [](../secgloss/s-gly.md) per un'applicazione di trasporto client/server usando i vari pacchetti di sicurezza disponibili in un computer o in una rete. SSPI consente a un'applicazione di utilizzare un pacchetto di sicurezza senza gestire i protocolli [*di sicurezza sottostanti*](../secgloss/s-gly.md) del pacchetto. Allo stesso tempo, SSPI consente anche alle applicazioni sofisticate e con supporto della sicurezza di sfruttare le funzionalità avanzate di pacchetti di sicurezza specifici.

Le applicazioni inizializzano SSPI usando la procedura seguente per proteggere una connessione di rete per la maggior parte dei pacchetti di sicurezza:

-   [Uso di SecBufferDesc e SecBuffer](using-secbufferdesc-and-secbuffer.md)
-   [Inizializzazione di SSPI](initializing-sspi.md)
-   [Stabilire una connessione protetta con l'autenticazione](establishing-a-secure-connection-with-authentication.md)
-   [Garantire l'integrità delle comunicazioni durante l'Exchange](ensuring-communication-integrity-during-message-exchange.md)
-   [Fine di una sessione SSPI](ending-an-sspi-session.md)

 

 
