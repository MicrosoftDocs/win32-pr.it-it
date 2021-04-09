---
title: Funzioni di acquisizione chiave
description: Per impostazione predefinita, il provider di servizi condivisi fornisce chiavi di crittografia ai programmi server che li richiedono. Ogni SSP implementa il proprio sistema di generazione delle chiavi. Il formato delle chiavi generate dal provider di servizi condivisi è specifico del provider di servizi condivisi.
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8c8e8cfb2f3b4f8f241b2401878576cbe7f90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856746"
---
# <a name="key-acquisition-functions"></a>Funzioni di acquisizione chiave

Per impostazione predefinita, il provider di servizi condivisi fornisce chiavi di crittografia ai programmi server che li richiedono. Ogni SSP implementa il proprio sistema di generazione delle chiavi. Il formato delle chiavi generate dal provider di servizi condivisi è specifico del provider di servizi condivisi.

RPC offre la possibilità di eseguire l'override del metodo predefinito di generazione delle chiavi di crittografia. L'applicazione può chiamare la funzione [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) e passargli un puntatore a una funzione di acquisizione della chiave. È possibile scrivere la funzione di acquisizione della chiave in modo che generi chiavi usando qualsiasi metodo scelto. Tuttavia, la chiave passata al programma server deve corrispondere al formato necessario per il provider di servizi condivisi.

> [!Note]  
> Per la maggior parte delle applicazioni non è necessario usare funzioni di acquisizione chiavi e può semplicemente fornire **null** a tutti i parametri in cui è richiesta una funzione di acquisizione di chiavi.

 

 

 




