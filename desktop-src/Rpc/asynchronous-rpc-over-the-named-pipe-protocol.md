---
title: RPC asincrona sul protocollo Named-Pipe
description: Se si usa Named Pipes (ncacn \_ NP) come protocollo di trasporto, è consigliabile evitare di consentire un numero elevato di chiamate in sospeso sul server.
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf46f9e1c2ea5eb3fe20203db274233f5c10dec5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963381"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a>RPC asincrona sul protocollo Named-Pipe

Se si usa Named Pipes ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)) come protocollo di trasporto, è consigliabile evitare di consentire un numero elevato di chiamate in sospeso sul server. Con Named Pipes, ogni client in attesa di una risposta avrà una lettura named pipe in sospeso sul server, ognuna delle quali richiede una certa quantità di memoria del kernel.

Ad esempio, non si desidera utilizzare una chiamata di notifica per un nuovo messaggio di posta elettronica con il trasporto named pipe, perché tale chiamata rimarrà in sospeso anche quando i client sono inattivi e la memoria kernel potrebbe essere esaurita. Si noti che questo non è un problema con gli altri protocolli orientati alla connessione, ad esempio [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp).

Poiché le named pipe sono un protocollo di trasporto, l'applicazione può usarle specificando [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) come protocollo in un'associazione di stringa. Per ulteriori informazioni sulle named pipe, vedere [Named Pipes](/windows/desktop/ipc/named-pipes). Per informazioni dettagliate sulla creazione di associazioni di stringa, vedere [uso di associazioni di stringa](finding-server-host-systems.md).

 

 