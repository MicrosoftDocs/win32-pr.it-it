---
title: Scrittura di un client o un server RPC sicuro
description: In questa sezione vengono fornite le procedure consigliate per la scrittura di un client o un server RPC protetto.
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- RPC (Remote Procedure Call), procedure consigliate, scrittura di un client o un server protetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac006f82a0db8abcd7184b2453a970521004145b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047107"
---
# <a name="writing-a-secure-rpc-client-or-server"></a>Scrittura di un client o un server RPC sicuro

In questa sezione vengono fornite le procedure consigliate per la scrittura di un client o un server RPC protetto.

Le informazioni contenute in questa sezione si applicano a Windows 2000 e Windows XP. Questa sezione si applica a tutte le sequenze di protocollo, incluso [**ncalrpc**](/windows/desktop/Midl/ncalrpc). Gli sviluppatori tendono a pensare che **ncalrpc** non sia una destinazione probabile per un attacco, che non è vero in un server terminal in cui potenzialmente centinaia di utenti hanno accesso a un servizio, e compromettere o persino arrestare un servizio può comportare l'acquisizione di un accesso aggiuntivo.

Questa sezione è divisa negli argomenti seguenti:

-   [Provider di sicurezza da usare](which-security-provider-to-use.md)
-   [Controllo dell'autenticazione client](controlling-client-authentication.md)
-   [Scelta di un livello di autenticazione](choosing-an-authentication-level.md)
-   [Scelta delle opzioni QOS di sicurezza](choosing-security-qos-options.md)
-   [Errore comune: supponendo che RpcServerRegisterAuthInfo impedisca a utenti non autorizzati di chiamare il server](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [Callback](callbacks.md)
-   [Sessioni null](null-sessions.md)
-   [Usare il flag/robust](use-the-robust-flag.md)
-   [Tecniche IDL per una migliore progettazione di interfacce e metodi](idl-techniques-for-better-interface-and-method-design.md)
-   [Handle di contesto Strict e di tipo strict](strict-and-type-strict-context-handles.md)
-   [Non considerare attendibile il peer](do-not-trust-your-peer.md)
-   [Non utilizzare la sicurezza degli endpoint](do-not-use-endpoint-security.md)
-   [Prestare attenzione ad altri endpoint RPC in esecuzione nello stesso processo](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [Verificare che il server sia quello che dichiara di essere](verify-the-server-is-who-it-claims-to-be.md)
-   [Usare le sequenze di protocollo mainstream](use-mainstream-protocol-sequences.md)
-   [Quanto è sicuro il server RPC?](how-secure-is-my-rpc-server-now.md)

 

 