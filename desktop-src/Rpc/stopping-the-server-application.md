---
title: Arresto dell'applicazione server
description: Un'applicazione server può arrestare l'ascolto dei client chiamando RpcMgmtStopServerListening e RpcServerUnregisterIf oppure semplicemente uscendo dal processo host.
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- RPC (Remote Procedure Call), attività, arresto dell'applicazione server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f95ba05588e0575949614e05370f86de78207d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713681"
---
# <a name="stopping-the-server-application"></a>Arresto dell'applicazione server

Un'applicazione server può arrestare l'ascolto dei client chiamando [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) e [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)oppure semplicemente uscendo dal processo host. Entrambi i metodi sono accettabili. Se il server segue il primo approccio, deve implementare i passaggi seguenti:

La funzione server [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) non torna al programma chiamante fino a quando non si verifica un'eccezione o fino a quando non si verifica una chiamata a [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) . Per impostazione predefinita, solo un altro thread del server può arrestare il server RPC utilizzando **RpcMgmtStopServerListening**. I client che tentano di arrestare il server riceveranno l' \_ errore \_ accesso RPC \_ negato. Tuttavia, è possibile configurare RPC per consentire ad alcuni o a tutti i client di arrestare il server. Per informazioni dettagliate, vedere **RpcMgmtStopServerListening** .

È inoltre possibile fare in modo che l'applicazione client effettui una chiamata di procedura remota a una routine di arresto sul server. La routine Shutdown chiama [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) e [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif). Questa esercitazione del programma di esempio utilizza questo approccio aggiungendo una nuova funzione remota, **Shutdown**, al file ciau. c.

Nella funzione **Shutdown** il singolo parametro null di [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indica che l'applicazione locale deve interrompere l'ascolto delle chiamate a procedure remote. I due parametri null per [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) sono caratteri jolly, a indicare che è necessario annullare la registrazione di tutte le interfacce. Il parametro **false** indica che l'interfaccia deve essere rimossa immediatamente dal registro di sistema, anziché attendere il completamento delle chiamate in sospeso.


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



 

 




