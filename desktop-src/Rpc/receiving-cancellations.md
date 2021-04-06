---
title: Ricezione di annullamenti
description: L'applicazione server può chiamare RpcServerTestCancel con l'handle di associazione della chiamata in questione per verificare se il client ha richiesto l'annullamento della chiamata asincrona. Restituisce la funzione RPC \_ \_ OK se il client ha annullato la chiamata.
ms.assetid: ac7d7a50-a788-40a9-b57d-1f528bdbd7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b8b48ef2796dab071ac705edf0ffca5156e235
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045083"
---
# <a name="receiving-cancellations"></a><span data-ttu-id="35e36-104">Ricezione di annullamenti</span><span class="sxs-lookup"><span data-stu-id="35e36-104">Receiving Cancellations</span></span>

<span data-ttu-id="35e36-105">L'applicazione server può chiamare [**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel) con l'handle di associazione della chiamata in questione per verificare se il client ha richiesto l'annullamento della chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="35e36-105">The server application can call [**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel) with the binding handle of the call in question to find out if the client has requested cancellation of the asynchronous call.</span></span> <span data-ttu-id="35e36-106">Restituisce la funzione RPC \_ \_ OK se il client ha annullato la chiamata.</span><span class="sxs-lookup"><span data-stu-id="35e36-106">It will return RPC\_S\_OK if the client canceled the call.</span></span>

 

 




