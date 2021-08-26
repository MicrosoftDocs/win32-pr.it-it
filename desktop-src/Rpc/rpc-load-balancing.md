---
title: Bilanciamento del carico RPC
description: Bilanciamento del carico RPC
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7fbace237f6d86ebadf3fadc5f3b376d94799b137153b114bc07fead3d64b09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101651"
---
# <a name="rpc-load-balancing"></a>Bilanciamento del carico RPC

Il bilanciamento del carico RPC Microsoft è progettato per offrire una soluzione scalabile per gli scenari che richiedono un carico elevato [di RPC sul traffico HTTP.](remote-procedure-calls-using-rpc-over-http.md) Lo scopo principale Load Balancer RPC è garantire che il traffico RPC/HTTP possa essere utilizzato da un server farm migliorare la scalabilità. A tale scopo, RPC deve garantire che tutte le connessioni da un processo client siano garantite dallo stesso endpoint server nel server farm. Il Load Balancer RPC viene implementato come servizio che viene eseguito insieme al servizio proxy RPC su HTTP.

Per abilitare il bilanciamento del carico, il servizio di bilanciamento del carico RPC in esecuzione in ognuno dei server comunica tra loro per determinare il server preferito per la connessione client iniziale. Questo processo è denominato arbitraggio e si verifica al momento della connessione client iniziale. Per ridurre il traffico tra server, il servizio di bilanciamento del carico RPC sceglie l'endpoint locale per la connessione se il client non è già associato a un server. Per una determinata connessione client, il risultato dell'arbitraggio è una delle due possibilità seguenti:

-   Se il client ha già effettuato una connessione, il server che riceverà prima la connessione gestirà le connessioni successive.
-   Se si tratta della prima connessione dal client, l'arbitraggio comporta la gestione della connessione da parte del server locale e quindi di tutte le connessioni dal client. Queste informazioni, una volta determinate, verranno inviate agli altri servizi rpc Load Balancer nel server farm, informandoli in tal modo del server che gestisce tutte le richieste del client.

In questa sezione viene fornita una panoramica del bilanciamento del carico RPC negli argomenti seguenti:

-   [Distribuzione del bilanciamento del carico](deploying-load-balancing.md)
-   [Configurazione del bilanciamento del carico](configuring-load-balancing.md)
-   [Procedure consigliate per il bilanciamento del carico](load-balancing-best-practices.md)

## <a name="requirements"></a>Requisiti

Il servizio di bilanciamento del carico RPC è supportato nei server che eseguono Windows Server 2008 R2 o versioni successive e nei client che eseguono Windows 7 o versioni successive di Windows.

Il servizio proxy RPC, il servizio di bilanciamento del carico RPC e gli endpoint server devono essere tutti in esecuzione nello stesso computer. Inoltre, tutti i server nel server farm essere in grado di manutenzione dell'endpoint richiesto. Per informazioni sulla configurazione del servizio proxy RPC e del servizio di bilanciamento del carico RPC, vedere rispettivamente [Configuring Computers for RPC over HTTP](configuring-computers-for-rpc-over-http.md) (Configurazione dei computer per RPC su HTTP) e [Configuring Load Balancing](configuring-load-balancing.md)(Configurazione del bilanciamento del carico).

## <a name="limitations"></a>Limitazioni

Al momento, il bilanciamento del carico RPC supporta solo server farm per risorsa. Tutti i server in tutte le server farm devono essere in grado di fornire assistenza anche a tutte le risorse.

 

 




