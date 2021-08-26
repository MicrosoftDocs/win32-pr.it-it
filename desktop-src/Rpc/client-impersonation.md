---
title: Rappresentazione client (RPC)
description: La rappresentazione è utile in un ambiente di elaborazione distribuito quando i server devono passare le richieste client ad altri processi server o al sistema operativo.
ms.assetid: 49d833d8-c61c-4746-91cf-c0753847cd3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73061a35c61a22a4d238e902c3dcb298e3ac0affaf4b0929c83311145a684f1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022826"
---
# <a name="client-impersonation"></a>Rappresentazione client

La rappresentazione è utile in un ambiente di elaborazione distribuito quando i server devono passare le richieste client ad altri processi server o al sistema operativo. In questo caso, un server rappresenta il contesto di sicurezza del client. Altri processi server possono quindi gestire la richiesta come se fosse stata effettuata dal client originale.

![il server rappresenta un client chiamante quando effettua chiamate successive per conto del client](images/impr.png)

Ad esempio, un client effettua una richiesta al server A. Se il server A deve eseguire una query sul server B per completare la richiesta, il server A rappresenta il contesto di sicurezza client e invia la richiesta al Server B per conto del client. Il server B usa il contesto di sicurezza del client originale, anziché l'identità di sicurezza per il server A, per determinare se completare l'attività.

Il server chiama [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) per sovrascrivere la sicurezza per il thread del server con il contesto di sicurezza client. Al termine dell'attività, il server chiama [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself) o [**RpcRevertToSelfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoselfex) per ripristinare il contesto di sicurezza definito per il thread del server.

Durante l'associazione, il client può specificare informazioni sulla qualità del servizio sulla sicurezza che specificano come il server può rappresentare il client. Ad esempio, una delle impostazioni consente al client di specificare che il server non è autorizzato a rappresentarlo. Per altre informazioni, vedere [Quality of Service](quality-of-service.md).

La possibilità di chiamare altri server durante la rappresentazione del client originale è detta *delega*. Quando si usa la delega, un server che rappresenta un client può chiamare un altro server e può effettuare chiamate di rete con le credenziali del client. Dal punto di vista del secondo server, le richieste provenienti dal primo server sono quindi indistinguibili dalle richieste provenienti dal client. Non tutti i provider di sicurezza supportano la delega. Microsoft viene fornito un solo provider di sicurezza che supporta la delega: Kerberos.

La delega può essere una funzionalità pericolosa a causa dei privilegi che il client concede al server durante una chiamata di procedura remota. Per questo motivo Kerberos consente le chiamate con il livello di rappresentazione di delega solo se viene richiesta l'autenticazione reciproca. Gli amministratori di dominio possono limitare i computer a cui vengono effettuate chiamate con livello di rappresentazione della delega per impedire ai client ignari di effettuare chiamate ai server che potrebbero usare le proprie credenziali.

Esiste un'eccezione alla regola di delega: chiamate che usano [**ncalrpc**](/windows/desktop/Midl/ncalrpc). Quando vengono effettuate queste chiamate, il server ottiene i diritti di delega, anche se viene specificato un livello di rappresentazione. In altre parole, un server può chiamare altri server per conto del client. Questa operazione funziona solo per una chiamata remota. Ad esempio, se il client A chiama LB del server locale usando **ncalrpc** local server LB può rappresentare e chiamare il server remoto RB. RB sarà in grado di agire per conto del client A, ma solo nel computer remoto in cui è in esecuzione RB. Non può effettuare un'altra chiamata di rete al computer remoto C a meno che LB non ha specificato un livello di rappresentazione di delegato quando ha chiamato RB.

> [!Note]  
> Il termine *rappresentazione* rappresenta due significati sovrapposti. Il primo significato della rappresentazione è il processo generale di azione per conto di un client. Il secondo significato è il livello di rappresentazione specifico denominato rappresentazione. Il contesto del testo in genere chiarisce il significato.

 

 

 