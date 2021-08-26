---
title: Ascolto di chiamate di procedura remota
description: Dopo che un programma server registra le informazioni di associazione e annuncia la presenza in un database del servizio nomi, può iniziare ad ascoltare l'endpoint per le chiamate di procedura remota.
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb60b6d383c7c31b7eb59aab6f17fcdad1fde108b6f26d4fa73627d34f74340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020111"
---
# <a name="listening-for-remote-procedure-calls"></a>Ascolto di chiamate di procedura remota

Dopo che un programma server registra le informazioni di associazione e annuncia la presenza in un database del servizio nomi, può iniziare ad ascoltare l'endpoint per le chiamate di procedura remota. I programmi server chiamano la [**funzione RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) per monitorare gli endpoint per le chiamate client di procedure remote.

La specifica DCE di [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indica che non deve restituire finché una funzione nel programma server non chiama [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening). L'implementazione RPC Microsoft di **RpcServerListen** usa due parametri che non sono presenti nella specifica DCE: *DontWait* e *MinimumCallThreads*. Il programma server può passare un valore diverso da zero per il *parametro DontWait.* In caso contrario, la **funzione RpcServerListen** restituirà immediatamente . Usare la [**routine RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) per eseguire l'operazione di attesa in genere associata a **RpcServerListen**.

 

 




