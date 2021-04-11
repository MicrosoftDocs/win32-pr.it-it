---
title: Registrazione dell'interfaccia
description: La registrazione dell'interfaccia supportata da un programma server consente di inviare chiamate a procedure remote da programmi client alla routine del server appropriata.
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- RPC (Remote Procedure Call), attività, registrazione dell'interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a12de37b39c719de246ceb79a92d6a51fc361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220905"
---
# <a name="registering-the-interface"></a>Registrazione dell'interfaccia

La registrazione dell'interfaccia supportata da un programma server consente di inviare chiamate a procedure remote da programmi client alla routine del server appropriata. I programmi server chiamano [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) per registrare le interfacce. Il frammento di codice seguente ne illustra l'uso:


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



Il primo parametro della funzione [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) è una struttura generata dal compilatore MIDL dal file IDL che definisce l'interfaccia (o le interfacce) per il server. Il secondo e il terzo parametro sono rispettivamente un UUID e un vettore del punto di ingresso. In questo esempio sono impostate su **null** . In molti casi, il programma server imposterà questi valori di parametro su **null**. I programmi server usano il secondo e il terzo parametro quando forniscono più implementazioni delle stesse procedure in un'interfaccia. Per altre informazioni, vedere [vettori di punti di ingresso](registering-interfaces.md).

I programmi server possono anche usare [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) per registrare un'interfaccia. Un vantaggio dell'uso di questa funzione è che fornisce all'applicazione la possibilità di impostare una funzione di callback di sicurezza. L'utilizzo delle funzioni di callback di sicurezza è l'approccio consigliato per la protezione di un'interfaccia.

> [!Note]  
> MIDL produce due strutture molto simili, una per il client e una per il server. La struttura passata alla funzione [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) è la versione server della struttura che produce MIDL.

 

 

 




