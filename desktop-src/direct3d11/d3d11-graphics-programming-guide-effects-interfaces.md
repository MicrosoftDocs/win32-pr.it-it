---
title: Interfacce di sistema effetto (Direct3D 11)
description: Il sistema degli effetti definisce diverse interfacce per la gestione dello stato dell'effetto.
ms.assetid: 5cba6055-d153-4837-9a08-96efbde5f48f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af76a54be06e52e320743ca945abb31d1d50d213
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708545"
---
# <a name="effect-system-interfaces-direct3d-11"></a><span data-ttu-id="4773b-103">Interfacce di sistema effetto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="4773b-103">Effect System Interfaces (Direct3D 11)</span></span>

<span data-ttu-id="4773b-104">Il sistema degli effetti definisce diverse interfacce per la gestione dello stato dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="4773b-104">The effect system defines several interfaces for managing effect state.</span></span> <span data-ttu-id="4773b-105">Esistono due tipi di interfacce: quelle usate dal runtime per eseguire il rendering di un effetto e delle interfacce di reflection per ottenere e impostare le variabili di effetto.</span><span class="sxs-lookup"><span data-stu-id="4773b-105">There are two types of interfaces: those used by the runtime to render an effect and reflection interfaces for getting and setting effect variables.</span></span>

-   [<span data-ttu-id="4773b-106">Interfacce di runtime degli effetti</span><span class="sxs-lookup"><span data-stu-id="4773b-106">Effect Runtime Interfaces</span></span>](#effect-runtime-interfaces)
-   [<span data-ttu-id="4773b-107">Interfacce di Reflection effetto</span><span class="sxs-lookup"><span data-stu-id="4773b-107">Effect Reflection Interfaces</span></span>](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a><span data-ttu-id="4773b-108">Interfacce di runtime degli effetti</span><span class="sxs-lookup"><span data-stu-id="4773b-108">Effect Runtime Interfaces</span></span>

<span data-ttu-id="4773b-109">Usare le interfacce di runtime per eseguire il rendering di un effetto.</span><span class="sxs-lookup"><span data-stu-id="4773b-109">Use runtime interfaces to render an effect.</span></span>



| <span data-ttu-id="4773b-110">Interfacce di runtime</span><span class="sxs-lookup"><span data-stu-id="4773b-110">Runtime Interfaces</span></span>                                       | <span data-ttu-id="4773b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4773b-111">Description</span></span>                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="4773b-112">**ID3DX11Effect**</span><span class="sxs-lookup"><span data-stu-id="4773b-112">**ID3DX11Effect**</span></span>](id3dx11effect.md)                   | <span data-ttu-id="4773b-113">Raccolta di uno o più gruppi e tecniche per il rendering.</span><span class="sxs-lookup"><span data-stu-id="4773b-113">Collection of one or more groups and techniques for rendering.</span></span> |
| [<span data-ttu-id="4773b-114">**ID3DX11EffectPass**</span><span class="sxs-lookup"><span data-stu-id="4773b-114">**ID3DX11EffectPass**</span></span>](id3dx11effectpass.md)           | <span data-ttu-id="4773b-115">Raccolta di assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="4773b-115">A collection of state assignments.</span></span>                             |
| [<span data-ttu-id="4773b-116">**ID3DX11EffectTechnique**</span><span class="sxs-lookup"><span data-stu-id="4773b-116">**ID3DX11EffectTechnique**</span></span>](id3dx11effecttechnique.md) | <span data-ttu-id="4773b-117">Raccolta di uno o più passaggi.</span><span class="sxs-lookup"><span data-stu-id="4773b-117">A collection of one or more passes.</span></span>                            |
| [<span data-ttu-id="4773b-118">**ID3DX11EffectGroup**</span><span class="sxs-lookup"><span data-stu-id="4773b-118">**ID3DX11EffectGroup**</span></span>](id3dx11effectgroup.md)         | <span data-ttu-id="4773b-119">Raccolta di una o più tecniche.</span><span class="sxs-lookup"><span data-stu-id="4773b-119">A collection of one or more techniques.</span></span>                        |



 

## <a name="effect-reflection-interfaces"></a><span data-ttu-id="4773b-120">Interfacce di Reflection effetto</span><span class="sxs-lookup"><span data-stu-id="4773b-120">Effect Reflection Interfaces</span></span>

<span data-ttu-id="4773b-121">La reflection è implementata nel sistema di effetti per supportare la lettura e la scrittura dello stato dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="4773b-121">Reflection is implemented in the effect system to support reading (and writing) effect state.</span></span> <span data-ttu-id="4773b-122">Sono disponibili diversi modi per accedere alle variabili di effetto.</span><span class="sxs-lookup"><span data-stu-id="4773b-122">There are multiple ways to access effect variables.</span></span>

### <a name="setting-groups-of-effect-state"></a><span data-ttu-id="4773b-123">Impostazione dei gruppi di stato effetto</span><span class="sxs-lookup"><span data-stu-id="4773b-123">Setting Groups of Effect State</span></span>

<span data-ttu-id="4773b-124">Usare queste interfacce per ottenere e impostare un gruppo di stato.</span><span class="sxs-lookup"><span data-stu-id="4773b-124">Use these interfaces to get and set a group of state.</span></span>



| <span data-ttu-id="4773b-125">Interfacce di Reflection</span><span class="sxs-lookup"><span data-stu-id="4773b-125">Reflection Interfaces</span></span>                                                          | <span data-ttu-id="4773b-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4773b-126">Description</span></span>                      |
|--------------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="4773b-127">**ID3DX11EffectBlendVariable**</span><span class="sxs-lookup"><span data-stu-id="4773b-127">**ID3DX11EffectBlendVariable**</span></span>](id3dx11effectblendvariable.md)               | <span data-ttu-id="4773b-128">Ottenere e impostare lo stato di Blend.</span><span class="sxs-lookup"><span data-stu-id="4773b-128">Get and set blend state.</span></span>         |
| [<span data-ttu-id="4773b-129">**ID3DX11EffectDepthStencilVariable**</span><span class="sxs-lookup"><span data-stu-id="4773b-129">**ID3DX11EffectDepthStencilVariable**</span></span>](id3dx11effectdepthstencilvariable.md) | <span data-ttu-id="4773b-130">Ottenere e impostare lo stato di stencil Depth.</span><span class="sxs-lookup"><span data-stu-id="4773b-130">Get and set depth-stencil state.</span></span> |
| [<span data-ttu-id="4773b-131">**ID3DX11EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="4773b-131">**ID3DX11EffectRasterizerVariable**</span></span>](id3dx11effectrasterizervariable.md)     | <span data-ttu-id="4773b-132">Ottiene e imposta lo stato di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="4773b-132">Get and set rasterizer state.</span></span>    |
| [<span data-ttu-id="4773b-133">**ID3DX11EffectSamplerVariable**</span><span class="sxs-lookup"><span data-stu-id="4773b-133">**ID3DX11EffectSamplerVariable**</span></span>](id3dx11effectsamplervariable.md)           | <span data-ttu-id="4773b-134">Ottiene e imposta lo stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="4773b-134">Get and set sampler state.</span></span>       |



 

