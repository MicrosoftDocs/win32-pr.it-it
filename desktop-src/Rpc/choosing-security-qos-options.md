---
title: Scelta delle opzioni QOS di sicurezza
description: Le opzioni QOS di sicurezza vengono passate come parte del parametro SecurityQOS specificato per la funzione RpcBindingSetAuthInfoEx. Utilizzare le seguenti procedure consigliate.
ms.assetid: 43befe3d-079a-4389-a1ff-6bda90935769
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c286b516438eae78117ef8d73939c3b4bed396d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300330"
---
# <a name="choosing-security-qos-options"></a>Scelta delle opzioni QOS di sicurezza

Le opzioni QOS di sicurezza vengono passate come parte del parametro *SecurityQOS* specificato per la funzione [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) . Utilizzare le seguenti procedure consigliate.

## <a name="use-mutual-authentication"></a>Usare l'autenticazione reciproca

L'autenticazione reciproca vera e propria è disponibile solo per determinati provider di sicurezza: Negotiate (when it negotiates Kerberos), Kerberos e Schannel. NTLM non supporta l'autenticazione reciproca. Per utilizzare l'autenticazione reciproca, è necessario fornire un nome di entità server ben formato. Molti sviluppatori utilizzano la seguente procedura di sicurezza non funzionante: il server viene chiamato per richiedere il nome principale ([**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)) e quindi richiede l'autenticazione reciproca usando il nome dell'entità. Questo approccio interrompe l'intera idea dell'autenticazione reciproca. il concetto di autenticazione reciproca è che vengono chiamati solo determinati server perché sono attendibili per l'analisi e la gestione dei dati. Utilizzando la procedura di sicurezza difettosa appena descritta, gli sviluppatori forniscono i dati a chiunque intelligente per restituirne il nome.

Ad esempio, se il software client deve chiamare solo un server in esecuzione con gli account di Joe, Pete o Alice, è necessario chiamare la funzione [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname) e il nome restituito deve essere controllato. Se è Joe, Pete o Alice, è necessario richiedere l'autenticazione reciproca usando il nome dell'entità server. Ciò garantisce che entrambe le metà della conversazione vadano alla stessa entità.

Se il software client deve chiamare un servizio in esecuzione solo con l'account di Joe, comporre direttamente il nome dell'entità server di Joe ed effettuare la chiamata. Se il server non è Joe, la chiamata avrà semplicemente esito negativo.

In molti casi, i servizi vengono eseguiti come servizi di sistema Windows, il che significa che vengono eseguiti con l'account del computer. È comunque consigliabile usare l'autenticazione reciproca e la creazione di un nome dell'entità server.

## <a name="use-the-lowest-impersonationtype-that-allows-the-call-to-go-through"></a>Usare il ImpersonationType più basso che consente la chiamata al passaggio

Questa procedura consigliata è piuttosto chiara. Anche se viene usata l'autenticazione reciproca, non concedere al server più diritti del necessario; un server legittimo potrebbe essere stato compromesso e anche se i dati inviati rientrano nelle mani sbagliate in questi casi, almeno il server non sarà in grado di accedere ad altri dati sulla rete per conto dell'utente. Alcuni server rifiuteranno una chiamata che non dispone di informazioni sufficienti per determinare ed eventualmente rappresentare il chiamante. Tenere inoltre presente che alcune sequenze di protocollo supportano la sicurezza a livello di trasporto ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) e [**ncalrpc**](/windows/desktop/Midl/ncalrpc)). In questi casi, il server può sempre rappresentare l'utente se si specifica un livello di rappresentazione sufficientemente elevato tramite il parametro *NetworkOptions* durante la creazione dell'handle di associazione.

Infine, alcuni provider o trasporti di sicurezza possono imbattersi in modo trasparente ImpersonationType a un livello superiore rispetto a quello specificato. Quando si sviluppa un programma, assicurarsi di provare a effettuare chiamate con il ImpersonationType previsto e verificare se si sta ottenendo una ImpersonationType superiore sul server.

 

 