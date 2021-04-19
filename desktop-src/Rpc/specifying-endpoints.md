---
title: Specifica di endpoint
description: Specifica di endpoint noti e dinamici in RPC (Remote Procedure Call).
ms.assetid: fc39b527-11e6-45a7-b3b5-8bcf469633d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 373fb2818dd14670f5a939aa524c81fcdb05e20b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300176"
---
# <a name="specifying-endpoints"></a>Specifica di endpoint

Un endpoint è un indirizzo specifico della rete di un processo server per le chiamate a procedure remote. Il nome effettivo dell'endpoint dipende dalla sequenza di protocollo utilizzata. Ad esempio, TCP, UDP e HTTP utilizzano le porte. Named Pipes usa un nome named pipe. Le applicazioni client/server possono utilizzare un endpoint noto o un endpoint dinamico. In questa sezione vengono presentate le tecniche utilizzate dai programmi server per specificare endpoint noti e dinamici. Le informazioni sono illustrate negli argomenti seguenti:

-   [Specifica di endpoint noti](#specifying-well-known-endpoints)
-   [Specifica di endpoint dinamici](#specifying-dynamic-endpoints)

## <a name="specifying-well-known-endpoints"></a>Specifica di endpoint noti

Quando il server utilizza un endpoint noto, può includere i dati dell'endpoint come parte della relativa voce del database di servizio del nome. In tal caso, l'handle di binding del client contiene un indirizzo server completo che include l'endpoint noto quando il client importa l'handle di associazione dalla voce del server.

Il programma server può inoltre specificare endpoint noti nello stesso momento in cui vengono specificate le sequenze del protocollo. Richiamare la funzione [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) o [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) . La differenza tra i due è che la seconda funzione presenta un parametro aggiuntivo che il server può utilizzare per controllare l'allocazione dinamica delle porte.

Se il programma server specifica le informazioni sull'endpoint in questo modo, deve chiamare anche la funzione [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) per registrare l'endpoint nella mappa dell'endpoint. Anche se l'endpoint è sempre lo stesso, il client può usare la mappa dell'endpoint per trovare il server.

Analogamente alle sequenze di protocollo, un'applicazione può specificare informazioni sugli endpoint nel file IDL. In tal caso, è necessario registrare contemporaneamente sia le sequenze di protocollo sia gli endpoint richiamando la funzione [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsif) o [**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex) . In questo caso, il client può accedere alle informazioni sull'endpoint tramite la specifica dell'interfaccia nel file IDL. Pertanto, non è necessario chiamare la funzione [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) .

## <a name="specifying-dynamic-endpoints"></a>Specifica di endpoint dinamici

Un endpoint dinamico è un endpoint assegnato dal computer host del server all'avvio dell'esecuzione del server. La maggior parte delle applicazioni server utilizza endpoint dinamici per evitare conflitti con altri programmi rispetto al numero limitato di porte disponibili nel computer host server. Tuttavia, i programmi che usano named pipe o la sequenza di protocollo [**ncalrpc**](/windows/desktop/Midl/ncalrpc) hanno uno spazio dei nomi di endpoint molto grande. Traggono meno vantaggio dagli endpoint dinamici rispetto ai programmi che usano altri trasporti.

I programmi server registrano endpoint dinamici in un database di mapping degli endpoint. Se si desidera che il server utilizzi un endpoint disponibile, chiamare [**RpcServerUseAllProtSeqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex), [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) o [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex). In questo modo viene impostata la libreria di runtime RPC per l'utilizzo di una o più sequenze di protocollo valide con endpoint dinamici. Il server deve quindi chiamare [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) per ottenere un set di handle di binding validi. Il server passa il set di handle di associazione o vettore di associazione alla funzione [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) per registrare tutti gli endpoint appropriati nella mappa dell'endpoint. Per ogni chiamata eseguita dal server a **RpcEpRegister**, dovrebbe essere presente una chiamata corrispondente a [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) per rilasciare la memoria utilizzata dal vettore di associazione.

Si noti che i programmi server possono usare la funzione [**RpcEpRegisterNoReplace**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregisternoreplace) anziché [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister). I programmi usano in genere **RpcEpRegisterNoReplace** quando più copie di un programma server devono essere eseguite in un sistema host server.

Entrambe le funzioni [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) e [**RpcEpRegisterNoReplace**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregisternoreplace) aggiungono le interfacce del server e gli handle di associazione al database di mapping degli endpoint. Quando il client effettua una chiamata di procedura remota utilizzando un handle parzialmente associato, la libreria di runtime del client richiede al mapper dell'endpoint del computer server per l'endpoint di un'istanza del server compatibile. La libreria client fornisce l'UUID dell'interfaccia, la sequenza di protocollo e, se presente, l'UUID dell'oggetto nell'handle di associazione client. Il mapper di endpoint cerca una voce di database corrispondente alle informazioni del client. L'UUID dell'interfaccia client/server, la versione principale dell'interfaccia e la sequenza del protocollo devono corrispondere esattamente. Inoltre, la versione secondaria dell'interfaccia del server deve essere maggiore o uguale alla versione secondaria del client.

Se tutti i test hanno esito positivo, il mapper dell'endpoint restituisce l'endpoint valido e la libreria di runtime del client aggiorna l'endpoint nell'handle di associazione.

Gli endpoint dinamici vengono eliminati automaticamente dal database di mapping degli endpoint quando il processo del server smette di funzionare. È possibile rimuovere l'endpoint dal database di mapping degli endpoint prima che il programma server venga chiuso utilizzando la funzione [**RpcEpUnregister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepunregister) oppure è possibile consentire la pulizia automatica per gestire la rimozione dell'endpoint.

 

 