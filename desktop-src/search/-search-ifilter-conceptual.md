---
description: Informazioni su come sviluppare gestori di filtri in Windows Search. La ricerca usa i filtri per estrarre gli elementi da includere in un indice full-text.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Sviluppo di gestori di filtri per Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa86c0a1e41ababf6f00db72a26784beb93e1879
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988860"
---
# <a name="developing-filter-handlers-for-windows-search"></a><span data-ttu-id="5b2fc-104">Sviluppo di gestori di filtri per Windows Search</span><span class="sxs-lookup"><span data-stu-id="5b2fc-104">Developing Filter Handlers for Windows Search</span></span>

<span data-ttu-id="5b2fc-105">Microsoft Windows Search i filtri per estrarre il contenuto degli elementi da includere in un indice full-text.</span><span class="sxs-lookup"><span data-stu-id="5b2fc-105">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="5b2fc-106">È possibile estendere Windows Search indicizzare tipi di file nuovi o proprietari scrivendo filtri per estrarre il contenuto e gestori di proprietà per estrarre le proprietà dei file.</span><span class="sxs-lookup"><span data-stu-id="5b2fc-106">You can extend Windows Search to index new or proprietary file types by writing filters to extract the content, and property handlers to extract the properties of files.</span></span>

<span data-ttu-id="5b2fc-107">Questa sezione fornisce il framework concettuale necessario per l'implementazione di un gestore di filtri (un'implementazione [**dell'interfaccia IFilter).**](/windows/win32/api/filter/nn-filter-ifilter)</span><span class="sxs-lookup"><span data-stu-id="5b2fc-107">This section provides the conceptual framework that is necessary for implementing a filter handler (an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface).</span></span>

- [<span data-ttu-id="5b2fc-108">Informazioni sui gestori di filtri in Windows Search</span><span class="sxs-lookup"><span data-stu-id="5b2fc-108">Understanding Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
- [<span data-ttu-id="5b2fc-109">Procedure consigliate per la creazione di gestori di filtri in Windows Search</span><span class="sxs-lookup"><span data-stu-id="5b2fc-109">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
- [<span data-ttu-id="5b2fc-110">Restituzione di proprietà da un gestore di filtri</span><span class="sxs-lookup"><span data-stu-id="5b2fc-110">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
- [<span data-ttu-id="5b2fc-111">Gestori di filtri forniti con Windows</span><span class="sxs-lookup"><span data-stu-id="5b2fc-111">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
- [<span data-ttu-id="5b2fc-112">Implementazione di gestori di filtri in Windows Search</span><span class="sxs-lookup"><span data-stu-id="5b2fc-112">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
- [<span data-ttu-id="5b2fc-113">Registrazione di gestori di filtri</span><span class="sxs-lookup"><span data-stu-id="5b2fc-113">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
- [<span data-ttu-id="5b2fc-114">Test dei gestori di filtri</span><span class="sxs-lookup"><span data-stu-id="5b2fc-114">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a><span data-ttu-id="5b2fc-115">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="5b2fc-115">Additional Resources</span></span>

- <span data-ttu-id="5b2fc-116">L'esempio di codice [IFilterSample,](-search-sample-ifiltersample.md) disponibile in [GitHub,](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)illustra come creare una classe di base IFilter per l'implementazione [**dell'interfaccia IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)</span><span class="sxs-lookup"><span data-stu-id="5b2fc-116">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="5b2fc-117">Per una panoramica del processo di indicizzazione, vedere [Processo di indicizzazione.](-search-indexing-process-overview.md)</span><span class="sxs-lookup"><span data-stu-id="5b2fc-117">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="5b2fc-118">Per una panoramica dei tipi di file, vedere [Tipi di file.](../shell/fa-file-types.md)</span><span class="sxs-lookup"><span data-stu-id="5b2fc-118">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="5b2fc-119">Per eseguire query su attributi di associazione di file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e Registrazione dell'applicazione.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5b2fc-119">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>
