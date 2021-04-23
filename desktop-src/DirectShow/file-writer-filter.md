---
description: Filtro writer file
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Filtro writer file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991536d505ee1bdfcaaaca5ce8660c4480decf6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909689"
---
# <a name="file-writer-filter"></a><span data-ttu-id="77586-103">Filtro writer file</span><span class="sxs-lookup"><span data-stu-id="77586-103">File Writer Filter</span></span>

<span data-ttu-id="77586-104">Il filtro Writer file può essere usato per scrivere file su disco indipendentemente dal formato.</span><span class="sxs-lookup"><span data-stu-id="77586-104">The File Writer filter can be used to write files to disc regardless of format.</span></span> <span data-ttu-id="77586-105">Il filtro scrive semplicemente su disco tutto ciò che riceve sul pin di input, quindi deve essere connesso upstream a un multiplexer in grado di formattare correttamente il file.</span><span class="sxs-lookup"><span data-stu-id="77586-105">The filter simply writes to disc whatever it receives on its input pin, so it must be connected upstream to a multiplexer that can format the file correctly.</span></span> <span data-ttu-id="77586-106">È possibile creare un nuovo file di output con il writer di file o specificare un file esistente. Se il file esiste già, verrà sovrascritto completamente con i nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="77586-106">You can create a new output file with the File Writer or specify an existing file; if the file already exists, it will be completely overwritten with the new data.</span></span>

<span data-ttu-id="77586-107">Il filtro del writer di file usa i timestamp del flusso di input come offset di file e fornisce l'accesso casuale al file.</span><span class="sxs-lookup"><span data-stu-id="77586-107">The file writer filter uses the input stream's time stamps as file offsets and provides random access to the file.</span></span> <span data-ttu-id="77586-108">Supporta **IStream** per consentire la lettura e la scrittura dell'intestazione del file dopo l'arresto del grafo.</span><span class="sxs-lookup"><span data-stu-id="77586-108">It supports **IStream** to allow reading and writing the file header after the graph is stopped.</span></span> <span data-ttu-id="77586-109">Per migliorare le prestazioni, supporta anche scritture sovrapposte senza buffer e gestisce la negoziazione del buffer corrispondente.</span><span class="sxs-lookup"><span data-stu-id="77586-109">To improve performance it also supports unbuffered overlapped writes and handles the corresponding buffer negotiation.</span></span>

> [!Note]  
> <span data-ttu-id="77586-110">Per scrivere file ASF, usare il [filtro WM ASF Writer.](wm-asf-writer-filter.md)</span><span class="sxs-lookup"><span data-stu-id="77586-110">To write ASF files, use the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

 



| <span data-ttu-id="77586-111">Label</span><span class="sxs-lookup"><span data-stu-id="77586-111">Label</span></span> | <span data-ttu-id="77586-112">Valore</span><span class="sxs-lookup"><span data-stu-id="77586-112">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77586-113">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="77586-113">Filter Interfaces</span></span>                        | <span data-ttu-id="77586-114">[**IAMFilterMiscFlags,**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSinkFilter,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) [**IFileSinkFilter2,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2) **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="77586-114">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span></span> |
| <span data-ttu-id="77586-115">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="77586-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="77586-116">Flusso \_ MEDIATYPE, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="77586-116">MEDIATYPE\_Stream, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                              |
| <span data-ttu-id="77586-117">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="77586-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="77586-118">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span><span class="sxs-lookup"><span data-stu-id="77586-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span></span>                                                                                |
| <span data-ttu-id="77586-119">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="77586-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="77586-120">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="77586-120">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="77586-121">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="77586-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="77586-122">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="77586-122">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="77586-123">CLSID del filtro</span><span class="sxs-lookup"><span data-stu-id="77586-123">Filter CLSID</span></span>                             | <span data-ttu-id="77586-124">CLSID \_ FileWriter</span><span class="sxs-lookup"><span data-stu-id="77586-124">CLSID\_FileWriter</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="77586-125">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="77586-125">Property Page CLSID</span></span>                      | <span data-ttu-id="77586-126">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="77586-126">No property page</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="77586-127">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="77586-127">Executable</span></span>                               | <span data-ttu-id="77586-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="77586-128">qcap.dll</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="77586-129">Merito</span><span class="sxs-lookup"><span data-stu-id="77586-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="77586-130">MERITO \_ NON \_ \_ USARE</span><span class="sxs-lookup"><span data-stu-id="77586-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="77586-131">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="77586-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="77586-132">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="77586-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="77586-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77586-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77586-134">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="77586-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



