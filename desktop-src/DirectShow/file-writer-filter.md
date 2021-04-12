---
description: Filtro del writer di file
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Filtro del writer di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f438f13f8d63b2856efd147c57ba6f071af26ff8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225465"
---
# <a name="file-writer-filter"></a><span data-ttu-id="b1256-103">Filtro del writer di file</span><span class="sxs-lookup"><span data-stu-id="b1256-103">File Writer Filter</span></span>

<span data-ttu-id="b1256-104">Il filtro del writer di file può essere usato per scrivere file su disco indipendentemente dal formato.</span><span class="sxs-lookup"><span data-stu-id="b1256-104">The File Writer filter can be used to write files to disc regardless of format.</span></span> <span data-ttu-id="b1256-105">Il filtro scrive semplicemente nel disco tutto ciò che riceve sul pin di input, quindi deve essere collegato a un multiplexer in grado di formattare il file in modo corretto.</span><span class="sxs-lookup"><span data-stu-id="b1256-105">The filter simply writes to disc whatever it receives on its input pin, so it must be connected upstream to a multiplexer that can format the file correctly.</span></span> <span data-ttu-id="b1256-106">È possibile creare un nuovo file di output con il writer di file o specificare un file esistente. Se il file esiste già, verrà completamente sovrascritto con i nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="b1256-106">You can create a new output file with the File Writer or specify an existing file; if the file already exists, it will be completely overwritten with the new data.</span></span>

<span data-ttu-id="b1256-107">Il filtro del writer di file usa i timestamp del flusso di input come offset del file e fornisce l'accesso casuale al file.</span><span class="sxs-lookup"><span data-stu-id="b1256-107">The file writer filter uses the input stream's time stamps as file offsets and provides random access to the file.</span></span> <span data-ttu-id="b1256-108">Supporta **IStream** per consentire la lettura e la scrittura dell'intestazione del file dopo l'arresto del grafo.</span><span class="sxs-lookup"><span data-stu-id="b1256-108">It supports **IStream** to allow reading and writing the file header after the graph is stopped.</span></span> <span data-ttu-id="b1256-109">Per migliorare le prestazioni, supporta anche le scritture sovrapposte senza buffer e gestisce la negoziazione del buffer corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b1256-109">To improve performance it also supports unbuffered overlapped writes and handles the corresponding buffer negotiation.</span></span>

> [!Note]  
> <span data-ttu-id="b1256-110">Per scrivere file ASF, usare il filtro [WM ASF Writer](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="b1256-110">To write ASF files, use the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

 



|                                          |                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1256-111">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="b1256-111">Filter Interfaces</span></span>                        | <span data-ttu-id="b1256-112">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="b1256-112">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span></span> |
| <span data-ttu-id="b1256-113">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="b1256-113">Input Pin Media Types</span></span>                    | <span data-ttu-id="b1256-114">\_Flusso MEDIATYPE, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="b1256-114">MEDIATYPE\_Stream, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                              |
| <span data-ttu-id="b1256-115">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="b1256-115">Input Pin Interfaces</span></span>                     | <span data-ttu-id="b1256-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span><span class="sxs-lookup"><span data-stu-id="b1256-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span></span>                                                                                |
| <span data-ttu-id="b1256-117">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="b1256-117">Output Pin Media Types</span></span>                   | <span data-ttu-id="b1256-118">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="b1256-118">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="b1256-119">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="b1256-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="b1256-120">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="b1256-120">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="b1256-121">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="b1256-121">Filter CLSID</span></span>                             | <span data-ttu-id="b1256-122">CLSID \_ FileWriter</span><span class="sxs-lookup"><span data-stu-id="b1256-122">CLSID\_FileWriter</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="b1256-123">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="b1256-123">Property Page CLSID</span></span>                      | <span data-ttu-id="b1256-124">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="b1256-124">No property page</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="b1256-125">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="b1256-125">Executable</span></span>                               | <span data-ttu-id="b1256-126">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="b1256-126">qcap.dll</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="b1256-127">Merito</span><span class="sxs-lookup"><span data-stu-id="b1256-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="b1256-128">il merito non viene \_ \_ \_ utilizzato</span><span class="sxs-lookup"><span data-stu-id="b1256-128">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="b1256-129">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="b1256-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="b1256-130">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="b1256-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="b1256-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1256-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1256-132">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="b1256-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



