---
description: Il filtro renderer null è un renderer che elimina tutti i campioni ricevuti, senza visualizzare o eseguire il rendering dei dati di esempio.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: Filtro renderer null (qedit. h)
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
ms.openlocfilehash: 7ff6c728276ca3fd69c14e304780b1d70c563265
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330170"
---
# <a name="null-renderer-filter"></a><span data-ttu-id="9f331-103">Filtro renderer null</span><span class="sxs-lookup"><span data-stu-id="9f331-103">Null Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="9f331-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="9f331-104">\[Deprecated.</span></span> <span data-ttu-id="9f331-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9f331-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9f331-106">Il filtro renderer null è un renderer che elimina tutti i campioni ricevuti, senza visualizzare o eseguire il rendering dei dati di esempio.</span><span class="sxs-lookup"><span data-stu-id="9f331-106">The Null Renderer filter is a renderer that discards every sample it receives, without displaying or rendering the sample data.</span></span>



|                                          |                                                                                                                      |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f331-107">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="9f331-107">Filter interfaces</span></span>                        | <span data-ttu-id="9f331-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="9f331-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span> |
| <span data-ttu-id="9f331-109">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="9f331-109">Input pin media types</span></span>                    | <span data-ttu-id="9f331-110">Qualsiasi tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="9f331-110">Any media type</span></span>                                                                                                       |
| <span data-ttu-id="9f331-111">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="9f331-111">Input pin interfaces</span></span>                     | <span data-ttu-id="9f331-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="9f331-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>               |
| <span data-ttu-id="9f331-113">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="9f331-113">Output pin media types</span></span>                   | <span data-ttu-id="9f331-114">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="9f331-114">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="9f331-115">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="9f331-115">Output pin interfaces</span></span>                    | <span data-ttu-id="9f331-116">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="9f331-116">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="9f331-117">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="9f331-117">Filter CLSID</span></span>                             | <span data-ttu-id="9f331-118">\_NULLRENDERER CLSID</span><span class="sxs-lookup"><span data-stu-id="9f331-118">CLSID\_NullRenderer</span></span>                                                                                                  |
| <span data-ttu-id="9f331-119">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="9f331-119">Property Page CLSID</span></span>                      | <span data-ttu-id="9f331-120">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="9f331-120">No property page.</span></span>                                                                                                    |
| <span data-ttu-id="9f331-121">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="9f331-121">Executable</span></span>                               | <span data-ttu-id="9f331-122">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="9f331-122">Qedit.dll</span></span>                                                                                                            |
| [<span data-ttu-id="9f331-123">Merito</span><span class="sxs-lookup"><span data-stu-id="9f331-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="9f331-124">il merito non viene \_ \_ \_ utilizzato</span><span class="sxs-lookup"><span data-stu-id="9f331-124">MERIT\_DO\_NOT\_USE</span></span>                                                                                                  |
| [<span data-ttu-id="9f331-125">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="9f331-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="9f331-126">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="9f331-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="9f331-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f331-127">Remarks</span></span>

<span data-ttu-id="9f331-128">Usare questo filtro quando un pin di output nel grafico richiede una connessione downstream, ma non si vuole eseguire il rendering dei dati dal pin.</span><span class="sxs-lookup"><span data-stu-id="9f331-128">Use this filter when an output pin in the graph requires a downstream connection, but you do not wish to render the data from that pin.</span></span> <span data-ttu-id="9f331-129">Connettendo il pin di output al renderer null, si completa la connessione senza eseguire il rendering dei dati.</span><span class="sxs-lookup"><span data-stu-id="9f331-129">By connecting the output pin to the Null Renderer, you complete the connection without rendering the data.</span></span>

<span data-ttu-id="9f331-130">Anche se questo filtro non esegue il rendering di alcun campione, attende il tempo di presentazione di ogni campione prima di rimuovere l'esempio.</span><span class="sxs-lookup"><span data-stu-id="9f331-130">Even though this filter does not render any samples, it does wait for each sample's presentation time before discarding the sample.</span></span> <span data-ttu-id="9f331-131">Il grafico viene pertanto eseguito alla tariffa normale.</span><span class="sxs-lookup"><span data-stu-id="9f331-131">Therefore, the graph will run at the normal rate.</span></span> <span data-ttu-id="9f331-132">Se si desidera che il grafico venga eseguito il più rapidamente possibile, impostare l'orologio di riferimento su **null**.</span><span class="sxs-lookup"><span data-stu-id="9f331-132">If you want the graph the run as quickly as possible, set the reference clock to **NULL**.</span></span> <span data-ttu-id="9f331-133">Per altre informazioni, vedere [Setting the Graph Clock](setting-the-graph-clock.md).</span><span class="sxs-lookup"><span data-stu-id="9f331-133">For more information, see [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f331-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f331-134">Requirements</span></span>



| <span data-ttu-id="9f331-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f331-135">Requirement</span></span> | <span data-ttu-id="9f331-136">Valore</span><span class="sxs-lookup"><span data-stu-id="9f331-136">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9f331-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f331-137">Header</span></span><br/> | <dl> <span data-ttu-id="9f331-138"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f331-138"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f331-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f331-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f331-140">Oggetti dei servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="9f331-140">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> </dl>

 

 




