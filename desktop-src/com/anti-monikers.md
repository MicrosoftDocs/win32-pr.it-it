---
title: Anti-moniker
description: OLE fornisce un'implementazione di un tipo speciale di moniker denominato anti-moniker.
ms.assetid: 3b52d3bd-8375-4463-a0e3-5117fa96a1c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d69c461268b486a040b36f59108bc8e8379656
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044853"
---
# <a name="anti-monikers"></a><span data-ttu-id="e90c3-103">Anti-moniker</span><span class="sxs-lookup"><span data-stu-id="e90c3-103">Anti-Monikers</span></span>

<span data-ttu-id="e90c3-104">OLE fornisce un'implementazione di un tipo speciale di moniker denominato *anti-moniker*.</span><span class="sxs-lookup"><span data-stu-id="e90c3-104">OLE provides an implementation of a special type of moniker called an *anti-moniker*.</span></span> <span data-ttu-id="e90c3-105">Questo moniker viene usato nella creazione di nuove classi moniker.</span><span class="sxs-lookup"><span data-stu-id="e90c3-105">You use this moniker in the creation of new moniker classes.</span></span> <span data-ttu-id="e90c3-106">Viene usato come inverso del moniker su cui è composto, annullando in modo efficace tale moniker, nello stesso modo in cui l'operatore ".." sposta un livello di directory in un file system comando.</span><span class="sxs-lookup"><span data-stu-id="e90c3-106">You use it as the inverse of the moniker that it is composed onto, effectively canceling that moniker, in much the same way that the ".." operator moves up a directory level in a file system command.</span></span>

<span data-ttu-id="e90c3-107">È necessario avere un anti-moniker disponibile perché, una volta creato un moniker composito, non è possibile eliminare parti del moniker se, ad esempio, un oggetto viene spostato.</span><span class="sxs-lookup"><span data-stu-id="e90c3-107">It is necessary to have an anti-moniker available, because once a composite moniker is created, it is not possible to delete parts of the moniker if, for example, an object moves.</span></span> <span data-ttu-id="e90c3-108">Usare invece un anti-moniker per rimuovere una o più voci da un moniker composito.</span><span class="sxs-lookup"><span data-stu-id="e90c3-108">Instead, you use an anti-moniker to remove one or more entries from a composite moniker.</span></span>

<span data-ttu-id="e90c3-109">Gli anti-moniker sono una classe moniker destinata in modo esplicito all'uso come inverso.</span><span class="sxs-lookup"><span data-stu-id="e90c3-109">Anti-monikers are a moniker class explicitly intended for use as an inverse.</span></span> <span data-ttu-id="e90c3-110">COM definisce la funzione [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) denominata, che restituisce un anti-moniker.</span><span class="sxs-lookup"><span data-stu-id="e90c3-110">COM defines the named [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) function, which returns an anti-moniker.</span></span> <span data-ttu-id="e90c3-111">Questa funzione viene in genere usata per implementare il metodo [**IMoniker:: inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) .</span><span class="sxs-lookup"><span data-stu-id="e90c3-111">You generally use this function to implement the [**IMoniker::Inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) method.</span></span>

<span data-ttu-id="e90c3-112">Un anti-moniker è solo un inverso per i tipi di moniker implementati per considerare gli anti-moniker come inverso.</span><span class="sxs-lookup"><span data-stu-id="e90c3-112">An anti-moniker is only an inverse for those types of monikers that are implemented to treat anti-monikers as an inverse.</span></span> <span data-ttu-id="e90c3-113">Se ad esempio si vuole rimuovere l'ultima parte di un moniker composito, è consigliabile non creare un anti-moniker e componerlo alla fine del composto.</span><span class="sxs-lookup"><span data-stu-id="e90c3-113">For example, if you want to remove the last piece of a composite moniker, you should not create an anti-moniker and compose it to the end of the composite.</span></span> <span data-ttu-id="e90c3-114">Non è possibile assicurarsi che l'ultima parte del composito consideri un anti-moniker come inverso.</span><span class="sxs-lookup"><span data-stu-id="e90c3-114">You cannot be sure that the last piece of the composite considers an anti-moniker to be its inverse.</span></span> <span data-ttu-id="e90c3-115">Al contrario, è necessario chiamare [**IMoniker:: enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) sul moniker composito, specificando **false** come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="e90c3-115">Instead, you should call [**IMoniker::Enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) on the composite moniker, specifying **FALSE** as the first parameter.</span></span> <span data-ttu-id="e90c3-116">Viene creato un enumeratore che restituisce i moniker dei componenti in ordine inverso.</span><span class="sxs-lookup"><span data-stu-id="e90c3-116">This creates an enumerator that returns the component monikers in reverse order.</span></span> <span data-ttu-id="e90c3-117">Utilizzare l'enumeratore per recuperare l'ultima parte del composito e chiamare [**inverso**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) su tale moniker.</span><span class="sxs-lookup"><span data-stu-id="e90c3-117">Use the enumerator to retrieve the last piece of the composite, and call [**Inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) on that moniker.</span></span> <span data-ttu-id="e90c3-118">Il moniker restituito da **inverse** è quello necessario per rimuovere l'ultima parte del composto.</span><span class="sxs-lookup"><span data-stu-id="e90c3-118">The moniker returned by **Inverse** is what you need to remove the last piece of the composite.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e90c3-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e90c3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e90c3-120">Moniker della classe</span><span class="sxs-lookup"><span data-stu-id="e90c3-120">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="e90c3-121">Moniker compositi</span><span class="sxs-lookup"><span data-stu-id="e90c3-121">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="e90c3-122">Moniker di file</span><span class="sxs-lookup"><span data-stu-id="e90c3-122">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="e90c3-123">Moniker elemento</span><span class="sxs-lookup"><span data-stu-id="e90c3-123">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="e90c3-124">Moniker puntatore</span><span class="sxs-lookup"><span data-stu-id="e90c3-124">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




