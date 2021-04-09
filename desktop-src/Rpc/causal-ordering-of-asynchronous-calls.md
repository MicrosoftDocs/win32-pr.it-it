---
title: Ordinamento causale di chiamate asincrone
description: In un'applicazione RPC asincrona è possibile che un thread client effettui una seconda chiamata asincrona su un handle di binding prima del completamento di una precedente chiamata eseguita su tale handle.
ms.assetid: 69beb3a4-39ae-4e3f-bb7d-31519278334d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754ae4733e5a3936bdd28fef72b9560fb9c9dfcd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044635"
---
# <a name="causal-ordering-of-asynchronous-calls"></a><span data-ttu-id="889fd-103">Ordinamento causale di chiamate asincrone</span><span class="sxs-lookup"><span data-stu-id="889fd-103">Causal Ordering of Asynchronous Calls</span></span>

<span data-ttu-id="889fd-104">In un'applicazione RPC asincrona è possibile che un thread client effettui una seconda chiamata asincrona su un handle di binding prima del completamento di una precedente chiamata eseguita su tale handle.</span><span class="sxs-lookup"><span data-stu-id="889fd-104">In an asynchronous RPC application, it is possible for a client thread to make a second asynchronous call on a binding handle before an earlier call made on that handle has completed.</span></span> <span data-ttu-id="889fd-105">La libreria di runtime RPC gestisce questa situazione come segue:</span><span class="sxs-lookup"><span data-stu-id="889fd-105">The RPC run-time library handles this situation as follows:</span></span>

-   <span data-ttu-id="889fd-106">Il meccanismo RPC asincrono garantisce che le chiamate asincrone effettuate sullo stesso handle di associazione sullo stesso thread, allo stesso livello di sicurezza, vengano inviate nell'ordine in cui sono state effettuate.</span><span class="sxs-lookup"><span data-stu-id="889fd-106">The asynchronous RPC mechanism guarantees that asynchronous calls made on the same binding handle, on the same thread, at the same security level, are dispatched in the order they were made.</span></span> <span data-ttu-id="889fd-107">L'esecuzione effettiva delle chiamate può non essere eseguita in ordine.</span><span class="sxs-lookup"><span data-stu-id="889fd-107">Actual execution of the calls may occur out of order.</span></span>
-   <span data-ttu-id="889fd-108">Come per le chiamate sincrone, le chiamate asincrone a procedure remote da thread client diversi vengono eseguite simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="889fd-108">As with synchronous calls, asynchronous remote procedure calls from different client threads execute simultaneously.</span></span>
-   <span data-ttu-id="889fd-109">Se una chiamata asincrona da un'applicazione client è seguita da una o più chiamate sincrone, la chiamata asincrona può essere eseguita durante l'esecuzione delle chiamate sincrone.</span><span class="sxs-lookup"><span data-stu-id="889fd-109">If an asynchronous call from a client application is followed by one or more synchronous calls, the asynchronous call can execute while the synchronous calls are executing.</span></span> <span data-ttu-id="889fd-110">Indipendentemente dallo stato della chiamata asincrona, le chiamate sincrone vengono eseguite nell'ordine in cui vengono ricevute dal server.</span><span class="sxs-lookup"><span data-stu-id="889fd-110">Regardless of the status of the asynchronous call, the synchronous calls are executed in the order in which they are received by the server.</span></span>
-   <span data-ttu-id="889fd-111">Se un'applicazione client seleziona un ordinamento non causale per un particolare handle di associazione, Disabilita la serializzazione per tale handle.</span><span class="sxs-lookup"><span data-stu-id="889fd-111">If a client application selects noncausal ordering for a particular binding handle, it disables serialization for that handle.</span></span> <span data-ttu-id="889fd-112">Le applicazioni abilitano l'ordinamento non causale chiamando [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) con il parametro *Option* impostato su RPC \_ C \_ opt \_ binding \_ noncausale e il parametro *OptionValue* impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="889fd-112">Applications enable noncausal ordering by calling [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) with the *Option* parameter set to RPC\_C\_OPT\_BINDING\_NONCAUSAL and the *OptionValue* parameter set to **TRUE**.</span></span> <span data-ttu-id="889fd-113">Per informazioni dettagliate, vedere [costanti delle opzioni di binding](binding-option-constants.md).</span><span class="sxs-lookup"><span data-stu-id="889fd-113">For details, see [Binding Option Constants](binding-option-constants.md).</span></span>

 

 




