---
title: Ascolto delle chiamate client
description: Dopo che l'applicazione server ha registrato le interfacce, creato le informazioni di binding necessarie e ha registrato gli endpoint, è pronto per iniziare ad ascoltare le chiamate di procedure remote da programmi client.
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- RPC, attività, ascolto per le chiamate client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f375a4620e301f59d168bf5f7a4dbeedc0fb89f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856742"
---
# <a name="listening-for-client-calls"></a>Ascolto delle chiamate client

Dopo che l'applicazione server ha registrato le interfacce, creato le informazioni di binding necessarie e ha registrato gli endpoint, è pronto per iniziare ad ascoltare le chiamate di procedure remote da programmi client.

Per ascoltare le chiamate a procedure remote, il programma server deve chiamare [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), come illustrato nel frammento di codice seguente:


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



Un server RPC ha uno o più thread che prelevano chiamate client e le inviano alle routine nelle interfacce registrate. Il primo parametro della funzione [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) è il numero minimo di thread da creare. Il parametro è solo un hint; il tempo di esecuzione RPC può scegliere di ignorarlo.

Il secondo parametro di [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) è il numero massimo di chiamate a procedure remote simultanee da gestire. Se si desidera che l'applicazione utilizzi il valore massimo predefinito, il passaggio RPC \_ C \_ Listen \_ Max \_ calls \_ default come valore per questo parametro.

La specifica DCE chiama per la continuazione dell'esecuzione di [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) fino a quando non riceve un segnale per l'arresto. Un'estensione Microsoft a questa funzione consente di iniziare l'ascolto e restituire immediatamente un risultato. Se si vuole che l'applicazione usi il comportamento predefinito di DCE, impostare il terzo parametro su zero. Per informazioni dettagliate, vedere [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)e [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) .

 

 




