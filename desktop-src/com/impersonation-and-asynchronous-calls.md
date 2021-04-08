---
title: Rappresentazione e chiamate asincrone
description: Rappresentazione e chiamate asincrone
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0854946b619f7580173ffcbc97c9af3f2540361b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730679"
---
# <a name="impersonation-and-asynchronous-calls"></a><span data-ttu-id="0cf43-103">Rappresentazione e chiamate asincrone</span><span class="sxs-lookup"><span data-stu-id="0cf43-103">Impersonation and Asynchronous Calls</span></span>

<span data-ttu-id="0cf43-104">Il server non può rappresentare il client dopo che la chiamata del server a [**ISynchronize:: Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) è stata completata, anche se il \_ metodo Begin non è stato ancora completato.</span><span class="sxs-lookup"><span data-stu-id="0cf43-104">The server cannot impersonate the client after the server's call to [**ISynchronize::Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) completes, even if the Begin\_ method has not yet completed.</span></span> <span data-ttu-id="0cf43-105">Si supponga, ad esempio, che un client chiami il \_ metodo Begin, il server elabori immediatamente la chiamata e il server chiami **Signal** per indicare che l'elaborazione è terminata.</span><span class="sxs-lookup"><span data-stu-id="0cf43-105">For example, suppose a client calls the Begin\_ method, the server processes the call immediately, and the server calls **Signal** to indicate it is finished processing.</span></span> <span data-ttu-id="0cf43-106">Anche se il lavoro continua a essere eseguito nel \_ metodo Begin, il server non può rappresentare il client al termine della chiamata a **Signal** .</span><span class="sxs-lookup"><span data-stu-id="0cf43-106">Even if work remains to be done in the Begin\_ method, the server cannot impersonate the client after the call to **Signal** completes.</span></span>

<span data-ttu-id="0cf43-107">Se il server rappresenta il client prima di chiamare il [**segnale**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), il token di rappresentazione non verrà rimosso dal thread finché il server non chiamerà [**IServerSecurity:: RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) o fino a quando non viene effettuata la chiamata al server per iniziare \_ , a seconda di quale si verifichi per primo.</span><span class="sxs-lookup"><span data-stu-id="0cf43-107">If the server impersonates the client before it calls [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), the impersonation token will not be removed from the thread until the server calls [**IServerSecurity::RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) or until the server's call to Begin\_ returns, whichever comes first.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cf43-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0cf43-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cf43-109">Delega e rappresentazione</span><span class="sxs-lookup"><span data-stu-id="0cf43-109">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> <dt>

[<span data-ttu-id="0cf43-110">Esecuzione di una chiamata asincrona</span><span class="sxs-lookup"><span data-stu-id="0cf43-110">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 