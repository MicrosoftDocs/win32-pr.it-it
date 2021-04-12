---
title: Distribuzione del bilanciamento del carico
description: Distribuzione del bilanciamento del carico
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00430e8e93334c04dc74c57fc8b50db7d3c899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221221"
---
# <a name="deploying-load-balancing"></a>Distribuzione del bilanciamento del carico

L'ambiente di distribuzione tipico e il caso d'uso sono i seguenti:![bilanciamento del carico RPC](images/rpc-load-balancing.png)

1.  Il client RPC esegue una connessione RPC/HTTP al server farm.
2.  La connessione viene trasmessa attraverso la rete a un servizio di bilanciamento del carico front-end
3.  Il servizio di bilanciamento del carico front-end sceglie un server per la manutenzione della richiesta. In questo esempio il servizio di bilanciamento del carico front-end trasmette la connessione al server 1.
4.  Il servizio di bilanciamento del carico RPC arbitraggio la connessione. Determina che si tratta della prima connessione dal client e associa la connessione al server locale, server 1.
5.  Il client effettua una seconda richiesta RPC/HTTP.
6.  La richiesta viene trasmessa attraverso la rete al servizio di bilanciamento del carico front-end.
7.  Il servizio di bilanciamento del carico front-end sceglie un server per la manutenzione della richiesta. In questo caso, il servizio di bilanciamento del carico front-end sceglie il server 2 per servire la richiesta.
8.  Il servizio RPC Load Balancer arbitraggio la connessione. Riconosce che le connessioni da questo client vengono gestite dal server 1.
9.  La connessione viene trasmessa al server 1.

 

 




