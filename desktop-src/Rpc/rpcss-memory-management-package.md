---
title: Pacchetto di gestione della memoria RpcSs
description: La coppia allocatore/deallocatore predefinita utilizzata dagli Stub e dalla fase di esecuzione durante l'allocazione della memoria per conto dell'applicazione è la versione \_ \_ gratuita dell'utente allocatore/MIDL dell'utente MIDL \_ \_ .
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca10ebea44fbb202240e981612e16e7960216
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473899"
---
# <a name="rpcss-memory-management-package"></a><span data-ttu-id="228ed-103">Pacchetto di gestione della memoria RpcSs</span><span class="sxs-lookup"><span data-stu-id="228ed-103">RpcSs Memory Management Package</span></span>

<span data-ttu-id="228ed-104">La coppia allocatore/deallocatore predefinita utilizzata dagli Stub e dalla fase di esecuzione durante l'allocazione della memoria per conto dell'applicazione è l' **utente MIDL che \_ \_ alloca** l' / **\_ utente MIDL \_ gratuitamente**.</span><span class="sxs-lookup"><span data-stu-id="228ed-104">The default allocator/deallocator pair used by the stubs and run time when allocating memory on behalf of the application is **midl\_user\_allocate**/**midl\_user\_free**.</span></span> <span data-ttu-id="228ed-105">Tuttavia, è possibile scegliere il pacchetto RpcSs anziché quello predefinito utilizzando l'attributo ACF **\[ enable \_ allocate \]**.</span><span class="sxs-lookup"><span data-stu-id="228ed-105">However, you can choose the RpcSs package instead of the default by using the ACF attribute **\[enable\_allocate\]**.</span></span> <span data-ttu-id="228ed-106">Il pacchetto RpcSs è costituito da funzioni RPC che iniziano con il prefisso **RPCSS** o **RpcSm**.</span><span class="sxs-lookup"><span data-stu-id="228ed-106">The RpcSs package consists of RPC functions that begin with the prefix **RpcSs** or **RpcSm**.</span></span> <span data-ttu-id="228ed-107">Il pacchetto RpcSs non è consigliato per le applicazioni Windows.</span><span class="sxs-lookup"><span data-stu-id="228ed-107">The RpcSs package is not recommended for Windows applications.</span></span>

> [!Note]  
> <span data-ttu-id="228ed-108">Il pacchetto di gestione della memoria RPCSS è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="228ed-108">The Rpcss Memory Management Package is obsolete.</span></span> <span data-ttu-id="228ed-109">È consigliabile usare al suo posto l'utente [**MIDL \_ \_ allocato**](/windows/desktop/Midl/midl-user-allocate-1) e gli [**utenti di MIDL \_ \_ Free**](/windows/desktop/Midl/midl-user-free-1) .</span><span class="sxs-lookup"><span data-stu-id="228ed-109">It is recommended that [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) and [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1) are used in its place.</span></span>

 

<span data-ttu-id="228ed-110">In modalità **/OSF** , il pacchetto RPCSS è abilitato automaticamente per gli stub generati da MIDL quando vengono utilizzati i puntatori completi, quando gli argomenti richiedono l'allocazione di memoria o come risultato dell'utilizzo dell'attributo **\[ enable \_ allocate \]** .</span><span class="sxs-lookup"><span data-stu-id="228ed-110">In **/osf** mode, the RpcSs package is enabled for MIDL-generated stubs automatically when full pointers are used, when the arguments require memory allocation, or as a result of using the **\[enable\_allocate\]** attribute.</span></span> <span data-ttu-id="228ed-111">Nella modalità predefinita (Microsoft Extended) il pacchetto RpcSs viene abilitato solo quando si usa l'attributo **\[ enable \_ allocate \]** .</span><span class="sxs-lookup"><span data-stu-id="228ed-111">In the default (Microsoft extended) mode, the RpcSs package is enabled only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="228ed-112">L'attributo **\[ enable \_ allocate \]** Abilita l'ambiente RPCSS dagli Stub lato server.</span><span class="sxs-lookup"><span data-stu-id="228ed-112">The **\[enable\_allocate\]** attribute enables the RpcSs environment by the server-side stubs.</span></span> <span data-ttu-id="228ed-113">Il lato client viene avvisato in modo che sia possibile abilitare il pacchetto RpcSs.</span><span class="sxs-lookup"><span data-stu-id="228ed-113">The client side becomes alerted to the possibility that the RpcSs package may be enabled.</span></span> <span data-ttu-id="228ed-114">In modalità **/OSF** , il lato client non è interessato.</span><span class="sxs-lookup"><span data-stu-id="228ed-114">In **/osf** mode, the client side is not affected.</span></span>

