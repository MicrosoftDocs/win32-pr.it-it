---
description: Simulazione della creazione di grafici con GraphEdit
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: Simulazione della creazione di grafici con GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76878997c873c74d454979ccda689a9c241489d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481965"
---
# <a name="simulating-graph-building-with-graphedit"></a><span data-ttu-id="3e003-103">Simulazione della creazione di grafici con GraphEdit</span><span class="sxs-lookup"><span data-stu-id="3e003-103">Simulating Graph Building with GraphEdit</span></span>

<span data-ttu-id="3e003-104">DirectShow fornisce un'utilità di debug denominata GraphEdit, che è possibile utilizzare per creare e testare i grafici dei filtri.</span><span class="sxs-lookup"><span data-stu-id="3e003-104">DirectShow provides a debugging utility called GraphEdit, which you can use to create and test filter graphs.</span></span>

<span data-ttu-id="3e003-105">GraphEdit è uno strumento visivo per la creazione di grafici di filtro.</span><span class="sxs-lookup"><span data-stu-id="3e003-105">GraphEdit is a visual tool for building filter graphs.</span></span> <span data-ttu-id="3e003-106">Con GraphEdit è possibile sperimentare un grafico di filtro prima di scrivere il codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3e003-106">With GraphEdit, you can experiment with a filter graph before you write any application code.</span></span> <span data-ttu-id="3e003-107">È anche possibile caricare un grafico di filtro creato dall'applicazione per verificare che l'applicazione stia creando il grafo corretto.</span><span class="sxs-lookup"><span data-stu-id="3e003-107">You can also load a filter graph that your application creates, to verify that your application is building the correct graph.</span></span> <span data-ttu-id="3e003-108">Se si sviluppa un filtro personalizzato, GraphEdit offre un modo rapido per testarlo: è sufficiente caricare un grafo con il filtro personalizzato e provare a eseguire il grafo.</span><span class="sxs-lookup"><span data-stu-id="3e003-108">If you develop a custom filter, GraphEdit provides a quick way to test it: Simply load a graph with your custom filter and try running the graph.</span></span> <span data-ttu-id="3e003-109">Se non si ha familiarità con DirectShow, GraphEdit è un modo efficace per acquisire familiarità con i grafici di filtro e l'architettura DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3e003-109">If you are new to DirectShow, GraphEdit is a good way to become familiar with filter graphs and the DirectShow architecture.</span></span>

<span data-ttu-id="3e003-110">Nella figura seguente viene illustrato come GraphEdit rappresenta un semplice grafico a filtro.</span><span class="sxs-lookup"><span data-stu-id="3e003-110">The following illustration shows how GraphEdit represents a simple filter graph.</span></span>

![grafico a filtro semplice in GraphEdit](images/gedit09.png)

<span data-ttu-id="3e003-112">Ogni filtro è rappresentato come rettangolo.</span><span class="sxs-lookup"><span data-stu-id="3e003-112">Each filter is represented as a rectangle.</span></span> <span data-ttu-id="3e003-113">I quadrati più piccoli lungo i bordi dei filtri rappresentano i pin.</span><span class="sxs-lookup"><span data-stu-id="3e003-113">Smaller squares along the edges of the filters represent pins.</span></span> <span data-ttu-id="3e003-114">I pin di input si trovano sul lato sinistro del filtro e i pin di output si trovano sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="3e003-114">Input pins are on the left side of the filter, and output pins are on the right side.</span></span> <span data-ttu-id="3e003-115">Le frecce rappresentano le connessioni tra i pin.</span><span class="sxs-lookup"><span data-stu-id="3e003-115">The arrows represent the connections between pins.</span></span>

<span data-ttu-id="3e003-116">Con GraphEdit è possibile:</span><span class="sxs-lookup"><span data-stu-id="3e003-116">With GraphEdit, you can:</span></span>

-   <span data-ttu-id="3e003-117">Creare e modificare i grafici di filtro usando un'interfaccia visiva, con trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="3e003-117">Create and modify filter graphs using a visual, drag-and-drop interface.</span></span>
-   <span data-ttu-id="3e003-118">Simula le chiamate a livello di codice per la compilazione di un grafico.</span><span class="sxs-lookup"><span data-stu-id="3e003-118">Simulate programmatic calls to build a graph.</span></span>
-   <span data-ttu-id="3e003-119">Eseguire, sospendere, arrestare e cercare un grafo.</span><span class="sxs-lookup"><span data-stu-id="3e003-119">Run, pause, stop, and seek a graph.</span></span>
-   <span data-ttu-id="3e003-120">Vedere quali filtri sono registrati nel computer e visualizzare le informazioni del registro di sistema per ogni filtro.</span><span class="sxs-lookup"><span data-stu-id="3e003-120">See what filters are registered on your computer, and view registry information for each filter.</span></span>
-   <span data-ttu-id="3e003-121">Visualizzare le pagine delle proprietà del filtro.</span><span class="sxs-lookup"><span data-stu-id="3e003-121">View filter property pages.</span></span>
-   <span data-ttu-id="3e003-122">Visualizzare i tipi di supporto delle connessioni pin.</span><span class="sxs-lookup"><span data-stu-id="3e003-122">View the media types of pin connections.</span></span>

<span data-ttu-id="3e003-123">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="3e003-123">This section contains the following topics:</span></span>

-   [<span data-ttu-id="3e003-124">Uso di GraphEdit</span><span class="sxs-lookup"><span data-stu-id="3e003-124">Using GraphEdit</span></span>](using-graphedit.md)
-   [<span data-ttu-id="3e003-125">Caricamento di un grafico da un processo esterno</span><span class="sxs-lookup"><span data-stu-id="3e003-125">Loading a Graph From an External Process</span></span>](loading-a-graph-from-an-external-process.md)
-   [<span data-ttu-id="3e003-126">Salvataggio di un grafico di filtro in un file GraphEdit</span><span class="sxs-lookup"><span data-stu-id="3e003-126">Saving a Filter Graph to a GraphEdit File</span></span>](saving-a-filter-graph-to-a-graphedit-file.md)
-   [<span data-ttu-id="3e003-127">Caricamento di un file GraphEdit a livello di codice</span><span class="sxs-lookup"><span data-stu-id="3e003-127">Loading a GraphEdit File Programmatically</span></span>](loading-a-graphedit-file-programmatically.md)
-   [<span data-ttu-id="3e003-128">Formato di file GraphEdit</span><span class="sxs-lookup"><span data-stu-id="3e003-128">GraphEdit File Format</span></span>](graphedit-file-format.md)

## <a name="related-topics"></a><span data-ttu-id="3e003-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3e003-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e003-130">Uso di DirectShow</span><span class="sxs-lookup"><span data-stu-id="3e003-130">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



