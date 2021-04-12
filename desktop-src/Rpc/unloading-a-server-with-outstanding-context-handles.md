---
title: Scaricamento di un server con handle di contesto in attesa
description: Tradizionalmente, lo scaricamento di una DLL che esegue il servizio di chiamate RPC mediante handle di contesto, senza prima arrestare il processo di hosting, è stato problematico.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1192b013a06def4bb1ee49e08e43b7165c9edfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221951"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a><span data-ttu-id="f1729-103">Scaricamento di un server con handle di contesto in attesa</span><span class="sxs-lookup"><span data-stu-id="f1729-103">Unloading a Server with Outstanding Context Handles</span></span>

<span data-ttu-id="f1729-104">Tradizionalmente, lo scaricamento di una DLL che esegue il servizio di chiamate RPC mediante handle di contesto, senza prima arrestare il processo di hosting, è stato problematico.</span><span class="sxs-lookup"><span data-stu-id="f1729-104">Traditionally, unloading a DLL that services RPC calls using context handles, without first stopping the hosting process, has been problematic.</span></span> <span data-ttu-id="f1729-105">Ciò è dovuto al fatto che la routine di esecuzione non è più valida quando la DLL viene scaricata.</span><span class="sxs-lookup"><span data-stu-id="f1729-105">This is because the run-down routine is no longer valid when the DLL is being unloaded.</span></span> <span data-ttu-id="f1729-106">Quando un client con un handle di contesto aperto in precedenza ha esito negativo e il tempo di esecuzione RPC tenta di chiudere l'handle del contesto, il tentativo di chiamare l'accesso alla routine di esecuzione viola e il server si arresta in modo anomalo.</span><span class="sxs-lookup"><span data-stu-id="f1729-106">When a client with a previously open context handle fails, and the RPC run time tries to close the context handle, its attempt to call the run-down routine access violates, and the server crashes.</span></span>

<span data-ttu-id="f1729-107">A partire da Windows XP, è stata aggiunta una nuova API denominata [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) .</span><span class="sxs-lookup"><span data-stu-id="f1729-107">Beginning with Windows XP, a new API called [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) has been added.</span></span> <span data-ttu-id="f1729-108">**RpcServerUnregisterIfEx** chiude gli handle di contesto aperti dall'interfaccia di cui viene annullata la registrazione; la funzione [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) non esiste.</span><span class="sxs-lookup"><span data-stu-id="f1729-108">**RpcServerUnregisterIfEx** closes context handles opened by the interface being unregistered; the [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) function does not.</span></span> <span data-ttu-id="f1729-109">L'uso di **RpcServerUnregisterIfEx** non è necessario quando l'intero processo viene arrestato, ma è necessario se una o più DLL che ospitano le routine di run-down vengono scaricate mentre sono presenti handle di contesto in attesa.</span><span class="sxs-lookup"><span data-stu-id="f1729-109">Using **RpcServerUnregisterIfEx** is not necessary when the entire process shuts down, but it is necessary if one or more DLLs hosting the run-down routines is unloaded while outstanding context handles exist.</span></span>

 

 




