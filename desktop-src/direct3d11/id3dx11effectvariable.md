---
title: Interfaccia ID3DX11EffectVariable (D3dx11effect. h)
description: L'interfaccia ID3DX11EffectVariable è la classe di base per tutte le variabili di effetto. La durata di un oggetto ID3DX11EffectVariable è uguale alla durata del relativo oggetto ID3DX11Effect padre.
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- Interfaccia ID3DX11EffectVariable Direct3D 11
- Interfaccia ID3DX11EffectVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df38a12c54776072bb922ffc4cd5bcd0d79776
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762197"
---
# <a name="id3dx11effectvariable-interface"></a><span data-ttu-id="a6244-105">Interfaccia ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="a6244-105">ID3DX11EffectVariable interface</span></span>

<span data-ttu-id="a6244-106">L'interfaccia **ID3DX11EffectVariable** è la classe di base per tutte le variabili di effetto.</span><span class="sxs-lookup"><span data-stu-id="a6244-106">The **ID3DX11EffectVariable** interface is the base class for all effect variables.</span></span>

<span data-ttu-id="a6244-107">La durata di un oggetto **ID3DX11EffectVariable** è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.</span><span class="sxs-lookup"><span data-stu-id="a6244-107">The lifetime of an **ID3DX11EffectVariable** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="a6244-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="a6244-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a6244-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="a6244-109">Methods</span></span>

<span data-ttu-id="a6244-110">L'interfaccia **ID3DX11EffectVariable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a6244-110">The **ID3DX11EffectVariable** interface has these methods.</span></span>



