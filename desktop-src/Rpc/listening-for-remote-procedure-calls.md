---
title: Ascolto delle chiamate a procedure remote
description: Dopo che un programma server ha registrato le informazioni di binding e ne annuncia la presenza in un database del servizio dei nomi, può iniziare l'ascolto dell'endpoint per le chiamate di procedura remota.
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d9463e0591279377502394541190be685cccd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044000"
---
# <a name="listening-for-remote-procedure-calls"></a>Ascolto delle chiamate a procedure remote

Dopo che un programma server ha registrato le informazioni di binding e ne annuncia la presenza in un database del servizio dei nomi, può iniziare l'ascolto dell'endpoint per le chiamate di procedura remota. I programmi server chiamano la funzione [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) per monitorare gli endpoint per le chiamate client di procedure remote.

La specifica DCE di [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indica che non deve essere restituita finché una funzione del programma server non chiama [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening). L'implementazione di Microsoft RPC di **RpcServerListen** usa due parametri che non sono presenti nella specifica DCE: *DontWait* e *MinimumCallThreads*. Il programma server può passare un valore diverso da zero per il parametro *DontWait* . In caso contrario, la funzione **RpcServerListen** restituirà immediatamente. Usare la routine [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) per eseguire l'operazione di attesa in genere associata a **RpcServerListen**.

 

 




