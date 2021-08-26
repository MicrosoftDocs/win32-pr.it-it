---
title: Funzioni di acquisizione delle chiavi
description: Per impostazione predefinita, il provider di servizi condivisi fornisce chiavi di crittografia ai programmi server che le richiedono. Ogni provider di servizi di configurazione implementa il proprio sistema di generazione delle chiavi. Il formato delle chiavi generate dal provider di servizi condivisi è specifico per il provider di servizi condivisi.
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292926f53e5af0e75957f9b363d3917b1c5f68ef3a4e0a0acf7111c6b37b6518
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020233"
---
# <a name="key-acquisition-functions"></a>Funzioni di acquisizione delle chiavi

Per impostazione predefinita, il provider di servizi condivisi fornisce chiavi di crittografia ai programmi server che le richiedono. Ogni provider di servizi di configurazione implementa il proprio sistema di generazione delle chiavi. Il formato delle chiavi generate dal provider di servizi condivisi è specifico per il provider di servizi condivisi.

RPC offre la possibilità di eseguire l'override del metodo predefinito di generazione delle chiavi di crittografia. L'applicazione può chiamare la [**funzione RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) e passarla a un puntatore a una funzione di acquisizione della chiave. È possibile scrivere la funzione di acquisizione delle chiavi in modo che generi le chiavi usando qualsiasi metodo scelto. Tuttavia, la chiave passata al programma server deve corrispondere al formato richiesto dal provider di servizi condivisi.

> [!Note]  
> La maggior parte delle applicazioni non deve usare le funzioni di acquisizione delle chiavi e può semplicemente fornire **NULL** a tutti i parametri in cui è richiesta una funzione di acquisizione della chiave.

 

 

 




