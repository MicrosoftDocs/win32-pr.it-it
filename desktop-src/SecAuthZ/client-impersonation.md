---
description: La rappresentazione è la capacità di un thread di eseguire usando informazioni di sicurezza diverse rispetto al processo proprietario del thread.
ms.assetid: a3f74372-bdc9-43eb-b72f-7d00a43e78a8
title: Rappresentazione client (autorizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 454e943b53cffbc4430c71b31e2b172095b999e2201c4cafc08b081bf1782e64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783067"
---
# <a name="client-impersonation-authorization"></a>Rappresentazione client (autorizzazione)

[*La rappresentazione*](/windows/desktop/SecGloss/i-gly) è la capacità di un thread di eseguire usando informazioni di sicurezza diverse rispetto al processo proprietario del thread. In genere, un thread in un'applicazione server rappresenta un client. In questo modo il thread del server può agire per conto di tale client per accedere agli oggetti nel server o convalidare l'accesso agli oggetti del client.

L'API microsoft Windows fornisce le funzioni seguenti per iniziare una rappresentazione:

-   Un'applicazione server DDE può chiamare la [**funzione DdeImpersonateClient**](/windows/win32/api/ddeml/nf-ddeml-ddeimpersonateclient) per rappresentare un client.
-   Un server named pipe può chiamare la [**funzione ImpersonateNamedPipeClient.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient)
-   È possibile chiamare la [**funzione ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) per rappresentare il contesto di sicurezza del token di accesso di un [*utente connesso.*](/windows/desktop/SecGloss/a-gly)
-   La [**funzione ImpersonateSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself) consente a un thread di generare una copia del proprio token di accesso. Ciò è utile quando un'applicazione deve modificare il contesto di sicurezza di un singolo thread. Ad esempio, a volte solo un thread di un processo deve abilitare un [*privilegio*](/windows/desktop/SecGloss/p-gly).
-   È possibile chiamare la [**funzione SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken) per fare in modo che il thread di destinazione sia eseguito nel contesto di sicurezza di un [*token di rappresentazione specificato.*](/windows/desktop/SecGloss/i-gly)
-   Un'applicazione server RPC (Remote Procedure Call) Microsoft può chiamare la [**funzione RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) per rappresentare un client.
-   Un [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly) o un server applicazioni può chiamare la funzione [**ImpersonateSecurityContext**](/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext) per rappresentare un client.

Per la maggior parte di queste rappresentazione, il thread di rappresentazione può ripristinare il proprio contesto di sicurezza chiamando la [**funzione RevertToSelf.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) L'eccezione è la rappresentazione RPC, in cui l'applicazione server RPC chiama [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) o [**RpcRevertToSelfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoselfex) per ripristinare il proprio contesto di sicurezza.

 

 