### <a name="setting-effect-resources"></a><span data-ttu-id="4773b-135">Impostazione delle risorse degli effetti</span><span class="sxs-lookup"><span data-stu-id="4773b-135">Setting Effect Resources</span></span>

<span data-ttu-id="4773b-136">Usare queste interfacce per ottenere e impostare le risorse.</span><span class="sxs-lookup"><span data-stu-id="4773b-136">Use these interfaces to get and set resources.</span></span>



| <span data-ttu-id="4773b-137">Interfacce di Reflection</span><span class="sxs-lookup"><span data-stu-id="4773b-137">Reflection Interfaces</span></span>                                                                        | <span data-ttu-id="4773b-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4773b-138">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="4773b-139">**ID3DX11EffectConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="4773b-139">**ID3DX11EffectConstantBuffer**</span></span>](id3dx11effectconstantbuffer.md)                           | <span data-ttu-id="4773b-140">Accedere ai dati in un buffer di trama o in un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="4773b-140">Access data in a texture buffer or constant buffer.</span></span> |
| [<span data-ttu-id="4773b-141">**ID3DX11EffectDepthStencilViewVariable**</span><span class="sxs-lookup"><span data-stu-id="4773b-141">**ID3DX11EffectDepthStencilViewVariable**</span></span>](id3dx11effectdepthstencilviewvariable.md)       | <span data-ttu-id="4773b-142">Accedere ai dati in una risorsa di stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="4773b-142">Access data in a depth-stencil resource.</span></span>            |
| [<span data-ttu-id="4773b-143">**ID3DX11EffectRenderTargetViewVariable**</span><span class="sxs-lookup"><span data-stu-id="4773b-143">**ID3DX11EffectRenderTargetViewVariable**</span></span>](id3dx11effectrendertargetviewvariable.md)       | <span data-ttu-id="4773b-144">Accedere ai dati in una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="4773b-144">Access data in a render target.</span></span>                     |
| [<span data-ttu-id="4773b-145">**ID3DX11EffectShaderResourceVariable**</span><span class="sxs-lookup"><span data-stu-id="4773b-145">**ID3DX11EffectShaderResourceVariable**</span></span>](id3dx11effectshaderresourcevariable.md)           | <span data-ttu-id="4773b-146">Accedere ai dati in una risorsa shader.</span><span class="sxs-lookup"><span data-stu-id="4773b-146">Access data in a shader resource.</span></span>                   |
| [<span data-ttu-id="4773b-147">**ID3DX11EffectUnorderedAccessViewVariable**</span><span class="sxs-lookup"><span data-stu-id="4773b-147">**ID3DX11EffectUnorderedAccessViewVariable**</span></span>](id3dx11effectunorderedaccessviewvariable.md) | <span data-ttu-id="4773b-148">Accedere ai dati in una visualizzazione di accesso non ordinata.</span><span class="sxs-lookup"><span data-stu-id="4773b-148">Access data in an unordered access view.</span></span>            |



 

