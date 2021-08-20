---
title: Certificati SSL
description: Secure Sockets Layer (SSL) è diventato uno standard per la protezione delle connessioni Internet e viene usato per evitare intercettazioni in rete. Il protocollo SSL consente a un client e a un server di autenticarsi a vicenda e negoziare gli algoritmi di crittografia.
ms.assetid: 2b78f609-473f-467b-8bf4-709b790bca53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e129ec25198ecb5758a143c8337f0c2956ed1aa4dd07b5e319262e29108d8905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995848"
---
# <a name="ssl-certificates"></a>Certificati SSL

Secure Sockets Layer (SSL), noto anche come Transport Layer Security (TLS), è diventato uno standard per la protezione delle connessioni Internet e viene usato per evitare intercettazioni nella rete. Il protocollo SSL/TLS consente a un client e a un server di autenticarsi a vicenda e negoziare gli algoritmi di crittografia.

SSL usa una chiave di crittografia e un algoritmo di crittografia per proteggere la connessione HTTP. Le chiavi di crittografia sono contenute nei certificati SSL usati sia dal client che dal server. Il certificato è in genere un documento X.509 ([RFC 2459).](https://www.ietf.org/rfc/rfc2459.txt) Il server fornisce il certificato SSL per la sessione e lo invia al client nella fase di handshake. Il client invia il certificato al server solo se il server invia una richiesta al client per un certificato. Il client autentica sempre il server, ma il server ha la possibilità di scegliere se autenticare o meno il client.

I certificati server devono essere archiviati nell'archivio permanente locale dell'API server HTTP, per l'uso ogni volta che viene creata una connessione sicura. Ogni voce dell'archivio certificati contiene anche l'indirizzo IP e la porta del server, l'hash del certificato (usato per firmare i messaggi) e l'ID applicazione. L'ID applicazione viene usato per identificare l'applicazione proprietaria del certificato.

Gli amministratori di sistema possono archiviare le informazioni sul certificato del server SSL con le API di configurazione. Uno strumento amministrativo chiama la [**funzione HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) e specifica il valore HttpServiceConfigSSLCertInfo per il parametro di configurazione del servizio per impostare le informazioni per un certificato SSL. È possibile configurare un solo certificato server per ogni coppia di indirizzi IP e porte nel computer. L'API server HTTP fornisce anche [**funzioni di query**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) ed [**eliminazione**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) per accedere o eliminare i certificati esistenti.

 

 




