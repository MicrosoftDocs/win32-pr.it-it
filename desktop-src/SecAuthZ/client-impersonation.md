---
description: La rappresentazione è la capacità di esecuzione di un thread utilizzando informazioni di sicurezza diverse da quelle del processo proprietario del thread.
ms.assetid: a3f74372-bdc9-43eb-b72f-7d00a43e78a8
title: Rappresentazione client (autorizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e72abb17c9f5f6271f55fbfc77da4f6b93ca2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966922"
---
# <a name="client-impersonation-authorization"></a>Rappresentazione client (autorizzazione)

La [*rappresentazione*](/windows/desktop/SecGloss/i-gly) è la capacità di esecuzione di un thread utilizzando informazioni di sicurezza diverse da quelle del processo proprietario del thread. Un thread in un'applicazione server rappresenta in genere un client. In questo modo il thread del server può agire per conto del client per accedere agli oggetti nel server o per convalidare l'accesso agli oggetti del client.

L'API Microsoft Windows fornisce le funzioni seguenti per iniziare una rappresentazione:

-   Un'applicazione server DDE può chiamare la funzione [**DdeImpersonateClient**](/windows/win32/api/ddeml/nf-ddeml-ddeimpersonateclient) per rappresentare un client.
-   Un server named pipe può chiamare la funzione [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) .
-   È possibile chiamare la funzione [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) per rappresentare il contesto di sicurezza di un [*token di accesso*](/windows/desktop/SecGloss/a-gly)dell'utente connesso.
-   La funzione [**ImpersonateSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself) consente a un thread di generare una copia del relativo token di accesso. Questa operazione è utile quando un'applicazione deve modificare il contesto di sicurezza di un singolo thread. Talvolta, ad esempio, solo un thread di un processo deve abilitare un [*privilegio*](/windows/desktop/SecGloss/p-gly).
-   È possibile chiamare la funzione [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken) per far sì che il thread di destinazione venga eseguito nel contesto di sicurezza di un [*token di rappresentazione*](/windows/desktop/SecGloss/i-gly)specificato.
-   Un'applicazione server RPC (Remote Procedure Call) Microsoft può chiamare la funzione [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) per rappresentare un client.
-   Un [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly) o un server applicazioni può chiamare la funzione [**ImpersonateSecurityContext**](/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext) per rappresentare un client.

Per la maggior parte di queste rappresentazioni, il thread di rappresentazione può ripristinare il proprio contesto di sicurezza chiamando la funzione [**RevertToSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) . L'eccezione è rappresentata dalla rappresentazione RPC, in cui l'applicazione server RPC chiama [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) o [**RpcRevertToSelfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoselfex) per ripristinare il proprio contesto di sicurezza.

 

 
