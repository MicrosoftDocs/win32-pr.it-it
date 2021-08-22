---
title: Scelta delle opzioni QOS di sicurezza
description: Le opzioni QOS di sicurezza vengono passate come parte del parametro SecurityQOS assegnato alla funzione RpcBindingSetAuthInfoEx. Usare le procedure consigliate seguenti.
ms.assetid: 43befe3d-079a-4389-a1ff-6bda90935769
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c943fd9e2b4104de87a24c6078499fa38acdf1b6d1ea2122bf9d3063cd80f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932197"
---
# <a name="choosing-security-qos-options"></a>Scelta delle opzioni QOS di sicurezza

Le opzioni QOS di sicurezza vengono passate come parte *del parametro SecurityQOS* assegnato alla [**funzione RpcBindingSetAuthInfoEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) Usare le procedure consigliate seguenti.

## <a name="use-mutual-authentication"></a>Usare l'autenticazione reciproca

L'autenticazione reciproca reale è disponibile solo per determinati provider di sicurezza: Negotiate (quando negozia Kerberos), Kerberos e Schannel. NTLM non supporta l'autenticazione reciproca. L'uso dell'autenticazione reciproca richiede che sia specificato un nome di entità server ben formato. Molti sviluppatori usano la procedura di sicurezza non valida seguente: il server viene chiamato per richiedere il nome dell'entità ([**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)) e quindi richiede l'autenticazione reciproca con tale nome. Questo approccio interrompe l'intera idea di autenticazione reciproca. L'idea dell'autenticazione reciproca è che vengono chiamati solo determinati server perché sono attendibili per analizzare e gestire i dati. Usando la procedura di sicurezza non valida appena descritta, gli sviluppatori assegnano i propri dati a chiunque sia abbastanza intelligente da restituire il proprio nome.

Ad esempio, se il software client deve chiamare solo un server in esecuzione con gli account di Joe, Pete o Alice, è necessario chiamare la funzione [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname) e controllare il nome inviato. Se si tratta di Joe, Pete o Alice, l'autenticazione reciproca deve essere richiesta usando il nome dell'entità server. In questo modo entrambe le metà della conversazione passano alla stessa entità.

Se il software client deve chiamare un servizio in esecuzione solo con l'account di Joe, comporre direttamente il nome dell'entità server di Joe ed effettuare la chiamata. Se il server non è Joe, la chiamata avrà semplicemente esito negativo.

In molti casi, i servizi vengono eseguiti Windows di sistema, ovvero vengono eseguiti con l'account del computer. L'autenticazione reciproca e la creazione di un nome dell'entità server sono comunque consigliate.

## <a name="use-the-lowest-impersonationtype-that-allows-the-call-to-go-through"></a>Usare il tipo di rappresentazione più basso che consente il passaggio della chiamata

Questa procedura consigliata è piuttosto auto-esplicativa. Anche se viene usata l'autenticazione reciproca, non concedere al server più diritti del necessario; Un server legittimo potrebbe essere stato compromesso e, anche se i dati inviati rientrano nelle mani sbagliate in questi casi, almeno il server non sarà in grado di accedere ad altri dati nella rete per conto dell'utente. Alcuni server rifiuteranno una chiamata che non dispone di informazioni sufficienti per determinare ed eventualmente rappresentare il chiamante. Tenere inoltre presente che alcune sequenze di protocollo supportano la sicurezza a livello di trasporto ([**ncacn \_ np**](/windows/desktop/Midl/ncacn-np) [**e ncalrpc**](/windows/desktop/Midl/ncalrpc)). In questi casi, il server può sempre rappresentare l'utente se si specifica un livello di rappresentazione sufficientemente elevato tramite il *parametro NetworkOptions* quando si crea l'handle di associazione.

Infine, alcuni provider o trasporti di sicurezza possono impostare in modo trasparente ImpersonationType su un livello superiore a quello specificato. Quando si sviluppa un programma, assicurarsi di provare a effettuare chiamate con il valore ImpersonationType previsto e verificare se si sta ottenendo un valore ImpersonationType superiore nel server.

 

 