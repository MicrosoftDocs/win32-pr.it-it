---
title: Scaricamento di un server con handle di contesto in attesa
description: Tradizionalmente, lo scaricamento di una DLL che esegue il servizio di chiamate RPC mediante handle di contesto, senza prima arrestare il processo di hosting, è stato problematico.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1192b013a06def4bb1ee49e08e43b7165c9edfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221951"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a>Scaricamento di un server con handle di contesto in attesa

Tradizionalmente, lo scaricamento di una DLL che esegue il servizio di chiamate RPC mediante handle di contesto, senza prima arrestare il processo di hosting, è stato problematico. Ciò è dovuto al fatto che la routine di esecuzione non è più valida quando la DLL viene scaricata. Quando un client con un handle di contesto aperto in precedenza ha esito negativo e il tempo di esecuzione RPC tenta di chiudere l'handle del contesto, il tentativo di chiamare l'accesso alla routine di esecuzione viola e il server si arresta in modo anomalo.

A partire da Windows XP, è stata aggiunta una nuova API denominata [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) . **RpcServerUnregisterIfEx** chiude gli handle di contesto aperti dall'interfaccia di cui viene annullata la registrazione; la funzione [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) non esiste. L'uso di **RpcServerUnregisterIfEx** non è necessario quando l'intero processo viene arrestato, ma è necessario se una o più DLL che ospitano le routine di run-down vengono scaricate mentre sono presenti handle di contesto in attesa.

 

 




