---
description: Tecniche di Graph-Building generali
ms.assetid: 66d93305-175c-4549-b825-2f3d7fd6bf09
title: Tecniche di Graph-Building generali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c73a005f1fbf7af0a53f11d44d600852f88752
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225319"
---
# <a name="general-graph-building-techniques"></a><span data-ttu-id="a3ab7-103">Tecniche di Graph-Building generali</span><span class="sxs-lookup"><span data-stu-id="a3ab7-103">General Graph-Building Techniques</span></span>

<span data-ttu-id="a3ab7-104">Ogni applicazione DirectShow inizia con la creazione di un grafico a filtro.</span><span class="sxs-lookup"><span data-stu-id="a3ab7-104">Every DirectShow application starts by building a filter graph.</span></span> <span data-ttu-id="a3ab7-105">Quando si leggono gli argomenti della panoramica nella documentazione di DirectShow, si noterà che la maggior parte dei casi descrive il tipo di grafico filtro necessario.</span><span class="sxs-lookup"><span data-stu-id="a3ab7-105">As you read the overview topics in the DirectShow documentation, you will find that most start by describing what kind of filter graph you need.</span></span> <span data-ttu-id="a3ab7-106">In alcuni casi, è disponibile un metodo o un oggetto helper appositamente progettato per la compilazione di questo tipo di grafico.</span><span class="sxs-lookup"><span data-stu-id="a3ab7-106">In some cases, there is a method or a helper object specifically designed for building that type of graph.</span></span> <span data-ttu-id="a3ab7-107">Ad esempio, l'oggetto [Generatore di DVD Graph](dvd-graph-builder.md) compila i grafici di riproduzione DVD.</span><span class="sxs-lookup"><span data-stu-id="a3ab7-107">For example, the [DVD Graph Builder](dvd-graph-builder.md) object builds DVD playback graphs.</span></span> <span data-ttu-id="a3ab7-108">In altri casi, l'applicazione deve creare il grafico aggiungendo filtri e connetterli.</span><span class="sxs-lookup"><span data-stu-id="a3ab7-108">In other cases, the application must construct the graph by adding filters and connecting them.</span></span>

<span data-ttu-id="a3ab7-109">In questa sezione vengono presentate alcune funzioni helper che implementano operazioni di base per la creazione di grafici.</span><span class="sxs-lookup"><span data-stu-id="a3ab7-109">This section presents some helper functions that implement basic graph-building operations.</span></span> <span data-ttu-id="a3ab7-110">Possono essere usati da qualsiasi applicazione DirectShow che deve compilare o modificare un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="a3ab7-110">They can be used by any DirectShow application that needs to build or modify a filter graph.</span></span> <span data-ttu-id="a3ab7-111">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="a3ab7-111">This section contains the following topics:</span></span>

-   [<span data-ttu-id="a3ab7-112">Aggiungere un filtro in base al CLSID</span><span class="sxs-lookup"><span data-stu-id="a3ab7-112">Add a Filter by CLSID</span></span>](add-a-filter-by-clsid.md)
-   [<span data-ttu-id="a3ab7-113">Trovare un PIN non connesso in un filtro</span><span class="sxs-lookup"><span data-stu-id="a3ab7-113">Find an Unconnected Pin on a Filter</span></span>](find-an-unconnected-pin-on-a-filter.md)
-   [<span data-ttu-id="a3ab7-114">Connetti due filtri</span><span class="sxs-lookup"><span data-stu-id="a3ab7-114">Connect Two Filters</span></span>](connect-two-filters.md)
-   [<span data-ttu-id="a3ab7-115">Trovare un'interfaccia su un filtro o un pin</span><span class="sxs-lookup"><span data-stu-id="a3ab7-115">Find an Interface on a Filter or Pin</span></span>](find-an-interface-on-a-filter-or-pin.md)
-   [<span data-ttu-id="a3ab7-116">Trovare il peer di un filtro</span><span class="sxs-lookup"><span data-stu-id="a3ab7-116">Find a Filter's Peer</span></span>](find-a-filters-peer.md)
-   [<span data-ttu-id="a3ab7-117">Rimuovere tutti i filtri nel grafico</span><span class="sxs-lookup"><span data-stu-id="a3ab7-117">Remove All the Filters in the Graph</span></span>](remove-all-the-filters-in-the-graph.md)
-   [<span data-ttu-id="a3ab7-118">Creazione di grafici con il generatore di grafici di acquisizione</span><span class="sxs-lookup"><span data-stu-id="a3ab7-118">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a><span data-ttu-id="a3ab7-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3ab7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3ab7-120">Attività DirectShow di base</span><span class="sxs-lookup"><span data-stu-id="a3ab7-120">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="a3ab7-121">Enumerazione dei dispositivi e dei filtri</span><span class="sxs-lookup"><span data-stu-id="a3ab7-121">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="a3ab7-122">Enumerazione di oggetti in un grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="a3ab7-122">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="a3ab7-123">Connessione intelligente</span><span class="sxs-lookup"><span data-stu-id="a3ab7-123">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 