| <span data-ttu-id="a6244-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="a6244-111">Method</span></span>                                                                           | <span data-ttu-id="a6244-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6244-112">Description</span></span>                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="a6244-113">**AsBlend**</span><span class="sxs-lookup"><span data-stu-id="a6244-113">**AsBlend**</span></span>](id3dx11effectvariable-asblend.md)                                 | <span data-ttu-id="a6244-114">Ottenere una variabile Effect-Blend.</span><span class="sxs-lookup"><span data-stu-id="a6244-114">Get a effect-blend variable.</span></span><br/>                |
| [<span data-ttu-id="a6244-115">**AsClassInstance**</span><span class="sxs-lookup"><span data-stu-id="a6244-115">**AsClassInstance**</span></span>](id3dx11effectvariable-asclassinstance.md)                 | <span data-ttu-id="a6244-116">Ottenere una variabile di istanza di classe.</span><span class="sxs-lookup"><span data-stu-id="a6244-116">Get a class-instance variable.</span></span><br/>              |
| [<span data-ttu-id="a6244-117">**AsConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="a6244-117">**AsConstantBuffer**</span></span>](id3dx11effectvariable-asconstantbuffer.md)               | <span data-ttu-id="a6244-118">Ottenere un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="a6244-118">Get a constant buffer.</span></span><br/>                      |
| [<span data-ttu-id="a6244-119">**AsDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="a6244-119">**AsDepthStencil**</span></span>](id3dx11effectvariable-asdepthstencil.md)                   | <span data-ttu-id="a6244-120">Ottenere una variabile di stencil Depth.</span><span class="sxs-lookup"><span data-stu-id="a6244-120">Get a depth-stencil variable.</span></span><br/>               |
| [<span data-ttu-id="a6244-121">**AsDepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="a6244-121">**AsDepthStencilView**</span></span>](id3dx11effectvariable-asdepthstencilview.md)           | <span data-ttu-id="a6244-122">Ottenere una variabile depth-stencil-View.</span><span class="sxs-lookup"><span data-stu-id="a6244-122">Get a depth-stencil-view variable.</span></span><br/>          |
| [<span data-ttu-id="a6244-123">**AsInterface**</span><span class="sxs-lookup"><span data-stu-id="a6244-123">**AsInterface**</span></span>](id3dx11effectvariable-asinterface.md)                         | <span data-ttu-id="a6244-124">Ottiene una variabile di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a6244-124">Get an interface variable.</span></span><br/>                  |
| [<span data-ttu-id="a6244-125">**AsMatrix**</span><span class="sxs-lookup"><span data-stu-id="a6244-125">**AsMatrix**</span></span>](id3dx11effectvariable-asmatrix.md)                               | <span data-ttu-id="a6244-126">Ottenere una variabile di matrice.</span><span class="sxs-lookup"><span data-stu-id="a6244-126">Get a matrix variable.</span></span><br/>                      |
| [<span data-ttu-id="a6244-127">**AsRasterizer**</span><span class="sxs-lookup"><span data-stu-id="a6244-127">**AsRasterizer**</span></span>](id3dx11effectvariable-asrasterizer.md)                       | <span data-ttu-id="a6244-128">Ottiene una variabile di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="a6244-128">Get a rasterizer variable.</span></span><br/>                  |
| [<span data-ttu-id="a6244-129">**AsRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="a6244-129">**AsRenderTargetView**</span></span>](id3dx11effectvariable-asrendertargetview.md)           | <span data-ttu-id="a6244-130">Ottenere una variabile di visualizzazione della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="a6244-130">Get a render-target-view variable.</span></span><br/>          |
| [<span data-ttu-id="a6244-131">**AsSampler**</span><span class="sxs-lookup"><span data-stu-id="a6244-131">**AsSampler**</span></span>](id3dx11effectvariable-assampler.md)                             | <span data-ttu-id="a6244-132">Ottiene una variabile del campionatore.</span><span class="sxs-lookup"><span data-stu-id="a6244-132">Get a sampler variable.</span></span><br/>                     |
| [<span data-ttu-id="a6244-133">**AsScalar**</span><span class="sxs-lookup"><span data-stu-id="a6244-133">**AsScalar**</span></span>](id3dx11effectvariable-asscalar.md)                               | <span data-ttu-id="a6244-134">Ottenere una variabile scalare.</span><span class="sxs-lookup"><span data-stu-id="a6244-134">Get a scalar variable.</span></span><br/>                      |
| [<span data-ttu-id="a6244-135">**AsShader**</span><span class="sxs-lookup"><span data-stu-id="a6244-135">**AsShader**</span></span>](id3dx11effectvariable-asshader.md)                               | <span data-ttu-id="a6244-136">Ottiene una variabile shader.</span><span class="sxs-lookup"><span data-stu-id="a6244-136">Get a shader variable.</span></span><br/>                      |
| [<span data-ttu-id="a6244-137">**AsShaderResource**</span><span class="sxs-lookup"><span data-stu-id="a6244-137">**AsShaderResource**</span></span>](id3dx11effectvariable-asshaderresource.md)               | <span data-ttu-id="a6244-138">Ottenere una variabile di risorsa shader.</span><span class="sxs-lookup"><span data-stu-id="a6244-138">Get a shader-resource variable.</span></span><br/>             |
| [<span data-ttu-id="a6244-139">**AsString**</span><span class="sxs-lookup"><span data-stu-id="a6244-139">**AsString**</span></span>](id3dx11effectvariable-asstring.md)                               | <span data-ttu-id="a6244-140">Ottiene una variabile di stringa.</span><span class="sxs-lookup"><span data-stu-id="a6244-140">Get a string variable.</span></span><br/>                      |
| [<span data-ttu-id="a6244-141">**AsUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="a6244-141">**AsUnorderedAccessView**</span></span>](id3dx11effectvariable-asunorderedaccessview.md)     | <span data-ttu-id="a6244-142">Ottenere una variabile di visualizzazione non ordinata.</span><span class="sxs-lookup"><span data-stu-id="a6244-142">Get an unordered-access-view variable.</span></span><br/>      |
| [<span data-ttu-id="a6244-143">**AsVector**</span><span class="sxs-lookup"><span data-stu-id="a6244-143">**AsVector**</span></span>](id3dx11effectvariable-asvector.md)                               | <span data-ttu-id="a6244-144">Ottenere una variabile vettoriale.</span><span class="sxs-lookup"><span data-stu-id="a6244-144">Get a vector variable.</span></span><br/>                      |
| [<span data-ttu-id="a6244-145">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="a6244-145">**GetAnnotationByIndex**</span></span>](id3dx11effectvariable-getannotationbyindex.md)       | <span data-ttu-id="a6244-146">Ottenere un'annotazione in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="a6244-146">Get an annotation by index.</span></span><br/>                 |
| [<span data-ttu-id="a6244-147">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="a6244-147">**GetAnnotationByName**</span></span>](id3dx11effectvariable-getannotationbyname.md)         | <span data-ttu-id="a6244-148">Ottenere un'annotazione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="a6244-148">Get an annotation by name.</span></span><br/>                  |
| [<span data-ttu-id="a6244-149">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="a6244-149">**GetDesc**</span></span>](id3dx11effectvariable-getdesc.md)                                 | <span data-ttu-id="a6244-150">Ottenere una descrizione.</span><span class="sxs-lookup"><span data-stu-id="a6244-150">Get a description.</span></span><br/>                          |
| [<span data-ttu-id="a6244-151">**GetElement**</span><span class="sxs-lookup"><span data-stu-id="a6244-151">**GetElement**</span></span>](id3dx11effectvariable-getelement.md)                           | <span data-ttu-id="a6244-152">Ottiene un elemento di matrice.</span><span class="sxs-lookup"><span data-stu-id="a6244-152">Get an array element.</span></span><br/>                       |
| [<span data-ttu-id="a6244-153">**GetMemberByIndex**</span><span class="sxs-lookup"><span data-stu-id="a6244-153">**GetMemberByIndex**</span></span>](id3dx11effectvariable-getmemberbyindex.md)               | <span data-ttu-id="a6244-154">Ottiene un membro della struttura in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="a6244-154">Get a structure member by index.</span></span><br/>            |
| [<span data-ttu-id="a6244-155">**GetMemberByName**</span><span class="sxs-lookup"><span data-stu-id="a6244-155">**GetMemberByName**</span></span>](id3dx11effectvariable-getmemberbyname.md)                 | <span data-ttu-id="a6244-156">Ottenere un membro della struttura in base al nome.</span><span class="sxs-lookup"><span data-stu-id="a6244-156">Get a structure member by name.</span></span><br/>             |
| [<span data-ttu-id="a6244-157">**GetMemberBySemantic**</span><span class="sxs-lookup"><span data-stu-id="a6244-157">**GetMemberBySemantic**</span></span>](id3dx11effectvariable-getmemberbysemantic.md)         | <span data-ttu-id="a6244-158">Ottenere un membro della struttura in base alla semantica.</span><span class="sxs-lookup"><span data-stu-id="a6244-158">Get a structure member by semantic.</span></span><br/>         |
| [<span data-ttu-id="a6244-159">**GetParentConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="a6244-159">**GetParentConstantBuffer**</span></span>](id3dx11effectvariable-getparentconstantbuffer.md) | <span data-ttu-id="a6244-160">Ottenere un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="a6244-160">Get a constant buffer.</span></span><br/>                      |
| [<span data-ttu-id="a6244-161">**GetRawValue**</span><span class="sxs-lookup"><span data-stu-id="a6244-161">**GetRawValue**</span></span>](id3dx11effectvariable-getrawvalue.md)                         | <span data-ttu-id="a6244-162">Recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="a6244-162">Get data.</span></span><br/>                                   |
| [<span data-ttu-id="a6244-163">**GetType**</span><span class="sxs-lookup"><span data-stu-id="a6244-163">**GetType**</span></span>](id3dx11effectvariable-gettype.md)                                 | <span data-ttu-id="a6244-164">Ottenere informazioni sul tipo.</span><span class="sxs-lookup"><span data-stu-id="a6244-164">Get type information.</span></span><br/>                       |
| [<span data-ttu-id="a6244-165">**isValid**</span><span class="sxs-lookup"><span data-stu-id="a6244-165">**IsValid**</span></span>](id3dx11effectvariable-isvalid.md)                                 | <span data-ttu-id="a6244-166">Confrontare il tipo di dati con i dati archiviati.</span><span class="sxs-lookup"><span data-stu-id="a6244-166">Compare the data type with the data stored.</span></span><br/> |
| [<span data-ttu-id="a6244-167">**SetRawValue**</span><span class="sxs-lookup"><span data-stu-id="a6244-167">**SetRawValue**</span></span>](id3dx11effectvariable-setrawvalue.md)                         | <span data-ttu-id="a6244-168">Impostare i dati.</span><span class="sxs-lookup"><span data-stu-id="a6244-168">Set data.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="a6244-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="a6244-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a6244-170">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="a6244-170">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a6244-171">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="a6244-171">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a6244-172">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a6244-172">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a6244-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6244-173">Requirements</span></span>



| <span data-ttu-id="a6244-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6244-174">Requirement</span></span> | <span data-ttu-id="a6244-175">Valore</span><span class="sxs-lookup"><span data-stu-id="a6244-175">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6244-176">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6244-176">Header</span></span><br/>  | <dl> <span data-ttu-id="a6244-177"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6244-177"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a6244-178">Libreria</span><span class="sxs-lookup"><span data-stu-id="a6244-178">Library</span></span><br/> | <dl> <span data-ttu-id="a6244-179"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="a6244-179"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6244-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6244-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6244-181">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="a6244-181">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a6244-182">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="a6244-182">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





