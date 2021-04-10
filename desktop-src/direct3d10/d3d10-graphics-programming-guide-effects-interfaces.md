---
description: "Il sistema degli effetti definisce diverse interfacce per la gestione dello stato dell'effetto. Esistono due tipi di interfacce: quelle usate dal runtime per eseguire il rendering di un effetto e delle interfacce di reflection per ottenere e impostare le variabili di effetto."
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: Interfacce di sistema effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40b21d98bedaec65550343260e7c52e2df1c302
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126324"
---
# <a name="effect-system-interfaces-direct3d-10"></a><span data-ttu-id="d9693-104">Interfacce di sistema effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d9693-104">Effect System Interfaces (Direct3D 10)</span></span>

<span data-ttu-id="d9693-105">Il sistema degli effetti definisce diverse interfacce per la gestione dello stato dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="d9693-105">The effect system defines several interfaces for managing effect state.</span></span> <span data-ttu-id="d9693-106">Esistono due tipi di interfacce: quelle usate dal runtime per eseguire il rendering di un effetto e delle interfacce di reflection per ottenere e impostare le variabili di effetto.</span><span class="sxs-lookup"><span data-stu-id="d9693-106">There are two types of interfaces: those used by the runtime to render an effect and reflection interfaces for getting and setting effect variables.</span></span>

