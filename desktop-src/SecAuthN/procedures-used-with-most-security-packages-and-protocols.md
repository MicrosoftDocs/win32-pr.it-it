---
description: Il modello SSPI (Security Support Provider Interface) fornisce una singola interfaccia per un'applicazione di trasporto client/server utilizzando i vari pacchetti di sicurezza disponibili in un computer o in una rete.
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: Procedure utilizzate con la maggior parte dei pacchetti e protocolli di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1053f21fdd085680da1e72f0acf9c7f816e788ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525854"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a>Procedure utilizzate con la maggior parte dei pacchetti e protocolli di sicurezza

Il modello SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) fornisce una singola interfaccia per un'applicazione di trasporto client/server utilizzando i vari [*pacchetti di sicurezza*](../secgloss/s-gly.md) disponibili in un computer o in una rete. SSPI consente a un'applicazione di utilizzare un pacchetto di sicurezza senza gestire i [*protocolli di sicurezza*](../secgloss/s-gly.md) sottostanti del pacchetto. Allo stesso tempo, SSPI consente inoltre alle applicazioni sofisticate e in grado di riconoscere la sicurezza di sfruttare le funzionalità avanzate di pacchetti di sicurezza specifici.

Le applicazioni inizializzano SSPI attenendosi alla procedura seguente per proteggere una connessione di rete per la maggior parte dei pacchetti di sicurezza:

-   [Uso di SecBufferDesc e SecBuffer](using-secbufferdesc-and-secbuffer.md)
-   [Inizializzazione di SSPI](initializing-sspi.md)
-   [Stabilire una connessione protetta con l'autenticazione](establishing-a-secure-connection-with-authentication.md)
-   [Verifica dell'integrità della comunicazione durante lo scambio di messaggi](ensuring-communication-integrity-during-message-exchange.md)
-   [Chiusura di una sessione SSPI](ending-an-sspi-session.md)

 

 
