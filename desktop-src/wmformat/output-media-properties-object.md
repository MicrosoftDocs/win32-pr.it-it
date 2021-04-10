---
title: Oggetto proprietà supporti di output
description: Oggetto proprietà supporti di output
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- Windows Media Format SDK, oggetti proprietà supporti di output
- ASF (Advanced Systems Format), oggetti proprietà dei supporti di output
- ASF (Advanced Systems Format), oggetti proprietà dei supporti di output
- oggetti, oggetti proprietà dei supporti di output
- oggetti proprietà supporti di output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61490464381a0b4e58be7994dfaeb0dfec2baa76
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046440"
---
# <a name="output-media-properties-object"></a><span data-ttu-id="2b703-108">Oggetto proprietà supporti di output</span><span class="sxs-lookup"><span data-stu-id="2b703-108">Output Media Properties Object</span></span>

<span data-ttu-id="2b703-109">Un oggetto proprietà del supporto di output viene usato per recuperare e impostare una proprietà di output.</span><span class="sxs-lookup"><span data-stu-id="2b703-109">An output media properties object is used to retrieve and set an output property.</span></span> <span data-ttu-id="2b703-110">Gli oggetti proprietà del supporto di output vengono creati per i formati di output supportati dei flussi in un file caricato in un oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="2b703-110">Output media properties objects are created for supported output formats of streams in a file that is loaded into a reader object.</span></span> <span data-ttu-id="2b703-111">Per i flussi compressi, le proprietà di output sono determinate dai possibili output del codec di decompressione.</span><span class="sxs-lookup"><span data-stu-id="2b703-111">For compressed streams, the output properties are determined by the possible outputs of the decompressing codec.</span></span>

<span data-ttu-id="2b703-112">Un oggetto proprietà del supporto di output viene creato da [**IWMReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) questo metodo crea un oggetto proprietà del supporto di output che contiene le proprietà del formato di output predefinito.</span><span class="sxs-lookup"><span data-stu-id="2b703-112">An output media properties object is created by [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) This method creates an output media properties object that contains the properties of the default output format.</span></span> <span data-ttu-id="2b703-113">Altri formati possono essere supportati per un output.</span><span class="sxs-lookup"><span data-stu-id="2b703-113">Other formats may be supported for an output.</span></span> <span data-ttu-id="2b703-114">Per ottenere formati di output aggiuntivi, è possibile chiamare [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) per ottenere il numero di formati di output supportati e quindi eseguirne il ciclo usando le chiamate a [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat).</span><span class="sxs-lookup"><span data-stu-id="2b703-114">To obtain additional output formats, you can call [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) to get the number of supported output formats and then loop through them using calls to [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat).</span></span> <span data-ttu-id="2b703-115">**GetOutputFormat** crea un oggetto proprietà del supporto di output popolato con i dati per il formato di output selezionato.</span><span class="sxs-lookup"><span data-stu-id="2b703-115">**GetOutputFormat** creates an output media properties object populated with the data for the selected output format.</span></span>

<span data-ttu-id="2b703-116">Gli oggetti proprietà del supporto di output possono anche essere creati con il lettore sincrono.</span><span class="sxs-lookup"><span data-stu-id="2b703-116">Output media properties objects can also be created with the synchronous reader.</span></span> <span data-ttu-id="2b703-117">Tutti i nomi dei metodi sono identici a quelli del lettore e sono tutti esposti dall'interfaccia [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .</span><span class="sxs-lookup"><span data-stu-id="2b703-117">All of the method names are identical to those in the reader and they are all exposed by the [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) interface.</span></span>

<span data-ttu-id="2b703-118">**GetOutputProps** e **GetOutputFormat** impostano entrambi un puntatore a un'interfaccia [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) .</span><span class="sxs-lookup"><span data-stu-id="2b703-118">**GetOutputProps** and **GetOutputFormat** both set a pointer to an [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface.</span></span> <span data-ttu-id="2b703-119">Le altre interfacce dell'oggetto proprietà del supporto di output possono essere ottenute chiamando il metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="2b703-119">The other interfaces of the output media properties object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="2b703-120">Le interfacce seguenti sono supportate da ogni oggetto proprietà del supporto di output.</span><span class="sxs-lookup"><span data-stu-id="2b703-120">The following interfaces are supported by every output media properties object.</span></span>



| <span data-ttu-id="2b703-121">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="2b703-121">Interface</span></span>                                          | <span data-ttu-id="2b703-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b703-122">Description</span></span>                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b703-123">**IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="2b703-123">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | <span data-ttu-id="2b703-124">Usato come interfaccia di base per le altre interfacce di proprietà del supporto (input, output e video).</span><span class="sxs-lookup"><span data-stu-id="2b703-124">Used as the base interface for the other media-property interfaces (input, output, and video).</span></span>             |
| [<span data-ttu-id="2b703-125">**IWMOutputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="2b703-125">**IWMOutputMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | <span data-ttu-id="2b703-126">Recupera le proprietà di un output.</span><span class="sxs-lookup"><span data-stu-id="2b703-126">Retrieves the properties of an output.</span></span>                                                                     |
| [<span data-ttu-id="2b703-127">**IWMVideoMediaProps**</span><span class="sxs-lookup"><span data-stu-id="2b703-127">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | <span data-ttu-id="2b703-128">Gestisce le proprietà di un flusso video.</span><span class="sxs-lookup"><span data-stu-id="2b703-128">Manages the properties of a video stream.</span></span> <span data-ttu-id="2b703-129">Si tratta di un'interfaccia facoltativa, disponibile solo per i flussi video.</span><span class="sxs-lookup"><span data-stu-id="2b703-129">This is an optional interface, available only for video streams.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2b703-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b703-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b703-131">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="2b703-131">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="2b703-132">**Oggetto Lettore**</span><span class="sxs-lookup"><span data-stu-id="2b703-132">**Reader Object**</span></span>](reader-object.md)
</dt> </dl>

 

 




