---
title: Pulizia della connessione inattiva
description: Per impostazione predefinita, le connessioni nel pool di thread non vengono chiuse fino a quando l'intera associazione non viene arrestata.
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75587781991c2aae86968d90c9da51331d7a29e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855622"
---
# <a name="idle-connection-cleanup"></a>Pulizia della connessione inattiva

Per impostazione predefinita, le connessioni nel pool di thread non vengono chiuse fino a quando l'intera associazione non viene arrestata. Questo criterio consente ai client con un numero elevato di thread o identità di sicurezza di eseguire chiamate RPC al server in modo efficiente. Lo svantaggio è che una quantità inordinata di risorse può essere impegnata a gestire tali connessioni. Per gestire il processo, RPC fornisce la funzione [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) . Questa funzione Abilita la pulizia della connessione inattiva; il client analizza periodicamente il pool di connessioni e chiude le connessioni che non sono state usate di recente. Se l'associazione ha mantenuto handle del contesto, la pulizia della connessione inattiva chiude tutte le connessioni inattive, ma verifica che almeno una connessione venga lasciata aperta, anche se la connessione è inattiva (in caso contrario, il server ottiene le esecuzioni dell'handle del contesto). Se l'associazione non ha mantenuto gli handle del contesto, la pulizia della connessione inattiva chiude tutte le connessioni inattive, anche se in questo modo non si lascia alcuna connessione nel pool.

In Windows XP, il tempo di esecuzione RPC tiene traccia del numero di connessioni aperte in un'associazione e attiva automaticamente la pulizia della connessione inattiva se il numero di connessioni in qualsiasi associazione supera una determinata soglia.

 

 




