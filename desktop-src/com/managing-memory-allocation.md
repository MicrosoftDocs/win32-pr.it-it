---
title: Gestione dell'allocazione di memoria
description: Gestione dell'allocazione di memoria
ms.assetid: 8a189fe8-5555-44bb-968b-04408fa7fce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2af04b4ecc5b8480230b17ae710b84ce8e6ce5d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399798"
---
# <a name="managing-memory-allocation"></a><span data-ttu-id="909fb-103">Gestione dell'allocazione di memoria</span><span class="sxs-lookup"><span data-stu-id="909fb-103">Managing Memory Allocation</span></span>

<span data-ttu-id="909fb-104">In COM, molti, se non più, i metodi di interfaccia vengono chiamati dal codice scritto da un'organizzazione di programmazione e implementati dal codice scritto da un altro.</span><span class="sxs-lookup"><span data-stu-id="909fb-104">In COM, many, if not most, interface methods are called by code written by one programming organization and implemented by code written by another.</span></span> <span data-ttu-id="909fb-105">Molti dei parametri e i valori restituiti di queste funzioni sono di tipo che può essere passato in base al valore.</span><span class="sxs-lookup"><span data-stu-id="909fb-105">Many of the parameters and return values of these functions are of types that can be passed around by value.</span></span> <span data-ttu-id="909fb-106">In alcuni casi, tuttavia, è necessario passare strutture di dati per le quali questo non è il caso, pertanto è necessario sia per il chiamante che per chiamare per avere un criterio di allocazione e deallocazione compatibile.</span><span class="sxs-lookup"><span data-stu-id="909fb-106">Sometimes, however, it is necessary to pass data structures for which this is not the case, so it is necessary for both caller and called to have a compatible allocation and de-allocation policy.</span></span> <span data-ttu-id="909fb-107">COM definisce una convenzione universale per l'allocazione di memoria, perché è più ragionevole rispetto alla definizione di regole maiuscole/minuscole e in modo che l'implementazione della chiamata di procedura remota COM possa gestire correttamente la memoria.</span><span class="sxs-lookup"><span data-stu-id="909fb-107">COM defines a universal convention for memory allocation, because it is more reasonable than defining case-by-case rules and so that the COM remote procedure call implementation can correctly manage memory.</span></span>

<span data-ttu-id="909fb-108">I metodi di un'interfaccia COM forniscono sempre la gestione della memoria dei puntatori all'interfaccia chiamando le funzioni [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) disponibili nell'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , da cui derivano tutte le altre interfacce com.</span><span class="sxs-lookup"><span data-stu-id="909fb-108">The methods of a COM interface always provide memory management of pointers to the interface by calling the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) functions found in the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, from which all other COM interfaces derive.</span></span> <span data-ttu-id="909fb-109">Per ulteriori informazioni, vedere [regole per la gestione dei conteggi dei riferimenti](rules-for-managing-reference-counts.md) .</span><span class="sxs-lookup"><span data-stu-id="909fb-109">(See [Rules for Managing Reference Counts](rules-for-managing-reference-counts.md) for more information.)</span></span>

<span data-ttu-id="909fb-110">In questa sezione viene descritto solo come allocare memoria per i parametri che non vengono passati per valore, non per i puntatori alle interfacce, ma più banali come le stringhe, i puntatori alle strutture e così via.</span><span class="sxs-lookup"><span data-stu-id="909fb-110">This section describes only how to allocate memory for parameters that are not passed by value — not pointers to interfaces, but more mundane things like strings, pointers to structures, and so forth.</span></span>

<span data-ttu-id="909fb-111">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="909fb-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="909fb-112">Allocatore di memoria OLE</span><span class="sxs-lookup"><span data-stu-id="909fb-112">The OLE Memory Allocator</span></span>](the-ole-memory-allocator.md)
-   [<span data-ttu-id="909fb-113">Regole di gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="909fb-113">Memory Management Rules</span></span>](memory-management-rules.md)
-   [<span data-ttu-id="909fb-114">Debug delle allocazioni di memoria</span><span class="sxs-lookup"><span data-stu-id="909fb-114">Debugging Memory Allocations</span></span>](debugging-memory-allocations.md)

 

 