---
title: Interfaccia ID3DX11EffectPass (D3dx11effect. h)
description: Un'interfaccia ID3DX11EffectPass incapsula le assegnazioni di stato all'interno di una tecnica. La durata di un oggetto ID3DX11EffectPass è uguale alla durata del relativo oggetto ID3DX11Effect padre.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- Interfaccia ID3DX11EffectPass Direct3D 11
- Interfaccia ID3DX11EffectPass Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectPass
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26732543d1033cfc439755df6ac397d2a28ec1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235152"
---
# <a name="id3dx11effectpass-interface"></a><span data-ttu-id="f260c-105">Interfaccia ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="f260c-105">ID3DX11EffectPass interface</span></span>

<span data-ttu-id="f260c-106">Un'interfaccia **ID3DX11EffectPass** incapsula le assegnazioni di stato all'interno di una tecnica.</span><span class="sxs-lookup"><span data-stu-id="f260c-106">An **ID3DX11EffectPass** interface encapsulates state assignments within a technique.</span></span>

<span data-ttu-id="f260c-107">La durata di un oggetto **ID3DX11EffectPass** è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.</span><span class="sxs-lookup"><span data-stu-id="f260c-107">The lifetime of an **ID3DX11EffectPass** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="f260c-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="f260c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f260c-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="f260c-109">Methods</span></span>

<span data-ttu-id="f260c-110">L'interfaccia **ID3DX11EffectPass** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f260c-110">The **ID3DX11EffectPass** interface has these methods.</span></span>



| <span data-ttu-id="f260c-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="f260c-111">Method</span></span>                                                                   | <span data-ttu-id="f260c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f260c-112">Description</span></span>                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="f260c-113">**Applica**</span><span class="sxs-lookup"><span data-stu-id="f260c-113">**Apply**</span></span>](id3dx11effectpass-apply.md)                                 | <span data-ttu-id="f260c-114">Impostare lo stato contenuto in un passaggio al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f260c-114">Set the state contained in a pass to the device.</span></span><br/>       |
| [<span data-ttu-id="f260c-115">**ComputeStateBlockMask**</span><span class="sxs-lookup"><span data-stu-id="f260c-115">**ComputeStateBlockMask**</span></span>](id3dx11effectpass-computestateblockmask.md) | <span data-ttu-id="f260c-116">Genera una maschera per consentire o impedire le modifiche di stato.</span><span class="sxs-lookup"><span data-stu-id="f260c-116">Generate a mask for allowing/preventing state changes.</span></span><br/> |
| [<span data-ttu-id="f260c-117">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="f260c-117">**GetAnnotationByIndex**</span></span>](id3dx11effectpass-getannotationbyindex.md)   | <span data-ttu-id="f260c-118">Ottenere un'annotazione in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="f260c-118">Get an annotation by index.</span></span><br/>                            |
| [<span data-ttu-id="f260c-119">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="f260c-119">**GetAnnotationByName**</span></span>](id3dx11effectpass-getannotationbyname.md)     | <span data-ttu-id="f260c-120">Ottenere un'annotazione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="f260c-120">Get an annotation by name.</span></span><br/>                             |
| [<span data-ttu-id="f260c-121">**GetComputeShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="f260c-121">**GetComputeShaderDesc**</span></span>](id3dx11effectpass-getcomputeshaderdesc.md)   | <span data-ttu-id="f260c-122">Ottenere una descrizione del compute shader.</span><span class="sxs-lookup"><span data-stu-id="f260c-122">Get a compute-shader description.</span></span><br/>                      |
| [<span data-ttu-id="f260c-123">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="f260c-123">**GetDesc**</span></span>](id3dx11effectpass-getdesc.md)                             | <span data-ttu-id="f260c-124">Ottenere una descrizione del passaggio.</span><span class="sxs-lookup"><span data-stu-id="f260c-124">Get a pass description.</span></span><br/>                                |
| [<span data-ttu-id="f260c-125">**GetDomainShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="f260c-125">**GetDomainShaderDesc**</span></span>](id3dx11effectpass-getdomainshaderdesc.md)     | <span data-ttu-id="f260c-126">Ottenere una descrizione dello shader di dominio.</span><span class="sxs-lookup"><span data-stu-id="f260c-126">Get a domain-shader description.</span></span><br/>                       |
| [<span data-ttu-id="f260c-127">**GetGeometryShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="f260c-127">**GetGeometryShaderDesc**</span></span>](id3dx11effectpass-getgeometryshaderdesc.md) | <span data-ttu-id="f260c-128">Ottenere una descrizione dello shader di geometria.</span><span class="sxs-lookup"><span data-stu-id="f260c-128">Get a geometry-shader description.</span></span><br/>                     |
| [<span data-ttu-id="f260c-129">**GetHullShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="f260c-129">**GetHullShaderDesc**</span></span>](id3dx11effectpass-gethullshaderdesc.md)         | <span data-ttu-id="f260c-130">Ottenere la descrizione di Hull-shader.</span><span class="sxs-lookup"><span data-stu-id="f260c-130">Get hull-shader description.</span></span><br/>                           |
| [<span data-ttu-id="f260c-131">**GetPixelShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="f260c-131">**GetPixelShaderDesc**</span></span>](id3dx11effectpass-getpixelshaderdesc.md)       | <span data-ttu-id="f260c-132">Ottenere una descrizione del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="f260c-132">Get a pixel-shader description.</span></span><br/>                        |
| [<span data-ttu-id="f260c-133">**GetVertexShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="f260c-133">**GetVertexShaderDesc**</span></span>](id3dx11effectpass-getvertexshaderdesc.md)     | <span data-ttu-id="f260c-134">Ottenere una descrizione del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="f260c-134">Get a vertex-shader description.</span></span><br/>                       |
| [<span data-ttu-id="f260c-135">**isValid**</span><span class="sxs-lookup"><span data-stu-id="f260c-135">**IsValid**</span></span>](id3dx11effectpass-isvalid.md)                             | <span data-ttu-id="f260c-136">Testare un passaggio per verificare se contiene una sintassi valida.</span><span class="sxs-lookup"><span data-stu-id="f260c-136">Test a pass to see if it contains valid syntax.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="f260c-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="f260c-137">Remarks</span></span>

