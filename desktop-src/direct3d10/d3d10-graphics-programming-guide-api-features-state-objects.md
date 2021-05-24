---
description: In Direct3D 10 lo stato del dispositivo è raggruppato in oggetti di stato che riducono notevolmente il costo delle modifiche dello stato.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Oggetti di stato (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a51c05e3e220e510c462265941549f91e6368a9
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335425"
---
# <a name="state-objects-direct3d-10"></a><span data-ttu-id="0a8b8-103">Oggetti di stato (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="0a8b8-103">State Objects (Direct3D 10)</span></span>

<span data-ttu-id="0a8b8-104">In Direct3D 10 lo stato del dispositivo è raggruppato in oggetti di stato che riducono notevolmente il costo delle modifiche dello stato.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-104">In Direct3D 10, device state is grouped into state objects which greatly reduce the cost of state changes.</span></span> <span data-ttu-id="0a8b8-105">Sono disponibili diversi oggetti stato e ognuno è progettato per inizializzare un set di stato per una determinata fase della pipeline.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-105">There are several state objects, and each one is designed to initialize a set of state for a particular pipeline stage.</span></span> <span data-ttu-id="0a8b8-106">È possibile creare fino a 4096 di ogni tipo di oggetto stato.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-106">You can create up to 4096 of each type of state object.</span></span>

-   [<span data-ttu-id="0a8b8-107">Stato del layout di input</span><span class="sxs-lookup"><span data-stu-id="0a8b8-107">Input-Layout State</span></span>](#input-layout-state)
-   [<span data-ttu-id="0a8b8-108">Stato rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="0a8b8-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="0a8b8-109">Stato depth-stencil</span><span class="sxs-lookup"><span data-stu-id="0a8b8-109">Depth-Stencil State</span></span>](#depth-stencil-state)
-   [<span data-ttu-id="0a8b8-110">Stato di blend</span><span class="sxs-lookup"><span data-stu-id="0a8b8-110">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="0a8b8-111">Stato del campionatore</span><span class="sxs-lookup"><span data-stu-id="0a8b8-111">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="0a8b8-112">Considerazioni sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="0a8b8-112">Performance Considerations</span></span>](#performance-considerations)
-   [<span data-ttu-id="0a8b8-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a8b8-113">Related topics</span></span>](#related-topics)

## <a name="input-layout-state"></a><span data-ttu-id="0a8b8-114">Input-Layout stato</span><span class="sxs-lookup"><span data-stu-id="0a8b8-114">Input-Layout State</span></span>

<span data-ttu-id="0a8b8-115">Questo gruppo di stato (vedere [**D3D10 \_ INPUT \_ ELEMENT \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)determina il modo in cui la fase dell'assembler di [input](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) legge i dati dai buffer di input e lo assembla per l'uso da parte del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-115">This group of state (see [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) dictates how the [input-assembler stage](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) reads data out of the input buffers and assembles it for use by the vertex shader.</span></span> <span data-ttu-id="0a8b8-116">Include lo stato, ad esempio il numero di elementi nel buffer di input e la firma dei dati di input.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-116">This includes state such as the number of elements in the input buffer and the signature of the input data.</span></span> <span data-ttu-id="0a8b8-117">La fase dell'assembler di input è una nuova fase della pipeline il cui processo è quello di trasmettere le primitive dalla memoria alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-117">The input-assembler stage is a new stage in the pipeline whose job is to stream primitives from memory into the pipeline.</span></span>

<span data-ttu-id="0a8b8-118">Per creare un oggetto input-layout-state, vedere [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="0a8b8-118">To create a input-layout-state object, see [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

## <a name="rasterizer-state"></a><span data-ttu-id="0a8b8-119">Stato rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="0a8b8-119">Rasterizer State</span></span>

<span data-ttu-id="0a8b8-120">Questo gruppo di stato (vedere [**D3D10 \_ RASTERIZER \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)inizializza la fase [del rasterizzatore](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span><span class="sxs-lookup"><span data-stu-id="0a8b8-120">This group of state (see [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) initializes the [rasterizer stage](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span></span> <span data-ttu-id="0a8b8-121">Questo oggetto include lo stato, ad esempio le modalità di riempimento o di interruzione, l'abilitazione di un rettangolo di forbice per il ritaglio e l'impostazione di parametri multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-121">This object includes state such as fill or cull modes, enabling a scissor rectangle for clipping, and setting multisample parameters.</span></span> <span data-ttu-id="0a8b8-122">Questa fase rasterizza le primitive in pixel, eseguendo operazioni come il ritaglio e il mapping delle primitive al viewport.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-122">This stage rasterizes primitives into pixels, performing operations like clipping and mapping primitives to the viewport.</span></span>

<span data-ttu-id="0a8b8-123">Per creare un oggetto stato di rasterizzazione, vedere [**CreateRasterizerState.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate)</span><span class="sxs-lookup"><span data-stu-id="0a8b8-123">To create a rasterizer-state object, see [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span></span>

## <a name="depth-stencil-state"></a><span data-ttu-id="0a8b8-124">Depth-Stencil stato</span><span class="sxs-lookup"><span data-stu-id="0a8b8-124">Depth-Stencil State</span></span>

<span data-ttu-id="0a8b8-125">Questo gruppo di stato (vedere [**D3D10 \_ DEPTH \_ STENCIL \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)inizializza la parte depth-stencil della fase [di unione dell'output.](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md)</span><span class="sxs-lookup"><span data-stu-id="0a8b8-125">This group of state (see [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) initializes the depth-stencil portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="0a8b8-126">In particolare, questo oggetto inizializza i test di profondità e stencil.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-126">More specifically, this object initializes depth and stencil testing.</span></span>

<span data-ttu-id="0a8b8-127">Per creare un oggetto depth-stencil-state, vedere [**CreateDepthStencilState.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate)</span><span class="sxs-lookup"><span data-stu-id="0a8b8-127">To create a depth-stencil-state object, see [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span></span>

## <a name="blend-state"></a><span data-ttu-id="0a8b8-128">Stato blend</span><span class="sxs-lookup"><span data-stu-id="0a8b8-128">Blend State</span></span>

<span data-ttu-id="0a8b8-129">Questo gruppo di stato (vedere [**D3D10 \_ BLEND \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)inizializza la parte di fusione della fase [di unione dell'output.](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md)</span><span class="sxs-lookup"><span data-stu-id="0a8b8-129">This group of state (see [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) initializes the blending portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span>

<span data-ttu-id="0a8b8-130">Per creare un oggetto stato di blend, vedere [**CreateBlendState.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate)</span><span class="sxs-lookup"><span data-stu-id="0a8b8-130">To create a blend-state object, see [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span></span>

## <a name="sampler-state"></a><span data-ttu-id="0a8b8-131">Stato del campionatore</span><span class="sxs-lookup"><span data-stu-id="0a8b8-131">Sampler State</span></span>

<span data-ttu-id="0a8b8-132">Questo gruppo di stato (vedere [**D3D10 \_ SAMPLER \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)inizializza un oggetto campionatore.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-132">This group of state (see [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) initializes a sampler object.</span></span> <span data-ttu-id="0a8b8-133">Un oggetto campionatore viene usato dalle fasi dello shader per filtrare le trame in memoria.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-133">A sampler object is used by the shader stages to filter textures in memory.</span></span>



<span data-ttu-id="0a8b8-134">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="0a8b8-134">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="0a8b8-135">In Direct3D 10 l'oggetto campionatore non è più associato a una trama specifica, ma descrive semplicemente come filtrare in base a qualsiasi risorsa collegata.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-135">In Direct3D 10, the sampler object is no longer bound to a specific texture, it just describes how to do filtering given any attached resource.</span></span>



 

<span data-ttu-id="0a8b8-136">Per creare un oggetto sampler-state, vedere [**CreateSamplerState.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate)</span><span class="sxs-lookup"><span data-stu-id="0a8b8-136">To create a sampler-state object, see [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span></span>

## <a name="performance-considerations"></a><span data-ttu-id="0a8b8-137">Considerazioni sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="0a8b8-137">Performance Considerations</span></span>

<span data-ttu-id="0a8b8-138">La progettazione dell'API per l'uso di oggetti di stato offre diversi vantaggi in termini di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-138">Designing the API to use state objects creates several performance advantages.</span></span> <span data-ttu-id="0a8b8-139">Questi includono la convalida dello stato al momento della creazione dell'oggetto, l'abilitazione della memorizzazione nella cache degli oggetti di stato nell'hardware e la riduzione notevolmente della quantità di stato passata durante una chiamata API di impostazione dello stato (passando un handle all'oggetto di stato anziché lo stato).</span><span class="sxs-lookup"><span data-stu-id="0a8b8-139">These include validating state at object creation time, enabling caching of state objects in hardware, and greatly reducing the amount of state that is passed during a state-setting API call (by passing a handle to the state object instead of the state).</span></span>

<span data-ttu-id="0a8b8-140">Per ottenere questi miglioramenti delle prestazioni, è necessario creare gli oggetti di stato all'avvio dell'applicazione, molto prima del ciclo di rendering.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-140">To achieve these performance improvements, you should create your state objects when your application starts up, well before your render loop.</span></span> <span data-ttu-id="0a8b8-141">Gli oggetti di stato non sono modificabili, in altri modo, una volta creati, non è possibile modificarli.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-141">State objects are immutable, that is, once they are created, you cannot change them.</span></span> <span data-ttu-id="0a8b8-142">È invece necessario eliminare e ricrearli.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-142">Instead you must destroy and recreate them.</span></span> <span data-ttu-id="0a8b8-143">Per far fronte a questa restrizione, è possibile creare fino a 4096 di ogni tipo di oggetti di stato.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-143">To cope with this restriction, you can create up to 4096 of each type of state objects.</span></span> <span data-ttu-id="0a8b8-144">Ad esempio, è possibile creare diversi oggetti campionatore con varie combinazioni di stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-144">For example, you could create several sampler objects with various sampler-state combinations.</span></span> <span data-ttu-id="0a8b8-145">La modifica dello stato del campionatore viene quindi eseguita chiamando l'API Set appropriata che passa un handle all'oggetto (anziché allo stato del campionatore).</span><span class="sxs-lookup"><span data-stu-id="0a8b8-145">Changing the sampler state is then accomplished by calling the appropriate Set API which passes a handle to the object (as opposed to the sampler state).</span></span> <span data-ttu-id="0a8b8-146">In questo modo si riduce notevolmente la quantità di overhead durante ogni frame di rendering per la modifica dello stato poiché il numero di chiamate e la quantità di dati vengono notevolmente ridotti.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-146">This significantly reduces the amount of overhead during each render frame for changing state since the number of calls and the amount of data are greatly reduced.</span></span>

<span data-ttu-id="0a8b8-147">In alternativa, è possibile scegliere di usare il sistema di effetti che gestirà automaticamente la creazione e la distruzione efficienti degli oggetti di stato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0a8b8-147">Alternatively, you can choose to use the effect system which will automatically manage efficient creation and destruction of state objects for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a8b8-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a8b8-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a8b8-149">Funzionalità API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="0a8b8-149">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
