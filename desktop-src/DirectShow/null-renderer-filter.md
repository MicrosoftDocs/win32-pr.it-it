---
description: Il filtro Renderer Null è un renderer che rimuove ogni campione ricevuto, senza visualizzare o eseguire il rendering dei dati di esempio.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: Filtro renderer Null (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Null Renderer Filter
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 64647cbcbcc836c400890fb173a29c76f8723029
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908809"
---
# <a name="null-renderer-filter"></a><span data-ttu-id="60115-103">Filtro renderer Null</span><span class="sxs-lookup"><span data-stu-id="60115-103">Null Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="60115-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="60115-104">\[Deprecated.</span></span> <span data-ttu-id="60115-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="60115-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="60115-106">Il filtro Renderer Null è un renderer che rimuove ogni campione ricevuto, senza visualizzare o eseguire il rendering dei dati di esempio.</span><span class="sxs-lookup"><span data-stu-id="60115-106">The Null Renderer filter is a renderer that discards every sample it receives, without displaying or rendering the sample data.</span></span>



| <span data-ttu-id="60115-107">Label</span><span class="sxs-lookup"><span data-stu-id="60115-107">Label</span></span> | <span data-ttu-id="60115-108">Valore</span><span class="sxs-lookup"><span data-stu-id="60115-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60115-109">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="60115-109">Filter interfaces</span></span>                        | <span data-ttu-id="60115-110">[**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="60115-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span> |
| <span data-ttu-id="60115-111">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="60115-111">Input pin media types</span></span>                    | <span data-ttu-id="60115-112">Qualsiasi tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="60115-112">Any media type</span></span>                                                                                                       |
| <span data-ttu-id="60115-113">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="60115-113">Input pin interfaces</span></span>                     | <span data-ttu-id="60115-114">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="60115-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>               |
| <span data-ttu-id="60115-115">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="60115-115">Output pin media types</span></span>                   | <span data-ttu-id="60115-116">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="60115-116">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="60115-117">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="60115-117">Output pin interfaces</span></span>                    | <span data-ttu-id="60115-118">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="60115-118">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="60115-119">Filtro CLSID</span><span class="sxs-lookup"><span data-stu-id="60115-119">Filter CLSID</span></span>                             | <span data-ttu-id="60115-120">CLSID \_ NullRenderer</span><span class="sxs-lookup"><span data-stu-id="60115-120">CLSID\_NullRenderer</span></span>                                                                                                  |
| <span data-ttu-id="60115-121">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="60115-121">Property Page CLSID</span></span>                      | <span data-ttu-id="60115-122">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="60115-122">No property page.</span></span>                                                                                                    |
| <span data-ttu-id="60115-123">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="60115-123">Executable</span></span>                               | <span data-ttu-id="60115-124">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="60115-124">Qedit.dll</span></span>                                                                                                            |
| [<span data-ttu-id="60115-125">Merito</span><span class="sxs-lookup"><span data-stu-id="60115-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="60115-126">NON \_ \_ USARE \_</span><span class="sxs-lookup"><span data-stu-id="60115-126">MERIT\_DO\_NOT\_USE</span></span>                                                                                                  |
| [<span data-ttu-id="60115-127">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="60115-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="60115-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="60115-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="60115-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="60115-129">Remarks</span></span>

<span data-ttu-id="60115-130">Usare questo filtro quando un segnaposto di output nel grafico richiede una connessione downstream, ma non si vuole eseguire il rendering dei dati da tale pin.</span><span class="sxs-lookup"><span data-stu-id="60115-130">Use this filter when an output pin in the graph requires a downstream connection, but you do not wish to render the data from that pin.</span></span> <span data-ttu-id="60115-131">Connettendo il pin di output al renderer Null, si completa la connessione senza eseguire il rendering dei dati.</span><span class="sxs-lookup"><span data-stu-id="60115-131">By connecting the output pin to the Null Renderer, you complete the connection without rendering the data.</span></span>

<span data-ttu-id="60115-132">Anche se questo filtro non esegue il rendering di alcun esempio, attende l'ora di presentazione di ogni campione prima di eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="60115-132">Even though this filter does not render any samples, it does wait for each sample's presentation time before discarding the sample.</span></span> <span data-ttu-id="60115-133">Di conseguenza, il grafico verrà eseguito alla velocità normale.</span><span class="sxs-lookup"><span data-stu-id="60115-133">Therefore, the graph will run at the normal rate.</span></span> <span data-ttu-id="60115-134">Se si vuole eseguire il grafico il più rapidamente possibile, impostare l'orologio di riferimento su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="60115-134">If you want the graph the run as quickly as possible, set the reference clock to **NULL**.</span></span> <span data-ttu-id="60115-135">Per altre informazioni, vedere [Impostazione dell'orologio del grafo.](setting-the-graph-clock.md)</span><span class="sxs-lookup"><span data-stu-id="60115-135">For more information, see [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60115-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60115-136">Requirements</span></span>



| <span data-ttu-id="60115-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="60115-137">Requirement</span></span> | <span data-ttu-id="60115-138">Valore</span><span class="sxs-lookup"><span data-stu-id="60115-138">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60115-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60115-139">Header</span></span><br/> | <dl> <span data-ttu-id="60115-140"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="60115-140"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60115-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60115-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60115-142">DirectShow Editing Services Objects</span><span class="sxs-lookup"><span data-stu-id="60115-142">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> </dl>

 

 




