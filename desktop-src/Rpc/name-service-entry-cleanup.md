---
title: Pulizia voce servizio nome
description: Una voce del servizio nomi deve contenere informazioni che non cambiano di frequente.
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe7484d1c6d557899e3b661a3a616c97d3890becfad51df0e91f5a69467faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019606"
---
# <a name="name-service-entry-cleanup"></a>Pulizia voce servizio nome

Una voce del servizio nomi deve contenere informazioni che non cambiano di frequente. Per questo motivo, non includere endpoint dinamici negli handle di associazione esportati perché cambieranno a ogni chiamata del server e ingombreranno la voce del servizio dei nomi. Per rimuovere questi handle di associazione, usare [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).

Ad esempio, una sequenza ragionevole di operazioni server sarebbe:

Per più di un trasporto:

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

Per inserire associazioni nel mapper di endpoint:

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

Per rimuovere gli endpoint dalle associazioni:

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

Per aggiungere associazioni al servizio dei nomi:

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




