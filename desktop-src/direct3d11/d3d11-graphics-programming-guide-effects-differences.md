---
title: Differenze tra gli effetti 10 e gli effetti 11
description: In questo argomento vengono illustrate le differenze tra gli effetti 10 e gli effetti 11.
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29af1b9e7aec72f96a62e0f62668b81a6eec8367
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728231"
---
# <a name="differences-between-effects-10-and-effects-11"></a><span data-ttu-id="f3472-103">Differenze tra gli effetti 10 e gli effetti 11</span><span class="sxs-lookup"><span data-stu-id="f3472-103">Differences Between Effects 10 and Effects 11</span></span>

<span data-ttu-id="f3472-104">In questo argomento vengono illustrate le differenze tra gli effetti 10 e gli effetti 11.</span><span class="sxs-lookup"><span data-stu-id="f3472-104">This topic shows the differences between Effects 10 and Effects 11.</span></span>

## <a name="device-contexts-threading-and-cloning"></a><span data-ttu-id="f3472-105">Contesti di dispositivo, Threading e clonazione</span><span class="sxs-lookup"><span data-stu-id="f3472-105">Device Contexts, Threading, and Cloning</span></span>

<span data-ttu-id="f3472-106">L'interfaccia ID3D10Device è stata suddivisa in due interfacce in Direct3D 11: ID3D11Device e sul ID3D11DeviceContext.</span><span class="sxs-lookup"><span data-stu-id="f3472-106">The ID3D10Device interface has been split into two interfaces in Direct3D 11: ID3D11Device and ID3D11DeviceContext.</span></span> <span data-ttu-id="f3472-107">È possibile creare più ID3D11DeviceContexts per semplificare l'esecuzione simultanea su più thread.</span><span class="sxs-lookup"><span data-stu-id="f3472-107">You can create multiple ID3D11DeviceContexts to facilitate concurrent execution on multiple threads.</span></span> <span data-ttu-id="f3472-108">Effects 11 estende questo concetto al Framework Effects.</span><span class="sxs-lookup"><span data-stu-id="f3472-108">Effects 11 extends this concept to the Effects framework.</span></span>

<span data-ttu-id="f3472-109">Il runtime di Effects 11 è a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="f3472-109">The Effects 11 runtime is single-threaded.</span></span> <span data-ttu-id="f3472-110">Per questo motivo, non è consigliabile usare una singola istanza di ID3DX11Effect con più thread contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="f3472-110">For this reason, you should not use a single ID3DX11Effect instance with multiple threads concurrently.</span></span>

<span data-ttu-id="f3472-111">Per usare il runtime di Effects 11 su più istanze, è necessario creare istanze separate di ID3DX11Effect.</span><span class="sxs-lookup"><span data-stu-id="f3472-111">To use the Effects 11 runtime on multiple instances, you must create separate ID3DX11Effect instances.</span></span> <span data-ttu-id="f3472-112">Poiché sul ID3D11DeviceContext è anche a thread singolo, è necessario passare diverse istanze di sul ID3D11DeviceContext a ogni istanza dell'effetto su Apply.</span><span class="sxs-lookup"><span data-stu-id="f3472-112">Because the ID3D11DeviceContext is also single-threaded, you should pass different ID3D11DeviceContext instances to each effect instance on Apply.</span></span> <span data-ttu-id="f3472-113">È possibile usare questi contesti di dispositivo distinti per creare elenchi di comandi, in modo che il thread di rendering possa applicarli nel contesto di dispositivo immediato.</span><span class="sxs-lookup"><span data-stu-id="f3472-113">You can use these separate device contexts to create command lists so that the rendering thread can apply them on the immediate device context.</span></span>

<span data-ttu-id="f3472-114">Il modo più semplice per creare più effetti che incapsulano la stessa funzionalità, da usare su più thread, consiste nel creare un effetto e quindi eseguire copie clonate.</span><span class="sxs-lookup"><span data-stu-id="f3472-114">The easiest way to create multiple effects that encapsulate the same functionality, for use on multiple threads, is to create one effect and then make cloned copies.</span></span> <span data-ttu-id="f3472-115">La clonazione presenta i vantaggi seguenti rispetto alla creazione di più copie da zero:</span><span class="sxs-lookup"><span data-stu-id="f3472-115">Cloning has the following advantages over creating multiple copies from scratch:</span></span>

