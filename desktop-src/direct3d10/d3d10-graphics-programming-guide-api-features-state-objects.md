---
description: In Direct3D 10 lo stato del dispositivo è raggruppato in oggetti di stato che consentono di ridurre notevolmente il costo delle modifiche di stato.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Oggetti stato (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a06e8603361a83049440774cfd2e12b4148b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304603"
---
# <a name="state-objects-direct3d-10"></a><span data-ttu-id="8071d-103">Oggetti stato (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8071d-103">State Objects (Direct3D 10)</span></span>

<span data-ttu-id="8071d-104">In Direct3D 10 lo stato del dispositivo è raggruppato in oggetti di stato che consentono di ridurre notevolmente il costo delle modifiche di stato.</span><span class="sxs-lookup"><span data-stu-id="8071d-104">In Direct3D 10, device state is grouped into state objects which greatly reduce the cost of state changes.</span></span> <span data-ttu-id="8071d-105">Sono disponibili diversi oggetti di stato e ognuno è progettato per inizializzare un set di stato per una determinata fase della pipeline.</span><span class="sxs-lookup"><span data-stu-id="8071d-105">There are several state objects, and each one is designed to initialize a set of state for a particular pipeline stage.</span></span> <span data-ttu-id="8071d-106">È possibile creare fino a 4096 di ogni tipo di oggetto di stato.</span><span class="sxs-lookup"><span data-stu-id="8071d-106">You can create up to 4096 of each type of state object.</span></span>

-   [<span data-ttu-id="8071d-107">Input-stato layout</span><span class="sxs-lookup"><span data-stu-id="8071d-107">Input-Layout State</span></span>](#input-layout-state)
-   [<span data-ttu-id="8071d-108">Stato rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="8071d-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="8071d-109">Stato stencil profondità</span><span class="sxs-lookup"><span data-stu-id="8071d-109">Depth-Stencil State</span></span>](#depth-stencil-state)
-   [<span data-ttu-id="8071d-110">Stato di Blend</span><span class="sxs-lookup"><span data-stu-id="8071d-110">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="8071d-111">Stato campionatore</span><span class="sxs-lookup"><span data-stu-id="8071d-111">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="8071d-112">Considerazioni sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="8071d-112">Performance Considerations</span></span>](#performance-considerations)
-   [<span data-ttu-id="8071d-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8071d-113">Related topics</span></span>](#related-topics)

## <a name="input-layout-state"></a><span data-ttu-id="8071d-114">Stato Input-Layout</span><span class="sxs-lookup"><span data-stu-id="8071d-114">Input-Layout State</span></span>

<span data-ttu-id="8071d-115">Questo gruppo di stato (vedere [**\_ elemento input \_ D3D10 \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) determina il modo in cui la [fase input-assembler](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) legge i dati dai buffer di input e li assembla per l'uso da parte del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="8071d-115">This group of state (see [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) dictates how the [input-assembler stage](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) reads data out of the input buffers and assembles it for use by the vertex shader.</span></span> <span data-ttu-id="8071d-116">Questo include lo stato, ad esempio il numero di elementi nel buffer di input e la firma dei dati di input.</span><span class="sxs-lookup"><span data-stu-id="8071d-116">This includes state such as the number of elements in the input buffer and the signature of the input data.</span></span> <span data-ttu-id="8071d-117">La fase input-assembler è una nuova fase della pipeline il cui compito è quello di trasmettere le primitive dalla memoria alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="8071d-117">The input-assembler stage is a new stage in the pipeline whose job is to stream primitives from memory into the pipeline.</span></span>

<span data-ttu-id="8071d-118">Per creare un oggetto di stato del layout di input, vedere [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="8071d-118">To create a input-layout-state object, see [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

## <a name="rasterizer-state"></a><span data-ttu-id="8071d-119">Stato rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="8071d-119">Rasterizer State</span></span>

<span data-ttu-id="8071d-120">Questo gruppo di stato (vedere [**D3D10 \_ rasterizzator \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) Inizializza la [fase di rasterizzazione](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span><span class="sxs-lookup"><span data-stu-id="8071d-120">This group of state (see [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) initializes the [rasterizer stage](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span></span> <span data-ttu-id="8071d-121">Questo oggetto include lo stato, ad esempio le modalità riempimento o selezione, l'abilitazione di un rettangolo a forbice per il ritaglio e l'impostazione di parametri multisample.</span><span class="sxs-lookup"><span data-stu-id="8071d-121">This object includes state such as fill or cull modes, enabling a scissor rectangle for clipping, and setting multisample parameters.</span></span> <span data-ttu-id="8071d-122">In questa fase le primitive vengono rasterizzate in pixel, eseguendo operazioni come il ritaglio e il mapping delle primitive al viewport.</span><span class="sxs-lookup"><span data-stu-id="8071d-122">This stage rasterizes primitives into pixels, performing operations like clipping and mapping primitives to the viewport.</span></span>

<span data-ttu-id="8071d-123">Per creare un oggetto di stato di rasterizzazione, vedere [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span><span class="sxs-lookup"><span data-stu-id="8071d-123">To create a rasterizer-state object, see [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span></span>

## <a name="depth-stencil-state"></a><span data-ttu-id="8071d-124">Stato Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="8071d-124">Depth-Stencil State</span></span>

<span data-ttu-id="8071d-125">Questo gruppo di stato (vedere [**D3D10 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) Inizializza la parte depth-stencil della [fase di Unione dell'output](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="8071d-125">This group of state (see [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) initializes the depth-stencil portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="8071d-126">In particolare, questo oggetto Inizializza la profondità e il test di stencil.</span><span class="sxs-lookup"><span data-stu-id="8071d-126">More specifically, this object initializes depth and stencil testing.</span></span>

<span data-ttu-id="8071d-127">Per creare un oggetto depth-stencil-state, vedere [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span><span class="sxs-lookup"><span data-stu-id="8071d-127">To create a depth-stencil-state object, see [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span></span>

## <a name="blend-state"></a><span data-ttu-id="8071d-128">Stato di Blend</span><span class="sxs-lookup"><span data-stu-id="8071d-128">Blend State</span></span>

<span data-ttu-id="8071d-129">Questo gruppo di stato (vedere [**D3D10 \_ Blend \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) Inizializza la parte di combinazione della [fase di Unione dell'output](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="8071d-129">This group of state (see [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) initializes the blending portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span>

<span data-ttu-id="8071d-130">Per creare un oggetto di stato Blend, vedere [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span><span class="sxs-lookup"><span data-stu-id="8071d-130">To create a blend-state object, see [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span></span>

## <a name="sampler-state"></a><span data-ttu-id="8071d-131">Stato campionatore</span><span class="sxs-lookup"><span data-stu-id="8071d-131">Sampler State</span></span>

<span data-ttu-id="8071d-132">Questo gruppo di stato (vedere [**D3D10 \_ Sampler \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) Inizializza un oggetto Sampler.</span><span class="sxs-lookup"><span data-stu-id="8071d-132">This group of state (see [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) initializes a sampler object.</span></span> <span data-ttu-id="8071d-133">Un oggetto Sampler viene usato dalle fasi dello shader per filtrare le trame in memoria.</span><span class="sxs-lookup"><span data-stu-id="8071d-133">A sampler object is used by the shader stages to filter textures in memory.</span></span>



|                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8071d-134">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="8071d-134">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="8071d-135">In Direct3D 10, l'oggetto Sampler non è più associato a una trama specifica, ma descrive semplicemente come applicare il filtro in base a qualsiasi risorsa collegata.</span><span class="sxs-lookup"><span data-stu-id="8071d-135">In Direct3D 10, the sampler object is no longer bound to a specific texture - it just describes how to do filtering given any attached resource.</span></span> |



 

<span data-ttu-id="8071d-136">Per creare un oggetto stato del campionatore, vedere [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="8071d-136">To create a sampler-state object, see [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span></span>

## <a name="performance-considerations"></a><span data-ttu-id="8071d-137">Considerazioni sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="8071d-137">Performance Considerations</span></span>

<span data-ttu-id="8071d-138">La progettazione dell'API per l'utilizzo di oggetti stato crea diversi vantaggi in merito alle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="8071d-138">Designing the API to use state objects creates several performance advantages.</span></span> <span data-ttu-id="8071d-139">Sono inclusi lo stato di convalida al momento della creazione dell'oggetto, l'abilitazione della memorizzazione nella cache degli oggetti stato nell'hardware e la riduzione sostanziale della quantità di stato passato durante una chiamata API di impostazione dello stato (passando un handle all'oggetto stato anziché allo stato).</span><span class="sxs-lookup"><span data-stu-id="8071d-139">These include validating state at object creation time, enabling caching of state objects in hardware, and greatly reducing the amount of state that is passed during a state-setting API call (by passing a handle to the state object instead of the state).</span></span>

<span data-ttu-id="8071d-140">Per ottenere questi miglioramenti delle prestazioni, è necessario creare gli oggetti di stato all'avvio dell'applicazione, ben prima del ciclo di rendering.</span><span class="sxs-lookup"><span data-stu-id="8071d-140">To achieve these performance improvements, you should create your state objects when your application starts up, well before your render loop.</span></span> <span data-ttu-id="8071d-141">Gli oggetti di stato non sono modificabili, ovvero, una volta creati, non è possibile modificarli.</span><span class="sxs-lookup"><span data-stu-id="8071d-141">State objects are immutable, that is, once they are created, you cannot change them.</span></span> <span data-ttu-id="8071d-142">È invece necessario eliminarli e ricrearli.</span><span class="sxs-lookup"><span data-stu-id="8071d-142">Instead you must destroy and recreate them.</span></span> <span data-ttu-id="8071d-143">Per ovviare a questa restrizione, è possibile creare fino a 4096 di ogni tipo di oggetti stato.</span><span class="sxs-lookup"><span data-stu-id="8071d-143">To cope with this restriction, you can create up to 4096 of each type of state objects.</span></span> <span data-ttu-id="8071d-144">Ad esempio, è possibile creare diversi oggetti sampler con diverse combinazioni di stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="8071d-144">For example, you could create several sampler objects with various sampler-state combinations.</span></span> <span data-ttu-id="8071d-145">La modifica dello stato del campionatore viene quindi eseguita chiamando l'API set appropriata che passa un handle all'oggetto (anziché lo stato del campionatore).</span><span class="sxs-lookup"><span data-stu-id="8071d-145">Changing the sampler state is then accomplished by calling the appropriate Set API which passes a handle to the object (as opposed to the sampler state).</span></span> <span data-ttu-id="8071d-146">Questo riduce significativamente la quantità di overhead durante ogni frame di rendering per la modifica dello stato, in quanto il numero di chiamate e la quantità di dati vengono notevolmente ridotti.</span><span class="sxs-lookup"><span data-stu-id="8071d-146">This significantly reduces the amount of overhead during each render frame for changing state since the number of calls and the amount of data are greatly reduced.</span></span>

<span data-ttu-id="8071d-147">In alternativa, è possibile scegliere di utilizzare il sistema di effetti che gestirà automaticamente la creazione e l'eliminazione efficienti degli oggetti stato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8071d-147">Alternatively, you can choose to use the effect system which will automatically manage efficient creation and destruction of state objects for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8071d-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8071d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8071d-149">Funzionalità API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8071d-149">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