-   [<span data-ttu-id="d9693-107">Interfacce di runtime degli effetti</span><span class="sxs-lookup"><span data-stu-id="d9693-107">Effect Runtime Interfaces</span></span>](#effect-runtime-interfaces)
-   [<span data-ttu-id="d9693-108">Interfacce di Reflection effetto</span><span class="sxs-lookup"><span data-stu-id="d9693-108">Effect Reflection Interfaces</span></span>](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a><span data-ttu-id="d9693-109">Interfacce di runtime degli effetti</span><span class="sxs-lookup"><span data-stu-id="d9693-109">Effect Runtime Interfaces</span></span>

<span data-ttu-id="d9693-110">Usare le interfacce di runtime per eseguire il rendering di un effetto.</span><span class="sxs-lookup"><span data-stu-id="d9693-110">Use runtime interfaces to render an effect.</span></span>



| <span data-ttu-id="d9693-111">Interfacce di runtime</span><span class="sxs-lookup"><span data-stu-id="d9693-111">Runtime Interfaces</span></span>                                               | <span data-ttu-id="d9693-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9693-112">Description</span></span>                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="d9693-113">**Interfaccia ID3D10Effect**</span><span class="sxs-lookup"><span data-stu-id="d9693-113">**ID3D10Effect Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | <span data-ttu-id="d9693-114">Raccolta di una o più tecniche per il rendering.</span><span class="sxs-lookup"><span data-stu-id="d9693-114">Collection of one or more techniques for rendering.</span></span>                  |
| <span data-ttu-id="d9693-115">[**Interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d9693-115">[**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>                 | <span data-ttu-id="d9693-116">Interfaccia per l'aggiunta di comportamenti personalizzati durante la lettura dei file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="d9693-116">An interface for adding custom behaviors when reading include files.</span></span> |
| [<span data-ttu-id="d9693-117">**Interfaccia ID3D10EffectPass**</span><span class="sxs-lookup"><span data-stu-id="d9693-117">**ID3D10EffectPass Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | <span data-ttu-id="d9693-118">Raccolta di assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="d9693-118">A collection of state assignments.</span></span>                                   |
| [<span data-ttu-id="d9693-119">**Interfaccia ID3D10EffectPool**</span><span class="sxs-lookup"><span data-stu-id="d9693-119">**ID3D10EffectPool Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | <span data-ttu-id="d9693-120">Creare una posizione di memoria per le variabili da condividere tra gli effetti.</span><span class="sxs-lookup"><span data-stu-id="d9693-120">Create a memory location for variables to be shared between effects.</span></span> |
| [<span data-ttu-id="d9693-121">**Interfaccia ID3D10EffectTechnique**</span><span class="sxs-lookup"><span data-stu-id="d9693-121">**ID3D10EffectTechnique Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | <span data-ttu-id="d9693-122">Raccolta di uno o più passaggi.</span><span class="sxs-lookup"><span data-stu-id="d9693-122">A collection of one or more passes.</span></span>                                  |



 

## <a name="effect-reflection-interfaces"></a><span data-ttu-id="d9693-123">Interfacce di Reflection effetto</span><span class="sxs-lookup"><span data-stu-id="d9693-123">Effect Reflection Interfaces</span></span>

<span data-ttu-id="d9693-124">La reflection è implementata nel sistema di effetti per supportare la lettura e la scrittura dello stato dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="d9693-124">Reflection is implemented in the effect system to support reading (and writing) effect state.</span></span> <span data-ttu-id="d9693-125">Sono disponibili diversi modi per accedere alle variabili di effetto.</span><span class="sxs-lookup"><span data-stu-id="d9693-125">There are multiple ways to access effect variables.</span></span>

### <a name="setting-groups-of-effect-state"></a><span data-ttu-id="d9693-126">Impostazione dei gruppi di stato effetto</span><span class="sxs-lookup"><span data-stu-id="d9693-126">Setting Groups of Effect State</span></span>

<span data-ttu-id="d9693-127">Usare queste interfacce per ottenere e impostare un gruppo di stato.</span><span class="sxs-lookup"><span data-stu-id="d9693-127">Use these interfaces to get and set a group of state.</span></span>



| <span data-ttu-id="d9693-128">Interfacce di Reflection</span><span class="sxs-lookup"><span data-stu-id="d9693-128">Reflection Interfaces</span></span>                                                                  | <span data-ttu-id="d9693-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9693-129">Description</span></span>                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="d9693-130">**Interfaccia ID3D10EffectBlendVariable**</span><span class="sxs-lookup"><span data-stu-id="d9693-130">**ID3D10EffectBlendVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | <span data-ttu-id="d9693-131">Ottenere e impostare lo stato di Blend.</span><span class="sxs-lookup"><span data-stu-id="d9693-131">Get and set blend state.</span></span>         |
| [<span data-ttu-id="d9693-132">**Interfaccia ID3D10EffectDepthStencilVariable**</span><span class="sxs-lookup"><span data-stu-id="d9693-132">**ID3D10EffectDepthStencilVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | <span data-ttu-id="d9693-133">Ottenere e impostare lo stato di stencil Depth.</span><span class="sxs-lookup"><span data-stu-id="d9693-133">Get and set depth-stencil state.</span></span> |
| [<span data-ttu-id="d9693-134">**Interfaccia ID3D10EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="d9693-134">**ID3D10EffectRasterizerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | <span data-ttu-id="d9693-135">Ottiene e imposta lo stato di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="d9693-135">Get and set rasterizer state.</span></span>    |
| [<span data-ttu-id="d9693-136">**Interfaccia ID3D10EffectSamplerVariable**</span><span class="sxs-lookup"><span data-stu-id="d9693-136">**ID3D10EffectSamplerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | <span data-ttu-id="d9693-137">Ottiene e imposta lo stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="d9693-137">Get and set sampler state.</span></span>       |



 

### <a name="setting-effect-resources"></a><span data-ttu-id="d9693-138">Impostazione delle risorse degli effetti</span><span class="sxs-lookup"><span data-stu-id="d9693-138">Setting Effect Resources</span></span>

<span data-ttu-id="d9693-139">Usare queste interfacce per ottenere e impostare le risorse.</span><span class="sxs-lookup"><span data-stu-id="d9693-139">Use these interfaces to get and set resources.</span></span>



| <span data-ttu-id="d9693-140">Interfacce di Reflection</span><span class="sxs-lookup"><span data-stu-id="d9693-140">Reflection Interfaces</span></span>                                                                          | <span data-ttu-id="d9693-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9693-141">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="d9693-142">**Interfaccia ID3D10EffectConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="d9693-142">**ID3D10EffectConstantBuffer Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | <span data-ttu-id="d9693-143">Accedere ai dati in un buffer di trama o in un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="d9693-143">Access data in a texture buffer or constant buffer.</span></span> |
| [<span data-ttu-id="d9693-144">**Interfaccia ID3D10EffectDepthStencilViewVariable**</span><span class="sxs-lookup"><span data-stu-id="d9693-144">**ID3D10EffectDepthStencilViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | <span data-ttu-id="d9693-145">Accedere ai dati in una risorsa di stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="d9693-145">Access data in a depth-stencil resource.</span></span>            |
| [<span data-ttu-id="d9693-146">**Interfaccia ID3D10EffectRenderTargetViewVariable**</span><span class="sxs-lookup"><span data-stu-id="d9693-146">**ID3D10EffectRenderTargetViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | <span data-ttu-id="d9693-147">Accedere ai dati in una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="d9693-147">Access data in a render target.</span></span>                     |
| [<span data-ttu-id="d9693-148">**Interfaccia ID3D10EffectShaderResourceVariable**</span><span class="sxs-lookup"><span data-stu-id="d9693-148">**ID3D10EffectShaderResourceVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | <span data-ttu-id="d9693-149">Accedere ai dati in una risorsa shader.</span><span class="sxs-lookup"><span data-stu-id="d9693-149">Access data in a shader resource.</span></span>                   |



 

### <a name="setting-other-effect-variables"></a><span data-ttu-id="d9693-150">Impostazione di altre variabili di effetto</span><span class="sxs-lookup"><span data-stu-id="d9693-150">Setting Other Effect Variables</span></span>

<span data-ttu-id="d9693-151">Usare queste interfacce per ottenere e impostare lo stato in base al tipo di variabile.</span><span class="sxs-lookup"><span data-stu-id="d9693-151">Use these interfaces to get and set state by the variable type.</span></span>



| <span data-ttu-id="d9693-152">Interfacce di Reflection</span><span class="sxs-lookup"><span data-stu-id="d9693-152">Reflection Interfaces</span></span>                                                      | <span data-ttu-id="d9693-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9693-153">Description</span></span>                    |
|----------------------------------------------------------------------------|--------------------------------|
| [<span data-ttu-id="d9693-154">**Interfaccia ID3D10EffectMatrixVariable**</span><span class="sxs-lookup"><span data-stu-id="d9693-154">**ID3D10EffectMatrixVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | <span data-ttu-id="d9693-155">Ottenere e impostare una matrice.</span><span class="sxs-lookup"><span data-stu-id="d9693-155">Get and set a matrix.</span></span>          |
| [<span data-ttu-id="d9693-156">**Interfaccia ID3D10EffectScalarVariable**</span><span class="sxs-lookup"><span data-stu-id="d9693-156">**ID3D10EffectScalarVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | <span data-ttu-id="d9693-157">Ottenere e impostare un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="d9693-157">Get and set a scalar.</span></span>          |
| [<span data-ttu-id="d9693-158">**Interfaccia ID3D10EffectShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="d9693-158">**ID3D10EffectShaderVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | <span data-ttu-id="d9693-159">Ottenere e impostare una variabile shader.</span><span class="sxs-lookup"><span data-stu-id="d9693-159">Get and set a shader variable.</span></span> |
| [<span data-ttu-id="d9693-160">**Interfaccia ID3D10EffectStringVariable**</span><span class="sxs-lookup"><span data-stu-id="d9693-160">**ID3D10EffectStringVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | <span data-ttu-id="d9693-161">Ottenere e impostare una stringa.</span><span class="sxs-lookup"><span data-stu-id="d9693-161">Get and set a string.</span></span>          |
| [<span data-ttu-id="d9693-162">**Interfaccia ID3D10EffectType**</span><span class="sxs-lookup"><span data-stu-id="d9693-162">**ID3D10EffectType Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | <span data-ttu-id="d9693-163">Ottiene un tipo di variabile.</span><span class="sxs-lookup"><span data-stu-id="d9693-163">Get a variable type.</span></span>           |
| [<span data-ttu-id="d9693-164">**Interfaccia ID3D10EffectVectorVariable**</span><span class="sxs-lookup"><span data-stu-id="d9693-164">**ID3D10EffectVectorVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | <span data-ttu-id="d9693-165">Ottenere e impostare un vettore.</span><span class="sxs-lookup"><span data-stu-id="d9693-165">Get and set a vector.</span></span>          |



 

<span data-ttu-id="d9693-166">Tutte le interfacce di Reflection derivano dall' [**interfaccia ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).</span><span class="sxs-lookup"><span data-stu-id="d9693-166">All reflection interfaces derive from [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9693-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9693-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9693-168">Effetti</span><span class="sxs-lookup"><span data-stu-id="d9693-168">Effects</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="d9693-169">Guida di programmazione per Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="d9693-169">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
