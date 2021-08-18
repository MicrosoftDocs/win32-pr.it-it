---
title: Registrazione dell'interfaccia
description: La registrazione dell'interfaccia che un programma server supporta consente l'invio delle chiamate di procedura remota dai programmi client alla routine del server appropriata.
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- Chiamata di procedura remota RPC, attività, registrazione dell'interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c444a82d30848f4f01643c08f17f484d027bc7b8c8efe3f10e7f3c194aac26a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926877"
---
# <a name="registering-the-interface"></a>Registrazione dell'interfaccia

La registrazione dell'interfaccia che un programma server supporta consente l'invio delle chiamate di procedura remota dai programmi client alla routine del server appropriata. I programmi server [**chiamano RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) per registrare le interfacce. Il frammento di codice seguente ne illustra l'uso:


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



Il primo parametro della funzione [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) è una struttura generata dal compilatore MIDL dal file IDL che definisce l'interfaccia (o le interfacce) per il server. Il secondo e il terzo parametro sono rispettivamente un UUID e un vettore del punto di ingresso. In questo esempio sono **impostate su NULL.** In molti casi, il programma server imposta questi valori di parametro su **NULL.** I programmi server usano il secondo e il terzo parametro quando forniscono più implementazioni delle stesse procedure in un'interfaccia. Per altre informazioni, vedere [Entry-Point Vectors](registering-interfaces.md).

I programmi server possono anche usare [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) per registrare un'interfaccia. Un vantaggio dell'uso di questa funzione è che offre all'applicazione la possibilità di impostare una funzione di callback di sicurezza. L'uso delle funzioni di callback di sicurezza è l'approccio consigliato per proteggere un'interfaccia.

> [!Note]  
> MIDL produce due strutture molto simili, una per il client e una per il server. La struttura passata alla [**funzione RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) è la versione server della struttura prodotta da MIDL.

 

 

 




