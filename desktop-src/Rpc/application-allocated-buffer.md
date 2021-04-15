---
title: Buffer Application-Allocated
description: L'attributo ACF \ byte \_ count \ indica agli stub di usare un buffer preallocato non allocato o liberato dalle routine di supporto client.
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db533495f16d37aca0bdae96035783650573a60f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473915"
---
# <a name="application-allocated-buffer"></a><span data-ttu-id="a53ac-103">Buffer Application-Allocated</span><span class="sxs-lookup"><span data-stu-id="a53ac-103">Application-Allocated Buffer</span></span>

<span data-ttu-id="a53ac-104">Il \[ [**\_ numero di byte**](/windows/desktop/Midl/byte-count) dell'attributo ACF \] indica agli stub di usare un buffer preallocato non allocato o liberato dalle routine di supporto client.</span><span class="sxs-lookup"><span data-stu-id="a53ac-104">The ACF attribute \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] directs the stubs to use a preallocated buffer that is not allocated or freed by the client support routines.</span></span> <span data-ttu-id="a53ac-105">L' \[ **attributo \_ conteggio byte** \] viene applicato a un puntatore o a un parametro di matrice che punta al buffer.</span><span class="sxs-lookup"><span data-stu-id="a53ac-105">The \[**byte\_count**\] attribute is applied to a pointer or array parameter that points to the buffer.</span></span> <span data-ttu-id="a53ac-106">Richiede un parametro che specifica la dimensione del buffer in byte.</span><span class="sxs-lookup"><span data-stu-id="a53ac-106">It requires a parameter that specifies the buffer size in bytes.</span></span>

<span data-ttu-id="a53ac-107">L'area di memoria allocata dal client può contenere strutture di dati complesse con più puntatori.</span><span class="sxs-lookup"><span data-stu-id="a53ac-107">The client-allocated memory area can contain complex data structures with multiple pointers.</span></span> <span data-ttu-id="a53ac-108">Poiché l'area di memoria è contigua, l'applicazione non deve effettuare diverse chiamate per liberare singolarmente ogni puntatore e struttura.</span><span class="sxs-lookup"><span data-stu-id="a53ac-108">Because the memory area is contiguous, the application does not have to make several calls to free each pointer and structure individually.</span></span> <span data-ttu-id="a53ac-109">Come quando si usa l' \[ attributo [**allocate (tutti i \_ nodi)**](/windows/desktop/Midl/allocate) \] , l'area di memoria può essere allocata o liberata con una sola chiamata alla routine di allocazione della memoria o alla routine gratuita.</span><span class="sxs-lookup"><span data-stu-id="a53ac-109">As when using the \[[**allocate(all\_nodes)**](/windows/desktop/Midl/allocate)\] attribute, the memory area can be allocated or freed with one call to the memory-allocation routine or the free routine.</span></span> <span data-ttu-id="a53ac-110">Tuttavia, a differenza dell'attributo \[ **allocate (tutti i \_ nodi)** \] , il parametro buffer non viene gestito dallo stub client ma dall'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="a53ac-110">However, unlike using the \[**allocate(all\_nodes)**\] attribute, the buffer parameter is not managed by the client stub but by the client application.</span></span>

<span data-ttu-id="a53ac-111">Il buffer deve essere un \[ [](/windows/desktop/Midl/out-idl) \] parametro di sola uscita e la lunghezza del buffer in byte deve essere un \[ [](/windows/desktop/Midl/in) \] parametro solo in.</span><span class="sxs-lookup"><span data-stu-id="a53ac-111">The buffer must be an \[[**out**](/windows/desktop/Midl/out-idl)\]-only parameter and the buffer length in bytes must be an \[[**in**](/windows/desktop/Midl/in)\]-only parameter.</span></span> <span data-ttu-id="a53ac-112">L' \[ [**attributo \_ conteggio byte**](/windows/desktop/Midl/byte-count) \] può essere applicato solo ai tipi di puntatore.</span><span class="sxs-lookup"><span data-stu-id="a53ac-112">The \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] attribute can only be applied to pointer types.</span></span> <span data-ttu-id="a53ac-113">L' \[ attributo ACF **\_ count bytes** \] è un'estensione Microsoft per DCE IDL e, di conseguenza, non è disponibile se si esegue la compilazione con l'opzione MIDL [**/OSF**](/windows/desktop/Midl/-osf) .</span><span class="sxs-lookup"><span data-stu-id="a53ac-113">The \[**byte\_count**\] ACF attribute is a Microsoft extension to DCE IDL and, as such, is not available if you compile using the MIDL [**/osf**](/windows/desktop/Midl/-osf) switch.</span></span>

<span data-ttu-id="a53ac-114">Nell'esempio seguente il parametro *pRoot* usa il numero di byte:</span><span class="sxs-lookup"><span data-stu-id="a53ac-114">In the following example, the parameter *pRoot* uses byte count:</span></span>

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

<span data-ttu-id="a53ac-115">L' \[ [**attributo \_ conteggio byte**](/windows/desktop/Midl/byte-count) \] viene visualizzato in ACF come:</span><span class="sxs-lookup"><span data-stu-id="a53ac-115">The \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] attribute appears in the ACF as:</span></span>

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

<span data-ttu-id="a53ac-116">Lo stub client generato da questi file IDL e ACF non alloca o libera la memoria per questo buffer.</span><span class="sxs-lookup"><span data-stu-id="a53ac-116">The client stub generated from these IDL and ACF files does not allocate or free the memory for this buffer.</span></span> <span data-ttu-id="a53ac-117">Lo stub del server alloca e libera il buffer in una singola chiamata utilizzando il parametro di dimensione fornito.</span><span class="sxs-lookup"><span data-stu-id="a53ac-117">The server stub allocates and frees the buffer in a single call using the provided size parameter.</span></span> <span data-ttu-id="a53ac-118">Se i dati sono troppo grandi per le dimensioni del buffer specificate, viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="a53ac-118">If the data is too large for the specified buffer size, an exception is raised.</span></span>

 

 