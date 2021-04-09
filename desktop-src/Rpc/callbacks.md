---
title: Callback (RPC)
description: Spesso il modello di programmazione richiede un callback del server a un client tramite una chiamata di procedura remota (RPC) o chiama il client in un server non attendibile. Questo introduce molti potenziali problemi.
ms.assetid: a4f3ea26-ac4b-41e5-abde-96b4baedf2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6260e2cff2cbaff86f210764e89d55859c4d33af
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047769"
---
# <a name="callbacks-rpc"></a>Callback (RPC)

Spesso il modello di programmazione richiede un callback del server a un client tramite una chiamata di procedura remota (RPC) o chiama il client in un server non attendibile. Questo introduce molti potenziali problemi.

Per prima cosa, il callback al client deve essere eseguito con un livello di rappresentazione sufficientemente basso. Se il server è un servizio di sistema con privilegi elevati, richiamando un client locale con un livello di rappresentazione di Impersonate o versioni successive è possibile fornire al client privilegi sufficienti per assumere il sistema. La chiamata di un client remoto con un livello di rappresentazione superiore al necessario può anche causare conseguenze indesiderate.

In secondo luogo, se un utente malintenzionato induce il servizio a eseguire un callback, può *avviare un attacco* di tipo Denial of Service. Tali attacchi non sono specifici di RPC; in questi attacchi, un computer induce a inviare il traffico, ma non risponde alle richieste. Si affondano sempre più risorse per chiamare il Black Hole, ma non vengono mai riportate. Un esempio generico di questo tipo di attacco è un attacco a livello di TCP denominato attacco di tipo SYN flood TCP/IP.

A livello di RPC, si verifica un semplice attacco di nero-Hole quando un utente malintenzionato chiama un'interfaccia e richiede al server di chiamare l'interfaccia. L'interfaccia è conforme, ma l'autore dell'attacco non restituisce mai la chiamata: un thread sul server è vincolato. L'utente malintenzionato esegue questa operazione 100 volte, legando 100 thread sul server. Alla fine, il server esaurisce la memoria. Il debug del server può potenzialmente rivelare l'identità del chiamante nero, ma spesso il server verrà riavviato senza sospettare la riproduzione o potrebbe non essere disponibile un'esperienza sufficiente per determinare l'autore dell'attacco.

Il terzo trabocchetto si trova nel client. Spesso un client effettua una chiamata al server per informare il server come richiamarlo (in genere un'associazione di stringa) e quindi attende che venga eseguita una chiamata dal server, accettando in modo cieco qualsiasi chiamata sull'endpoint che dichiara di provenire dal server. Il protocollo di callback dal server al client deve includere un meccanismo di verifica per assicurarsi che, quando il callback viene portato al client, sia stato effettivamente originato sul server.

 

 




