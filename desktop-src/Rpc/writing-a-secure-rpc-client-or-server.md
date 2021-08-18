---
title: Scrittura di un client o di un server RPC sicuro
description: In questa sezione vengono fornite indicazioni sulle procedure consigliate per la scrittura di un client o un server RPC sicuro.
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- RPC remote procedure call , procedure consigliate, scrittura di un client o di un server sicuro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b752d8dab216691105e428833c83bce28b974f121ddcc77861fbb6671d72dd22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010389"
---
# <a name="writing-a-secure-rpc-client-or-server"></a>Scrittura di un client o di un server RPC sicuro

In questa sezione vengono fornite indicazioni sulle procedure consigliate per la scrittura di un client o un server RPC sicuro.

Le informazioni contenute in questa sezione si applicano Windows 2000 e Windows XP. Questa sezione si applica a tutte le sequenze di protocollo, incluso [**ncalrpc**](/windows/desktop/Midl/ncalrpc). Gli sviluppatori tendono a pensare che **ncalrpc** non sia un probabile obiettivo per un attacco, il che non è vero in un server terminal in cui potenzialmente centinaia di utenti hanno accesso a un servizio e compromettere o addirittura eliminare un servizio può comportare l'acquisizione di un accesso aggiuntivo.

Questa sezione è suddivisa negli argomenti seguenti:

-   [Provider di sicurezza da usare](which-security-provider-to-use.md)
-   [Controllo dell'autenticazione client](controlling-client-authentication.md)
-   [Scelta di un livello di autenticazione](choosing-an-authentication-level.md)
-   [Scelta delle opzioni QOS di sicurezza](choosing-security-qos-options.md)
-   [Errore comune: presupponendo che RpcServerRegisterAuthInfo impedisca a utenti non autorizzati di chiamare il server](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [Callback](callbacks.md)
-   [Sessioni Null](null-sessions.md)
-   [Usare il flag /robust](use-the-robust-flag.md)
-   [Tecniche IDL per una migliore progettazione di interfacce e metodi](idl-techniques-for-better-interface-and-method-design.md)
-   [Handle di contesto Strict e Type Strict](strict-and-type-strict-context-handles.md)
-   [Non considerare attendibile il peer](do-not-trust-your-peer.md)
-   [Non usare la sicurezza degli endpoint](do-not-use-endpoint-security.md)
-   [Diffidato da altri endpoint RPC in esecuzione nello stesso processo](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [Verificare che il server Who che dichiara di essere](verify-the-server-is-who-it-claims-to-be.md)
-   [Usare sequenze di protocolli mainstream](use-mainstream-protocol-sequences.md)
-   [Quanto è sicuro il server RPC?](how-secure-is-my-rpc-server-now.md)

 

 