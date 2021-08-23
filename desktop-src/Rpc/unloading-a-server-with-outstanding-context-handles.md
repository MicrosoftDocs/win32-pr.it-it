---
title: Scaricamento di un server con handle di contesto in sospeso
description: In genere, lo scaricamento di una DLL che gestisce chiamate RPC tramite handle di contesto, senza prima arrestare il processo di hosting, è stato problematico.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e581ff142c7453f4a9e9f1e40a5ab9991257a350a84b2fcb2ea08a0e157288cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010949"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a>Scaricamento di un server con handle di contesto in sospeso

In genere, lo scaricamento di una DLL che gestisce chiamate RPC tramite handle di contesto, senza prima arrestare il processo di hosting, è stato problematico. Ciò è dovuto al fatto che la routine di esecuzione non è più valida quando la DLL viene scaricata. Quando un client con un handle di contesto aperto in precedenza ha esito negativo e la fase di esecuzione RPC tenta di chiudere l'handle di contesto, il tentativo di chiamare l'accesso alla routine run-down viola e il server si arresta in modo anomalo.

A partire Windows XP, è stata aggiunta una nuova API denominata [**RpcServerUnregisterIfEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) **RpcServerUnregisterIfEx chiude** gli handle di contesto aperti dall'interfaccia di cui viene annullata la registrazione. La [**funzione RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) non esegue questa operazione. L'uso di **RpcServerUnregisterIfEx** non è necessario all'arresto dell'intero processo, ma è necessario se una o più DLL che ospitano le routine di esecuzione vengono scaricate mentre sono presenti handle di contesto in sospeso.

 

 