### <a name="setting-other-effect-variables"></a><span data-ttu-id="4773b-149">Impostazione di altre variabili di effetto</span><span class="sxs-lookup"><span data-stu-id="4773b-149">Setting Other Effect Variables</span></span>

<span data-ttu-id="4773b-150">Usare queste interfacce per ottenere e impostare lo stato in base al tipo di variabile.</span><span class="sxs-lookup"><span data-stu-id="4773b-150">Use these interfaces to get and set state by the variable type.</span></span>



| <span data-ttu-id="4773b-151">Interfacce di Reflection</span><span class="sxs-lookup"><span data-stu-id="4773b-151">Reflection Interfaces</span></span>                                                            | <span data-ttu-id="4773b-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4773b-152">Description</span></span>               |
|----------------------------------------------------------------------------------|---------------------------|
| [<span data-ttu-id="4773b-153">**ID3DX11EffectClassInstanceVariable**</span><span class="sxs-lookup"><span data-stu-id="4773b-153">**ID3DX11EffectClassInstanceVariable**</span></span>](id3dx11effectclassinstancevariable.md) | <span data-ttu-id="4773b-154">Ottenere un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="4773b-154">Get a class instance.</span></span>     |
| [<span data-ttu-id="4773b-155">**ID3DX11EffectInterfaceVariable**</span><span class="sxs-lookup"><span data-stu-id="4773b-155">**ID3DX11EffectInterfaceVariable**</span></span>](id3dx11effectinterfacevariable.md)         | <span data-ttu-id="4773b-156">Ottenere e impostare un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4773b-156">Get and set an interface.</span></span> |
| [<span data-ttu-id="4773b-157">**ID3DX11EffectMatrixVariable**</span><span class="sxs-lookup"><span data-stu-id="4773b-157">**ID3DX11EffectMatrixVariable**</span></span>](id3dx11effectmatrixvariable.md)               | <span data-ttu-id="4773b-158">Ottenere e impostare una matrice.</span><span class="sxs-lookup"><span data-stu-id="4773b-158">Get and set a matrix.</span></span>     |
| [<span data-ttu-id="4773b-159">**ID3DX11EffectScalarVariable**</span><span class="sxs-lookup"><span data-stu-id="4773b-159">**ID3DX11EffectScalarVariable**</span></span>](id3dx11effectscalarvariable.md)               | <span data-ttu-id="4773b-160">Ottenere e impostare un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="4773b-160">Get and set a scalar.</span></span>     |
| [<span data-ttu-id="4773b-161">**ID3DX11EffectShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="4773b-161">**ID3DX11EffectShaderVariable**</span></span>](id3dx11effectshadervariable.md)               | <span data-ttu-id="4773b-162">Ottiene una variabile shader.</span><span class="sxs-lookup"><span data-stu-id="4773b-162">Get a shader variable.</span></span>    |
| [<span data-ttu-id="4773b-163">**ID3DX11EffectStringVariable**</span><span class="sxs-lookup"><span data-stu-id="4773b-163">**ID3DX11EffectStringVariable**</span></span>](id3dx11effectstringvariable.md)               | <span data-ttu-id="4773b-164">Ottenere e impostare una stringa.</span><span class="sxs-lookup"><span data-stu-id="4773b-164">Get and set a string.</span></span>     |
| [<span data-ttu-id="4773b-165">**ID3DX11EffectType**</span><span class="sxs-lookup"><span data-stu-id="4773b-165">**ID3DX11EffectType**</span></span>](id3dx11effecttype.md)                                   | <span data-ttu-id="4773b-166">Ottiene un tipo di variabile.</span><span class="sxs-lookup"><span data-stu-id="4773b-166">Get a variable type.</span></span>      |
| [<span data-ttu-id="4773b-167">**ID3DX11EffectVectorVariable**</span><span class="sxs-lookup"><span data-stu-id="4773b-167">**ID3DX11EffectVectorVariable**</span></span>](id3dx11effectvectorvariable.md)               | <span data-ttu-id="4773b-168">Ottenere e impostare un vettore.</span><span class="sxs-lookup"><span data-stu-id="4773b-168">Get and set a vector.</span></span>     |



 

<span data-ttu-id="4773b-169">Tutte le interfacce di Reflection derivano da [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="4773b-169">All reflection interfaces derive from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4773b-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4773b-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4773b-171">Effetti (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="4773b-171">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="4773b-172">Guida alla programmazione per Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="4773b-172">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

 




