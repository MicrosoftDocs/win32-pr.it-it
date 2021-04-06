---
title: Pulizia voce servizio nome
description: Una voce del servizio nome deve contenere informazioni che non cambiano di frequente.
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0ed6a21074a49a472d7505dcfea37cf182026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045047"
---
# <a name="name-service-entry-cleanup"></a>Pulizia voce servizio nome

Una voce del servizio nome deve contenere informazioni che non cambiano di frequente. Per questo motivo, non includere gli endpoint dinamici negli handle di binding esportati perché verranno modificati a ogni chiamata del server e creerà un disordine per la voce del servizio del nome. Per rimuovere questi handle di binding, utilizzare [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).

Una sequenza ragionevole di operazioni del server, ad esempio, è la seguente:

Per più di un trasporto:

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

Per inserire i binding nel mapper dell'endpoint:

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

Per aggiungere binding al servizio nome:

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




