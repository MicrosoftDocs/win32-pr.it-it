---
title: Arresto dell'applicazione server
description: Un'applicazione server può interrompere l'ascolto dei client chiamando RpcMgmtStopServerListening e RpcServerUnregisterIf oppure semplicemente chiudendo il processo host.
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- Chiamata di procedura remota RPC, attività, arresto dell'applicazione server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83f0a96732b1c862cf3e00d25cc2d2d9caf27ae5d764a9edab00c78aaf18682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925141"
---
# <a name="stopping-the-server-application"></a>Arresto dell'applicazione server

Un'applicazione server può interrompere l'ascolto dei client chiamando [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) e [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)oppure semplicemente chiudendo il processo host. Entrambi i metodi sono accettabili. Se il server segue il primo approccio, deve implementare i passaggi seguenti:

La funzione server [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) non torna al programma chiamante fino a quando non si verifica un'eccezione o fino a quando non si verifica una chiamata a [**RpcMgmtStopServerListening.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) Per impostazione predefinita, solo un altro thread del server può arrestare il server RPC usando **RpcMgmtStopServerListening**. I client che tentano di arrestare il server riceveranno l'errore RPC \_ S \_ ACCESS \_ DENIED. Tuttavia, è possibile configurare RPC per consentire ad alcuni o a tutti i client di arrestare il server. Per **informazioni dettagliate, vedere RpcMgmtStopServerListening.**

È anche possibile fare in modo che l'applicazione client eserviti una chiamata di procedura remota a una routine di arresto nel server. La routine di arresto [**chiama RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) e [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif). Questa applicazione del programma di esempio dell'esercitazione usa questo approccio aggiungendo una nuova funzione remota, **Shutdown**, al file Hellop.c.

Nella funzione **Shutdown** il singolo parametro Null di [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indica che l'applicazione locale deve interrompere l'ascolto delle chiamate di procedura remota. I due parametri Null per [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) sono caratteri jolly, a indicare che è necessario annullare la registrazione di tutte le interfacce. Il **parametro FALSE** indica che l'interfaccia deve essere rimossa immediatamente dal Registro di sistema, anziché attendere il completamento delle chiamate in sospeso.


```C++
/* add this function to hellop.c */
void Shutdown(void)
{
    RPC_STATUS status;
 
    status = RpcMgmtStopServerListening(NULL);
 
    if (status) 
    {
       exit(status);
    }
 
    status = RpcServerUnregisterIf(NULL, NULL, FALSE);
 
    if (status) 
    {
       exit(status);
    }
} //end Shutdown
```



 

 




