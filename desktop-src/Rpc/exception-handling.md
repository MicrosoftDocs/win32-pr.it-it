---
title: Gestione delle eccezioni (RPC)
description: RPC usa lo stesso approccio alla gestione delle eccezioni come API Windows.
ms.assetid: 7133d3f4-ed84-4cde-bc77-88e73ced9073
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25de594a648cddb70f26b42e8b0dbf1d6a9dd51d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474951"
---
# <a name="exception-handling-rpc"></a>Gestione delle eccezioni (RPC)

RPC usa lo stesso approccio alla gestione delle eccezioni come API Windows.

La struttura [**RpcTryFinally**](rpctryfinally.md)  /  [**RpcFinally**](/previous-versions/aa375699(v=vs.80))  /  [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) è equivalente all'istruzione **try-finally** di Windows. Il costrutto di eccezione RPC [**RpcTryExcept**](rpctryexcept.md)  /  [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)  /  [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) è equivalente all'istruzione **try-except** di Windows.

Quando si utilizzano i gestori di eccezioni RPC, il codice sorgente lato client è portabile. I diversi file di intestazione RPC forniti per ogni piattaforma risolvono le macro **RpcTry** e [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) per ogni piattaforma. Nell'ambiente Windows le macro vengono mappate direttamente alle istruzioni try- **finally** e **try-except** di Windows. In altri ambienti queste macro sono mappate ad altre implementazioni specifiche della piattaforma di gestori di eccezioni.

Le potenziali eccezioni generate da queste strutture includono il set di codici di errore restituiti dalle funzioni RPC con i prefissi RPC \_ S \_ e RPC \_ X e il set di eccezioni restituite da Windows. Per informazioni dettagliate, vedere [valori restituiti RPC](rpc-return-values.md).

Sebbene le macro **RpcTry** e [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) forniscano un metodo personalizzabile indipendente dalla piattaforma per gestire le eccezioni, in Windows Vista e nelle versioni successive di Windows, [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) è il metodo consigliato per gestire le eccezioni. Non richiede la scrittura di filtri personalizzati per l'acquisizione di molte delle eccezioni strutturate più comuni; Tuttavia, i filtri eccezioni personalizzati richiedono ancora **RpcExcept**.

Le eccezioni che si verificano nell'applicazione server, nello stub server e nella libreria di runtime del server (sopra il livello di trasporto) vengono propagate al client. Nessuna eccezione viene propagata dal livello di trasporto del server. Il metodo consigliato per la restituzione di errori al runtime RPC da parte di una routine del server consiste nel generare un'eccezione. Una routine server può utilizzare qualsiasi metodo appropriato per la comunicazione di errori tra routine del server. Tuttavia, se viene rilevato un errore che impedisce l'esecuzione della procedura remota, deve generare un'eccezione dopo la pulizia e prima di tornare al runtime RPC, anziché restituire un valore a RPC che solo la routine del server riconosca come un errore.

Nella figura seguente viene illustrato il modo in cui le eccezioni vengono restituite dal server al client.

![le eccezioni vengono restituite dal server al client tramite il rispettivo runtime RPC di ogni componente](images/prog-a20.png)

I gestori di eccezioni RPC differiscono leggermente dalle macro di gestione delle eccezioni Open Software Foundation-Distributed Computing Environment (OSF-DCE), che **tentano**, **infine**, e **intercettano**. Diversi fornitori forniscono file di inclusione che mappano le funzioni RPC OSF-DCE alle funzioni RPC di Microsoft, tra cui **try**, **catch**, **catch** \_ **All** e **ENDTRY**. Questi file di intestazione consentono inoltre di eseguire il mapping dei \_ \_ \* codici di errore RPC nelle controparti di eccezione OSF-DCE, \_ \_ \* in RPC e di mappare i \_ \_ \* codici di errore RPC x a RPC \_ x \_ \* . Per la portabilità OSF-DCE, usare i file di inclusione. Per ulteriori informazioni sui gestori di eccezioni RPC, vedere [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter), [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept), [**RpcFinally**](/previous-versions/aa375699(v=vs.80)). Per altre informazioni sui gestori di eccezioni di Windows, vedere [gestione delle eccezioni strutturata](/windows/desktop/Debug/structured-exception-handling).

 

 