<span data-ttu-id="228ed-115">Quando il pacchetto RpcSs è abilitato, l'allocazione della memoria sul lato server viene eseguita con l'allocatore di gestione della memoria di RpcSs privato e la coppia di deallocatori.</span><span class="sxs-lookup"><span data-stu-id="228ed-115">When the RpcSs package is enabled, allocation of memory on the server side is accomplished with the private RpcSs memory management allocator and deallocator pair.</span></span> <span data-ttu-id="228ed-116">È possibile allocare memoria utilizzando lo stesso meccanismo chiamando [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (o [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)).</span><span class="sxs-lookup"><span data-stu-id="228ed-116">You can allocate memory using the same mechanism by calling [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (or [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)).</span></span> <span data-ttu-id="228ed-117">Al ritorno dallo stub del server, tutta la memoria allocata dal pacchetto RpcSs viene liberata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="228ed-117">Upon return from the server stub, all the memory allocated by the RpcSs package is automatically freed.</span></span> <span data-ttu-id="228ed-118">Nell'esempio seguente viene illustrato come abilitare il pacchetto RpcSs:</span><span class="sxs-lookup"><span data-stu-id="228ed-118">The following example shows how to enable the RpcSs package:</span></span>

``` syntax
/* ACF file fragment */

[ 
    implicit_handle(handle_t GlobalHandle),
    enable_allocate
]
interface iface
{
}

/*Server management routine fragment. Replaces p=midl_user_allocate(size); */

    p=RpcSsAllocate(size);                /*raises exception */
    p=RpcSmAllocate(size, &status);       /*returns error code */
```

<span data-ttu-id="228ed-119">L'applicazione può liberare la memoria in modo esplicito richiamando la funzione [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) o [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) .</span><span class="sxs-lookup"><span data-stu-id="228ed-119">Your application can explicitly free memory by invoking the [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) or [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) function.</span></span> <span data-ttu-id="228ed-120">Si noti che queste funzioni non liberano effettivamente la memoria.</span><span class="sxs-lookup"><span data-stu-id="228ed-120">Note that these functions do not actually free memory.</span></span> <span data-ttu-id="228ed-121">Il contrassegno viene contrassegnato per l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="228ed-121">They mark it for deletion.</span></span> <span data-ttu-id="228ed-122">La libreria RPC rilascia la memoria quando il programma chiama [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) o [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).</span><span class="sxs-lookup"><span data-stu-id="228ed-122">The RPC library releases the memory when your program calls [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) or [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).</span></span>

<span data-ttu-id="228ed-123">È anche possibile abilitare l'ambiente di gestione della memoria per l'applicazione chiamando la routine [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) (ed è possibile disabilitarla chiamando la routine [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) ).</span><span class="sxs-lookup"><span data-stu-id="228ed-123">You can also enable the memory management environment for your application by calling the [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) routine (and you can disable it by calling the [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) routine).</span></span> <span data-ttu-id="228ed-124">Una volta abilitata, il codice dell'applicazione può allocare e deallocare memoria chiamando funzioni dal pacchetto RpcSs.</span><span class="sxs-lookup"><span data-stu-id="228ed-124">Once enabled, application code can allocate and deallocate memory by calling functions from the RpcSs package.</span></span>

 

 