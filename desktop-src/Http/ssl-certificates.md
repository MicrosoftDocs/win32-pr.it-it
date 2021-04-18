---
title: Certificati SSL
description: Secure Sockets Layer (SSL) è diventato uno standard per la protezione delle connessioni Internet e viene usato per impedire l'intercettazione sulla rete. Il protocollo SSL consente a un client e a un server di autenticarsi a vicenda e di negoziare gli algoritmi di crittografia.
ms.assetid: 2b78f609-473f-467b-8bf4-709b790bca53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e15e4e6f2b0fe9e3bb058ba506f8a36728540443
ms.sourcegitcommit: be2b23d847b9717224c5f31816594c8abda388a7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/18/2020
ms.locfileid: "106299544"
---
# <a name="ssl-certificates"></a>Certificati SSL

Secure Sockets Layer (SSL), noto anche come Transport Layer Security (TLS), è diventato uno standard per la protezione delle connessioni Internet e viene usato per impedire l'intercettazione sulla rete. Il protocollo SSL/TLS consente a un client e a un server di autenticarsi a vicenda e di negoziare gli algoritmi di crittografia.

SSL usa una chiave di crittografia e un algoritmo di crittografia per proteggere la connessione HTTP. Le chiavi di crittografia sono contenute nei certificati SSL usati dal client e dal server. Il certificato è in genere un documento X. 509 ([RFC 2459](https://www.ietf.org/rfc/rfc2459.txt)). Il server fornisce il certificato SSL per la sessione e invia il certificato al client nella fase di handshake. Il client invia il certificato al server solo se il server invia una richiesta al client per un certificato. Il client autentica quindi sempre il server, ma il server ha l'opzione per autenticare il client.

I certificati del server devono essere archiviati nell'archivio permanente locale dell'API del server HTTP, per l'utilizzo ogni volta che viene creata una connessione protetta. Ogni voce dell'archivio certificati contiene anche l'indirizzo IP e la porta del server, l'hash del certificato (usato per firmare i messaggi) e l'ID applicazione. L'ID applicazione viene usato per identificare l'applicazione proprietaria del certificato.

Gli amministratori di sistema possono archiviare le informazioni sul certificato del server SSL con le API di configurazione. Uno strumento di amministrazione chiama la funzione [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) e specifica il valore HttpServiceConfigSSLCertInfo per il parametro di configurazione del servizio per impostare le informazioni per un certificato SSL. È possibile configurare un solo certificato server per ogni coppia di porta e indirizzo IP nel computer. L'API server HTTP fornisce anche funzioni di [**query**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) e di [**eliminazione**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) per accedere ai certificati esistenti o eliminarli.

 

 




