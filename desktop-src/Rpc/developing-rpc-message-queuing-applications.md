---
title: Sviluppo di applicazioni di Accodamento RPC-Message
description: Per sfruttare al meglio il trasporto MSMQ nell'applicazione RPC, è necessario molto poco sforzo.
ms.assetid: 1ea97df8-cdf5-43b8-88aa-9e8fa6ae845a
keywords:
- RPC (Remote Procedure Call), attività, sviluppo di applicazioni di Accodamento messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e51707c0a6903200e51dd35e50e998430c8eae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047250"
---
# <a name="developing-rpc-message-queuing-applications"></a>Sviluppo di applicazioni di Accodamento RPC-Message

Per sfruttare al meglio il trasporto MSMQ nell'applicazione RPC, è necessario molto poco sforzo. Per la messaggistica sincrona è necessario specificare solo il trasporto della coda di messaggi ([**ncadg \_ mq**](/windows/desktop/Midl/ncadg-mq)) come sequenza di protocollo. Il protocollo **ncadg \_ mq** supporta tutte le funzionalità di datagramma standard, ad eccezione delle chiamate broadcast. Si noti inoltre che attualmente il trasporto della coda di messaggi non supporta gli endpoint dinamici.

Applicando l' \[ [](/windows/desktop/Midl/message) \] attributo Message alle dichiarazioni di procedura remota nel file IDL, viene automaticamente implementato l'Accodamento messaggi in modalità asincrona per tali chiamate. Ciò consente alle applicazioni client e server di controllare molte delle proprietà associate ai messaggi e alle code di messaggi, tra cui:

-   Qualità del servizio
-   Riconoscimento della ricevuta
-   Journaling
-   Priorità di chiamata
-   Persistenza della coda del processo server

Qualità del servizio è il lavoro che il trasporto farà per recapitare la chiamata al processo server. Il recapito rapido verrà accodato in memoria, quindi è piuttosto veloce, ma la chiamata andrà persa se un computer o una connessione di rete si arresta in un momento errato. Un recapito reversibile verrà inserito in un file su disco fino a quando non viene recapitato, quindi la chiamata non andrà persa, anche in caso di arresto anomalo del computer. Ciò garantisce un recapito garantito, ma con un costo in termini di prestazioni, quando ogni chiamata viene scritta su disco.

È inoltre possibile indicare al trasporto MSMQ di attendere il riconoscimento che la chiamata ha raggiunto la coda di destinazione (Server) prima di restituire. La scelta di questa opzione blocca il client fino a quando il server non riconosce la chiamata. in caso contrario, il controllo torna al client immediatamente dopo la chiamata.

Utilizzando il journaling, le chiamate possono essere registrate su disco. Se l'inserimento nel journal è attivato, ogni chiamata viene registrata su disco mentre viene trasmessa all'hop successivo fino al processo server.

La priorità delle chiamate può essere utilizzata insieme all'attributo della funzione del \[ [**messaggio**](/windows/desktop/Midl/message) RPC \] per consentire alle chiamate con priorità più alta di avere la precedenza sulle chiamate con priorità più bassa, anche se le chiamate con priorità alta arrivano in un secondo momento. La priorità di chiamata funziona anche in modo limitato con RPC sincrona, ma le chiamate RPC sincrone non possono essere impilate nello stesso modo delle chiamate asincrone.

Il processo client controlla tutte le proprietà precedenti chiamando [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption). Una volta impostate, queste proprietà rimangono attive fino a quando non vengono modificate in un'altra chiamata a **RpcBindingSetOption**.

Il processo server RPC può controllare la durata della coda di ricezione. Per impostazione predefinita, la coda viene eliminata al termine del processo server. Tuttavia, il processo server può utilizzare [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) quando si configura l'endpoint per indicare al trasporto di continuare a esistere e accettare richieste di chiamata anche quando il processo server non è in esecuzione. In questo caso, le chiamate vengono accodate ed eseguite in un secondo momento, quando il processo server torna in linea.

> [!Note]  
> Se si usano chiamate asincrone \[ [**ai messaggi**](/windows/desktop/Midl/message) \] in un'interfaccia, è necessario registrare l'interfaccia chiamando [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) o [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) prima di chiamare [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)**(ncadg \_ mq)**. Una volta accesa la sequenza di protocollo, tutte le chiamate già in attesa nella coda per il server inizieranno a essere lette fuori dalla coda. Se l'interfaccia RPC corrispondente non è stata registrata, le chiamate avranno esito negativo. Questa situazione può verificarsi se si dispone di una configurazione di un endpoint permanente per le chiamate a procedure remote, il server è stato arrestato e i client hanno continuato a inviare chiamate al server. Queste chiamate verranno impilate nella coda, in attesa di essere lette dopo che il server tornerà online.

 

Per altre informazioni, vedere [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption), [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)e \[ [**Message**](/windows/desktop/Midl/message) \] , [**ncadg \_ mq**](/windows/desktop/Midl/ncadg-mq).

 

 