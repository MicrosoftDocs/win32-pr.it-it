---
title: Rendere disponibile il server in rete
description: Prima che un'applicazione server possa accettare chiamate a procedure remote, è necessario che sia disponibile in rete.
ms.assetid: 1fad55e2-7221-4153-b530-b36ea42e03e1
keywords:
- RPC (Remote Procedure Call), attività, rendere disponibile il server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2826e4e63e7e78e7f87f6afc120b80e885cd3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044922"
---
# <a name="making-the-server-available-on-the-network"></a>Rendere disponibile il server in rete

Prima che un'applicazione server possa accettare chiamate a procedure remote, è necessario che sia disponibile in rete. A tale scopo, il server indica al tempo di esecuzione RPC che è disposto ad accettare le chiamate su una o più sequenze di protocollo. La scelta delle sequenze di protocollo supportate da un'applicazione server è una decisione importante. diverse sequenze di protocollo hanno funzionalità molto diverse. I server che prevedono la ricezione locale delle chiamate devono usare **ncalrpc**. I server che accettano chiamate remote devono **usare \_ \_ TCP IP di ncacn**. I server non devono verificare che la sequenza di protocollo su cui ricevono chiamate sia la sequenza di protocollo su cui si aspettano di ricevere chiamate. Per ulteriori informazioni, vedere prestare attenzione ad altri endpoint RPC in esecuzione nello stesso processo in procedure di programmazione RPC ottimali.

Nell'esempio seguente viene usato **ncacn \_ IP \_ TCP**.

La maggior parte dei programmi server utilizza tutte le sequenze di protocollo disponibili sulla rete. A tale scopo, richiamano la funzione [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) , come illustrato nel frammento di codice seguente:


```C++
RPC_STATUS status;
status = RpcServerUseAllProtseq(
    L"ncacn_ip_tcp",
    RPC_C_PROTSEQ_MAX_REQS_DEFAULT,    // Protseq dependent parameter
    NULL);                             // Always specify NULL here.
```



Il primo parametro della funzione [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) è la sequenza del protocollo. Il secondo parametro dipende dalla sequenza del protocollo. Come illustrato nel frammento di codice, la maggior parte dei programmi server imposta questo parametro su **RPC \_ C \_ PROTSEQ \_ Max \_ Rich \_ default**. Questo valore imposta la libreria RPC per l'utilizzo del valore predefinito. Il terzo parametro è un descrittore di sicurezza e non deve essere usato nelle applicazioni. Per ulteriori informazioni, vedere [**sicurezza**](security.md).

È anche possibile usare le funzioni [**RpcServerUseAllProtSeqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)o [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) .

Quando un'applicazione server seleziona almeno una sequenza di protocolli, i server che utilizzano endpoint dinamici devono creare informazioni di binding per ogni sequenza di protocollo utilizzata. Il server archivia le informazioni di binding in un vettore di associazione che può quindi esportare nel servizio di mapping degli endpoint.

Usare la funzione [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) per ottenere un vettore di associazione per l'applicazione server, come illustrato nell'esempio seguente:


```C++
RPC_STATUS status;
RPC_BINDING_VECTOR *rpcBindingVector;
 
status = RpcServerInqBindings(&rpcBindingVector);
```



L'unico parametro passato alla funzione [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) è un puntatore a un puntatore a una struttura [**di \_ \_ vettori di binding RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) . La libreria di runtime RPC alloca dinamicamente una matrice di vettori di associazione e archivia l'indirizzo della matrice nella variabile del parametro (in questo caso, **rpcBindingVector**). Ogni applicazione server è responsabile di liberare questo vettore di associazione usando la funzione [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) una volta che ha terminato l'uso (ad esempio, dopo averla passata alle funzioni appropriate).

 

 




