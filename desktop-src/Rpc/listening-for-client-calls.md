---
title: Ascolto di chiamate client
description: Dopo che l'applicazione server ha registrato le interfacce, creato le informazioni di associazione necessarie e ne ha registrato gli endpoint, è pronto per iniziare ad ascoltare le chiamate di procedura remota dai programmi client.
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- Chiamata di procedura remota RPC, attività, ascolto di chiamate client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f94453a3250cfc1adae72aa0af96297a741beb501839f7f7831e3f88a8c218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928606"
---
# <a name="listening-for-client-calls"></a>Ascolto di chiamate client

Dopo che l'applicazione server ha registrato le interfacce, creato le informazioni di associazione necessarie e ne ha registrato gli endpoint, è pronto per iniziare ad ascoltare le chiamate di procedura remota dai programmi client.

Per restare in ascolto delle chiamate di procedura remota, il programma server deve chiamare [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), come illustrato nel frammento di codice seguente:


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



Un server RPC ha uno o più thread che prelevano le chiamate client e le recapitavano alle routine nelle interfacce registrate. Il primo parametro della [**funzione RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) è il numero minimo di thread da creare. Il parametro è solo un hint. il tempo di esecuzione RPC può scegliere di ignorarlo.

Il secondo parametro per [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) è il numero massimo di chiamate di procedura remota simultanee da gestire. Se si desidera che l'applicazione usi il valore massimo predefinito, passare RPC C LISTEN MAX CALLS DEFAULT come \_ \_ valore per questo \_ \_ \_ parametro.

La specifica DCE richiede che [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) continui l'esecuzione fino a quando non riceve un segnale di arresto. Un'estensione Microsoft a questa funzione è consentire l'inizio dell'ascolto e la restituzione immediata. Se si vuole che l'applicazione usi il comportamento DCE predefinito, impostare il terzo parametro su zero. Per [**informazioni dettagliate, vedere RpcServerListen,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)e [**RpcMgmtWaitServerListen.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten)

 

 




