---
title: Bilanciamento del carico RPC
description: Bilanciamento del carico RPC
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4039742fcfcc67280c610270908bed51034f691a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044157"
---
# <a name="rpc-load-balancing"></a>Bilanciamento del carico RPC

Il bilanciamento del carico di Microsoft RPC è progettato per offrire una soluzione scalabile per gli scenari che richiedono un elevato carico di [RPC sul traffico http](remote-procedure-calls-using-rpc-over-http.md) . Lo scopo principale del Load Balancer RPC è garantire che il traffico RPC/HTTP possa essere gestito da un server farm per migliorare la scalabilità. Per ottenere questo risultato, RPC deve garantire che tutte le connessioni da un processo client siano gestite dallo stesso endpoint server nel server farm. Il Load Balancer RPC viene implementato come un servizio che viene eseguito insieme al servizio proxy RPC su HTTP.

Per abilitare il bilanciamento del carico, il servizio di bilanciamento del carico RPC in esecuzione su ogni server comunica tra loro per determinare il server preferito per la connessione client iniziale. Questo processo viene chiamato arbitraggio e si verifica al momento della connessione iniziale del client. Per ridurre il traffico tra server, il servizio di bilanciamento del carico RPC sceglie l'endpoint locale per servire la connessione se il client non è già associato a un server. Per una determinata connessione client, il risultato dell'arbitraggio è una delle due opzioni seguenti:

-   Se il client ha già eseguito una connessione, il server per la prima ricezione della connessione gestirà le connessioni successive.
-   Se si tratta della prima connessione dal client, l'arbitraggio comporterà la gestione della connessione da parte del server locale e quindi tutte le connessioni dal client. Queste informazioni, una volta determinate, verranno sottoposte a commit per gli altri servizi RPC Load Balancer nel server farm, in modo da informarli del server che gestisce tutte le richieste del client.

In questa sezione viene fornita una panoramica del bilanciamento del carico RPC negli argomenti seguenti:

-   [Distribuzione del bilanciamento del carico](deploying-load-balancing.md)
-   [Configurazione del bilanciamento del carico](configuring-load-balancing.md)
-   [Procedure consigliate per il bilanciamento del carico](load-balancing-best-practices.md)

## <a name="requirements"></a>Requisiti

Il servizio di bilanciamento del carico RPC è supportato nei server che eseguono Windows Server 2008 R2 o versione successiva e i client che eseguono Windows 7 o versioni successive di Windows.

Il servizio proxy RPC, il servizio di bilanciamento del carico RPC e gli endpoint server devono essere tutti in esecuzione nello stesso computer. Inoltre, tutti i server nel server farm devono essere in grado di gestire l'endpoint richiesto. Per informazioni sulla configurazione del servizio proxy RPC e del servizio di bilanciamento del carico RPC, vedere [configurazione dei computer per RPC su http](configuring-computers-for-rpc-over-http.md) e [configurazione del bilanciamento del carico](configuring-load-balancing.md), rispettivamente.

## <a name="limitations"></a>Limitazioni

A questo punto, il bilanciamento del carico RPC supporta solo un server farm per risorsa. Tutti i server in tutte le server farm devono essere in grado di gestire anche tutte le risorse.

 

 