1.  <span data-ttu-id="f3472-116">La routine di clonazione è più veloce rispetto alla routine di creazione.</span><span class="sxs-lookup"><span data-stu-id="f3472-116">The cloning routine is faster than the creation routine.</span></span>
2.  <span data-ttu-id="f3472-117">Gli effetti clonati condividono gli shader creati, i blocchi di stato e le istanze di classe (pertanto non devono essere ricreati).</span><span class="sxs-lookup"><span data-stu-id="f3472-117">Cloned effects share created shaders, state blocks, and class instances (so they don't have to be recreated).</span></span>
3.  <span data-ttu-id="f3472-118">Gli effetti clonati possono condividere buffer costanti.</span><span class="sxs-lookup"><span data-stu-id="f3472-118">Cloned effects can share constant buffers.</span></span>
4.  <span data-ttu-id="f3472-119">Gli effetti clonati iniziano con lo stato che corrisponde all'effetto corrente (valori di variabile, indipendentemente dal fatto che sia stato ottimizzato).</span><span class="sxs-lookup"><span data-stu-id="f3472-119">Cloned effects begin with state that matches the current effect (variable values, whether or not it has been optimized).</span></span>

<span data-ttu-id="f3472-120">Per ulteriori informazioni, vedere [clonazione di un effetto](d3d11-graphics-programming-guide-effects-cloning.md) .</span><span class="sxs-lookup"><span data-stu-id="f3472-120">See [Cloning an Effect](d3d11-graphics-programming-guide-effects-cloning.md) for more information.</span></span>

## <a name="effect-pools-and-groups"></a><span data-ttu-id="f3472-121">Gruppi e pool di effetti</span><span class="sxs-lookup"><span data-stu-id="f3472-121">Effect Pools and Groups</span></span>

<span data-ttu-id="f3472-122">Di gran lunga l'uso più diffuso dei pool di effetti in Direct3D 10 era per il raggruppamento di materiali.</span><span class="sxs-lookup"><span data-stu-id="f3472-122">By far the most prevalent use of effect pools in Direct3D 10 was for grouping materials.</span></span> <span data-ttu-id="f3472-123">I pool di effetti sono stati rimossi dagli effetti 11 e sono stati aggiunti gruppi, un metodo più efficiente per raggruppare i materiali.</span><span class="sxs-lookup"><span data-stu-id="f3472-123">Effect Pools have been removed from Effects 11 and groups have been added, which is a more efficient method of grouping materials.</span></span>

<span data-ttu-id="f3472-124">Un gruppo di effetti è semplicemente un set di tecniche.</span><span class="sxs-lookup"><span data-stu-id="f3472-124">An effect group is simply a set of techniques.</span></span> <span data-ttu-id="f3472-125">Per ulteriori informazioni, vedere la [sintassi del gruppo di effetti (Direct3D 11)](d3d11-effect-group-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="f3472-125">See [Effect Group Syntax (Direct3D 11)](d3d11-effect-group-syntax.md) for more information.</span></span>

<span data-ttu-id="f3472-126">Si consideri la gerarchia degli effetti seguente con quattro effetti figlio e un pool di effetti:</span><span class="sxs-lookup"><span data-stu-id="f3472-126">Consider the following effect hierarchy with four child effects and one effect pool:</span></span>


```
// Effect Pool
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

// Effect Child 1
#include "EffectPool.fx"
technique10 GrassMaterialLowSpec { ... }

// Effect Child 2
#include "EffectPool.fx"
technique10 GrassMaterialHighSpec { ... }

// Effect Child 3
#include "EffectPool.fx"
technique10 WaterMaterialLowSpec { ... }

// Effect Child 4
#include "EffectPool.fx"
technique10 WaterMaterialHighSpec { ... }
```



<span data-ttu-id="f3472-127">È possibile ottenere la stessa funzionalità in Effects 11 usando i gruppi:</span><span class="sxs-lookup"><span data-stu-id="f3472-127">You can achieve the same functionality in Effects 11 by using groups:</span></span>


```
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

fxgroup GrassMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}

fxgroup WaterMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}
```



## <a name="new-shader-stages"></a><span data-ttu-id="f3472-128">Nuove fasi dello shader</span><span class="sxs-lookup"><span data-stu-id="f3472-128">New Shader Stages</span></span>

<span data-ttu-id="f3472-129">In Direct3D 11 sono disponibili tre nuove fasi dello shader: Hull shader, Domain shader e compute shader.</span><span class="sxs-lookup"><span data-stu-id="f3472-129">There are three new shader stages in Direct3D 11: the hull shader, domain shader, and compute shader.</span></span> <span data-ttu-id="f3472-130">Effects 11 li gestisce in modo analogo ai vertex shader, alla geometria shader e ai pixel shader.</span><span class="sxs-lookup"><span data-stu-id="f3472-130">Effects 11 handles these in a similar manner to vertex shaders, geometry shaders, and pixel shaders.</span></span>

<span data-ttu-id="f3472-131">Sono stati aggiunti tre nuovi tipi di variabili agli effetti 11:</span><span class="sxs-lookup"><span data-stu-id="f3472-131">Three new variable types have been added to Effects 11:</span></span>

-   <span data-ttu-id="f3472-132">HullShader</span><span class="sxs-lookup"><span data-stu-id="f3472-132">HullShader</span></span>
-   <span data-ttu-id="f3472-133">DomainShader</span><span class="sxs-lookup"><span data-stu-id="f3472-133">DomainShader</span></span>
-   <span data-ttu-id="f3472-134">ComputeShader</span><span class="sxs-lookup"><span data-stu-id="f3472-134">ComputeShader</span></span>

<span data-ttu-id="f3472-135">Se si usano questi shader in una tecnica, è necessario etichettare la tecnica "technique11" e non "technique10".</span><span class="sxs-lookup"><span data-stu-id="f3472-135">If you use these shaders in a technique, you must label that technique "technique11", and not "technique10".</span></span> <span data-ttu-id="f3472-136">Compute shader non può essere impostato nello stesso passaggio di qualsiasi altro stato di grafica (altri shader, blocchi di stato o destinazioni di rendering).</span><span class="sxs-lookup"><span data-stu-id="f3472-136">The compute shader cannot be set in the same pass as any other graphics state (other shaders, state blocks, or render targets).</span></span>

## <a name="new-texture-types"></a><span data-ttu-id="f3472-137">Nuovi tipi di trama</span><span class="sxs-lookup"><span data-stu-id="f3472-137">New Texture Types</span></span>

<span data-ttu-id="f3472-138">Direct3D 11 supporta i tipi di trama seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3472-138">Direct3D 11 supports the following texture types:</span></span>

-   [<span data-ttu-id="f3472-139">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="f3472-139">AppendStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [<span data-ttu-id="f3472-140">ByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="f3472-140">ByteAddressBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [<span data-ttu-id="f3472-141">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="f3472-141">ConsumeStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [<span data-ttu-id="f3472-142">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="f3472-142">StructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a><span data-ttu-id="f3472-143">Viste di accesso non ordinate</span><span class="sxs-lookup"><span data-stu-id="f3472-143">Unordered Access Views</span></span>

<span data-ttu-id="f3472-144">Effects 11 supporta il recupero e l'impostazione dei nuovi tipi di visualizzazione di accesso non ordinato.</span><span class="sxs-lookup"><span data-stu-id="f3472-144">Effects 11 supports getting and setting the new unordered access view types.</span></span> <span data-ttu-id="f3472-145">Funziona in modo analogo alle trame.</span><span class="sxs-lookup"><span data-stu-id="f3472-145">This works in a similar manner as textures.</span></span>

<span data-ttu-id="f3472-146">Considerare questo esempio di effetti HLSL:</span><span class="sxs-lookup"><span data-stu-id="f3472-146">Consider this Effects HLSL example:</span></span>


```
  
RWTexture1D<float> myUAV;
```



<span data-ttu-id="f3472-147">È possibile impostare questa variabile in C++ come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f3472-147">You can set this variable in C++ as follows:</span></span>


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



<span data-ttu-id="f3472-148">Direct3D 11 supporta i tipi di vista di accesso non ordinati seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3472-148">Direct3D 11 supports the following unordered access view types:</span></span>

-   <span data-ttu-id="f3472-149">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="f3472-149">RWBuffer</span></span>
-   <span data-ttu-id="f3472-150">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="f3472-150">RWByteAddressBuffer</span></span>
-   <span data-ttu-id="f3472-151">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="f3472-151">RWStructuredBuffer</span></span>
-   <span data-ttu-id="f3472-152">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="f3472-152">RWTexture1D</span></span>
-   <span data-ttu-id="f3472-153">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="f3472-153">RWTexture1DArray</span></span>
-   <span data-ttu-id="f3472-154">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="f3472-154">RWTexture2D</span></span>
-   <span data-ttu-id="f3472-155">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="f3472-155">RWTexture2DArray</span></span>
-   <span data-ttu-id="f3472-156">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="f3472-156">RWTexture3D</span></span>

## <a name="interfaces-and-class-instances"></a><span data-ttu-id="f3472-157">Interfacce e istanze di classe</span><span class="sxs-lookup"><span data-stu-id="f3472-157">Interfaces and Class Instances</span></span>

<span data-ttu-id="f3472-158">Per la sintassi dell'interfaccia e della classe, vedere [interfacce e classi](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span><span class="sxs-lookup"><span data-stu-id="f3472-158">For interface and class syntax, see [Interfaces and Classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span></span>

<span data-ttu-id="f3472-159">Per l'uso di interfacce e classi in effetti, vedere [interfacce e classi in effetti](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="f3472-159">For using interfaces and classes in effects, see [Interfaces and Classes in Effects](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).</span></span>

## <a name="addressable-stream-out"></a><span data-ttu-id="f3472-160">Flusso indirizzabile in uscita</span><span class="sxs-lookup"><span data-stu-id="f3472-160">Addressable Stream Out</span></span>

<span data-ttu-id="f3472-161">In Direct3D 10, Geometry shaders può restituire un flusso di dati all'unità di output del flusso e all'unità di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="f3472-161">In Direct3D 10, geometry shaders could output one stream of data to the stream output unit and the rasterizer unit.</span></span> <span data-ttu-id="f3472-162">In Direct3D11, la geometria shader può restituire fino a quattro flussi di dati all'unità di output del flusso e al massimo uno di questi flussi per l'unità di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="f3472-162">In Direct3D11, geometry shaders can output up to four streams of data to the stream output unit, and at most one of those streams to the rasterizer unit.</span></span> <span data-ttu-id="f3472-163">La funzione intrinseca **ConstructGSWithSO** è stata aggiornata per riflettere questa nuova funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f3472-163">The **ConstructGSWithSO** intrinsic has been updated to reflect this new functionality.</span></span>

<span data-ttu-id="f3472-164">Per ulteriori informazioni, vedere la [sintassi di streaming](d3d11-graphics-reference-effect-streamout.md) .</span><span class="sxs-lookup"><span data-stu-id="f3472-164">See [Stream Out Syntax](d3d11-graphics-reference-effect-streamout.md) for more information.</span></span>

## <a name="setting-and-unsetting-device-state"></a><span data-ttu-id="f3472-165">Impostazione e disimpostazione dello stato del dispositivo</span><span class="sxs-lookup"><span data-stu-id="f3472-165">Setting and Unsetting Device State</span></span>

<span data-ttu-id="f3472-166">Negli effetti 10, è possibile rendere i buffer costanti e i buffer di trama gestiti dall'utente usando le funzioni [**ID3D10EffectConstantBuffer:: SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) e [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="f3472-166">In Effects 10, you could make constant buffers and texture buffers user-managed by using the [**ID3D10EffectConstantBuffer::SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) and [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) functions.</span></span> <span data-ttu-id="f3472-167">Dopo aver chiamato queste funzioni, il runtime di Effects 10 non gestisce più il buffer costante o il buffer di trama e l'utente deve riempire i dati usando l'interfaccia ID3D10Device.</span><span class="sxs-lookup"><span data-stu-id="f3472-167">After you call these functions, the Effects 10 runtime no longer manages the constant buffer or texture buffer and the user must fill the data by using the ID3D10Device interface.</span></span>

<span data-ttu-id="f3472-168">In Effects 11 è inoltre possibile rendere gestiti dall'utente i blocchi di stato (stato di Blend, stato di rasterizzazione, stato dello stencil Depth e stato del campionatore) tramite le chiamate seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3472-168">In Effects 11, you can also make the state blocks (blend state, rasterizer state, depth-stencil state, and sampler state) user-managed by using the following calls:</span></span>

-   [<span data-ttu-id="f3472-169">**ID3DX11EffectBlendVariable::SetBlendState**</span><span class="sxs-lookup"><span data-stu-id="f3472-169">**ID3DX11EffectBlendVariable::SetBlendState**</span></span>](id3dx11effectblendvariable-setblendstate.md)
-   [<span data-ttu-id="f3472-170">**ID3DX11EffectRasterizerVariable::SetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="f3472-170">**ID3DX11EffectRasterizerVariable::SetRasterizerState**</span></span>](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [<span data-ttu-id="f3472-171">**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="f3472-171">**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [<span data-ttu-id="f3472-172">**ID3DX11EffectSamplerVariable:: sesampler**</span><span class="sxs-lookup"><span data-stu-id="f3472-172">**ID3DX11EffectSamplerVariable::SetSampler**</span></span>](id3dx11effectsamplervariable-setsampler.md)

<span data-ttu-id="f3472-173">Una volta chiamate queste funzioni, il runtime di Effects 11 non gestisce più le variabili del blocco di stato e i valori rimarranno invariati.</span><span class="sxs-lookup"><span data-stu-id="f3472-173">After you call these functions, the Effects 11 runtime no longer manages the state block variables, and there values will remain unchanged.</span></span> <span data-ttu-id="f3472-174">Si noti che poiché i blocchi di stato non sono modificabili, l'utente deve impostare un nuovo blocco di stato per modificare i valori.</span><span class="sxs-lookup"><span data-stu-id="f3472-174">Note that because state blocks are immutable, the user must set a new state block to change the values.</span></span>

<span data-ttu-id="f3472-175">È anche possibile ripristinare i buffer costanti, i buffer di trama e i blocchi di stato allo stato non gestito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f3472-175">You can also revert constant buffers, texture buffers, and state blocks to the non-user managed state.</span></span> <span data-ttu-id="f3472-176">Se si impostano queste variabili, il runtime di Effects 11 continuerà ad aggiornarle quando necessario.</span><span class="sxs-lookup"><span data-stu-id="f3472-176">If you unset these variables, the Effects 11 runtime will continue to update them when necessary.</span></span> <span data-ttu-id="f3472-177">Per annullare le variabili gestite dall'utente, è possibile usare le chiamate seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3472-177">You can use the following calls to unset user managed variables:</span></span>

-   [<span data-ttu-id="f3472-178">**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="f3472-178">**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [<span data-ttu-id="f3472-179">**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="f3472-179">**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [<span data-ttu-id="f3472-180">**ID3DX11EffectBlendVariable::UndoSetBlendState**</span><span class="sxs-lookup"><span data-stu-id="f3472-180">**ID3DX11EffectBlendVariable::UndoSetBlendState**</span></span>](id3dx11effectblendvariable-undosetblendstate.md)
-   [<span data-ttu-id="f3472-181">**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="f3472-181">**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**</span></span>](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [<span data-ttu-id="f3472-182">**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="f3472-182">**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [<span data-ttu-id="f3472-183">**ID3DX11EffectSamplerVariable::UndoSetSampler**</span><span class="sxs-lookup"><span data-stu-id="f3472-183">**ID3DX11EffectSamplerVariable::UndoSetSampler**</span></span>](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a><span data-ttu-id="f3472-184">Effetti della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="f3472-184">Effects Virtual Machine</span></span>

<span data-ttu-id="f3472-185">La macchina virtuale Effects, che ha valutato espressioni complesse al di fuori delle funzioni, è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="f3472-185">The effects virtual machine, which evaluated complex expressions outside of functions, has been removed.</span></span>

<span data-ttu-id="f3472-186">Gli esempi di espressioni complesse seguenti non sono supportati:</span><span class="sxs-lookup"><span data-stu-id="f3472-186">The following examples of complex expressions are not supported:</span></span>

1.  <span data-ttu-id="f3472-187">SetPixelShader (myPSArray (i \* 3 + j));</span><span class="sxs-lookup"><span data-stu-id="f3472-187">SetPixelShader( myPSArray( i \* 3 + j ) );</span></span>
2.  <span data-ttu-id="f3472-188">SetPixelShader (myPSArray ((float) i);</span><span class="sxs-lookup"><span data-stu-id="f3472-188">SetPixelShader( myPSArray( (float)i );</span></span>
3.  <span data-ttu-id="f3472-189">FILTER = i + 2;</span><span class="sxs-lookup"><span data-stu-id="f3472-189">FILTER = i + 2;</span></span>

<span data-ttu-id="f3472-190">Sono supportati gli esempi seguenti di espressioni non complesse:</span><span class="sxs-lookup"><span data-stu-id="f3472-190">The following examples of non-complex expressions are supported:</span></span>

1.  <span data-ttu-id="f3472-191">SetPixelShader( myPS );</span><span class="sxs-lookup"><span data-stu-id="f3472-191">SetPixelShader( myPS );</span></span>
2.  <span data-ttu-id="f3472-192">SetPixelShader (myPS \[ i \] );</span><span class="sxs-lookup"><span data-stu-id="f3472-192">SetPixelShader( myPS\[i\] );</span></span>
3.  <span data-ttu-id="f3472-193">SetPixelShader (myPS \[ uIndex \] );//uIndex è una variabile uint</span><span class="sxs-lookup"><span data-stu-id="f3472-193">SetPixelShader( myPS\[ uIndex \] ); // uIndex is a uint variable</span></span>
4.  <span data-ttu-id="f3472-194">FILTRO = i;</span><span class="sxs-lookup"><span data-stu-id="f3472-194">FILTER = i;</span></span>
5.  <span data-ttu-id="f3472-195">FILTER = ANISOTROPICO;</span><span class="sxs-lookup"><span data-stu-id="f3472-195">FILTER = ANISOTROPIC;</span></span>

<span data-ttu-id="f3472-196">Queste espressioni possono essere visualizzate nelle espressioni di blocco di stato (ad esempio filtro) e nelle espressioni Pass (ad esempio SetPixelShader).</span><span class="sxs-lookup"><span data-stu-id="f3472-196">These expressions could appear in state block expressions (such as FILTER) and pass expressions (such as SetPixelShader).</span></span>

## <a name="source-availability-and-location"></a><span data-ttu-id="f3472-197">Disponibilità e percorso di origine</span><span class="sxs-lookup"><span data-stu-id="f3472-197">Source Availability and Location</span></span>

<span data-ttu-id="f3472-198">Gli effetti 10 sono stati distribuiti in D3D10.dll.</span><span class="sxs-lookup"><span data-stu-id="f3472-198">Effects 10 was distributed in D3D10.dll.</span></span> <span data-ttu-id="f3472-199">Effects 11 viene distribuito come origine, con le soluzioni di Visual Studio corrispondenti per compilarlo.</span><span class="sxs-lookup"><span data-stu-id="f3472-199">Effects 11 is distributed as source, with corresponding Visual Studio solutions to compile it.</span></span> <span data-ttu-id="f3472-200">Quando si creano applicazioni di tipo Effects, è consigliabile includere l'origine Effects 11 direttamente in tali applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f3472-200">When you create effects-type applications, we recommend that you include the Effects 11 source directly in those applications.</span></span>

<span data-ttu-id="f3472-201">È possibile ottenere gli effetti 11 dagli [effetti per l'aggiornamento di Direct3D 11](https://github.com/Microsoft/FX11).</span><span class="sxs-lookup"><span data-stu-id="f3472-201">You can get Effects 11 from [Effects for Direct3D 11 Update](https://github.com/Microsoft/FX11).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3472-202">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3472-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3472-203">Effetti (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="f3472-203">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 