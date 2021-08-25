---
title: Pulizia connessione inattiva
description: Per impostazione predefinita, le connessioni nel pool di thread non vengono chiuse fino a quando non viene arrestata l'intera associazione.
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc7a7d4cefcead53e9b92678867cd76ceb6fab7f1ab5f1a573cf75378cf2a5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020801"
---
# <a name="idle-connection-cleanup"></a>Pulizia connessione inattiva

Per impostazione predefinita, le connessioni nel pool di thread non vengono chiuse fino a quando non viene arrestata l'intera associazione. Questo criterio consente ai client con un numero elevato di thread o identità di sicurezza di effettuare chiamate RPC al server in modo efficiente. Lo svantaggio è che può essere eseguito il commit di una quantità eccessiva di risorse per la gestione di tali connessioni. Per gestire il processo, RPC fornisce la [**funzione RpcMgmtEnableIdleCleanup.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) Questa funzione abilita la pulizia della connessione inattiva. il client analizza periodicamente il pool di connessioni e chiude le connessioni che non sono state usate di recente. Se l'associazione ha gestito gli handle di contesto, la pulizia della connessione inattiva chiude tutte le connessioni inattive, ma assicura che almeno una connessione venga lasciata aperta, anche se la connessione è inattiva (in caso contrario il server ottiene l'esecuzione dell'handle di contesto). Se l'associazione non ha mantenuto gli handle di contesto, la pulizia della connessione inattiva chiude tutte le connessioni inattive, anche se questa operazione non lascia connessioni nel pool.

In Windows XP, il tempo di esecuzione RPC tiene traccia del numero di connessioni aperte in un'associazione e attiva automaticamente la pulizia delle connessioni inattive se il numero di connessioni in qualsiasi associazione supera una determinata soglia.

 

 