<span data-ttu-id="f260c-138">Un passaggio è un blocco di codice che imposta gli shader e gli oggetti dello stato di rendering.</span><span class="sxs-lookup"><span data-stu-id="f260c-138">A pass is a block of code that sets render-state objects and shaders.</span></span> <span data-ttu-id="f260c-139">Una sessione viene dichiarata all'interno di una tecnica.</span><span class="sxs-lookup"><span data-stu-id="f260c-139">A pass is declared within a technique.</span></span>

<span data-ttu-id="f260c-140">Per ottenere un'interfaccia Effect-Pass, chiamare un metodo come [**ID3DX11EffectTechnique:: GetPassByName**](id3dx11effecttechnique-getpassbyname.md).</span><span class="sxs-lookup"><span data-stu-id="f260c-140">To get an effect-pass interface, call a method like [**ID3DX11EffectTechnique::GetPassByName**](id3dx11effecttechnique-getpassbyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="f260c-141">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="f260c-141">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f260c-142">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="f260c-142">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f260c-143">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f260c-143">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f260c-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f260c-144">Requirements</span></span>



| <span data-ttu-id="f260c-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="f260c-145">Requirement</span></span> | <span data-ttu-id="f260c-146">Valore</span><span class="sxs-lookup"><span data-stu-id="f260c-146">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f260c-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f260c-147">Header</span></span><br/>  | <dl> <span data-ttu-id="f260c-148"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f260c-148"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f260c-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="f260c-149">Library</span></span><br/> | <dl> <span data-ttu-id="f260c-150"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="f260c-150"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f260c-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f260c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f260c-152">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="f260c-152">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f260c-153">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="f260c-153">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





