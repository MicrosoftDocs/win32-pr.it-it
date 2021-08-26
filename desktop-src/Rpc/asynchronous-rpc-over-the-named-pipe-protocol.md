---
title: RPC asincrona sul protocollo Named-Pipe
description: Se si usano named pipe (ncacn np) come protocollo di trasporto, è consigliabile evitare di consentire un numero elevato di chiamate in sospeso \_ inattive sul server.
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1dade78846bc978abeb8bbbe5c324144db2645177722ca5afd1a62f99a3ea5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023671"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a>RPC asincrona sul protocollo Named-Pipe

Se si usano named pipe ([**ncacn \_ np**](/windows/desktop/Midl/ncacn-np)) come protocollo di trasporto, è consigliabile evitare di consentire un numero elevato di chiamate in sospeso inattive sul server. Con le named pipe, ogni client in attesa di una risposta avrà un named pipe in sospeso nel server, ognuno dei quali richiede una determinata quantità di memoria kernel.

Ad esempio, non si desidera utilizzare una chiamata di notifica per il nuovo messaggio di posta elettronica con il trasporto named pipe, perché tale chiamata rimarrà in sospeso anche quando i client sono inattivi e la memoria del kernel potrebbe essere esaurita. Si noti che questo non è un problema con gli altri protocolli orientati alla connessione, ad esempio [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp).

Poiché le named pipe sono un protocollo di trasporto, l'applicazione può usarle specificando [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np) come protocollo in un'associazione di stringhe. Per altre informazioni sulle named pipe, vedere [Named Pipes.](/windows/desktop/ipc/named-pipes) Per informazioni dettagliate sulla creazione di associazioni di stringhe, vedere [Using String Bindings](finding-server-host-systems.md).

 

 