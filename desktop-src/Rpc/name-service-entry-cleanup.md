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
# <a name="name-service-entry-cleanup"></a><span data-ttu-id="c57ab-103">Pulizia voce servizio nome</span><span class="sxs-lookup"><span data-stu-id="c57ab-103">Name Service Entry Cleanup</span></span>

<span data-ttu-id="c57ab-104">Una voce del servizio nome deve contenere informazioni che non cambiano di frequente.</span><span class="sxs-lookup"><span data-stu-id="c57ab-104">A name service entry should contain information that does not change frequently.</span></span> <span data-ttu-id="c57ab-105">Per questo motivo, non includere gli endpoint dinamici negli handle di binding esportati perché verranno modificati a ogni chiamata del server e creerà un disordine per la voce del servizio del nome.</span><span class="sxs-lookup"><span data-stu-id="c57ab-105">For this reason, do not include dynamic endpoints in your exported binding handles because they will change at each invocation of the server and will clutter up your name service entry.</span></span> <span data-ttu-id="c57ab-106">Per rimuovere questi handle di binding, utilizzare [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).</span><span class="sxs-lookup"><span data-stu-id="c57ab-106">To remove these binding handles, use [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).</span></span>

<span data-ttu-id="c57ab-107">Una sequenza ragionevole di operazioni del server, ad esempio, è la seguente:</span><span class="sxs-lookup"><span data-stu-id="c57ab-107">For example, a reasonable sequence of server operations would be:</span></span>

<span data-ttu-id="c57ab-108">Per più di un trasporto:</span><span class="sxs-lookup"><span data-stu-id="c57ab-108">For more than one transport:</span></span>

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

<span data-ttu-id="c57ab-109">Per inserire i binding nel mapper dell'endpoint:</span><span class="sxs-lookup"><span data-stu-id="c57ab-109">To place bindings in the endpoint mapper:</span></span>

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

<span data-ttu-id="c57ab-110">Per rimuovere gli endpoint dalle associazioni:</span><span class="sxs-lookup"><span data-stu-id="c57ab-110">To remove endpoints from bindings:</span></span>

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

<span data-ttu-id="c57ab-111">Per aggiungere binding al servizio nome:</span><span class="sxs-lookup"><span data-stu-id="c57ab-111">To add bindings to the name service:</span></span>

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




