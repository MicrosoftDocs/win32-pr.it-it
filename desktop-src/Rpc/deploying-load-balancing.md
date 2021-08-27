---
title: Distribuzione del bilanciamento del carico
description: Distribuzione del bilanciamento del carico
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36d1ba29aedd5e94c29095d18fb84790ec4b76956ea20bc2ffd584b5a6a179f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021846"
---
# <a name="deploying-load-balancing"></a>Distribuzione del bilanciamento del carico

L'ambiente di distribuzione tipico e il caso d'uso in cui viene utilizzato il servizio di bilanciamento del carico RPC sono indicati di seguito:![bilanciamento del carico RPC](images/rpc-load-balancing.png)

1.  Il client RPC effettua una connessione RPC/HTTP al server farm.
2.  La connessione viene inoltrata attraverso la rete a un servizio di bilanciamento del carico front-end
3.  Il servizio di bilanciamento del carico front-end sceglie un server per la richiesta. In questo esempio il servizio di bilanciamento del carico front-end inoltra la connessione al Server 1.
4.  Il servizio di bilanciamento del carico RPC abitrate la connessione. Determina che si tratta della prima connessione dal client e associa la connessione al server locale, server 1.
5.  Il client effettua una seconda richiesta RPC/HTTP.
6.  La richiesta viene inoltrata tramite la rete al servizio di bilanciamento del carico front-end.
7.  Il servizio di bilanciamento del carico front-end sceglie un server per la richiesta. In questo caso, il servizio di bilanciamento del carico front-end sceglie server 2 per la gestione della richiesta.
8.  Il servizio Load Balancer RPC arbita la connessione. Riconosce che le connessioni da questo client vengono service da Server 1.
9.  La connessione viene inoltrata al Server 1.

 

 




