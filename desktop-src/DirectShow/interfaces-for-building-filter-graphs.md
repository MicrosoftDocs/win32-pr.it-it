---
description: Interfacce per la compilazione di grafici di filtro
ms.assetid: 18d5217a-7f4e-49e9-ac14-2f4ba229e065
title: Interfacce per la compilazione di grafici di filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862d581f44a711cc6f2aa094210571995b15005b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746010"
---
# <a name="interfaces-for-building-filter-graphs"></a><span data-ttu-id="60130-103">Interfacce per la compilazione di grafici di filtro</span><span class="sxs-lookup"><span data-stu-id="60130-103">Interfaces for Building Filter Graphs</span></span>

<span data-ttu-id="60130-104">Le applicazioni utilizzano queste interfacce per creare vari tipi di grafici dei filtri.</span><span class="sxs-lookup"><span data-stu-id="60130-104">Applications use these interfaces to build various types of filter graphs.</span></span>



| <span data-ttu-id="60130-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="60130-105">Interface</span></span>                                                  | <span data-ttu-id="60130-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60130-106">Description</span></span>                                                 |
|------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="60130-107">**IAMFilterGraphCallback**</span><span class="sxs-lookup"><span data-stu-id="60130-107">**IAMFilterGraphCallback**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamfiltergraphcallback)   | <span data-ttu-id="60130-108">Ricevere notifiche di callback se non è possibile eseguire il rendering di un PIN.</span><span class="sxs-lookup"><span data-stu-id="60130-108">Receive callback notifications if a pin cannot be rendered.</span></span> |
| [<span data-ttu-id="60130-109">**IAMGraphBuilderCallback**</span><span class="sxs-lookup"><span data-stu-id="60130-109">**IAMGraphBuilderCallback**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) | <span data-ttu-id="60130-110">Fornisce un meccanismo di callback durante la compilazione del grafo.</span><span class="sxs-lookup"><span data-stu-id="60130-110">Provides a callback mechanism during graph building.</span></span>        |
| [<span data-ttu-id="60130-111">**ICaptureGraphBuilder2**</span><span class="sxs-lookup"><span data-stu-id="60130-111">**ICaptureGraphBuilder2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)     | <span data-ttu-id="60130-112">Grafici filtro compilazione per acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="60130-112">Build filter graphs for video capture.</span></span>                      |
| [<span data-ttu-id="60130-113">**ICreateDevEnum**</span><span class="sxs-lookup"><span data-stu-id="60130-113">**ICreateDevEnum**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)                   | <span data-ttu-id="60130-114">Enumerare i dispositivi di sistema, ad esempio i dispositivi di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="60130-114">Enumerate system devices, such as capture devices.</span></span>          |
| [<span data-ttu-id="60130-115">**IDvdGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="60130-115">**IDvdGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)               | <span data-ttu-id="60130-116">Crea grafici filtro per la navigazione e la riproduzione di DVD.</span><span class="sxs-lookup"><span data-stu-id="60130-116">Build filter graphs for DVD navigation and playback.</span></span>        |
| [<span data-ttu-id="60130-117">**IEnumFilters**</span><span class="sxs-lookup"><span data-stu-id="60130-117">**IEnumFilters**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ienumfilters)                       | <span data-ttu-id="60130-118">Enumerare i filtri nel grafico.</span><span class="sxs-lookup"><span data-stu-id="60130-118">Enumerate the filters in the graph.</span></span>                         |
| [<span data-ttu-id="60130-119">**IFilterGraph2**</span><span class="sxs-lookup"><span data-stu-id="60130-119">**IFilterGraph2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)                     | <span data-ttu-id="60130-120">Aggiunta, rimozione o connessione dei filtri.</span><span class="sxs-lookup"><span data-stu-id="60130-120">Add, remove, or connect filters.</span></span>                            |
| [<span data-ttu-id="60130-121">**IFilterMapper2**</span><span class="sxs-lookup"><span data-stu-id="60130-121">**IFilterMapper2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)                   | <span data-ttu-id="60130-122">Enumerare i filtri registrati nel sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="60130-122">Enumerate the filters registered on the user's system.</span></span>      |
| [<span data-ttu-id="60130-123">**IGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="60130-123">**IGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)                     | <span data-ttu-id="60130-124">Crea grafici filtro per la riproduzione di file o per usi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="60130-124">Build filter graphs for file playback or for custom uses.</span></span>   |
| [<span data-ttu-id="60130-125">**IGraphConfig**</span><span class="sxs-lookup"><span data-stu-id="60130-125">**IGraphConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)                       | <span data-ttu-id="60130-126">Riconfigurare dinamicamente un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="60130-126">Dynamically reconfigure a filter graph.</span></span>                     |
| [<span data-ttu-id="60130-127">**IGraphVersion**</span><span class="sxs-lookup"><span data-stu-id="60130-127">**IGraphVersion**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphversion)                     | <span data-ttu-id="60130-128">Determinare quando il grafico viene modificato.</span><span class="sxs-lookup"><span data-stu-id="60130-128">Determine when the graph changes.</span></span>                           |



 

 

 



