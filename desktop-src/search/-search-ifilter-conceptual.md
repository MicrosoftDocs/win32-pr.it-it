---
description: Microsoft Windows Search USA i filtri per estrarre il contenuto degli elementi da includere in un indice full-text.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Sviluppo di gestori di filtri per la ricerca di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8f45892549dc3f392824c31c78884b209d283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049387"
---
# <a name="developing-filter-handlers-for-windows-search"></a><span data-ttu-id="4fdf6-103">Sviluppo di gestori di filtri per la ricerca di Windows</span><span class="sxs-lookup"><span data-stu-id="4fdf6-103">Developing Filter Handlers for Windows Search</span></span>

<span data-ttu-id="4fdf6-104">Microsoft Windows Search USA i filtri per estrarre il contenuto degli elementi da includere in un indice full-text.</span><span class="sxs-lookup"><span data-stu-id="4fdf6-104">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="4fdf6-105">È possibile estendere la ricerca di Windows per indicizzare i tipi di file nuovi o proprietari scrivendo i filtri per estrarre il contenuto e i gestori delle proprietà per estrarre le proprietà dei file.</span><span class="sxs-lookup"><span data-stu-id="4fdf6-105">You can extend Windows Search to index new or proprietary file types by writing filters to extract the content, and property handlers to extract the properties of files.</span></span>

<span data-ttu-id="4fdf6-106">In questa sezione viene fornito il framework concettuale necessario per l'implementazione di un gestore di filtri, ovvero un'implementazione dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="4fdf6-106">This section provides the conceptual framework that is necessary for implementing a filter handler (an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface).</span></span>

- [<span data-ttu-id="4fdf6-107">Informazioni sui gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="4fdf6-107">Understanding Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
- [<span data-ttu-id="4fdf6-108">Procedure consigliate per la creazione di gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="4fdf6-108">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
- [<span data-ttu-id="4fdf6-109">Restituzione di proprietà da un gestore di filtro</span><span class="sxs-lookup"><span data-stu-id="4fdf6-109">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
- [<span data-ttu-id="4fdf6-110">Gestori di filtri forniti con Windows</span><span class="sxs-lookup"><span data-stu-id="4fdf6-110">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
- [<span data-ttu-id="4fdf6-111">Implementazione di gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="4fdf6-111">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
- [<span data-ttu-id="4fdf6-112">Registrazione di gestori di filtro</span><span class="sxs-lookup"><span data-stu-id="4fdf6-112">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
- [<span data-ttu-id="4fdf6-113">Test di gestori filtro</span><span class="sxs-lookup"><span data-stu-id="4fdf6-113">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a><span data-ttu-id="4fdf6-114">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="4fdf6-114">Additional Resources</span></span>

- <span data-ttu-id="4fdf6-115">Nell'esempio di codice [IFilterSample](-search-sample-ifiltersample.md) , disponibile in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), viene illustrato come creare una classe di base IFilter per implementare l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="4fdf6-115">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="4fdf6-116">Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4fdf6-116">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="4fdf6-117">Per una panoramica dei tipi di file, vedere [tipi di file](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="4fdf6-117">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="4fdf6-118">Per eseguire query sugli attributi di associazione file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e registrazione dell'applicazione](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4fdf6-118">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>
