---
description: Enumerazione di oggetti in un grafico di filtro
ms.assetid: 04a3dbc8-33c4-4b70-930e-686be2f8301f
title: Enumerazione di oggetti in un grafico di filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369cd3400d3b7fc9944662ed6d32fd67234af90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124407"
---
# <a name="enumerating-objects-in-a-filter-graph"></a><span data-ttu-id="43142-103">Enumerazione di oggetti in un grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="43142-103">Enumerating Objects in a Filter Graph</span></span>

<span data-ttu-id="43142-104">Un'applicazione potrebbe dover individuare un filtro particolare nel grafico del filtro o anche un particolare pin su un filtro.</span><span class="sxs-lookup"><span data-stu-id="43142-104">An application might need to locate a particular filter in the filter graph, or even a particular pin on a filter.</span></span> <span data-ttu-id="43142-105">Ad esempio, potrebbe utilizzare un'interfaccia esposta da un filtro specifico.</span><span class="sxs-lookup"><span data-stu-id="43142-105">For example, it might use an interface that a particular filter exposes.</span></span> <span data-ttu-id="43142-106">In alternativa, è possibile creare un grafico di filtro specializzato ed è necessario chiamare i metodi sui singoli pin per connettere i filtri.</span><span class="sxs-lookup"><span data-stu-id="43142-106">Or, it might construct a specialized filter graph and need to call methods on individual pins to connect the filters.</span></span> <span data-ttu-id="43142-107">A questo scopo, DirectShow fornisce diversi metodi per l'enumerazione degli oggetti in un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="43142-107">For this purpose, DirectShow provides several methods for enumerating objects in a filter graph.</span></span>

<span data-ttu-id="43142-108">Gli enumeratori descritti in questa sezione seguono il formato standard usato dalle interfacce di enumerazione COM.</span><span class="sxs-lookup"><span data-stu-id="43142-108">The enumerators discussed in this section follow the standard form used by COM enumeration interfaces.</span></span> <span data-ttu-id="43142-109">Per ulteriori informazioni, vedere l'argomento "IEnumXXXX" in Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="43142-109">For more information, see the "IEnumXXXX" topic in the Platform SDK.</span></span> <span data-ttu-id="43142-110">Per informazioni sull'enumerazione dei filtri registrati nel computer dell'utente, ma che non sono ancora presenti nel grafico di filtro, vedere [enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="43142-110">For information on enumerating filters that are registered on the user's computer, but aren't yet in the filter graph, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

<span data-ttu-id="43142-111">Questo articolo contiene gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="43142-111">This article contains the following topics:</span></span>

-   [<span data-ttu-id="43142-112">Enumerazione dei filtri</span><span class="sxs-lookup"><span data-stu-id="43142-112">Enumerating Filters</span></span>](enumerating-filters.md)
-   [<span data-ttu-id="43142-113">Enumerazione dei pin</span><span class="sxs-lookup"><span data-stu-id="43142-113">Enumerating Pins</span></span>](enumerating-pins.md)
-   [<span data-ttu-id="43142-114">Enumerazione dei tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="43142-114">Enumerating Media Types</span></span>](enumerating-media-types.md)

## <a name="related-topics"></a><span data-ttu-id="43142-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43142-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43142-116">Attività DirectShow di base</span><span class="sxs-lookup"><span data-stu-id="43142-116">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



