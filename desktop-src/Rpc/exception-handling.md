---
title: Gestione delle eccezioni (RPC)
description: RPC usa lo stesso approccio alla gestione delle eccezioni dell'API Windows.
ms.assetid: 7133d3f4-ed84-4cde-bc77-88e73ced9073
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b88cea6e1a2046b957baf5afe72be4cbec9f82d7da32215d2434fbf681f64d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080876"
---
# <a name="exception-handling-rpc"></a>Gestione delle eccezioni (RPC)

RPC usa lo stesso approccio alla gestione delle eccezioni dell'API Windows.

La [**struttura RpcTryFinally**](rpctryfinally.md)  /  [**RpcFinally**](/previous-versions/aa375699(v=vs.80))  /  [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) equivale all'istruzione Windows **try-finally.** Il costrutto di eccezione RPC [**RpcTryExcept**](rpctryexcept.md)  /  [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)  /  [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) equivale all'istruzione **Windows try-except.**

Quando si usano i gestori di eccezioni RPC, il codice sorgente sul lato client è portabile. I diversi file di intestazione RPC forniti per ogni piattaforma risolvono le macro **RpcTry** e [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) per ogni piattaforma. Nell'Windows, queste macro vengono mappate direttamente all'Windows **istruzioni try-finally** e **try-except.** In altri ambienti queste macro vengono mappate ad altre implementazioni specifiche della piattaforma di gestori di eccezioni.

Le possibili eccezioni generate da queste strutture includono il set di codici di errore restituiti dalle funzioni RPC con i prefissi RPC S e RPC X e il set di eccezioni restituite da \_ \_ \_ Windows. Per informazioni dettagliate, vedere [Valori restituiti RPC.](rpc-return-values.md)

Mentre le macro **RpcTry** e [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) offrono un modo personalizzabile indipendente dalla piattaforma per gestire le eccezioni, in Windows Vista e nelle versioni successive di Windows, [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) è il modo consigliato per gestire le eccezioni. Non richiede la scrittura di filtri personalizzati per acquisire molte delle eccezioni strutturate più comuni. Tuttavia, i filtri eccezioni personalizzati richiedono **ancora RpcExcept**.

Le eccezioni che si verificano nell'applicazione server, nello stub del server e nella libreria di runtime del server (sopra il livello di trasporto) vengono propagate al client. Non vengono propagate eccezioni dal livello di trasporto del server. Il metodo consigliato per una routine del server per restituire errori al runtime RPC è generare un'eccezione. Una routine del server può usare tutti i metodi appropriati per la comunicazione degli errori tra le routine del server, ma se rileva un errore che ne impedisce l'esecuzione, deve generare un'eccezione dopo la pulizia e prima di tornare al runtime RPC, anziché restituire un valore a RPC che solo la routine del server riconosce come errore.

Nella figura seguente viene illustrato come vengono restituite le eccezioni dal server al client.

![Le eccezioni vengono restituite dal server al client tramite il rispettivo runtime rpc di ogni componente](images/prog-a20.png)

I gestori di eccezioni RPC sono leggermente diversi dalle macro di gestione delle eccezioni Open Software Foundation-Distributed Computing Environment (OSF-DCE) **TRY,** **FINALLY** e **CATCH.** Diversi fornitori forniscono file di inclusione che eserciteranno il mapping delle funzioni RPC OSF-DCE alle funzioni RPC Microsoft, tra cui **TRY**, **CATCH**, **CATCH** \_ **ALL** e **ENDTRY**. Questi file di intestazione e mappano anche i codici di errore RPC S alle controparti di eccezioni \_ \_ \* OSF-DCE, rpc \_ s \_ \* e \_ \_ \* \_ \_ \* i codici di errore RPC X a rpc x . Per la portabilità di OSF-DCE, usare questi file di inclusione. Per altre informazioni sui gestori di eccezioni RPC, vedere [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter), [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept), [**RpcFinally**](/previous-versions/aa375699(v=vs.80)). Per altre informazioni sui gestori eccezioni Windows, vedere [Gestione delle eccezioni strutturata](/windows/desktop/Debug/structured-exception-handling).

 

 
