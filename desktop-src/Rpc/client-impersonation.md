---
title: Rappresentazione client (RPC)
description: La rappresentazione è utile in un ambiente di elaborazione distribuita quando i server devono passare richieste client ad altri processi del server o al sistema operativo.
ms.assetid: 49d833d8-c61c-4746-91cf-c0753847cd3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d03ad3b4d9e2984708e8b274ab9bc57c3235808b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118235"
---
# <a name="client-impersonation"></a>Rappresentazione client

La rappresentazione è utile in un ambiente di elaborazione distribuita quando i server devono passare richieste client ad altri processi del server o al sistema operativo. In questo caso, un server rappresenta il contesto di sicurezza del client. Gli altri processi server possono quindi gestire la richiesta come se venisse eseguita dal client originale.

![il server rappresenta un client chiamante quando si effettuano chiamate successive per conto dell'utente](images/impr.png)

Un client, ad esempio, effettua una richiesta al server A. Se il server A deve eseguire una query sul server B per completare la richiesta, il server A rappresenta il contesto di sicurezza del client ed effettua la richiesta al server B per conto del client. Il server B usa il contesto di sicurezza del client originale, anziché l'identità di sicurezza per il server A, per determinare se completare l'attività.

Il server chiama [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) per sovrascrivere la sicurezza per il thread del server con il contesto di sicurezza del client. Al termine dell'attività, il server chiama [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself) o [**RpcRevertToSelfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoselfex) per ripristinare il contesto di sicurezza definito per il thread del server.

Quando si esegue l'associazione, il client può specificare informazioni di qualità del servizio sulla sicurezza, che specifica come il server può rappresentare il client. Una delle impostazioni, ad esempio, consente al client di specificare che il server non può rappresentare l'utente. Per ulteriori informazioni, vedere la pagina relativa alla [qualità del servizio](quality-of-service.md).

La possibilità di chiamare altri server durante la rappresentazione del client originale viene chiamata *delega*. Quando si usa la delega, un server che rappresenta un client può chiamare un altro server e può effettuare chiamate di rete con le credenziali del client. Ovvero dal punto di vista del secondo server, le richieste provenienti dal primo server non sono distinguibili dalle richieste provenienti dal client. Non tutti i provider di sicurezza supportano la delega. Microsoft fornisce un solo provider di sicurezza che supporta la delega: Kerberos.

La delega può essere una funzionalità pericolosa a causa dei privilegi che il client assegna al server durante una chiamata di procedura remota. Questo è il motivo per cui Kerberos consente le chiamate con il livello di rappresentazione della delega solo se è richiesta l'autenticazione reciproca. Gli amministratori di dominio possono limitare i computer a cui vengono effettuate chiamate con livello di rappresentazione della delega per impedire ai client non sospetti di effettuare chiamate a server che potrebbero usare le credenziali.

Un'eccezione alla regola di delega esiste: chiama usando [**ncalrpc**](/windows/desktop/Midl/ncalrpc). Quando queste chiamate vengono effettuate, il server ottiene i diritti di delega, anche se viene specificato un livello di rappresentazione di Impersonate. Ovvero, un server può chiamare altri server per conto del client. Funziona solo per una chiamata remota. Se, ad esempio, il client A chiama il server locale LB usando **ncalrpc** local server lb, può rappresentare e chiamare il server remoto RB. RB potrà agire per conto del client A, ma solo sul computer remoto su cui è in esecuzione RB. Non è possibile effettuare un'altra chiamata di rete al computer remoto C, a meno che LB non abbia specificato un livello di rappresentazione delegata quando si chiama RB.

> [!Note]  
> Il termine *rappresentazione* rappresenta due significati sovrapposti. Il primo significato della rappresentazione è il processo generale di agire per conto di un client. Il secondo significato è il livello di rappresentazione specifico definito rappresentazione. Il contesto del testo indica in genere il significato.

 

 

 