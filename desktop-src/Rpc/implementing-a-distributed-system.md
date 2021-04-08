---
title: Implementazione di un sistema distribuito
description: Un modo per implementare il software in un sistema distribuito consiste nell'usare il supporto di rete non elaborato.
ms.assetid: 46abbbec-caa1-4fee-a713-4a4a2b462051
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab45f8175e82bdd1f5d6e49f3d94578473ed5c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855786"
---
# <a name="implementing-a-distributed-system"></a>Implementazione di un sistema distribuito

Un modo per implementare il software in un sistema distribuito consiste nell'usare il supporto di rete non elaborato. Questo approccio include socket, named pipe o HTTP post, ottiene e così via. Tutti questi modelli forzano lo sviluppatore a usare le primitive di programmazione di basso livello, in un modo o un altro, che forzano lo sviluppatore a gestire la rappresentazione dei dati di rete (NDR), il packaging dei dati, la gestione del traffico di rete e le condizioni di errore, la protezione dell'integrità dei dati e la crittografia e così via.

RPC offre un modello di programmazione in cui lo sviluppatore mantiene il controllo granulare dell'interazione di rete tra il client e il server tramite un'API avanzata, risparmiando così gli sviluppatori dai dettagli e dagli oneri che un sistema distribuito tende a introdurre.

Si consideri, ad esempio, l'onere associato a diversi approcci alla protezione dell'integrità e della privacy degli scambi di messaggi in un sistema distribuito. Quando si prende in considerazione la sicurezza di rete per gli scambi di pacchetti, alcune protezioni sono più vulnerabili. Non esiste una vera sicurezza di rete, ma solo diversi meccanismi di sicurezza basati su pacchetti; sicurezza che identifica il chiamante (che tende a essere debole, dal momento che i contenuti dei pacchetti possono spesso essere modificati in transito), protezione che protegge l'integrità del pacchetto senza proteggerne la privacy (varie firme e hash) e protezione per la privacy dello scambio di messaggi (vari meccanismi di crittografia).

Un altro carico di implementazione di un sistema distribuito sicuro è costituito dagli algoritmi necessari per implementare primitive di sicurezza, ad esempio crittografia, firma, autenticazione e così via. Uno sviluppatore può implementare tali algoritmi, ma questa operazione è difficile, soggetta a errori e persino rischiosa, dal momento che gli algoritmi risultanti hanno spesso problemi di sicurezza impercettibili. In alternativa, uno sviluppatore può utilizzare un provider di sicurezza disponibile per implementare la protezione per le interazioni di rete all'interno di un sistema distribuito.

Utilizzando RPC, entrambi questi oneri vengono risolti molto facilmente. Uno sviluppatore deve semplicemente indicare a RPC il pacchetto di sicurezza da usare e la protezione della sicurezza da applicare allo scambio di messaggi (in termini di autenticazione, crittografia, autenticazione reciproca, rilevamento dell'identità del chiamante e così via). RPC gestisce in modo efficiente tutti i dettagli dietro le quinte, ma offre allo sviluppatore il controllo completo sul modo in cui i dati verranno protetti.

 

 




